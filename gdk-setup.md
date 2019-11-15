# GitLab Development Kit Setup

Based on [Set up GDK](https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/set-up-gdk.md) guide.

<details><summary><a href="https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/set-up-gdk.md#install-the-gitlab-development-kit-gem">Install the <code>gitlab-development-kit</code> gem</a></summary>

```bash
$ gem install gitlab-development-kit
Fetching gitlab-development-kit-0.2.5.gem
Successfully installed gitlab-development-kit-0.2.5
Parsing documentation for gitlab-development-kit-0.2.5
Installing ri documentation for gitlab-development-kit-0.2.5
Done installing documentation for gitlab-development-kit after 0 seconds
1 gem installed

# Verify installation
$ gdk version
GitLab Development Kit gem version 0.2.5
```

</details>

<details><summary><a href="https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/set-up-gdk.md#initialize-a-new-gdk-directory">Initialize a new GDK directory</a></summary>

```bash
$ mkdir ~/Code/GitLab && cd ~/Code/GitLab
# blank

# Initialize in `gdk` custom directory
$ gdk init gdk
Cloning into 'gdk'...
remote: Enumerating objects: 8969, done.
remote: Counting objects: 100% (8969/8969), done.
remote: Compressing objects: 100% (3168/3168), done.
remote: Total 8969 (delta 5784), reused 8818 (delta 5644)KiB/s
Receiving objects: 100% (8969/8969), 2.15 MiB | 1.20 MiB/s, done.
Resolving deltas: 100% (5784/5784), done.
Adding /Users/zain/Code/GitLab/gdk to trusted_directories in /Users/zain/.gdk.yml
```

</details>

<details><summary><a href="https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/set-up-gdk.md#install-gdk-components">Install GDK components</a></summary>

````bash
$ cd gdk
# blank

$ gdk install gitlab_repo=git@gitlab.com:zainfathoni/gitlab.git
(in /Users/zain/Code/GitLab/gdk)
command -v rake > /dev/null || gem install rake
rake preflight-checks
git clone  git@gitlab.com:zainfathoni/gitlab.git gitlab
Cloning into 'gitlab'...
The authenticity of host 'gitlab.com (35.231.145.151)' can't be established.
ECDSA key fingerprint is SHA256:HbW3g8zUjNSksFbqTiUWPWg2Bq1x8xdGUrliXFzSnUw.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'gitlab.com,35.231.145.151' (ECDSA) to the list of known hosts.
remote: Enumerating objects: 1730217, done.
remote: Counting objects: 100% (1730217/1730217), done.
remote: Compressing objects: 100% (361279/361279), done.
remote: Total 1730217 (delta 1354789), reused 1716116 (delta 1344416)
Receiving objects: 100% (1730217/1730217), 664.94 MiB | 3.30 MiB/s, done.
Resolving deltas: 100% (1354789/1354789), done.
Updating files: 100% (25818/25818), done.
ln -s /Users/zain/Code/GitLab/gdk/gitlab/.ruby-version /Users/zain/Code/GitLab/gdk/.ruby-version
rake gitlab/config/gitlab.yml
bin/safe-sed "gitlab/config/database.yml" \
  -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
  -e "s|5432|5432|" \
  "database.yml.example"
bin/safe-sed "gitlab/config/unicorn.rb" \
  -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
  "gitlab/config/unicorn.rb.example.development"
bin/safe-sed "gitlab/config/resque.yml" \
  -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
  "redis/resque.yml.example"
mkdir gitlab/public/uploads
bin/safe-sed "gitlab/config/puma.rb" \
  -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
  "gitlab/config/puma.example.development.rb"
cd /Users/zain/Code/GitLab/gdk/gitlab && bundle install --jobs 4 --without production
Fetching gem metadata from https://rubygems.org/........
Fetching rake 12.3.3
Installing rake 12.3.3
...
Bundle complete! 247 Gemfile dependencies, 465 gems now installed.
Gems in the group production were not installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
Post-install message from i18n:

HEADS UP! i18n 1.1 changed fallbacks to exclude default locale.
But that may break your application.

