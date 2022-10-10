---
Date: 2022-08-11
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/Bash", "#Topic/Dev/Linux"]
Alias: []
---

# Bash - Install and Setup [[Developer/Git]]

*Source: *

```bash
# update and upgrade packages
sudo apt-get -y update && sudo apt-get -y upgrade

# install git
sudo apt-get -y install git

# check git version
git --version

# check path for git
which git

# configure git

# user name and email
git config --global user.name "Jimmy Briggs"
git config --global user.email "jimmy.briggs@jimbrig.com"

# default branch = 'main'
git config --global init.defaultbranch "main"

# default protocol
git config --global default.protocol "ssh"

# speed up untracked files when running git status - see https://git-scm.com/docs/git-update-index#_untracked_cache
git config --global core.untrackedCache true

# mainly for windows
git config --global core.longpaths true
git config --global autocrlf false
git config --global safecrlf warn
git config --global symlinks true

# global gitignore and gitattributes
git config --global core.excludesFile ""
git config --global core.attributesFile ""

# configure GPG signing keys
git config --global gpg.program ""
git config --global user.signingkey ""
git config --global commit.gpgSign true
git config --global tag.forceSignAnnotated true

# colors
git config --global color.ui auto

# fix whitespace
git config --global apply.whitespace fix

# help
git config --global help.autocorrect 1

# sub-modules
git config --global submodule.recurse true

# URL shorthands
git config --global 

# aliases
git config --global alias.aliases "!git config --get-regexp ^alias\\. | sed -e s/^alias\\.// -e s/\\ /\\ =\\ / | grep -v ^'alias '"
git config --global alias.l "log --pretty=oneline -n 20 --graph --abbrev-commit"





```

***

## Appendix: Links and References

- [[_README 3|Code]]
- [[Developer/Development]]
- [[OS/Linux]]
- [[_README 2|Bash]]
- [[Developer/Git]]
- [[Version Control]]
- [[GitHub]]
- [[GitHub CLI]]
- [[Development Environment Essentials]]
- [[Setup and Configure Git]]
- [[SSH]]
- [[GPG]]
- [[Configuration Management]]
- [[Dotfiles]]
- [[WSL]]
- [[Windows]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022

