---
Date: 2022-08-14
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/PowerShell", "#Topic/Dev/PowerShell"]
Alias: []
---

# PowerShell - Admin Script

*Source: [Scripts/Admin.ps1 at main · jimbrig/Scripts · GitHub](https://github.com/jimbrig/Scripts/blob/main/PowerShell/Admin.ps1)*

```powershell
If (!([Security.Principal.WindowsPrincipal][Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole]'Administrator')) {
    Write-Host "You didn't run this script as an Administrator. This script will self elevate to run as an Administrator and continue."
    Start-Sleep 1
    Write-Host "                                               3"
    Start-Sleep 1
    Write-Host "                                               2"
    Start-Sleep 1
    Write-Host "                                               1"
    Start-Sleep 1
    Start-Process powershell.exe -ArgumentList ("-NoProfile -ExecutionPolicy Bypass -File `"{0}`"" -f $PSCommandPath) -Verb RunAs
    Exit
}
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