Please check your Rails app for 'config.i18n.fallbacks = true'.
If you're using I18n (>= 1.1.0) and Rails (< 5.2.2), this should be
'config.i18n.fallbacks = [I18n.default_locale]'.
If not, fallbacks will be broken in your app by I18n 1.1.x.

For more info see:
https://github.com/svenfuchs/i18n/releases/tag/v1.1.0

Post-install message from acts-as-taggable-on:
When upgrading

Re-run the migrations generator

    rake acts_as_taggable_on_engine:install:migrations

This will create any new migrations and skip existing ones
Version 3.5.0 has a migration for mysql adapter
Post-install message from encryptor:



Please be aware that Encryptor v2.0.0 had a major security bug when using AES-*-GCM algorithms.

By default You will not be able to decrypt data that was previously encrypted using an AES-*-GCM algorithm.

Please see the README and https://github.com/attr-encrypted/encryptor/pull/22 for more information.


Post-install message from attr_encrypted:



WARNING: Several insecure default options and features were deprecated in attr_encrypted v2.0.0.

Additionally, there was a bug in Encryptor v2.0.0 that insecurely encrypted data when using an AES-*-GCM algorithm.

This bug was fixed but introduced breaking changes between v2.x and v3.x.

Please see the README for more information regarding upgrading to attr_encrypted v3.0.0.


Post-install message from html-pipeline:
-------------------------------------------------
Thank you for installing html-pipeline!
You must bundle Filter gem dependencies.
See html-pipeline README.md for more details.
https://github.com/jch/html-pipeline#dependencies
-------------------------------------------------
Post-install message from httparty:
When you HTTParty, you must party hard!
Post-install message from rubocop:
Performance cops have been removed from RuboCop 0.68. Use the `rubocop-performance` gem instead.

Put this in your `Gemfile`.

gem 'rubocop-performance'

And then execute:

$ bundle install
# blank

Put this into your `.rubocop.yml`.

require: rubocop-performance

More information: https://github.com/rubocop-hq/rubocop-performance
Post-install message from icalendar:
HEADS UP! iCalendar 2.0 is not backwards-compatible with 1.x. Please see the README for the new syntax

HEADS UP! icalendar 2.2.0 switches to non-strict parsing as default. Please see the README if you
rely on strict parsing for information on how to enable it.

ActiveSupport is required for TimeWithZone support, but not required for general use.
touch .gitlab-bundle
cd /Users/zain/Code/GitLab/gdk/gitlab && yarn install --pure-lockfile
yarn install v1.19.1
[1/5] 🔍 Validating package.json...
[2/5] 🔍 Resolving packages...
warning Resolution field "ts-jest@24.0.0" is incompatible with requested version "ts-jest@^23.10.5"
[3/5] 🚚 Fetching packages...
[4/5] 🔗 Linking dependencies...
[5/5] 🔨 Building fresh packages...
\$ node ./scripts/frontend/postinstall.js
success Dependency postinstall check passed.
✨ Done in 33.87s.
touch .gitlab-yarn
cd /Users/zain/Code/GitLab/gdk/gitlab && bundle exec rake gettext:compile > /Users/zain/Code/GitLab/gdk/gettext.log 2>&1
git -C /Users/zain/Code/GitLab/gdk/gitlab checkout locale/\*/gitlab.po
Updated 0 paths from the index
touch .gettext
support/symlink gitlab-shell go-gitlab-shell/src/gitlab.com/gitlab-org/gitlab-shell
git clone --quiet --branch "v10.2.0" https://gitlab.com/gitlab-org/gitlab-shell.git go-gitlab-shell/src/gitlab.com/gitlab-org/gitlab-shell
Note: switching to '9ed13ca8848b2020bbcd8a52120a58731730745a'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

git switch -c <new-branch-name>

Or undo this operation with:

git switch -

Turn off this advice by setting config variable advice.detachedHead to false

bin/safe-sed "gitlab-shell/config.yml" \
 -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
 -e "s|^gitlab*url:.*|gitlab*url: http+unix://%2FUsers%2Fzain%2FCode%2FGitLab%2Fgdk%2Fgitlab.socket|" \
 -e "s|/usr/bin/redis-cli|/usr/local/bin/redis-cli|" \
 -e "s|^ socket: .*| socket: /Users/zain/Code/GitLab/gdk/redis/redis.socket|" \
 -e "s|^# migration|migration|" \
 "gitlab-shell/config.yml.example"
