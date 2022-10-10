---
Date: 2022-07-25
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/Bash", "#Topic/Dev/Linux"]
Alias: []
---

# Bash - Install oh-my-zsh

*Source: [GitHub - ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh#basic-installation)*

*See Also: [[Bash - Install Zsh]]*

[TOC]

```bash
# curl
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# wget
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# fetch
sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Prerequisites

- A [[Unix]]-like operating system: [[macOS]], [[OS/Linux]], BSD. On Windows: [[WSL]] is preferred, but `cygwin` or `msys` also mostly work.
- [Zsh](https://www.zsh.org) should be installed (v4.3.9 or more recent is fine but we prefer 5.0.8 and newer). If not pre-installed (run `zsh --version` to confirm), check the following wiki instructions here: [Installing ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` or `wget` should be installed
- `git` should be installed (recommended v2.4.11 or higher)

## Basic Installation

[[Oh-My-Zsh]] is installed by running one of the following commands in your terminal. You can install this via the command-line with either `curl`, `wget` or another similar tool.

| Method    | Command                                                                                           |
| :-------- | :------------------------------------------------------------------------------------------------ |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

_Note that any previous `.zshrc` will be renamed to `.zshrc.pre-oh-my-zsh`. After installation, you can move the configuration you want to preserve into the new `.zshrc`._

## Manual inspection

It's a good idea to inspect the install script from projects you don't yet know. You can do
that by downloading the install script first, looking through it so everything looks normal,
then running it:

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

## Zsh?

**Oh My Zsh** is a framework for [Zsh](https://www.zsh.org/), the [[Z shell]].

-   In order for **Oh My Zsh** to work, **Zsh must be installed**.
    -   Please run `zsh --version` to confirm.
    -   Expected result: `zsh 5.0.8` or more recent
-   Additionally, Zsh should be set as your default shell.
    -   Please run `echo $SHELL` from a new terminal to confirm.
    -   Expected result: `/usr/bin/zsh` or similar

***

## Appendix: Links and References

- [[Code]]
- [[Developer/Development]]
- [[OS/Linux]]
- [[_README 2|Bash]]
- [[Zsh]]
- [[Oh-My-Zsh]]
- [[macOS]]
- [[Shell]]
- [[Terminal]]
- [[Zsh Setup Guide]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022