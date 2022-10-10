---
Date: 2022-08-14
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/PowerShell", "#Topic/Dev/PowerShell"]
Alias: []
---

# PowerShell - Add Defender Exclusions

*Source: [Scripts/setup.ps1 at ae4c8459682fcd98732bc2dd502bcda37782d0ea · jimbrig/Scripts · GitHub](https://github.com/jimbrig/Scripts/blob/ae4c8459682fcd98732bc2dd502bcda37782d0ea/PowerShell/Configurations/setup.ps1#L10)*

```powershell
# Tweak Defender
Add-MpPreference -ExclusionPath 'C:\Users\jimbr\scoop'
Add-MpPreference -ExclusionPath 'C:\ProgramData\scoop'
Add-MpPreference -ExclusionPath 'C:\ProgramData\chocolatey'

Write-Host "Added Windows Defender Exclusions." -ForegroundColor Green
```

***

## Appendix: Links and References

- [[_README 3|Code]]
- [[Developer/Development]]
- [[Software Development]]
- [[Templates/PowerShell/_README|PowerShell]]
- [[Windows]]


***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022