cd /Users/zain/Code/GitLab/gdk/gitlab-shell && bundle install --jobs 4 --without production
Fetching gem metadata from https://rubygems.org/..........
...
Bundle complete! 2 Gemfile dependencies, 16 gems now installed.
Gems in the group production were not installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
touch .gitlab-shell-bundle
ln -s /Users/zain/Code/GitLab/gdk/gitlab/.gitlab_shell_secret gitlab-shell/.gitlab_shell_secret
make -C gitlab-shell build
bin/compile
go: downloading github.com/mattn/go-shellwords v0.0.0-20190425161501-2444a32a19f4
...
git clone --quiet --branch "v8.14.0" https://gitlab.com/gitlab-org/gitlab-workhorse.git gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse
Note: switching to '9d06288b2c6d2630773d3c13794b830e24aa1ca2'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

git switch -c <new-branch-name>

Or undo this operation with:

git switch -

Turn off this advice by setting config variable advice.detachedHead to false

/Library/Developer/CommandLineTools/usr/bin/make -C gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse install PREFIX=/Users/zain/Code/GitLab/gdk/gitlab-workhorse

### Setting up target directory

rm -rf "/Users/zain/Code/GitLab/gdk/gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse/\_build"
mkdir -p "/Users/zain/Code/GitLab/gdk/gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse/\_build"
touch "/Users/zain/Code/GitLab/gdk/gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse/\_build/.ok"

### Building gitlab-workhorse

go build -ldflags "-X main.Version=v8.14.0-20191115.231817" -tags "tracer_static tracer_static_jaeger" -o /Users/zain/Code/GitLab/gdk/gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse/gitlab-workhorse gitlab.com/gitlab-org/gitlab-workhorse
go: downloading gitlab.com/gitlab-org/labkit v0.0.0-20190731061835-905271af7abb
...

### Building gitlab-zip-cat

go build -ldflags "-X main.Version=v8.14.0-20191115.231817" -tags "tracer_static tracer_static_jaeger" -o /Users/zain/Code/GitLab/gdk/gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse/gitlab-zip-cat gitlab.com/gitlab-org/gitlab-workhorse/cmd/gitlab-zip-cat

### Building gitlab-zip-metadata

go build -ldflags "-X main.Version=v8.14.0-20191115.231817" -tags "tracer_static tracer_static_jaeger" -o /Users/zain/Code/GitLab/gdk/gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse/gitlab-zip-metadata gitlab.com/gitlab-org/gitlab-workhorse/cmd/gitlab-zip-metadata

### install

mkdir -p /Users/zain/Code/GitLab/gdk/gitlab-workhorse/bin/
cd /Users/zain/Code/GitLab/gdk/gitlab-workhorse/src/gitlab.com/gitlab-org/gitlab-workhorse && install gitlab-workhorse gitlab-zip-cat gitlab-zip-metadata /Users/zain/Code/GitLab/gdk/gitlab-workhorse/bin/
bin/safe-sed "gitlab-workhorse/config.toml" \
 -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
 "gitlab-workhorse/config.toml.example"
git clone --quiet --branch "v1.11.0" https://gitlab.com/gitlab-org/gitlab-pages.git gitlab-pages/src/gitlab.com/gitlab-org/gitlab-pages
Note: switching to 'fa804e9f422cb1525324e917a4b318bea8596067'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

git switch -c <new-branch-name>

Or undo this operation with:

git switch -

Turn off this advice by setting config variable advice.detachedHead to false

