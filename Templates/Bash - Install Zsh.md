---
Date: 2022-07-25
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/Bash", "#Topic/Dev/Linux"]
Alias: []
---

# Bash - Install Zsh

*Source: [Installing ZSH · ohmyzsh/ohmyzsh Wiki · GitHub](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)*

```bash
# update and install
sudo apt-get -y update
sudo apt-get -y install zsh

# verify
zsh --version

# make default shell
chsh -s $(which zsh)

# 

```

## Install and set up Zsh as default

If necessary, follow these steps to install Zsh:

1.  There are two main ways to install Zsh:
    
    -   With the package manager of your choice, _e.g._ `sudo apt install zsh` (see [more examples](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#how-to-install-zsh-on-many-platforms))
    -   From [source](https://zsh.sourceforge.io/Arc/source.html), following [the instructions from the Zsh FAQ](https://zsh.sourceforge.io/FAQ/zshfaq01.html#l7).
    
2.  Verify installation by running `zsh --version`. Expected result: `zsh 5.0.8` or more recent.
    
3.  Make it your default shell: `chsh -s $(which zsh)`
    
    -   Note that this will not work if Zsh is not in your authorized shells list (`/etc/shells`) or if you don't have permission to use `chsh`. If that's the case [you'll need to use a different procedure](https://www.google.com/search?q=zsh+default+without+chsh).

4.  Log out and log back in again to use your new default shell.
    
5.  Test that it worked with `echo $SHELL`. Expected result: `/bin/zsh` or similar.
    
6.  Test with `$SHELL --version`. Expected result: 'zsh 5.8' or similar
    

## How to install zsh on many platforms

### macOS

**Try `zsh --version` before installing it from [[Homebrew]]. Preferably newer than or equal to `5.0.8`.**

```bash
brew install zsh
```

To set zsh as your default shell, execute the following assuming a default install of Homebrew

-   Recent macOS versions:

```bash
chsh -s /usr/local/bin/zsh
```

-   macOS **High Sierra** and older:

```bash    
chsh -s /bin/zsh
```    

Assuming you have [Homebrew](https://brew.sh/) installed. If not, most versions of **macOS** ship zsh by default, but it's normally an older version. Alternatively, you may also use [MacPorts](https://www.macports.org/)

```bash
sudo port install zsh zsh-completions
```

### Ubuntu, Debian & derivatives (Windows WSL)

```bash
apt install zsh
```

If you don't have `apt`, the recommended package manager for end users [[1]](https://askubuntu.com/a/446484) [[2]](https://askubuntu.com/a/775264) [[3]](https://help.ubuntu.com/lts/serverguide/apt.html) [[4]](https://www.howtogeek.com/234583/simplify-command-line-package-management-with-apt-instead-of-apt-get/) , you can try `apt-get` or `aptitude`.

[Other distributions that apply](https://en.wikipedia.org/wiki/List_of_Linux_distributions#Debian-based) include: Linux Mint, elementary OS, Zorin OS, Raspbian, MX Linux, Deepin.

### OpenSUSE

```bash
zypper install zsh
```


### Arch Linux or Manjaro

```bash
pacman -S zsh
```

### Void Linux

```bash
xbps-install zsh
```

### Fedora

```
dnf install zsh
```

### OpenBSD

To install the package:

```bash
pkg_add zsh
```

### FreeBSD

To install the package:

```bash
pkg install zsh
```

To install the port:

```bash
cd /usr/ports/shells/zsh/ && make install clean
```

To reduce memory usage, optionally enable zsh-mem options with ![installation screen to enable zsh-mem](https://camo.githubusercontent.com/68720a867a939ffaf119cfbddb8d4aa64670b3366f22e20793fbaa36a064f0cd/68747470733a2f2f692e696d6775722e636f6d2f6c34696436456b2e706e67)

```bash
make config
```

before running `make install`.

### Centos/RHEL

```bash
sudo yum update && sudo yum -y install zsh
```

### Cygwin

Install the zsh package using the installer. Unfortunately Cygwin doesn't have a standard command line interface. You could, however, setup [apt-cyg](https://github.com/kou1okada/apt-cyg) and install zsh as follows:

```bash
apt-cyg install zsh
```

The easiest way to change the default shell is to set your SHELL user environment variable. Search for "Edit Environment variables for your account" to bring up the environment variables window, create a new variable named "SHELL" and give it the value "/usr/bin/zsh/".

_Alternatively:_ Open Cygwin (in BASH) then type:

```bash
sudo nano ~/.bashrc
```

Once the `.bashrc` file is open, add this line to the very top:

```bash
exec zsh
```

Close and save the file. Close and reopen [[Cygwin]]. It will execute the command every time you load the terminal and run your zsh shell.

***

## Appendix: Links and References

- [[_README 3|Code]]
- [[Developer/Development]]
- [[OS/Linux]]
- [[_README 2|Bash]]
- [[Oh-My-Zsh]]
- [[Shell]]
- [[WSL]]
- [[Zsh Setup Guide]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022