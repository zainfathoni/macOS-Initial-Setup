# GitLab Development Kit Preparation

Based on [Install OS X prerequisites using Homebrew](https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/prepare.md#install-os-x-prerequisites-using-homebrew) section.

<details><summary>Install only missing brew formulas</summary>

```bash
# List installed formulas
$ brew list
autoconf automake coreutils gettext git libgpg-error libksba libtool libyaml openssl@1.1 pcre2 pkg-config readline zlib

# Strip out git pkg-config openssl coreutils node@12 yarn google-chrome chromedriver
$ brew install redis postgresql@10 libiconv cmake re2 graphicsmagick runit icu4c exiftool
==> Downloading https://homebrew.bintray.com/bottles/redis-5.0.6.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/8a/8ae4fed5494daa20391ab16d4be0ba4eca3d55235c02aa576604bee568559608?__gda__=exp=1573853247~hmac=72a7e3c02643c2dff205e23e4b9178e1147aacd059685d8dcdcf57730456ee2b&response-content-disposition=at
######################################################################## 100.0%
==> Pouring redis-5.0.6.catalina.bottle.tar.gz
==> Caveats
To have launchd start redis now and restart at login:
  brew services start redis
Or, if you don't want/need a background service you can just run:
  redis-server /usr/local/etc/redis.conf
==> Summary
🍺  /usr/local/Cellar/redis/5.0.6: 13 files, 3.1MB
==> Installing dependencies for postgresql@10: icu4c
==> Installing postgresql@10 dependency: icu4c
==> Downloading https://homebrew.bintray.com/bottles/icu4c-64.2.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/e9/e9ae7bb5a76b48e82f56bc744eaaa1e9bdb5ca49ea6b5a2e4d52f57ad331f063?__gda__=exp=1573853253~hmac=42367c9441f3b80903c3ca1222ff8bbe74bc6a103c151ebc33e39125d24586bc&response-content-disposition=at
######################################################################## 100.0%
==> Pouring icu4c-64.2.catalina.bottle.tar.gz
==> Caveats
icu4c is keg-only, which means it was not symlinked into /usr/local,
because macOS provides libicucore.dylib (but nothing else).

If you need to have icu4c first in your PATH run:
  echo 'export PATH="/usr/local/opt/icu4c/bin:$PATH"' >> ~/.zshrc
  echo 'export PATH="/usr/local/opt/icu4c/sbin:$PATH"' >> ~/.zshrc

For compilers to find icu4c you may need to set:
  export LDFLAGS="-L/usr/local/opt/icu4c/lib"
  export CPPFLAGS="-I/usr/local/opt/icu4c/include"

For pkg-config to find icu4c you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/icu4c/lib/pkgconfig"

==> Summary
🍺  /usr/local/Cellar/icu4c/64.2: 257 files, 69.3MB
==> Installing postgresql@10
==> Downloading https://homebrew.bintray.com/bottles/postgresql@10-10.10_1.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/36/366f1eeb324e064dc0dc7feb2daec0c516cd8f3efcdaeacf5dd3ac18b09e3eef?__gda__=exp=1573853268~hmac=a296d6d0079b141d0447de6c7e66fca562421a6ba31d65d13c5fe1f94ac35717&response-content-disposition=at
######################################################################## 100.0%
==> Pouring postgresql@10-10.10_1.catalina.bottle.tar.gz
==> /usr/local/Cellar/postgresql@10/10.10_1/bin/initdb /usr/local/var/postgresql@10
==> Caveats
To migrate existing data from a previous major version of PostgreSQL run:
  brew postgresql-upgrade-database

postgresql@10 is keg-only, which means it was not symlinked into /usr/local,
because this is an alternate version of another formula.

If you need to have postgresql@10 first in your PATH run:
  echo 'export PATH="/usr/local/opt/postgresql@10/bin:$PATH"' >> ~/.zshrc

For compilers to find postgresql@10 you may need to set:
  export LDFLAGS="-L/usr/local/opt/postgresql@10/lib"
  export CPPFLAGS="-I/usr/local/opt/postgresql@10/include"

For pkg-config to find postgresql@10 you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/postgresql@10/lib/pkgconfig"


To have launchd start postgresql@10 now and restart at login:
  brew services start postgresql@10
Or, if you don't want/need a background service you can just run:
  pg_ctl -D /usr/local/var/postgresql@10 start
==> Summary
🍺  /usr/local/Cellar/postgresql@10/10.10_1: 1,708 files, 21.7MB
==> Downloading https://homebrew.bintray.com/bottles/libiconv-1.16.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/24/24d81638fcd7416a56c3dbdac7e2265d7b0476b17a71b631045425380122e6b1?__gda__=exp=1573853291~hmac=9f71887fa2b28f8b36ef4ec04da2bcaa90f9f2ee1e5cadd76bf7832483e24642&response-content-disposition=at
######################################################################## 100.0%
==> Pouring libiconv-1.16.catalina.bottle.tar.gz
==> Caveats
libiconv is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

If you need to have libiconv first in your PATH run:
  echo 'export PATH="/usr/local/opt/libiconv/bin:$PATH"' >> ~/.zshrc

For compilers to find libiconv you may need to set:
  export LDFLAGS="-L/usr/local/opt/libiconv/lib"
  export CPPFLAGS="-I/usr/local/opt/libiconv/include"

==> Summary
🍺  /usr/local/Cellar/libiconv/1.16: 30 files, 2.4MB
==> Downloading https://homebrew.bintray.com/bottles/cmake-3.15.5.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/46/46b47f448f7690bbed70526a42f27bea54aa7562c9eefb86955102fc83d1366d?__gda__=exp=1573853297~hmac=459a8fd3f06db57ead2e7bf30e438a85609b9064460bab2fb465ed1de16d5211&response-content-disposition=at
######################################################################## 100.0%
==> Pouring cmake-3.15.5.catalina.bottle.tar.gz
==> Caveats
Emacs Lisp files have been installed to:
  /usr/local/share/emacs/site-lisp/cmake
==> Summary
🍺  /usr/local/Cellar/cmake/3.15.5: 5,801 files, 53.4MB
==> Downloading https://homebrew.bintray.com/bottles/re2-20191101.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/08/08eb2896f304e147b44fc2b3ef9631277bc09bc2ac574e8d8d951e0349c4858b?__gda__=exp=1573853312~hmac=c66b709850c20ab1b700a6b6f17a7952b7c3dea024c06b6091001e328887c54c&response-content-disposition=at
######################################################################## 100.0%
==> Pouring re2-20191101.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/re2/20191101: 14 files, 1MB
==> Installing dependencies for graphicsmagick: libpng, freetype, jpeg, jasper, libtiff, little-cms2 and webp
==> Installing graphicsmagick dependency: libpng
==> Downloading https://homebrew.bintray.com/bottles/libpng-1.6.37.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/c8/c8e74da602c21f978cd7ee3d489979b4fc6681e71f678a1d99012943ee3a909f?__gda__=exp=1573853320~hmac=78170657f8ba520c72e2bf16a9e5bc9652ee176bac675f73841859195ead9630&response-content-disposition=at
######################################################################## 100.0%
==> Pouring libpng-1.6.37.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/libpng/1.6.37: 27 files, 1.2MB
==> Installing graphicsmagick dependency: freetype
==> Downloading https://homebrew.bintray.com/bottles/freetype-2.10.1.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/dd/ddd686141a969caec11ea248324e3736f6db50a54673187be103dde39cb01ebf?__gda__=exp=1573853325~hmac=c4cda7151cd318dcb9251599fcba0452c804609a7c4d42d6b778c52d6eccc93e&response-content-disposition=at
######################################################################## 100.0%
==> Pouring freetype-2.10.1.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/freetype/2.10.1: 61 files, 2.2MB
==> Installing graphicsmagick dependency: jpeg
==> Downloading https://homebrew.bintray.com/bottles/jpeg-9c.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/b9/b94875481e23ee43f98c5d87085e47821a0100e2d79da309c31303f4c933f076?__gda__=exp=1573853331~hmac=02e9327dd7defe8bb3b96f7ef9f20a2dfdbd82d28cc903387808329f7944c432&response-content-disposition=at
######################################################################## 100.0%
==> Pouring jpeg-9c.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/jpeg/9c: 21 files, 764.9KB
==> Installing graphicsmagick dependency: jasper
==> Downloading https://homebrew.bintray.com/bottles/jasper-2.0.16_1.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/eb/eb5d0888be36aa8afb0eccc43957eeda99ded64ec5a5531240a4ec99450ba183?__gda__=exp=1573853337~hmac=eb0cbe411b2eede2fb285d54afdad200fe273db73a8d524b3d6a18622975cc78&response-content-disposition=at
######################################################################## 100.0%
==> Pouring jasper-2.0.16_1.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/jasper/2.0.16_1: 40 files, 1.4MB
==> Installing graphicsmagick dependency: libtiff
==> Downloading https://homebrew.bintray.com/bottles/libtiff-4.1.0.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/44/449bd9123e73e4c4eab85b77322d769cc9df0f6adab05e9b9319b012d1215a68?__gda__=exp=1573853342~hmac=ea0313c8bf649b8f13bbb0849e457e98694fad620f4e3d0ad624041d443265fc&response-content-disposition=at
######################################################################## 100.0%
==> Pouring libtiff-4.1.0.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/libtiff/4.1.0: 247 files, 3.7MB
==> Installing graphicsmagick dependency: little-cms2
==> Downloading https://homebrew.bintray.com/bottles/little-cms2-2.9.catalina.bottle.1.tar.gz
==> Downloading from https://akamai.bintray.com/fc/fc3b420e222a614a0f5b9fb91af41117ea1290ff19ea73dfc5e1b2021289b1b1?__gda__=exp=1573853349~hmac=a4fdb8e7d73a903d8aebbc32d14a664e21fd5cf49848204eae24cde264072731&response-content-disposition=at
######################################################################## 100.0%
==> Pouring little-cms2-2.9.catalina.bottle.1.tar.gz
🍺  /usr/local/Cellar/little-cms2/2.9: 18 files, 1MB
==> Installing graphicsmagick dependency: webp
==> Downloading https://homebrew.bintray.com/bottles/webp-1.0.3.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/6b/6bce8ee7b2b0cb615ea73deed3de3f345bcec05720222bd23882d4d8b7424fb6?__gda__=exp=1573853354~hmac=71b4dfbe3a9887b00b1a4fd21d9c231e059566622fe50074f4e916b4c82662aa&response-content-disposition=at
######################################################################## 100.0%
==> Pouring webp-1.0.3.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/webp/1.0.3: 39 files, 2.1MB
==> Installing graphicsmagick
==> Downloading https://homebrew.bintray.com/bottles/graphicsmagick-1.3.33.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/f7/f7a2699874e537fd81c0bcd0e06e72d987d0b951a34d724812459c42a6f6d16c?__gda__=exp=1573853360~hmac=b0d5b679cccabed652c90e5a0e632787acca6d7f0f1327c73478b8a90f10e81e&response-content-disposition=at
######################################################################## 100.0%
==> Pouring graphicsmagick-1.3.33.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/graphicsmagick/1.3.33: 490 files, 12.9MB
==> Downloading https://homebrew.bintray.com/bottles/runit-2.1.2.catalina.bottle.1.tar.gz
######################################################################## 100.0%
==> Pouring runit-2.1.2.catalina.bottle.1.tar.gz
==> Caveats
This formula does not install runit as a replacement for init.
The service directory is /usr/local/var/service instead of /service.

A system service that runs runsvdir with the default service directory is
provided. Alternatively you can run runsvdir manually:

     runsvdir -P /usr/local/var/service

Depending on the services managed by runit, this may need to start as root.

To have launchd start runit now and restart at login:
  brew services start runit
Or, if you don't want/need a background service you can just run:
  runit
==> Summary
🍺  /usr/local/Cellar/runit/2.1.2: 21 files, 310.1KB
==> Downloading https://homebrew.bintray.com/bottles/exiftool-11.70.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/fe/fed471f04fc57bfb8c5710d39a01f1a1176a85cf9cc0de2a9d8120382c287a2b?__gda__=exp=1573853375~hmac=5980563adbd43c1efe9857519d1ac23b5f6660e0b84f7bc4021722143369e83a&response-content-disposition=at
######################################################################## 100.0%
==> Pouring exiftool-11.70.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/exiftool/11.70: 556 files, 22.1MB
==> Caveats
==> redis
To have launchd start redis now and restart at login:
  brew services start redis
Or, if you don't want/need a background service you can just run:
  redis-server /usr/local/etc/redis.conf
==> icu4c
icu4c is keg-only, which means it was not symlinked into /usr/local,
because macOS provides libicucore.dylib (but nothing else).

If you need to have icu4c first in your PATH run:
  echo 'export PATH="/usr/local/opt/icu4c/bin:$PATH"' >> ~/.zshrc
  echo 'export PATH="/usr/local/opt/icu4c/sbin:$PATH"' >> ~/.zshrc

For compilers to find icu4c you may need to set:
  export LDFLAGS="-L/usr/local/opt/icu4c/lib"
  export CPPFLAGS="-I/usr/local/opt/icu4c/include"

For pkg-config to find icu4c you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/icu4c/lib/pkgconfig"

==> postgresql@10
To migrate existing data from a previous major version of PostgreSQL run:
  brew postgresql-upgrade-database

postgresql@10 is keg-only, which means it was not symlinked into /usr/local,
because this is an alternate version of another formula.

If you need to have postgresql@10 first in your PATH run:
  echo 'export PATH="/usr/local/opt/postgresql@10/bin:$PATH"' >> ~/.zshrc

For compilers to find postgresql@10 you may need to set:
  export LDFLAGS="-L/usr/local/opt/postgresql@10/lib"
  export CPPFLAGS="-I/usr/local/opt/postgresql@10/include"

For pkg-config to find postgresql@10 you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/postgresql@10/lib/pkgconfig"


To have launchd start postgresql@10 now and restart at login:
  brew services start postgresql@10
Or, if you don't want/need a background service you can just run:
  pg_ctl -D /usr/local/var/postgresql@10 start
==> libiconv
libiconv is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

If you need to have libiconv first in your PATH run:
  echo 'export PATH="/usr/local/opt/libiconv/bin:$PATH"' >> ~/.zshrc

For compilers to find libiconv you may need to set:
  export LDFLAGS="-L/usr/local/opt/libiconv/lib"
  export CPPFLAGS="-I/usr/local/opt/libiconv/include"

==> cmake
Emacs Lisp files have been installed to:
  /usr/local/share/emacs/site-lisp/cmake
==> runit
This formula does not install runit as a replacement for init.
The service directory is /usr/local/var/service instead of /service.

A system service that runs runsvdir with the default service directory is
provided. Alternatively you can run runsvdir manually:

     runsvdir -P /usr/local/var/service

Depending on the services managed by runit, this may need to start as root.

To have launchd start runit now and restart at login:
  brew services start runit
Or, if you don't want/need a background service you can just run:
  runit
```

</details>

<details><summary>Post-installation additional setup</code></summary>

```bash
# Pin icu4c & readline
$ brew pin icu4c readline
# blank

$ bundle config build.eventmachine --with-cppflags=-I/usr/local/opt/openssl/include
# blank
```

</details>
