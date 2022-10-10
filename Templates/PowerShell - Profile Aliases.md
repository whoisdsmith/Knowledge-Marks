---
Date: 2022-08-14
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/PowerShell", "#Topic/Dev/PowerShell"]
Alias: []
---

# PowerShell - Profile Aliases

*Source: [PowerShell/aliases.ps1 at main · jimbrig/PowerShell · GitHub](https://github.com/jimbrig/PowerShell/blob/main/Profile/aliases.ps1)*

```powershell
# -------------------------
# PowerShell Aliases
# -------------------------

Set-Alias -Name pro -Value Edit-Profile
Set-Alias -Name aliases -Value Get-Alias
Set-Alias -Name refresh -Value refreshenv
Set-Alias -Name touch -Value New-File
Set-Alias -Name rproj -Value openrproj
Set-Alias -Name chkdisk -Value Check-Disk
Set-Alias -Name cdd -Value CreateAndSet-Directory
Set-Alias -Name emptytrash -Value Clear-RecycleBin
Set-Alias -Name checkdisk -Value Invoke-Checkdisk
Set-Alias -Name sfc -Value Invoke-SFCScan
Set-Alias -Name expl -Value explorer.exe
Set-Alias -Name np -Value 'C:\Program Files\WindowsApps\Microsoft.WindowsNotepad_11.2111.0.0_x64__8wekyb3d8bbwe\Notepad\Notepad.exe'

# Set-Alias -Name files -Value 'C:\Program Files\WindowsApps\49306atecsolution.FilesUWP_2.0.34.0_x64__et10x9a9vyk8t\Files.exe'

# Remove stupid 'touch' alias for 'set-filetime'
Remove-Alias -Name touch

# Ensure `R` is for launching an R Terminal:
if (Get-Command R.exe -ErrorAction SilentlyContinue | Test-Path) {
	Remove-Item Alias:r -ErrorAction SilentlyContinue
	${function:r} = { R.exe @args }
}

# VSCode / VSCode Insiders
If (!(Get-Command code -ErrorAction SilentlyContinue)) {
	Set-Alias -Name code -Value code-insiders
}

# Ensure gpg points to correct program
# Set-Alias -Name gpg -Value 'C:\Program Files (x86)\GnuPG\bin\gpg.exe'

# Chocolatey
If (Get-Command choco -ErrorAction SilentlyContinue) {
	Set-Alias -Name cpkgs -Value chocopkgs
	Set-Alias -Name csearch -Value chocosearch
	Set-Alias -Name cup -Value chocoupgrade

	If (Get-Command choco-cleaner -ErrorAction SilentlyContinue) {
		Set-Alias -Name cclean -Value chococlean
	}
	If (Get-Command choco-package-list-backup -ErrorAction SilentlyContinue) {
		Set-Alias -Name cbackup -Value chocobackup
	}
}

# gcalcli
If (Get-Command gcalcli -ErrorAction SilentlyContinue) {
	Set-Alias -Name gcal -Value gcalcli
	Set-Alias -Name agenda -Value Get-Agenda
	Set-Alias -Name gcalm -Value Get-CalendarMonth
	Set-Alias -Name gcalw -Value Get-CalendarWeek
	Set-Alias -Name calm -Value Get-CalendarMonth
	Set-Alias -Name calw -Value Get-CalendarWeek
	Set-Alias -Name gcaladd -Value New-CalendarEvent
	Set-Alias -Name caladd -Value New-CalendarEvent
}

# git-crypt
If (Get-Command git-crypt -ErrorAction SilentlyContinue) {
	Set-Alias -Name gcrypts -Value Get-GitCryptStatus
	Set-Alias -Name gcrypt -Value git-crypt
	Set-Alias -Name gcryptf Invoke-GitCryptStatus
}

# If using code-insiders
If (Get-Command code-insiders -ErrorAction SilentlyContinue) {
	Set-Alias -Name codee -Value code-insiders
}

# lsd
If (Get-Command lsd -ErrorAction SilentlyContinue) {
	${function:lsa} = { & lsd -a }
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