# Google Chrome Setup

This setup is necessary if you want to use [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) to run Selenium tests in your machine.
Again, this is also based on [GitLab Development Kit preparation](https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/prepare.md).

<details><summary><a href="https://www.kenst.com/2015/03/installing-chromedriver-on-mac-osx/">Install ChromeDriver using Homebrew</a></summary>

```bash
$ brew cask install chromedriver
==> Tapping homebrew/cask
Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask'...
remote: Enumerating objects: 3575, done.
remote: Counting objects: 100% (3575/3575), done.
remote: Compressing objects: 100% (3564/3564), done.
remote: Total 3575 (delta 27), reused 462 (delta 9), pack-reused 0
Receiving objects: 100% (3575/3575), 1.20 MiB | 1.29 MiB/s, done.
Resolving deltas: 100% (27/27), done.
Tapped 1 command and 3463 casks (3,581 files, 3.9MB).
==> Downloading https://chromedriver.storage.googleapis.com/78.0.3904.70/chromedriver_mac64.zip
######################################################################## 100.0%
==> Verifying SHA-256 checksum for Cask 'chromedriver'.
==> Installing Cask chromedriver
==> Linking Binary 'chromedriver' to '/usr/local/bin/chromedriver'.
🍺  chromedriver was successfully installed!

# Verify installation
$ chromedriver --version
ChromeDriver 78.0.3904.70 (edb9c9f3de0247fd912a77b7f6cae7447f6d3ad5-refs/branch-heads/3904@{#800})
```

</details>
