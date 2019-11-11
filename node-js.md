# NodeJS Setup

## [Node Version Manager](https://github.com/nvm-sh/nvm)

<details><summary>Install using the <a href="https://github.com/nvm-sh/nvm#install--update-script">install script</a></summary>

```bash
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | zsh
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 13527  100 13527    0     0  30534      0 --:--:-- --:--:-- --:--:-- 30466
=> Downloading nvm from git to '/Users/zain/.nvm'
=> Cloning into '/Users/zain/.nvm'...
remote: Enumerating objects: 286, done.
remote: Counting objects: 100% (286/286), done.
remote: Compressing objects: 100% (256/256), done.
remote: Total 286 (delta 34), reused 93 (delta 17), pack-reused 0
Receiving objects: 100% (286/286), 146.21 KiB | 296.00 KiB/s, done.
Resolving deltas: 100% (34/34), done.
=> Compressing and cleaning up git repository

=> Appending nvm source string to /Users/zain/.zshrc
=> Appending bash_completion source string to /Users/zain/.zshrc
=> Close and reopen your terminal to start using nvm or run the following to use it now:

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && . "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

$ source ~/.zshrc
# blank

# Verify Installation https://github.com/nvm-sh/nvm#verify-installation
$ command -v nvm
nvm
```

</details>