mkdir -p gitlab-pages/bin
/Library/Developer/CommandLineTools/usr/bin/make -C gitlab-pages/src/gitlab.com/gitlab-org/gitlab-pages
mkdir -p ".GOPATH/src/gitlab.com/gitlab-org/"
ln -s ../../../.. ".GOPATH/src/gitlab.com/gitlab-org/gitlab-pages"
mkdir -p .GOPATH/test .GOPATH/cover
mkdir -p bin
ln -s ../bin .GOPATH/bin
touch .GOPATH/.ok
go install -v -ldflags='-X "main.VERSION=1.11.0" -X "main.REVISION=fa804e9"' -buildmode exe gitlab.com/gitlab-org/gitlab-pages
...
cp -f ./bin/gitlab-pages .
install -m755 gitlab-pages/src/gitlab.com/gitlab-org/gitlab-pages/gitlab-pages gitlab-pages/bin
rake Procfile
bin/safe-sed "redis/redis.conf" \
 -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
 "redis/redis.conf.example"
git clone --quiet --branch "v1.70.0" https://gitlab.com/gitlab-org/gitaly.git /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly
Note: switching to '67f4fe73a05048a1b90afece1d3cf6a5a395eda6'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

git switch -c <new-branch-name>

Or undo this operation with:

git switch -

Turn off this advice by setting config variable advice.detachedHead to false

/Library/Developer/CommandLineTools/usr/bin/make -C /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly assemble ASSEMBLY_ROOT=/Users/zain/Code/GitLab/gdk/gitaly/assembly BUNDLE_FLAGS=--no-deployment BUILD_TAGS="tracer_static tracer_static_jaeger"
mkdir -p \_build/src/gitlab.com/gitlab-org
cd \_build/src/gitlab.com/gitlab-org && rm -f gitaly && \
 ln -sf ../../../.. gitaly
touch \_build/.ok
(cd \_build && go mod init \_build)
go: creating new go.mod: module \_build
cd \_build && go build -o /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly/\_build/makegen /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly/\_support/makegen.go
cd \_build && ./makegen > Makefile
cd \_build && /Library/Developer/CommandLineTools/usr/bin/make assemble
rm -f ../.ruby-bundle
cd /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly/ruby && bundle config # for debugging
Settings are listed in order of priority. The top value will be used.
build.eventmachine
Set for the current user (/Users/zain/.bundle/config): "--with-cppflags=-I/usr/local/opt/openssl/include"

flags
Set via BUNDLE_FLAGS: "--no-deployment"

cd /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly/ruby && bundle install --no-deployment
Fetching gem metadata from https://rubygems.org/.........
...
Bundle complete! 25 Gemfile dependencies, 97 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
Post-install message from i18n:

HEADS UP! i18n 1.1 changed fallbacks to exclude default locale.
But that may break your application.

Please check your Rails app for 'config.i18n.fallbacks = true'.
If you're using I18n (>= 1.1.0) and Rails (< 5.2.2), this should be
'config.i18n.fallbacks = [I18n.default_locale]'.
If not, fallbacks will be broken in your app by I18n 1.1.x.

For more info see:
https://github.com/svenfuchs/i18n/releases/tag/v1.1.0

touch ../.ruby-bundle

# go install

...
mkdir -p /Users/zain/Code/GitLab/gdk/gitaly/assembly
rm -rf /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly/ruby/tmp /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly/ruby/gitlab-shell/tmp
mkdir -p /Users/zain/Code/GitLab/gdk/gitaly/assembly/ruby/
rsync -a --delete /Users/zain/Code/GitLab/gdk/gitaly/src/gitlab.com/gitlab-org/gitaly/ruby/ /Users/zain/Code/GitLab/gdk/gitaly/assembly/ruby/
rm -rf /Users/zain/Code/GitLab/gdk/gitaly/assembly/ruby/spec /Users/zain/Code/GitLab/gdk/gitaly/assembly/ruby/gitlab-shell/spec /Users/zain/Code/GitLab/gdk/gitaly/assembly/ruby/gitlab-shell/gitlab-shell.log
rm -rf /Users/zain/Code/GitLab/gdk/gitaly/assembly/bin
mkdir -p /Users/zain/Code/GitLab/gdk/gitaly/assembly/bin
cd bin && install gitaly gitaly-debug gitaly-hooks gitaly-ssh gitaly-wrapper praefect /Users/zain/Code/GitLab/gdk/gitaly/assembly/bin
mkdir -p /Users/zain/Code/GitLab/gdk/gitaly/bin
ln -sf /Users/zain/Code/GitLab/gdk/gitaly/assembly/bin/\* /Users/zain/Code/GitLab/gdk/gitaly/bin
rm -rf /Users/zain/Code/GitLab/gdk/gitaly/ruby
ln -sf /Users/zain/Code/GitLab/gdk/gitaly/assembly/ruby /Users/zain/Code/GitLab/gdk/gitaly/ruby
rake gitaly/gitaly.config.toml
rake gitaly/praefect.config.toml
mkdir -p jaeger-artifacts
./bin/download-jaeger "1.10.1" "jaeger-artifacts/jaeger-1.10.1.tar.gz"
% Total % Received % Xferd Average Speed Time Time Time Current
Dload Upload Total Spent Left Speed
100 623 0 623 0 0 1622 0 --:--:-- --:--:-- --:--:-- 1622
100 72.1M 100 72.1M 0 0 4831k 0 0:00:15 0:00:15 --:--:-- 6715k
jaeger-artifacts/jaeger-1.10.1.tar.gz: OK

