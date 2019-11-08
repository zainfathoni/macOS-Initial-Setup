# Terminal Setup

## Basic Environment

### Default Shell

Right after installing [iTerm2], you must be getting this prompt:

> The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit [Use zsh as the default shell on your Mac](https://support.apple.com/kb/HT208050).

As instructed, run

```bash
$ chsh -s /bin/zsh
```

### Package Manager

Install [Homebrew](https://brew.sh/) package manager.

```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Git Version

Install [the latest Git version](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git#Installing-on-Mac) using Homebrew

```bash
$ brew install git
```

- [ ] Clone [dotfiles](https://github.com/zainfathoni/dotfiles)
