---
Date: 2022-08-14
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/PowerShell", "#Topic/Dev/PowerShell"]
Alias: []
---

# PowerShell - Enable LongPaths

*Source: [Scripts/setup.ps1 at ae4c8459682fcd98732bc2dd502bcda37782d0ea · jimbrig/Scripts · GitHub](https://github.com/jimbrig/Scripts/blob/ae4c8459682fcd98732bc2dd502bcda37782d0ea/PowerShell/Configurations/setup.ps1#L6)*

```powershell
# Support Long Paths
Set-ItemProperty 'HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem' -Name 'LongPathsEnabled' -Value 1
Write-Host "Long Path Support has been enabled via the registry." -ForegroundColor Green
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