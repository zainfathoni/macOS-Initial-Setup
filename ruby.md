# Ruby Setup

## [Ruby Version Manager](https://rvm.io/)

<details><summary>Install <a href="https://rvm.io/rvm/security#install-our-keys">maintainer's GPG keys</a></summary>

```bash
$ gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
gpg: key 105BD0E739499BDB: public key "Piotr Kuczynski <piotr.kuczynski@gmail.com>" imported
gpg: key 3804BB82D39DC0E3: public key "Michal Papis (RVM signing) <mpapis@gmail.com>" imported
gpg: Total number processed: 2
gpg:               imported: 2

# Ensure keys are properly installed
$ gpg2 --refresh-keys
gpg: refreshing 5 keys from hkps://keys.openpgp.org
gpg: key 3804BB82D39DC0E3: "Michal Papis (RVM signing) <mpapis@gmail.com>" not changed
gpg: key 105BD0E739499BDB: "Piotr Kuczynski <piotr.kuczynski@gmail.com>" not changed
gpg: key 1646B01B86E50310: "Yarn Packaging <yarn@dan.cx>" not changed
gpg: key 3E5591EDA5F9175F: "Zain Fathoni <zain.fathoni@gmail.com>" not changed
gpg: key 76D78F0500D026C4: "GPGTools Team <team@gpgtools.org>" not changed
gpg: Total number processed: 5
gpg:              unchanged: 5
```

</details>

<details><summary>Install <a href="https://rvm.io/">RVM</a></summary>

```bash
$ \curl -sSL https://get.rvm.io | bash -s stable
Downloading https://github.com/rvm/rvm/archive/1.29.9.tar.gz
Downloading https://github.com/rvm/rvm/releases/download/1.29.9/1.29.9.tar.gz.asc
gpg: Signature made Wed Jul 10 16:31:02 2019 +08
gpg:                using RSA key 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
gpg: Good signature from "Piotr Kuczynski <piotr.kuczynski@gmail.com>" [unknown]
gpg: WARNING: This key is not certified with a trusted signature!
gpg:          There is no indication that the signature belongs to the owner.
Primary key fingerprint: 7D2B AF1C F37B 13E2 069D  6956 105B D0E7 3949 9BDB
GPG verified '/Users/zain/.rvm/archives/rvm-1.29.9.tgz'
Installing RVM to /Users/zain/.rvm/
    RVM PATH line found in /Users/zain/.zshrc.
    RVM PATH line not found for Bash, rerun this command with '--auto-dotfiles' flag to fix it.
    RVM sourcing line found in /Users/zain/.zshrc.
    RVM sourcing line not found for Bash, rerun this command with '--auto-dotfiles' flag to fix it.
Installation of RVM in /Users/zain/.rvm/ is almost complete:

  * To start using RVM you need to run `source /Users/zain/.rvm/scripts/rvm`
    in all your open shell windows, in rare cases you need to reopen all shell windows.
Thanks for installing RVM 🙏
Please consider donating to our open collective to help us maintain RVM.

👉  Donate: https://opencollective.com/rvm/donate

# Verify Installation
$ rvm --version
rvm 1.29.9 (latest) by Michal Papis, Piotr Kuczynski, Wayne E. Seguin [https://rvm.io]
```

</details>

## Ruby

<details><summary>Install <a href="">Ruby</a></summary>

```bash
# TODO:
```

</details>
