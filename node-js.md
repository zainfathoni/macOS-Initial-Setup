# NodeJS Setup

## [Node Version Manager](https://github.com/nvm-sh/nvm)

<details><summary>Install <a href="https://github.com/lukechilds/zsh-nvm#as-an-oh-my-zsh-custom-plugin">as an oh-my-zsh custom plugn</a></summary>

```bash
$ git clone https://github.com/lukechilds/zsh-nvm ~/.oh-my-zsh/custom/plugins/zsh-nvm
Cloning into '/Users/zain/.oh-my-zsh/custom/plugins/zsh-nvm'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 523 (delta 1), reused 2 (delta 0), pack-reused 517
Receiving objects: 100% (523/523), 74.10 KiB | 267.00 KiB/s, done.
Resolving deltas: 100% (272/272), done.

$ source ~/.zshrc
Installing nvm...
Cloning into '/Users/zain/.nvm'...
remote: Enumerating objects: 17, done.
remote: Counting objects: 100% (17/17), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 7566 (delta 5), reused 14 (delta 4), pack-reused 7549
Receiving objects: 100% (7566/7566), 2.50 MiB | 480.00 KiB/s, done.
Resolving deltas: 100% (4777/4777), done.

# Verify Installation https://github.com/nvm-sh/nvm#verify-installation
$ command -v nvm
nvm

# Ensure Upgrade command is working https://github.com/lukechilds/zsh-nvm#upgrade
$ nvm upgrade
Installed version is v0.35.1
Checking latest version of nvm...
You're already up to date
```

</details>

## NodeJS

<details><summary>Install <a href="https://github.com/nvm-sh/nvm#long-term-support">latest LTS version of NodeJS</a></summary>

```bash
$ nvm install --lts
Installing latest LTS version.
Downloading and installing node v12.13.0...
Downloading https://nodejs.org/dist/v12.13.0/node-v12.13.0-darwin-x64.tar.gz...
######################################################################################################################################################################################################################################### 100.0%
Computing checksum with shasum -a 256
Checksums matched!
Now using node v12.13.0 (npm v6.12.0)
Creating default alias: default -> lts/* (-> v12.13.0)

# Verify Installation
$ nvm current
v12.13.0

$ node --version
v12.13.0

$ npm --version
6.12.0
```

</details>

## Yarn

<details><summary>Install <a href="https://yarnpkg.com/en/docs/install/#mac-stable">Yarn</a> using <a href="https://github.com/yarnpkg/website/issues/913#issuecomment-506660318">Installation Script</a></summary>

```bash
$ curl -o- -L https://yarnpkg.com/install.sh | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  7152    0  7152    0     0  66841      0 --:--:-- --:--:-- --:--:-- 66841
Installing Yarn!
> Downloading tarball...

[1/2]: https://yarnpkg.com/latest.tar.gz --> /var/folders/5q/bylvzmn17nd7zqyx6gsvr08h0000gn/T/yarn.tar.gz.XXXXXXXXXX.EnIkfC0T
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    93  100    93    0     0   1309      0 --:--:-- --:--:-- --:--:--  1291
100   609    0   609    0     0   1164      0 --:--:-- --:--:-- --:--:--  1164
100 1214k  100 1214k    0     0   374k      0  0:00:03  0:00:03 --:--:--  568k

[2/2]: https://yarnpkg.com/latest.tar.gz.asc --> /var/folders/5q/bylvzmn17nd7zqyx6gsvr08h0000gn/T/yarn.tar.gz.XXXXXXXXXX.EnIkfC0T.asc
100    97  100    97    0     0   4041      0 --:--:-- --:--:-- --:--:--  4041
100   613    0   613    0     0   1583      0 --:--:-- --:--:-- --:--:--  1583
100   832  100   832    0     0   1258      0 --:--:-- --:--:-- --:--:--  1258
> Verifying integrity...
gpg: key 1646B01B86E50310: public key "Yarn Packaging <yarn@dan.cx>" imported
gpg: Total number processed: 1
gpg:               imported: 1
gpg: Signature made Tue Oct  8 19:36:57 2019 +08
gpg:                using RSA key 6D98490C6F1ACDDD448E45954F77679369475BAA
gpg: Good signature from "Yarn Packaging <yarn@dan.cx>" [unknown]
gpg: WARNING: This key is not certified with a trusted signature!
gpg:          There is no indication that the signature belongs to the owner.
Primary key fingerprint: 72EC F46A 56B4 AD39 C907  BBB7 1646 B01B 86E5 0310
     Subkey fingerprint: 6D98 490C 6F1A CDDD 448E  4595 4F77 6793 6947 5BAA
> GPG signature looks good
> Extracting to ~/.yarn...
> Adding to $PATH...
> We've added the following to your /Users/zain/.zshrc
> If this isn't the profile of your current shell then please add the following to your correct profile:

export PATH="$HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH"

> Successfully installed Yarn 1.19.1! Please open another terminal where the `yarn` command will now be available.

# Verify installation
$ source ~/.zshrc
#blank

$ yarn --version
1.19.1
```

</details>
