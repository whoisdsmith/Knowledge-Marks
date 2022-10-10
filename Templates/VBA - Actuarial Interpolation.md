---
Date: 2022-08-16
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/VBA", "#Topic/Dev/VBA", "#Topic/Tools/Excel"]
Alias: []
---

# VBA - Actuarial Interpolation

*Source: [Tools – Archer Actuarial](https://archeractuarial.com/tools/)*

![[Pasted image 20220816183935.png]]

## interpolateAYLDF Function

**Arguments:**

interp_age: desired interpolation age  
age_range: range of ages of existing LDFs  
LDF_range: range of existing LDFs (these values should **not** reflect exposure adjustment)  
descending: _optional; default=true_; existing LDFs in descending order with respect to age (_true_ or _false_)  
exponential: _optional; default=true_; _true_=exponential interpolation, _false_=linear interpolation

- x: Current age
- index_range: ages range
- value_range: CDFs range
- (Optional) Descending (Boolean):
- (Optional) Exponential (Boolean):

```vba
Public Function interpolateAYLDF(x, index_range, value_range, Optional Descending As Boolean, Optional Exponential As Boolean)

    Dim Low, High, index_high, index_low, value_high, value_low, value_high_adj, value_low_adj As Double
    Dim EarlyExit As Boolean
    Dim i As Integer
    EarlyExit = False
    
    Select Case Descending
    
    Case False
        Low = Application.Match(x, index_range, 1)
        index_low = Application.Index(index_range, Low, 1)
        If Application.Index(value_range, Low) <> 0 Then value_low = 1 / Application.Index(value_range, Low) Else value_low = 0
        If WorksheetFunction.Min(12, index_low) = 0 Then
            value_low_adj = 0
        Else: value_low_adj = value_low * 12 / WorksheetFunction.Min(12, index_low)
        End If
    
        If index_low = x Then
            interpolateAYLDF = value_low
            EarlyExit = True
        Else
            High = Low + 1
            index_high = Application.Index(index_range, High, 1)
            value_high = 1 / Application.Index(value_range, High)
            value_high_adj = value_high * 12 / WorksheetFunction.Min(12, index_high)
            If value_low_adj > value_high_adj Then
                interpolateAYLDF = "NA"
                EarlyExit = True
            End If
        End If
    Case True
        High = Application.Match(x, index_range, -1)
        index_high = Application.Index(index_range, High, 1)
        If Application.Index(value_range, High) <> 0 Then value_high = 1 / Application.Index(value_range, High) Else value_high = 0
        If WorksheetFunction.Min(12, index_high) = 0 Then
            value_high_adj = 0
        Else: value_high_adj = value_high * 12 / WorksheetFunction.Min(12, index_high)
        End If
        
        If index_high = x Then
            interpolateAYLDF = value_high
            EarlyExit = True
        Else
            Low = High + 1
            index_low = Application.Index(index_range, Low, 1)
            value_low = 1 / Application.Index(value_range, Low)
            value_low_adj = value_low * 12 / WorksheetFunction.Min(12, index_low)
            If value_low_adj > value_high_adj Then
                interpolateAYLDF = "NA"
                EarlyExit = True
            End If
        End If
    End Select

    If Exponential = True Then
        If EarlyExit <> True Then interpolateAYLDF = (1 - (((1 - value_low_adj) ^ (index_high - x)) * ((1 - value_high_adj) ^ (x - index_low))) ^ (1 / (index_high - index_low))) * WorksheetFunction.Min(12, x) / 12
    Else: If EarlyExit <> True Then interpolateAYLDF = ((x - index_low) / (index_high - index_low) * (value_high_adj - value_low_adj) + value_low_adj) * WorksheetFunction.Min(12, x) / 12
    End If
    
    If interpolateAYLDF <> 0 Then interpolateAYLDF = 1 / interpolateAYLDF
    
End Function
```

***

## Appendix: Links and References

- [[_README 3|Code]]
- [[Developer/Development]]
- [[Templates/VBA/_README|VBA]]
- [[Actuarial Science]]
- [[Microsoft Excel|Excel]]
- [[Mathematics and Statistics]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022