# To save disk space, delete old versions of the download,

# but to save bandwidth keep the current version....

find jaeger-artifacts ! -path "jaeger-artifacts/jaeger-1.10.1.tar.gz" -type f -exec rm -f {} + -print
mkdir -p "jaeger/jaeger-1.10.1"
tar -xf "jaeger-artifacts/jaeger-1.10.1.tar.gz" -C "jaeger/jaeger-1.10.1" --strip-components 1
/usr/local/opt/postgresql@10/bin/initdb --locale=C -E utf-8 /Users/zain/Code/GitLab/gdk/postgresql/data
The files belonging to this database system will be owned by user "zain".
This user must also own the server process.

The database cluster will be initialized with locale "C".
The default text search configuration will be set to "english".

Data page checksums are disabled.

creating directory /Users/zain/Code/GitLab/gdk/postgresql/data ... ok
creating subdirectories ... ok
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting default timezone ... Asia/Singapore
selecting dynamic shared memory implementation ... posix
creating configuration files ... ok
running bootstrap script ... ok
performing post-bootstrap initialization ... ok
syncing data to disk ... ok

WARNING: enabling "trust" authentication for local connections
You can change this by editing pg_hba.conf or using the option -A, or
--auth-local and --auth-host, the next time you run initdb.

Success. You can now start the database server using:

    '/usr/local/opt/postgresql@10/bin/pg_ctl' -D /Users/zain/Code/GitLab/gdk/postgresql/data -l logfile start

support/bootstrap-rails
(in /Users/zain/Code/GitLab/gdk)
ok: run: ./services/postgresql: (pid 40121) 1s, normally down
ok: run: ./services/praefect: (pid 40122) 1s, normally down
ok: run: ./services/praefect-gitaly-0: (pid 40123) 1s, normally down
ok: run: ./services/redis: (pid 40124) 1s, normally down
Waiting for praefect to boot.................... OK
Created database 'gitlabhq_development'
Created database 'gitlabhq_test'
WARNING: sha_attribute :source_sha is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha_attribute :target_sha is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha_attribute :project_fingerprint is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha_attribute :location_fingerprint is invalid since the table doesn't exist - you may need to run database migrations
Dropped database 'gitlabhq_development'
Dropped database 'gitlabhq_test'
Created database 'gitlabhq_development'
Created database 'gitlabhq_test'
...

== Seed from /Users/zain/Code/GitLab/gdk/gitlab/db/fixtures/development/01_admin.rb

---

⛔️ WARNING: Sidekiq testing API enabled, but this is not the test environment. Your jobs will not go to Redis.

---

.
OK
...

bin/safe-sed "openssh/sshd_config" \
 -e "s|/home/git|/Users/zain/Code/GitLab/gdk|g" \
 -e "s/GDK_USERNAME/zain/g" \
 "openssh/sshd_config.example"
