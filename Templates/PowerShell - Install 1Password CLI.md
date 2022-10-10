---
Date: 2022-08-20
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/PowerShell", "#Topic/Dev/PowerShell"]
Alias: []
---

# PowerShell - Install 1Password CLI

*Source: [Get started with 1Password CLI 2 - 1Password Developer Documentation](https://developer.1password.com/docs/cli/get-started#:~:text=%24arch%20%3D%20)*

```powershell
$arch = (Get-CimInstance Win32_OperatingSystem).OSArchitecture
switch ($arch) {
    '64-bit' { $opArch = 'amd64'; break }
    '32-bit' { $opArch = '386'; break }
    Default { Write-Error "Sorry, your operating system architecture '$arch' is unsupported" -ErrorAction Stop }
}
$installDir = Join-Path -Path $env:ProgramFiles -ChildPath '1Password CLI'
Invoke-WebRequest -Uri "https://cache.agilebits.com/dist/1P/op2/pkg/v2.4.1/op_windows_$($opArch)_v2.4.1.zip" -OutFile op.zip
Expand-Archive -Path op.zip -DestinationPath $installDir -Force
$envMachinePath = [System.Environment]::GetEnvironmentVariable('PATH','machine')
if ($envMachinePath -split ';' -notcontains $installDir){
    [Environment]::SetEnvironmentVariable('PATH', "$envMachinePath;$installDir", 'Machine')
}
Remove-Item -Path op.zip
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