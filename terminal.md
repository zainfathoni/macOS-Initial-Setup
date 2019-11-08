# Terminal Setup

## Basic Environment

### Default Shell

Right after installing [iTerm2](https://iterm2.com/), you must be getting this prompt:

> The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit [Use zsh as the default shell on your Mac](https://support.apple.com/kb/HT208050).

<details><summary>chsh -s /bin/zsh</summary>

```bash
$ chsh -s /bin/zsh
Changing shell for zain.
Password for zain:
```

</details>

### Package Manager

Install [Homebrew](https://brew.sh/) package manager.

<details><summary>/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</summary>

```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
==> This script will install:
/usr/local/bin/brew
/usr/local/share/doc/homebrew
/usr/local/share/man/man1/brew.1
/usr/local/share/zsh/site-functions/_brew
/usr/local/etc/bash_completion.d/brew
/usr/local/Homebrew
==> The following new directories will be created:
/usr/local/bin
/usr/local/etc
/usr/local/include
/usr/local/lib
/usr/local/sbin
/usr/local/share
/usr/local/var
/usr/local/opt
/usr/local/share/zsh
/usr/local/share/zsh/site-functions
/usr/local/var/homebrew
/usr/local/var/homebrew/linked
/usr/local/Cellar
/usr/local/Caskroom
/usr/local/Homebrew
/usr/local/Frameworks
==> The Xcode Command Line Tools will be installed.

Press RETURN to continue or any other key to abort
==> /usr/bin/sudo /bin/mkdir -p /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
Password:
==> /usr/bin/sudo /bin/chmod g+rwx /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
==> /usr/bin/sudo /bin/chmod 755 /usr/local/share/zsh /usr/local/share/zsh/site-functions
==> /usr/bin/sudo /usr/sbin/chown zain /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
==> /usr/bin/sudo /usr/bin/chgrp admin /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
==> /usr/bin/sudo /bin/mkdir -p /Users/zain/Library/Caches/Homebrew
==> /usr/bin/sudo /bin/chmod g+rwx /Users/zain/Library/Caches/Homebrew
==> /usr/bin/sudo /usr/sbin/chown zain /Users/zain/Library/Caches/Homebrew
==> Searching online for the Command Line Tools
==> /usr/bin/sudo /usr/bin/touch /tmp/.com.apple.dt.CommandLineTools.installondemand.in-progress
==> Installing Command Line Tools for Xcode-11.2
==> /usr/bin/sudo /usr/sbin/softwareupdate -i Command\ Line\ Tools\ for\ Xcode-11.2
Software Update Tool


Downloading Command Line Tools for Xcode
Downloaded Command Line Tools for Xcode
Installing Command Line Tools for Xcode
Done with Command Line Tools for Xcode
Done.
==> /usr/bin/sudo /bin/rm -f /tmp/.com.apple.dt.CommandLineTools.installondemand.in-progress
==> /usr/bin/sudo /usr/bin/xcode-select --switch /Library/Developer/CommandLineTools
==> Downloading and installing Homebrew...
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (16/16), done.
remote: Total 128580 (delta 6), reused 1 (delta 0), pack-reused 128564
Receiving objects: 100% (128580/128580), 30.65 MiB | 7.56 MiB/s, done.
Resolving deltas: 100% (94350/94350), done.
From https://github.com/Homebrew/brew
 * [new branch]      master     -> origin/master
 * [new tag]         0.1        -> 0.1
 * [new tag]         0.2        -> 0.2
 * [new tag]         0.3        -> 0.3
 * [new tag]         0.4        -> 0.4
 * [new tag]         0.5        -> 0.5
 * [new tag]         0.6        -> 0.6
 * [new tag]         0.7        -> 0.7
 * [new tag]         0.7.1      -> 0.7.1
 * [new tag]         0.8        -> 0.8
 * [new tag]         0.8.1      -> 0.8.1
 * [new tag]         0.9        -> 0.9
 * [new tag]         0.9.1      -> 0.9.1
 * [new tag]         0.9.2      -> 0.9.2
 * [new tag]         0.9.3      -> 0.9.3
 * [new tag]         0.9.4      -> 0.9.4
 * [new tag]         0.9.5      -> 0.9.5
 * [new tag]         0.9.8      -> 0.9.8
 * [new tag]         0.9.9      -> 0.9.9
 * [new tag]         1.0.0      -> 1.0.0
 * [new tag]         1.0.1      -> 1.0.1
 * [new tag]         1.0.2      -> 1.0.2
 * [new tag]         1.0.3      -> 1.0.3
 * [new tag]         1.0.4      -> 1.0.4
 * [new tag]         1.0.5      -> 1.0.5
 * [new tag]         1.0.6      -> 1.0.6
 * [new tag]         1.0.7      -> 1.0.7
 * [new tag]         1.0.8      -> 1.0.8
 * [new tag]         1.0.9      -> 1.0.9
 * [new tag]         1.1.0      -> 1.1.0
 * [new tag]         1.1.1      -> 1.1.1
 * [new tag]         1.1.10     -> 1.1.10
 * [new tag]         1.1.11     -> 1.1.11
 * [new tag]         1.1.12     -> 1.1.12
 * [new tag]         1.1.13     -> 1.1.13
 * [new tag]         1.1.2      -> 1.1.2
 * [new tag]         1.1.3      -> 1.1.3
 * [new tag]         1.1.4      -> 1.1.4
 * [new tag]         1.1.5      -> 1.1.5
 * [new tag]         1.1.6      -> 1.1.6
 * [new tag]         1.1.7      -> 1.1.7
 * [new tag]         1.1.8      -> 1.1.8
 * [new tag]         1.1.9      -> 1.1.9
 * [new tag]         1.2.0      -> 1.2.0
 * [new tag]         1.2.1      -> 1.2.1
 * [new tag]         1.2.2      -> 1.2.2
 * [new tag]         1.2.3      -> 1.2.3
 * [new tag]         1.2.4      -> 1.2.4
 * [new tag]         1.2.5      -> 1.2.5
 * [new tag]         1.2.6      -> 1.2.6
 * [new tag]         1.3.0      -> 1.3.0
 * [new tag]         1.3.1      -> 1.3.1
 * [new tag]         1.3.2      -> 1.3.2
 * [new tag]         1.3.3      -> 1.3.3
 * [new tag]         1.3.4      -> 1.3.4
 * [new tag]         1.3.5      -> 1.3.5
 * [new tag]         1.3.6      -> 1.3.6
 * [new tag]         1.3.7      -> 1.3.7
 * [new tag]         1.3.8      -> 1.3.8
 * [new tag]         1.3.9      -> 1.3.9
 * [new tag]         1.4.0      -> 1.4.0
 * [new tag]         1.4.1      -> 1.4.1
 * [new tag]         1.4.2      -> 1.4.2
 * [new tag]         1.4.3      -> 1.4.3
 * [new tag]         1.5.0      -> 1.5.0
 * [new tag]         1.5.1      -> 1.5.1
 * [new tag]         1.5.10     -> 1.5.10
 * [new tag]         1.5.11     -> 1.5.11
 * [new tag]         1.5.12     -> 1.5.12
 * [new tag]         1.5.13     -> 1.5.13
 * [new tag]         1.5.14     -> 1.5.14
 * [new tag]         1.5.2      -> 1.5.2
 * [new tag]         1.5.3      -> 1.5.3
 * [new tag]         1.5.4      -> 1.5.4
 * [new tag]         1.5.5      -> 1.5.5
 * [new tag]         1.5.6      -> 1.5.6
 * [new tag]         1.5.7      -> 1.5.7
 * [new tag]         1.5.8      -> 1.5.8
 * [new tag]         1.5.9      -> 1.5.9
 * [new tag]         1.6.0      -> 1.6.0
 * [new tag]         1.6.1      -> 1.6.1
 * [new tag]         1.6.10     -> 1.6.10
 * [new tag]         1.6.11     -> 1.6.11
 * [new tag]         1.6.12     -> 1.6.12
 * [new tag]         1.6.13     -> 1.6.13
 * [new tag]         1.6.14     -> 1.6.14
 * [new tag]         1.6.15     -> 1.6.15
 * [new tag]         1.6.16     -> 1.6.16
 * [new tag]         1.6.17     -> 1.6.17
 * [new tag]         1.6.2      -> 1.6.2
 * [new tag]         1.6.3      -> 1.6.3
 * [new tag]         1.6.4      -> 1.6.4
 * [new tag]         1.6.5      -> 1.6.5
 * [new tag]         1.6.6      -> 1.6.6
 * [new tag]         1.6.7      -> 1.6.7
 * [new tag]         1.6.8      -> 1.6.8
 * [new tag]         1.6.9      -> 1.6.9
 * [new tag]         1.7.0      -> 1.7.0
 * [new tag]         1.7.1      -> 1.7.1
 * [new tag]         1.7.2      -> 1.7.2
 * [new tag]         1.7.3      -> 1.7.3
 * [new tag]         1.7.4      -> 1.7.4
 * [new tag]         1.7.5      -> 1.7.5
 * [new tag]         1.7.6      -> 1.7.6
 * [new tag]         1.7.7      -> 1.7.7
 * [new tag]         1.8.0      -> 1.8.0
 * [new tag]         1.8.1      -> 1.8.1
 * [new tag]         1.8.2      -> 1.8.2
 * [new tag]         1.8.3      -> 1.8.3
 * [new tag]         1.8.4      -> 1.8.4
 * [new tag]         1.8.5      -> 1.8.5
 * [new tag]         1.8.6      -> 1.8.6
 * [new tag]         1.9.0      -> 1.9.0
 * [new tag]         1.9.1      -> 1.9.1
 * [new tag]         1.9.2      -> 1.9.2
 * [new tag]         1.9.3      -> 1.9.3
 * [new tag]         2.0.0      -> 2.0.0
 * [new tag]         2.0.1      -> 2.0.1
 * [new tag]         2.0.2      -> 2.0.2
 * [new tag]         2.0.3      -> 2.0.3
 * [new tag]         2.0.4      -> 2.0.4
 * [new tag]         2.0.5      -> 2.0.5
 * [new tag]         2.0.6      -> 2.0.6
 * [new tag]         2.1.0      -> 2.1.0
 * [new tag]         2.1.1      -> 2.1.1
 * [new tag]         2.1.10     -> 2.1.10
 * [new tag]         2.1.11     -> 2.1.11
 * [new tag]         2.1.12     -> 2.1.12
 * [new tag]         2.1.13     -> 2.1.13
 * [new tag]         2.1.14     -> 2.1.14
 * [new tag]         2.1.15     -> 2.1.15
 * [new tag]         2.1.16     -> 2.1.16
 * [new tag]         2.1.2      -> 2.1.2
 * [new tag]         2.1.3      -> 2.1.3
 * [new tag]         2.1.4      -> 2.1.4
 * [new tag]         2.1.5      -> 2.1.5
 * [new tag]         2.1.6      -> 2.1.6
 * [new tag]         2.1.7      -> 2.1.7
 * [new tag]         2.1.8      -> 2.1.8
 * [new tag]         2.1.9      -> 2.1.9
HEAD is now at e2c76cce8 Merge pull request #6713 from papz/master
==> Homebrew is run entirely by unpaid volunteers. Please consider donating:
  https://github.com/Homebrew/brew#donations
==> Tapping homebrew/core
Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-core'...
remote: Enumerating objects: 5084, done.
remote: Counting objects: 100% (5084/5084), done.
remote: Compressing objects: 100% (4879/4879), done.
remote: Total 5084 (delta 45), reused 380 (delta 10), pack-reused 0
Receiving objects: 100% (5084/5084), 4.17 MiB | 1.97 MiB/s, done.
Resolving deltas: 100% (45/45), done.
Tapped 2 commands and 4867 formulae (5,126 files, 12.9MB).
Already up-to-date.
==> Installation successful!

==> Homebrew has enabled anonymous aggregate formulae and cask analytics.
Read the analytics documentation (and how to opt-out) here:
  https://docs.brew.sh/Analytics

==> Homebrew is run entirely by unpaid volunteers. Please consider donating:
  https://github.com/Homebrew/brew#donations
==> Next steps:
- Run `brew help` to get started
- Further documentation:
    https://docs.brew.sh
```

</details>

### Official Git

Install [the latest official Git version](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git#Installing-on-Mac) (as opposed to the [Apple Git version](http://modulesunraveled.com/installing-git/updating-git-if-you-have-version-apple-well-official-install)) using Homebrew.

<details><summary>brew install git</summary>

```bash
$ brew install git
==> Installing dependencies for git: gettext and pcre2
==> Installing git dependency: gettext
==> Downloading https://homebrew.bintray.com/bottles/gettext-0.20.1.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/10/107d7f386fbeea6979f9376cdbbcf3f60943caaad61bdc754d3019ce625dffe6?__gda__=exp=1573233830~hmac=1bcb001fb839dc8886
######################################################################## 100.0%
==> Pouring gettext-0.20.1.catalina.bottle.tar.gz
==> Caveats
gettext is keg-only, which means it was not symlinked into /usr/local,
because macOS provides the BSD gettext library & some software gets confused if both are in the library path.

If you need to have gettext first in your PATH run:
  echo 'export PATH="/usr/local/opt/gettext/bin:$PATH"' >> ~/.zshrc

For compilers to find gettext you may need to set:
  export LDFLAGS="-L/usr/local/opt/gettext/lib"
  export CPPFLAGS="-I/usr/local/opt/gettext/include"

==> Summary
🍺  /usr/local/Cellar/gettext/0.20.1: 1,893 files, 18.4MB
==> Installing git dependency: pcre2
==> Downloading https://homebrew.bintray.com/bottles/pcre2-10.33.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/7b/7b92993a7ad0487cabc4395e3633d8294896fa9ffa9e46507d9a7ef25a213ab8?__gda__=exp=1573233836~hmac=931bf03fae3350118d
######################################################################## 100.0%
==> Pouring pcre2-10.33.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/pcre2/10.33: 226 files, 5.8MB
==> Installing git
==> Downloading https://homebrew.bintray.com/bottles/git-2.24.0.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/fa/fa754c684673a191b999528995c1dc4b0d597a95ed6a2b1dd213c8e7018885ab?__gda__=exp=1573233845~hmac=94da9661072522e3cf
######################################################################## 100.0%
==> Pouring git-2.24.0.catalina.bottle.tar.gz
==> Caveats
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d

zsh completions and functions have been installed to:
  /usr/local/share/zsh/site-functions

Emacs Lisp files have been installed to:
  /usr/local/share/emacs/site-lisp/git
==> Summary
🍺  /usr/local/Cellar/git/2.24.0: 1,547 files, 45.5MB
==> Caveats
==> gettext
gettext is keg-only, which means it was not symlinked into /usr/local,
because macOS provides the BSD gettext library & some software gets confused if both are in the library path.

If you need to have gettext first in your PATH run:
  echo 'export PATH="/usr/local/opt/gettext/bin:$PATH"' >> ~/.zshrc

For compilers to find gettext you may need to set:
  export LDFLAGS="-L/usr/local/opt/gettext/lib"
  export CPPFLAGS="-I/usr/local/opt/gettext/include"

==> git
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d

zsh completions and functions have been installed to:
  /usr/local/share/zsh/site-functions

Emacs Lisp files have been installed to:
  /usr/local/share/emacs/site-lisp/git
```

</details>

### Dotfiles

Clone your personal [dotfiles](https://github.com/zainfathoni/dotfiles) repository over **HTTPS** using [personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line).

<details><summary>https://git.io/dotbot</summary>

```bash
$ git clone https://github.com/zainfathoni/dotfiles.git
Cloning into 'dotfiles'...
remote: Enumerating objects: 56, done.
remote: Counting objects: 100% (56/56), done.
remote: Compressing objects: 100% (40/40), done.
remote: Total 164 (delta 21), reused 46 (delta 15), pack-reused 108
Receiving objects: 100% (164/164), 54.99 KiB | 244.00 KiB/s, done.
Resolving deltas: 100% (74/74), done.

$ cd dotfiles

$ ./install
Submodule 'dotbot' (https://github.com/anishathalye/dotbot) registered for path 'dotbot'
Cloning into '/Users/zain/Code/GitHub/zainfathoni/dotfiles/dotbot'...
Submodule path 'dotbot': checked out 'fe9ca6f5ede35d16f28e0c5db781fb39437fd171'
Submodule 'lib/pyyaml' (https://github.com/anishathalye/pyyaml) registered for path 'dotbot/lib/pyyaml'
Cloning into '/Users/zain/Code/GitHub/zainfathoni/dotfiles/dotbot/lib/pyyaml'...
Submodule path 'dotbot/lib/pyyaml': checked out 'f30c956c11aa6b5e7827fe5840cc9ed40b938d17'
All targets have been cleaned
Creating link ~/bamboo-agent.cfg.xml -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/bamboo-agent.cfg.xml
Creating link ~/.dotfiles -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/
Creating link ~/.gitconfig -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/gitconfig
Creating link ~/.gitconfig_ninjavan -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/gitconfig_ninjavan
Creating link ~/.gitconfig_zainfathoni -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/gitconfig_zainfathoni
Creating link ~/.gitignore_global -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/gitignore_global
Creating directory /Users/zain/.ssh
Creating link ~/.ssh/config -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/ssh/config
Creating link ~/.ssl -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/ssl
Creating link ~/.vimrc -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/vimrc
Creating link ~/.zsh -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/zsh
Creating link ~/.zshrc -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/zshrc
All links have been set up

==> All tasks executed successfully
```

</details>

### SSH

[Add your SSH key to the ssh-agent](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#adding-your-ssh-key-to-the-ssh-agent)

<details><summary>Start the ssh-agent in the background.</summary>

```bash
$ eval "$(ssh-agent -s)"
Agent pid 27674
```

</details>

<details><summary>Symlink SSH keys from <a href="https://www.box.com/resources/downloads">Box</a> folder</summary>

```bash
$ chmod +x ~/Box/dotfiles/install-ssh-keys.sh

$ ~/Box/dotfiles/install-ssh-keys.sh

$ ls -al ~/.ssh
total 0
drwxr-xr-x   5 zain  staff   160 Nov  9 02:11 .
drwxr-xr-x+ 37 zain  staff  1184 Nov  9 02:11 ..
lrwxr-xr-x   1 zain  staff    55 Nov  9 01:57 config -> /Users/zain/Code/GitHub/zainfathoni/dotfiles/ssh/config
lrwxr-xr-x   1 zain  staff    41 Nov  9 02:11 zainfathoni -> /Users/zain/Box/dotfiles/.ssh/zainfathoni
lrwxr-xr-x   1 zain  staff    45 Nov  9 02:11 zainfathoni.pub -> /Users/zain/Box/dotfiles/.ssh/zainfathoni.pub
```

</details>

<details><summary>Add your SSH private key to the ssh-agent and store your passphrase in the keychain</summary>

```bash
$ ssh-add -K ~/.ssh/zainfathoni
Enter passphrase for /Users/zain/.ssh/zainfathoni:
Identity added: /Users/zain/.ssh/zainfathoni (/Users/zain/.ssh/zainfathoni)
```

</details>

## Advanced Environment

### GPG Key for [signing commits](https://help.github.com/en/github/authenticating-to-github/signing-commits)

#### 1. Install [GPG Suite](https://gpgtools.org/).

Refer to their [first steps](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-mail) tutorial if necessary.

#### 2. Install [LastPass binary-version](https://apps.apple.com/id/app/lastpass-password-manager/id926036361?mt=12) from AppStore

So you can download your GPG secret key file.

<details><summary>GPG Key file stored at LastPass</summary>
<img width="382" alt="GPG Key file stored at LastPass" src="https://user-images.githubusercontent.com/6315466/68503184-2a681d80-025a-11ea-989a-a8aa6cf657b6.png">
</details>

#### 3. Import GPG Key to GPG Keychain

<details><summary>Import GPG Key to GPG Keychain</summary>
<img width="1217" alt="Import GPG Key to GPG Keychain" src="https://user-images.githubusercontent.com/6315466/68503332-787d2100-025a-11ea-81fd-57fac6b0a2bc.png">
</details>

#### 4. If you performed above steps properly, when you're committing in Visual Studio Code for the first time, you will be prompted for a passphrase to unlock your OpenPGP secret key.

Please make sure that you check ✅ **Save in Keychain** so that you don't need to enter the passphrase anymore in the future.

<details><summary>Save GPG Passphrase in Keychain</summary>
<img width="657" alt="Save GPG Passphrase in Keychain" src="https://user-images.githubusercontent.com/6315466/68504245-774cf380-025c-11ea-9be4-f36be153c301.png">
</details>

#### 5. To ensure that it's working, restart the laptop and try committing again through Visual Studio Code.

You should not be required to enter the passphrase anymore while keep getting your commits signed properly.

<details><summary>Signed Commits 🎉</summary>
<img width="902" alt="Signed Commits" src="https://user-images.githubusercontent.com/6315466/68505182-87fe6900-025e-11ea-8342-d5ab5d217e23.png">
</details>

## Cosmetics

Based on [Badassify your terminal and shell](https://jilles.me/badassify-your-terminal-and-shell/) article.

### Install [oh-my-zsh](https://ohmyz.sh/)

<details><summary>Install oh-my-zsh</summary>

```bash
$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
Cloning Oh My Zsh...
Cloning into '/Users/zain/.oh-my-zsh'...
remote: Enumerating objects: 1102, done.
remote: Counting objects: 100% (1102/1102), done.
remote: Compressing objects: 100% (1054/1054), done.
remote: Total 1102 (delta 23), reused 884 (delta 19), pack-reused 0
Receiving objects: 100% (1102/1102), 721.38 KiB | 401.00 KiB/s, done.
Resolving deltas: 100% (23/23), done.

Looking for an existing zsh config...
Found ~/.zshrc. Backing up to /Users/zain/.zshrc.pre-oh-my-zsh
Using the Oh My Zsh template file and adding it to ~/.zshrc.

         __                                     __
  ____  / /_     ____ ___  __  __   ____  _____/ /_
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                        /____/                       ....is now installed!


Please look over the ~/.zshrc file to select plugins, themes, and options.

p.s. Follow us on https://twitter.com/ohmyzsh

p.p.s. Get stickers, shirts, and coffee mugs at https://shop.planetargon.com/collections/oh-my-zsh
```

</details>

### Install [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh)

<details><summary>Install zsh-autosuggestions</summary>

```bash
$ git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
Cloning into '/Users/zain/.oh-my-zsh/custom/plugins/zsh-autosuggestions'...
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 2275 (delta 2), reused 4 (delta 0), pack-reused 2266
Receiving objects: 100% (2275/2275), 519.66 KiB | 586.00 KiB/s, done.
Resolving deltas: 100% (1449/1449), done.
```

### Install [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

<details><summary>Install zsh-syntax-highlighting</summary>

```bash
$ cd ~/.oh-my-zsh && git clone git://github.com/zsh-users/zsh-syntax-highlighting.git
Cloning into 'zsh-syntax-highlighting'...
remote: Enumerating objects: 104, done.
remote: Counting objects: 100% (104/104), done.
remote: Compressing objects: 100% (65/65), done.
remote: Total 5492 (delta 66), reused 70 (delta 39), pack-reused 5388
Receiving objects: 100% (5492/5492), 1.13 MiB | 340.00 KiB/s, done.
Resolving deltas: 100% (3642/3642), done.
```

</details>

### Install [z](https://github.com/rupa/z)

<details><summary>Install z</summary>

```bash
$ brew install z
==> Downloading https://github.com/rupa/z/archive/v1.9.tar.gz
==> Downloading from https://codeload.github.com/rupa/z/tar.gz/v1.9
##O#- #
==> Caveats
For Bash or Zsh, put something like this in your $HOME/.bashrc or $HOME/.zshrc:
  . /usr/local/etc/profile.d/z.sh
==> Summary
🍺  /usr/local/Cellar/z/1.9: 5 files, 20.7KB, built in 4 seconds
```

</details>