ssh-keygen -f openssh/ssh_host_rsa_key -N '' -t rsa
Generating public/private rsa key pair.
Your identification has been saved in openssh/ssh_host_rsa_key.
Your public key has been saved in openssh/ssh_host_rsa_key.pub.
The key fingerprint is:
SHA256:VnzO/ZpdODkpxc71qX75p3cgddxt1QAWgY5ER3baWHM zain@Zains-MacBook-Pro.local
The key's randomart image is:
+---[RSA 2048]----+
| ...+.O+E..|
| .+.B o o|
| . o= o .+|
| ...+ o. *|
| S o.+o.|
| . .+.*o|
| ..Oo=|
| ..O=|
| .o=o\*|
+----[SHA256]-----+
rake nginx/conf/nginx.conf
mkdir -p nginx/logs
mkdir -p nginx/tmp
mkdir -p registry/storage
echo 'false' > auto_devops_enabled
cp registry/config.yml.example registry/config.yml
if false; then \
 protocol='https' gitlab_host=0.0.0.0 gitlab_port=3000 registry_port=5000 \
 support/edit-registry-config.yml registry/config.yml; \
 else \
 gitlab_host=docker.for.mac.localhost gitlab_port=3000 registry_port=5000 \
 support/edit-registry-config.yml registry/config.yml; \
 fi
openssl req -new -subj "/CN=localhost/" -x509 -days 365 -newkey rsa:2048 -nodes -keyout "localhost.key" -out "localhost.crt"
Generating a 2048 bit RSA private key
...+++
......................+++
writing new private key to 'localhost.key'

---

chmod 600 localhost.key
curl -L -o elasticsearch-6.5.1.tar.gz.tmp https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.5.1.tar.gz
% Total % Received % Xferd Average Speed Time Time Time Current
Dload Upload Total Spent Left Speed
100 108M 100 108M 0 0 9238k 0 0:00:11 0:00:11 --:--:-- 14.0M
echo "5903e1913a7c96aad96a8227517c40490825f672 elasticsearch-6.5.1.tar.gz.tmp" | shasum -a1 -c -
elasticsearch-6.5.1.tar.gz.tmp: OK
mv elasticsearch-6.5.1.tar.gz.tmp elasticsearch-6.5.1.tar.gz
rm -rf elasticsearch
tar zxf elasticsearch-6.5.1.tar.gz
mv elasticsearch-6.5.1 elasticsearch
touch elasticsearch/bin/elasticsearch

---

**\*\***\*\***\*\*** Setup finished! **\*\***\*\***\*\***

---

cat HELP

# GitLab Development Kit cheat sheet

gdk start # Start everything
gdk start redis postgresql # Start specifc services
gdk stop # Stop all services and unload Runit
gdk stop redis postgresql # Stop specific service
gdk status # See status of all services
gdk restart # Restart everything
gdk restart redis postgresql # Restart specific services

gdk tail # Tail all logs
gdk tail redis postgresql # Tail specific logs

gdk thin # Run rails web server with thin in foreground

gdk install gitlab_repo=https://my-fork # Install everything
gdk update # Pull application changes from Git
gdk reconfigure # Delete and regenerate all config files created by GDK
gdk psql -d gitlabhq_development # Postgres console
gdk redis-cli # Redis console

# Development admin account: root / 5iveL!fe

For more information about GitLab development see
https://docs.gitlab.com/ce/development/README.html.

---

if [ "" = "Linux" ]; then \
 sed -i -e 's/docker\.for\.mac\.localhost/localhost/g' /Users/zain/Code/GitLab/gdk/prometheus/prometheus.yml; \
 fi
mkdir -p minio/data/lfs-objects
mkdir -p minio/data/artifacts
mkdir -p minio/data/uploads
mkdir -p minio/data/packages
git clone --quiet --branch "v1.5.0" https://gitlab.com/gitlab-org/gitlab-elasticsearch-indexer.git gitlab-elasticsearch-indexer
Note: switching to '9299f10abb9376582e790cfe1bd54fc32d82f5b5'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

git switch -c <new-branch-name>

Or undo this operation with:

git switch -

Turn off this advice by setting config variable advice.detachedHead to false

/Library/Developer/CommandLineTools/usr/bin/make -C gitlab-elasticsearch-indexer build

```

</details>
````
