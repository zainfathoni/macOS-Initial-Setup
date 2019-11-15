# GitLab Development Kit preparation

Based on [Install OS X prerequisites using Homebrew](https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/prepare.md#install-os-x-prerequisites-using-homebrew) section.

<details><summary>Install only missing brew formulas</summary>

```bash
# List installed formulas
$ brew list
autoconf automake coreutils gettext git libgpg-error libksba libtool libyaml openssl@1.1 pcre2 pkg-config readline zlib

# Strip out go? git pkg-config openssl node@12
$ brew install redis postgresql@10 libiconv cmake coreutils re2 graphicsmagick runit icu4c exiftool
```

</details>
