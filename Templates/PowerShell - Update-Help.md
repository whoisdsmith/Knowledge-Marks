---
Date: 2022-08-14
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/PowerShell", "#Topic/Dev/PowerShell"]
Alias: []
---

# PowerShell - Update-Help

*Source: [Scripts/Update-Help.ps1 at main · jimbrig/Scripts · GitHub](https://github.com/jimbrig/Scripts/blob/main/PowerShell/Update-Help.ps1)*

```powershell
Start-Job -Name "UpdateHelp" -ScriptBlock { Update-Help -Force -ErrorAction SilentlyContinue } | Out-Null
Write-Host "Updating Help in background (Get-Help to check)" -ForegroundColor Yellow
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