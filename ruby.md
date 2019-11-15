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

Based on [GitLab Development Kit preparation](https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/prepare.md).

<details><summary>Install <a href="https://www.ruby-lang.org/en/">Ruby</a></summary>

```bash
# Install the current gitlab Ruby version https://gitlab.com/gitlab-org/gitlab/blob/master/.ruby-version
$ rvm install 2.6.3
Searching for binary rubies, this might take some time.
No binary rubies available for: osx/10.15/x86_64/ruby-2.6.3.
Continuing with compilation. Please read 'rvm help mount' to get more information on binary rubies.
Checking requirements for osx.
Installing requirements for osx.
Updating system - please wait
Installing required packages: autoconf, automake, libtool, pkg-config, coreutils, libyaml, libksba, readline, zlib, openssl@1.1 - please wait
Certificates bundle '/usr/local/etc/openssl@1.1/cert.pem' is already up to date.
Requirements installation successful.
Installing Ruby from source to: /Users/zain/.rvm/rubies/ruby-2.6.3, this may take a while depending on your cpu(s)...
ruby-2.6.3 - #downloading ruby-2.6.3, this may take a while depending on your connection...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 13.8M  100 13.8M    0     0  17.5M      0 --:--:-- --:--:-- --:--:-- 17.5M
ruby-2.6.3 - #extracting ruby-2.6.3 to /Users/zain/.rvm/src/ruby-2.6.3 - please wait
ruby-2.6.3 - #configuring - please wait
ruby-2.6.3 - #post-configuration - please wait
ruby-2.6.3 - #compiling - please wait
ruby-2.6.3 - #installing - please wait
ruby-2.6.3 - #making binaries executable - please wait
ruby-2.6.3 - #downloading rubygems-3.0.6
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  866k  100  866k    0     0  7468k      0 --:--:-- --:--:-- --:--:-- 7468k
No checksum for downloaded archive, recording checksum in user configuration.
ruby-2.6.3 - #extracting rubygems-3.0.6 - please wait
ruby-2.6.3 - #removing old rubygems - please wait
$LANG was empty, setting up LANG=en_US.US-ASCII, if it fails again try setting LANG to something sane and try again.
ruby-2.6.3 - #installing rubygems-3.0.6 - please wait
ruby-2.6.3 - #gemset created /Users/zain/.rvm/gems/ruby-2.6.3@global
ruby-2.6.3 - #importing gemset /Users/zain/.rvm/gemsets/global.gems - please wait
ruby-2.6.3 - #generating global wrappers - please wait
ruby-2.6.3 - #gemset created /Users/zain/.rvm/gems/ruby-2.6.3
ruby-2.6.3 - #importing gemsetfile /Users/zain/.rvm/gemsets/default.gems evaluated to empty gem list
ruby-2.6.3 - #generating default wrappers - please wait
ruby-2.6.3 - #adjusting #shebangs for (gem irb erb ri rdoc testrb rake).
Install of ruby-2.6.3 - #complete
Ruby was built without documentation, to build it run: rvm docs generate-ri

# Verify installation
$ ruby --version
ruby 2.6.3p62 (2019-04-16 revision 67580) [x86_64-darwin19]
```

</details>

## Bundler

Install the version of [Bundler](https://bundler.io/) specified in [Gemfile.lock](https://gitlab.com/gitlab-org/gitlab/blob/master/Gemfile.lock), right below the text `BUNDLED WITH`.

<details><summary>Install <a href="https://bundler.io/">Bundler</a></summary>
$ gem install bundler -v 1.17.3
Fetching bundler-1.17.3.gem
Successfully installed bundler-1.17.3
Parsing documentation for bundler-1.17.3
Installing ri documentation for bundler-1.17.3
Done installing documentation for bundler after 3 seconds
1 gem installed
</details>
