Awesome CLI is a simple command line tool to give you a fancy command line interface to dive into [Awesome](https://github.com/sindresorhus/awesome) lists.

[![AWESOME CLI](https://github.com/umutphp/awesome-cli/raw/master/assets/images/awesome-cli-banner.png)](https://github.com/umutphp/awesome-cli/blob/master/assets/images/awesome-cli-banner.png)

[![Build](https://github.com/umutphp/awesome-cli/workflows/Test%20&%20Build/badge.svg)](https://github.com/umutphp/awesome-cli/workflows/Test%20&%20Build/badge.svg) [![WOSPM Checker](https://github.com/umutphp/awesome-cli/workflows/WOSPM%20Checker/badge.svg)](https://github.com/umutphp/awesome-cli/workflows/WOSPM%20Checker/badge.svg)

___

-   [Introduction](https://github.com/umutphp/awesome-cli#introduction)
-   [How To Use](https://github.com/umutphp/awesome-cli#how-to-use)
    -   [Interactive Mode](https://github.com/umutphp/awesome-cli#interactive-mode)
    -   [Random Mode](https://github.com/umutphp/awesome-cli#random-mode)
    -   [Surprise Mode](https://github.com/umutphp/awesome-cli#surprise-mode)
-   [How To Install](https://github.com/umutphp/awesome-cli#how-to-install)
    -   [Basic](https://github.com/umutphp/awesome-cli#basic)
    -   [Build as binary](https://github.com/umutphp/awesome-cli#build-as-binary)
    -   [Download and use official binary](https://github.com/umutphp/awesome-cli#download-and-use-official-binary)
    -   [CLI Options](https://github.com/umutphp/awesome-cli#cli-options)
    -   [Sample Execution](https://github.com/umutphp/awesome-cli#sample-execution)
-   [How To Contribute](https://github.com/umutphp/awesome-cli#how-to-contribute)

___

## Introduction

The CLI starts with the root repository [sindresorhus/awesome](https://github.com/sindresorhus/awesome) and guides to to the final repo according to your choices. It fetches Readme files of the repositories and parses them to create the select lists. So, the CLI needs a working network :). It also uses file caches to cache the Readme file contents. You can find the cache folder with name ".awesomecache" under your home folder.

[![Avesome-cli Sample](https://github.com/umutphp/awesome-cli/raw/master/assets/images/awesome-cli.gif)](https://github.com/umutphp/awesome-cli/blob/master/assets/images/awesome-cli.gif)

## How To Use

### Interactive Mode

In order to use awesome-cli interactively, just execute it without giving any option. You will walk through the categories and repositories by using "↓ ↑ → ←" buttons. Your choices will be saved to use them in [surprise mode](https://github.com/umutphp/awesome-cli#surprise-mode).

\> $ awesome-cli
Use the arrow keys to navigate: ↓ ↑ → ← 
? Select from 'Awesome' list: 
  ▸ Platforms
    Programming Languages
    Front-End Development
    Back-End Development
    Computer Science
    Big Data
    Theory
    Books
    Editors
↓   Gaming

### Random Mode

You can use "random" option to go a random awesome repository under a random category.

\> $ awesome-cli random
aweome-cli Version 0.3.0
✔ Programming Languages
✔ Eta
✔ Community
✔ IRC
https://kiwiirc.com/client/irc.freenode.net/#eta-lang

### Surprise Mode

When you use "surprise" option, awesome-cli will use your previous selections in [interactive mode](https://github.com/umutphp/awesome-cli#interactive-mode) to find a random repository for you.

\> $ awesome-cli surprise
aweome-cli Version 0.3.0
✔ Back-End Development
✔ Docker
✔ Videos
✔ From Local Docker Development to Production Deployments
https://www.youtube.com/watch?v=7CZFpHUPqXw

## How To Install

### Basic

Follow the steps;

\> $ git clone git@github.com:umutphp/awesome-cli.git
\> $ cd awesome-cli
\> $ go run main.go

### Build as binary

Follow the steps;

\> $ git clone git@github.com:umutphp/awesome-cli.git
\> $ cd awesome-cli
\> $ sudo go build -o /usr/local/bin/awesome-cli .
\> $ awesome-cli

### Download and use official binary

Visit the [latest release](https://github.com/umutphp/awesome-cli/releases/latest) page and download the binary correspondingly.

\> $ wget -O /usr/local/bin/awesome-cli https://latest-binary-url
\> $ awesome-cli

### CLI Options

The CLI works in interactive mode without any given option. But, It can be also called some options described below;

\> $ awesome-cli help
awesome-cli Version 0.6.0

Options of awesome-cli:
  help      To print this screen.
  random    To go to a random awesome content.
  surprise  To go to a surprise awesome content according to your previos choices.
  profile   To see your previous choices.
  reset     To clean your choices to start from the beginning.
  update    Update awesome-cli to the latest version.

### Sample Execution

\> $ awesome-cli random
aweome-cli Version 0.2.0
✔ Platforms
✔ Linux
✔ Applications
✔ Gedit
https://wiki.gnome.org/Apps/Gedit

## How To Contribute

Please follow the instructions in [CONTRIBUTING](https://github.com/umutphp/awesome-cli/blob/master/CONTRIBUTING.md) file and beware of [CODE\_OF\_CONDUCT](https://github.com/umutphp/awesome-cli/blob/master/CODE_OF_CONDUCT).