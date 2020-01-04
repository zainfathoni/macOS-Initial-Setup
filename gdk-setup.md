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
$ gdk init
Cloning into '/Users/zain/Code/GitLab/gitlab-development-kit'...
remote: Enumerating objects: 9889, done.
remote: Counting objects: 100% (9889/9889), done.
remote: Compressing objects: 100% (3563/3563), done.
remote: Total 9889 (delta 6418), reused 9607 (delta 6158), pack-reused 0
Receiving objects: 100% (9889/9889), 2.30 MiB | 432.00 KiB/s, done.
Resolving deltas: 100% (6418/6418), done.
Adding /Users/zain/Code/GitLab/gitlab-development-kit to trusted_directories in /Users/zain/.gdk.yml
```

</details>

<details><summary><a href="https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/set-up-gdk.md#install-gdk-components">Install GDK components</a></summary>

```bash
$ cd gitlab-development-kit
# blank

$ gdk install gitlab_repo=git@gitlab.com:zainfathoni/gitlab.git
(in /Users/zain/Code/GitLab/gitlab-development-kit)
Cloning into 'gitlab'...
remote: Enumerating objects: 1794895, done.
remote: Counting objects: 100% (1794895/1794895), done.
remote: Compressing objects: 100% (384455/384455), done.
remote: Total 1794895 (delta 1404465), reused 1771227 (delta 1384548), pack-reused 0
Receiving objects: 100% (1794895/1794895), 688.48 MiB | 4.27 MiB/s, done.
Resolving deltas: 100% (1404465/1404465), done.
Updating files: 100% (27452/27452), done.

warning Resolution field "ts-jest@24.0.0" is incompatible with requested version "ts-jest@^23.10.5"
warning " > monaco-editor-webpack-plugin@1.7.0" has incorrect peer dependency "monaco-editor@^0.15.1".
warning " > eslint-import-resolver-jest@2.1.1" has unmet peer dependency "eslint-plugin-import@>=1.4.0".
warning " > eslint-import-resolver-webpack@0.10.1" has unmet peer dependency "eslint-plugin-import@>=1.4.0".
Updated 0 paths from the index
Note: switching to '24156ea1e31c1cac2471b57217e683de8dccbd46'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

Note: switching to '9a9a83e7f92ceea5fb0e1542d604171c58615e28'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

go: downloading gitlab.com/gitlab-org/labkit v0.0.0-20190902063225-3253d7975ca7
go: downloading gitlab.com/gitlab-org/gitaly v1.74.0
go: extracting gitlab.com/gitlab-org/labkit v0.0.0-20190902063225-3253d7975ca7
go: downloading golang.org/x/crypto v0.0.0-20190701094942-4def268fd1a4
go: extracting golang.org/x/crypto v0.0.0-20190701094942-4def268fd1a4
go: downloading golang.org/x/sys v0.0.0-20190813064441-fde4db37ae7a
go: extracting gitlab.com/gitlab-org/gitaly v1.74.0
go: extracting golang.org/x/sys v0.0.0-20190813064441-fde4db37ae7a
go: finding gitlab.com/gitlab-org/labkit v0.0.0-20190902063225-3253d7975ca7
go: finding golang.org/x/crypto v0.0.0-20190701094942-4def268fd1a4
go: finding gitlab.com/gitlab-org/gitaly v1.74.0
go: finding golang.org/x/sys v0.0.0-20190813064441-fde4db37ae7a
Note: switching to '9c69ac5306545be017701dfff7afe25c8b814c3f'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

go: downloading gitlab.com/gitlab-org/labkit v0.0.0-20190902063225-3253d7975ca7
go: downloading gitlab.com/lupine/go-mimedb v0.0.0-20180307000149-e8af1d659877
go: downloading golang.org/x/net v0.0.0-20190909003024-a7b16738d86b
go: downloading github.com/rs/cors v1.7.0
go: downloading github.com/gorilla/context v1.1.1
go: downloading github.com/sirupsen/logrus v1.4.2
go: downloading golang.org/x/sys v0.0.0-20190910064555-bbd175535a8b
go: downloading github.com/prometheus/client_golang v1.1.0
go: extracting github.com/gorilla/context v1.1.1
go: downloading github.com/gorilla/sessions v1.2.0
go: extracting gitlab.com/gitlab-org/labkit v0.0.0-20190902063225-3253d7975ca7
go: extracting gitlab.com/lupine/go-mimedb v0.0.0-20180307000149-e8af1d659877
go: extracting github.com/rs/cors v1.7.0
go: extracting github.com/sirupsen/logrus v1.4.2
go: downloading github.com/namsral/flag v1.7.4-pre
go: downloading github.com/gorilla/securecookie v1.1.1
go: extracting github.com/prometheus/client_golang v1.1.0
go: downloading github.com/kardianos/osext v0.0.0-20190222173326-2bc1f35cddc0
go: downloading github.com/client9/reopen v1.0.0
go: downloading github.com/sebest/xff v0.0.0-20160910043805-6c115e0ffa35
go: extracting github.com/gorilla/sessions v1.2.0
go: downloading github.com/karrick/godirwalk v1.10.12
go: downloading github.com/beorn7/perks v1.0.1
go: downloading golang.org/x/crypto v0.0.0-20190911031432-227b76d455e7
go: extracting github.com/namsral/flag v1.7.4-pre
go: extracting github.com/kardianos/osext v0.0.0-20190222173326-2bc1f35cddc0
go: extracting github.com/beorn7/perks v1.0.1
go: extracting github.com/gorilla/securecookie v1.1.1
go: extracting github.com/sebest/xff v0.0.0-20160910043805-6c115e0ffa35
go: extracting github.com/client9/reopen v1.0.0
go: downloading github.com/prometheus/common v0.6.0
go: downloading github.com/prometheus/client_model v0.0.0-20190129233127-fd36f4220a90
go: downloading github.com/golang/protobuf v1.3.2
go: extracting github.com/karrick/godirwalk v1.10.12
go: extracting golang.org/x/sys v0.0.0-20190910064555-bbd175535a8b
go: downloading github.com/prometheus/procfs v0.0.3
go: extracting github.com/prometheus/client_model v0.0.0-20190129233127-fd36f4220a90
go: extracting golang.org/x/net v0.0.0-20190909003024-a7b16738d86b
go: downloading github.com/getsentry/raven-go v0.1.2
go: extracting github.com/prometheus/common v0.6.0
go: extracting github.com/golang/protobuf v1.3.2
go: extracting github.com/prometheus/procfs v0.0.3
go: downloading github.com/matttproud/golang_protobuf_extensions v1.0.1
go: extracting github.com/matttproud/golang_protobuf_extensions v1.0.1
go: extracting github.com/getsentry/raven-go v0.1.2
go: downloading github.com/pkg/errors v0.8.0
go: downloading github.com/certifi/gocertifi v0.0.0-20190905060710-a5e0173ced67
go: extracting github.com/pkg/errors v0.8.0
go: extracting golang.org/x/crypto v0.0.0-20190911031432-227b76d455e7
go: extracting github.com/certifi/gocertifi v0.0.0-20190905060710-a5e0173ced67
go: downloading golang.org/x/text v0.3.0
go: extracting golang.org/x/text v0.3.0
go: finding github.com/namsral/flag v1.7.4-pre
go: finding github.com/kardianos/osext v0.0.0-20190222173326-2bc1f35cddc0
go: finding github.com/gorilla/context v1.1.1
go: finding github.com/prometheus/client_golang v1.1.0
go: finding github.com/rs/cors v1.7.0
go: finding github.com/sirupsen/logrus v1.4.2
go: finding gitlab.com/gitlab-org/labkit v0.0.0-20190902063225-3253d7975ca7
go: finding github.com/gorilla/securecookie v1.1.1
go: finding github.com/gorilla/sessions v1.2.0
go: finding golang.org/x/sys v0.0.0-20190910064555-bbd175535a8b
go: finding github.com/prometheus/client_model v0.0.0-20190129233127-fd36f4220a90
go: finding github.com/prometheus/common v0.6.0
go: finding github.com/getsentry/raven-go v0.1.2
go: finding golang.org/x/crypto v0.0.0-20190911031432-227b76d455e7
go: finding gitlab.com/lupine/go-mimedb v0.0.0-20180307000149-e8af1d659877
go: finding github.com/beorn7/perks v1.0.1
go: finding golang.org/x/net v0.0.0-20190909003024-a7b16738d86b
go: finding github.com/karrick/godirwalk v1.10.12
go: finding github.com/client9/reopen v1.0.0
go: finding github.com/golang/protobuf v1.3.2
go: finding github.com/sebest/xff v0.0.0-20160910043805-6c115e0ffa35
go: finding github.com/matttproud/golang_protobuf_extensions v1.0.1
go: finding github.com/prometheus/procfs v0.0.3
go: finding github.com/certifi/gocertifi v0.0.0-20190905060710-a5e0173ced67
go: finding github.com/pkg/errors v0.8.0
go: finding golang.org/x/text v0.3.0
github.com/beorn7/perks/quantile
golang.org/x/crypto/hkdf
golang.org/x/text/transform
github.com/prometheus/common/internal/bitbucket.org/ww/goautoneg
golang.org/x/sys/unix
github.com/kardianos/osext
github.com/namsral/flag
github.com/golang/protobuf/proto
net
github.com/prometheus/common/model
github.com/prometheus/procfs/internal/fs
github.com/client9/reopen
gitlab.com/gitlab-org/labkit/mask
github.com/pkg/errors
github.com/karrick/godirwalk
github.com/gorilla/securecookie
gitlab.com/gitlab-org/gitlab-pages/internal/deprecatedargs
gitlab.com/lupine/go-mimedb
golang.org/x/text/unicode/bidi
golang.org/x/text/unicode/norm
golang.org/x/net/http2/hpack
golang.org/x/text/secure/bidirule
gitlab.com/gitlab-org/gitlab-pages/internal/jail
github.com/sirupsen/logrus
golang.org/x/net/idna
gitlab.com/gitlab-org/gitlab-pages/internal/netutil
vendor/golang.org/x/net/http/httpproxy
net/textproto
github.com/prometheus/procfs
crypto/x509
golang.org/x/net/http/httpguts
vendor/golang.org/x/net/http/httpguts
github.com/prometheus/client_model/go
github.com/matttproud/golang_protobuf_extensions/pbutil
github.com/prometheus/client_golang/prometheus/internal
github.com/certifi/gocertifi
crypto/tls
net/http/httptrace
gitlab.com/gitlab-org/gitlab-pages/internal/tlsconfig
net/http
gitlab.com/gitlab-org/gitlab-pages/internal/host
gitlab.com/gitlab-org/gitlab-pages/internal/httputil/header
github.com/rs/cors
gitlab.com/gitlab-org/gitlab-pages/internal/httperrors
gitlab.com/gitlab-org/gitlab-pages/internal/httptransport
github.com/gorilla/context
gitlab.com/gitlab-org/gitlab-pages/internal/serving
github.com/prometheus/common/expfmt
github.com/sebest/xff
gitlab.com/gitlab-org/gitlab-pages/internal/acme
gitlab.com/gitlab-org/gitlab-pages/internal/httputil
gitlab.com/gitlab-org/labkit/correlation
github.com/getsentry/raven-go
gitlab.com/gitlab-org/gitlab-pages/internal/config
github.com/gorilla/sessions
gitlab.com/gitlab-org/gitlab-pages/internal/serving/disk
gitlab.com/gitlab-org/gitlab-pages/internal
golang.org/x/net/http2
gitlab.com/gitlab-org/labkit/log
gitlab.com/gitlab-org/gitlab-pages/internal/domain
gitlab.com/gitlab-org/gitlab-pages/internal/request
gitlab.com/gitlab-org/gitlab-pages/internal/logging
gitlab.com/gitlab-org/gitlab-pages/internal/handlers
gitlab.com/gitlab-org/labkit/errortracking
github.com/prometheus/client_golang/prometheus
gitlab.com/gitlab-org/gitlab-pages/internal/artifact
gitlab.com/gitlab-org/gitlab-pages/metrics
github.com/prometheus/client_golang/prometheus/promhttp
gitlab.com/gitlab-org/gitlab-pages/internal/source/disk
gitlab.com/gitlab-org/gitlab-pages/internal/source
gitlab.com/gitlab-org/gitlab-pages/internal/auth
gitlab.com/gitlab-org/labkit/metrics
gitlab.com/gitlab-org/gitlab-pages
git clone --quiet --branch "v1.78.0"  https://gitlab.com/gitlab-org/gitaly.git /Users/zain/Code/GitLab/gitlab-development-kit/gitaly/src/gitlab.com/gitlab-org/gitaly
Note: switching to '8079c7d15963c5e89a0fc9290e781d7677bea6dd'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

go: creating new go.mod: module _build
go: downloading github.com/getsentry/sentry-go v0.3.0
go: downloading github.com/prometheus/procfs v0.0.3
go: downloading github.com/beorn7/perks v1.0.1
go: downloading github.com/lib/pq v1.2.0
go: downloading golang.org/x/text v0.3.2
go: extracting github.com/prometheus/procfs v0.0.3
go: extracting github.com/beorn7/perks v1.0.1
go: extracting github.com/lib/pq v1.2.0
go: extracting github.com/getsentry/sentry-go v0.3.0
go: extracting golang.org/x/text v0.3.2
go: finding github.com/getsentry/sentry-go v0.3.0
go: finding github.com/beorn7/perks v1.0.1
go: finding github.com/lib/pq v1.2.0
go: finding github.com/prometheus/procfs v0.0.3
go: finding golang.org/x/text v0.3.2
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   623    0   623    0     0   1422      0 --:--:-- --:--:-- --:--:--  1422
100 72.1M  100 72.1M    0     0  4535k      0  0:00:16  0:00:16 --:--:-- 5941k
jaeger-artifacts/jaeger-1.10.1.tar.gz: OK
# To save disk space, delete old versions of the download,
# but to save bandwidth keep the current version....

-------------------------------------------------------
Installing jaeger 1.10.1..
-------------------------------------------------------
The files belonging to this database system will be owned by user "zain".
This user must also own the server process.

The database cluster will be initialized with locale "C".
The default text search configuration will be set to "english".

Data page checksums are disabled.

creating directory /Users/zain/Code/GitLab/gitlab-development-kit/postgresql/data ... ok
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

    '/usr/local/opt/postgresql@10/bin/pg_ctl' -D /Users/zain/Code/GitLab/gitlab-development-kit/postgresql/data -l logfile start

(in /Users/zain/Code/GitLab/gitlab-development-kit)
ok: run: ./services/postgresql: (pid 22527) 0s, normally down
ok: run: ./services/praefect: (pid 22524) 0s, normally down
ok: run: ./services/praefect-gitaly-0: (pid 22526) 0s, normally down
ok: run: ./services/redis: (pid 22525) 0s, normally down
Waiting for praefect to boot. OK
Created database 'gitlabhq_development'
Created database 'gitlabhq_test'
WARNING: sha_attribute :source_sha is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha_attribute :target_sha is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha_attribute :squash_commit_sha is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha256_attribute :fingerprint_sha256 is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha_attribute :project_fingerprint is invalid since the table doesn't exist - you may need to run database migrations
WARNING: sha_attribute :location_fingerprint is invalid since the table doesn't exist - you may need to run database migrations
Dropped database 'gitlabhq_development'
Dropped database 'gitlabhq_test'
Created database 'gitlabhq_development'
Created database 'gitlabhq_test'
-- enable_extension("pg_trgm")
   -> 0.0341s
-- enable_extension("plpgsql")
   -> 0.0036s
-- create_table("abuse_reports", {:id=>:serial, :force=>:cascade})
   -> 0.0164s
-- create_table("alerts_service_data", {:force=>:cascade})
   -> 0.0138s
-- create_table("allowed_email_domains", {:force=>:cascade})
   -> 0.0066s
-- create_table("analytics_cycle_analytics_group_stages", {:force=>:cascade})
   -> 0.0267s
-- create_table("analytics_cycle_analytics_project_stages", {:force=>:cascade})
   -> 0.0153s
-- create_table("analytics_language_trend_repository_languages", {:id=>false, :force=>:cascade})
   -> 0.0165s
-- create_table("analytics_repository_file_commits", {:force=>:cascade})
   -> 0.0117s
-- create_table("analytics_repository_file_edits", {:force=>:cascade})
   -> 0.0082s
-- create_table("analytics_repository_files", {:force=>:cascade})
   -> 0.0060s
-- create_table("appearances", {:id=>:serial, :force=>:cascade})
   -> 0.0106s
-- create_table("application_setting_terms", {:id=>:serial, :force=>:cascade})
   -> 0.0054s
-- create_table("application_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0930s
-- create_table("approval_merge_request_rule_sources", {:force=>:cascade})
   -> 0.0116s
-- create_table("approval_merge_request_rules", {:force=>:cascade})
   -> 0.0318s
-- create_table("approval_merge_request_rules_approved_approvers", {:force=>:cascade})
   -> 0.0079s
-- create_table("approval_merge_request_rules_groups", {:force=>:cascade})
   -> 0.0105s
-- create_table("approval_merge_request_rules_users", {:force=>:cascade})
   -> 0.0136s
-- create_table("approval_project_rules", {:force=>:cascade})
   -> 0.0154s
-- create_table("approval_project_rules_groups", {:force=>:cascade})
   -> 0.0090s
-- create_table("approval_project_rules_users", {:force=>:cascade})
   -> 0.0139s
-- create_table("approvals", {:id=>:serial, :force=>:cascade})
   -> 0.0100s
-- create_table("approver_groups", {:id=>:serial, :force=>:cascade})
   -> 0.0097s
-- create_table("approvers", {:id=>:serial, :force=>:cascade})
   -> 0.0151s
-- create_table("audit_events", {:id=>:serial, :force=>:cascade})
   -> 0.0127s
-- create_table("award_emoji", {:id=>:serial, :force=>:cascade})
   -> 0.0104s
-- create_table("aws_roles", {:primary_key=>"user_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0084s
-- create_table("badges", {:id=>:serial, :force=>:cascade})
   -> 0.0140s
-- create_table("board_assignees", {:id=>:serial, :force=>:cascade})
   -> 0.0097s
-- create_table("board_group_recent_visits", {:force=>:cascade})
   -> 0.0279s
-- create_table("board_labels", {:id=>:serial, :force=>:cascade})
   -> 0.0170s
-- create_table("board_project_recent_visits", {:force=>:cascade})
   -> 0.0140s
-- create_table("boards", {:id=>:serial, :force=>:cascade})
   -> 0.0177s
-- create_table("broadcast_messages", {:id=>:serial, :force=>:cascade})
   -> 0.0093s
-- create_table("chat_names", {:id=>:serial, :force=>:cascade})
   -> 0.0130s
-- create_table("chat_teams", {:id=>:serial, :force=>:cascade})
   -> 0.0105s
-- create_table("ci_build_needs", {:id=>:serial, :force=>:cascade})
   -> 0.0083s
-- create_table("ci_build_trace_chunks", {:force=>:cascade})
   -> 0.0085s
-- create_table("ci_build_trace_section_names", {:id=>:serial, :force=>:cascade})
   -> 0.0064s
-- create_table("ci_build_trace_sections", {:id=>false, :force=>:cascade})
   -> 0.0108s
-- create_table("ci_builds", {:id=>:serial, :force=>:cascade})
   -> 0.1058s
-- create_table("ci_builds_metadata", {:id=>:serial, :force=>:cascade})
   -> 0.0154s
-- create_table("ci_builds_runner_session", {:force=>:cascade})
   -> 0.0095s
-- create_table("ci_group_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0146s
-- create_table("ci_job_artifacts", {:id=>:serial, :force=>:cascade})
   -> 0.0183s
-- create_table("ci_job_variables", {:force=>:cascade})
   -> 0.0146s
-- create_table("ci_pipeline_chat_data", {:force=>:cascade})
   -> 0.0116s
-- create_table("ci_pipeline_schedule_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0088s
-- create_table("ci_pipeline_schedules", {:id=>:serial, :force=>:cascade})
   -> 0.0144s
-- create_table("ci_pipeline_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0125s
-- create_table("ci_pipelines", {:id=>:serial, :force=>:cascade})
   -> 0.0549s
-- create_table("ci_pipelines_config", {:primary_key=>"pipeline_id", :force=>:cascade})
   -> 0.0061s
-- create_table("ci_resource_groups", {:force=>:cascade})
   -> 0.0050s
-- create_table("ci_resources", {:force=>:cascade})
   -> 0.0169s
-- create_table("ci_runner_namespaces", {:id=>:serial, :force=>:cascade})
   -> 0.0102s
-- create_table("ci_runner_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0081s
-- create_table("ci_runners", {:id=>:serial, :force=>:cascade})
   -> 0.0283s
-- create_table("ci_sources_pipelines", {:id=>:serial, :force=>:cascade})
   -> 0.0178s
-- create_table("ci_stages", {:id=>:serial, :force=>:cascade})
   -> 0.0219s
-- create_table("ci_subscriptions_projects", {:force=>:cascade})
   -> 0.0080s
-- create_table("ci_trigger_requests", {:id=>:serial, :force=>:cascade})
   -> 0.0095s
-- create_table("ci_triggers", {:id=>:serial, :force=>:cascade})
   -> 0.0145s
-- create_table("ci_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0176s
-- create_table("cluster_groups", {:id=>:serial, :force=>:cascade})
   -> 0.0109s
-- create_table("cluster_platforms_kubernetes", {:id=>:serial, :force=>:cascade})
   -> 0.0117s
-- create_table("cluster_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0136s
-- create_table("cluster_providers_aws", {:force=>:cascade})
   -> 0.0145s
-- create_table("cluster_providers_gcp", {:id=>:serial, :force=>:cascade})
   -> 0.0152s
-- create_table("clusters", {:id=>:serial, :force=>:cascade})
   -> 0.0207s
-- create_table("clusters_applications_cert_managers", {:id=>:serial, :force=>:cascade})
   -> 0.0074s
-- create_table("clusters_applications_crossplane", {:id=>:serial, :force=>:cascade})
   -> 0.0174s
-- create_table("clusters_applications_elastic_stacks", {:force=>:cascade})
   -> 0.0108s
-- create_table("clusters_applications_helm", {:id=>:serial, :force=>:cascade})
   -> 0.0063s
-- create_table("clusters_applications_ingress", {:id=>:serial, :force=>:cascade})
   -> 0.0067s
-- create_table("clusters_applications_jupyter", {:id=>:serial, :force=>:cascade})
   -> 0.0187s
-- create_table("clusters_applications_knative", {:id=>:serial, :force=>:cascade})
   -> 0.0101s
-- create_table("clusters_applications_prometheus", {:id=>:serial, :force=>:cascade})
   -> 0.0070s
-- create_table("clusters_applications_runners", {:id=>:serial, :force=>:cascade})
   -> 0.0138s
-- create_table("clusters_kubernetes_namespaces", {:force=>:cascade})
   -> 0.0254s
-- create_table("commit_user_mentions", {:force=>:cascade})
   -> 0.0086s
-- create_table("container_expiration_policies", {:primary_key=>"project_id", :id=>:bigint, :default=>nil, :force=>:cascade})
   -> 0.0138s
-- create_table("container_repositories", {:id=>:serial, :force=>:cascade})
   -> 0.0307s
-- create_table("conversational_development_index_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0189s
-- create_table("dependency_proxy_blobs", {:id=>:serial, :force=>:cascade})
   -> 0.0119s
-- create_table("dependency_proxy_group_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0090s
-- create_table("deploy_keys_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0150s
-- create_table("deploy_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0176s
-- create_table("deployment_merge_requests", {:id=>false, :force=>:cascade})
   -> 0.0079s
-- create_table("deployments", {:id=>:serial, :force=>:cascade})
   -> 0.0707s
-- create_table("description_versions", {:force=>:cascade})
   -> 0.0177s
-- create_table("design_management_designs", {:force=>:cascade})
   -> 0.0182s
-- create_table("design_management_designs_versions", {:id=>false, :force=>:cascade})
   -> 0.0158s
-- create_table("design_management_versions", {:force=>:cascade})
   -> 0.0319s
-- create_table("design_user_mentions", {:force=>:cascade})
   -> 0.0096s
-- create_table("draft_notes", {:force=>:cascade})
   -> 0.0179s
-- create_table("elasticsearch_indexed_namespaces", {:id=>false, :force=>:cascade})
   -> 0.0052s
-- create_table("elasticsearch_indexed_projects", {:id=>false, :force=>:cascade})
   -> 0.0046s
-- create_table("emails", {:id=>:serial, :force=>:cascade})
   -> 0.0129s
-- create_table("environments", {:id=>:serial, :force=>:cascade})
   -> 0.1087s
-- create_table("epic_issues", {:id=>:serial, :force=>:cascade})
   -> 0.0094s
-- create_table("epic_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0055s
-- create_table("epic_user_mentions", {:force=>:cascade})
   -> 0.0179s
-- create_table("epics", {:id=>:serial, :force=>:cascade})
   -> 0.0449s
-- create_table("events", {:id=>:serial, :force=>:cascade})
   -> 0.0237s
-- create_table("evidences", {:force=>:cascade})
   -> 0.0097s
-- create_table("external_pull_requests", {:force=>:cascade})
   -> 0.0129s
-- create_table("feature_gates", {:id=>:serial, :force=>:cascade})
   -> 0.0087s
-- create_table("features", {:id=>:serial, :force=>:cascade})
   -> 0.0069s
-- create_table("fork_network_members", {:id=>:serial, :force=>:cascade})
   -> 0.0137s
-- create_table("fork_networks", {:id=>:serial, :force=>:cascade})
   -> 0.0080s
-- create_table("forked_project_links", {:id=>:serial, :force=>:cascade})
   -> 0.0108s
-- create_table("geo_cache_invalidation_events", {:force=>:cascade})
   -> 0.0038s
-- create_table("geo_container_repository_updated_events", {:force=>:cascade})
   -> 0.0054s
-- create_table("geo_event_log", {:force=>:cascade})
   -> 0.0432s
-- create_table("geo_hashed_storage_attachments_events", {:force=>:cascade})
   -> 0.0115s
-- create_table("geo_hashed_storage_migrated_events", {:force=>:cascade})
   -> 0.0096s
-- create_table("geo_job_artifact_deleted_events", {:force=>:cascade})
   -> 0.0096s
-- create_table("geo_lfs_object_deleted_events", {:force=>:cascade})
   -> 0.0064s
-- create_table("geo_node_namespace_links", {:id=>:serial, :force=>:cascade})
   -> 0.0169s
-- create_table("geo_node_statuses", {:id=>:serial, :force=>:cascade})
   -> 0.0110s
-- create_table("geo_nodes", {:id=>:serial, :force=>:cascade})
   -> 0.0191s
-- create_table("geo_repositories_changed_events", {:force=>:cascade})
   -> 0.0098s
-- create_table("geo_repository_created_events", {:force=>:cascade})
   -> 0.0092s
-- create_table("geo_repository_deleted_events", {:force=>:cascade})
   -> 0.0093s
-- create_table("geo_repository_renamed_events", {:force=>:cascade})
   -> 0.0072s
-- create_table("geo_repository_updated_events", {:force=>:cascade})
   -> 0.0142s
-- create_table("geo_reset_checksum_events", {:force=>:cascade})
   -> 0.0077s
-- create_table("geo_upload_deleted_events", {:force=>:cascade})
   -> 0.0110s
-- create_table("gitlab_subscription_histories", {:force=>:cascade})
   -> 0.0057s
-- create_table("gitlab_subscriptions", {:force=>:cascade})
   -> 0.0093s
-- create_table("gpg_key_subkeys", {:id=>:serial, :force=>:cascade})
   -> 0.0162s
-- create_table("gpg_keys", {:id=>:serial, :force=>:cascade})
   -> 0.0134s
-- create_table("gpg_signatures", {:id=>:serial, :force=>:cascade})
   -> 0.0185s
-- create_table("grafana_integrations", {:force=>:cascade})
   -> 0.0132s
-- create_table("group_custom_attributes", {:id=>:serial, :force=>:cascade})
   -> 0.0122s
-- create_table("group_deletion_schedules", {:primary_key=>"group_id", :id=>:bigint, :default=>nil, :force=>:cascade})
   -> 0.0066s
-- create_table("group_group_links", {:force=>:cascade})
   -> 0.0115s
-- create_table("historical_data", {:id=>:serial, :force=>:cascade})
   -> 0.0038s
-- create_table("identities", {:id=>:serial, :force=>:cascade})
   -> 0.0158s
-- create_table("import_export_uploads", {:id=>:serial, :force=>:cascade})
   -> 0.0108s
-- create_table("import_failures", {:force=>:cascade})
   -> 0.0204s
-- create_table("index_statuses", {:id=>:serial, :force=>:cascade})
   -> 0.0099s
-- create_table("insights", {:id=>:serial, :force=>:cascade})
   -> 0.0113s
-- create_table("internal_ids", {:force=>:cascade})
   -> 0.0216s
-- create_table("ip_restrictions", {:force=>:cascade})
   -> 0.0095s
-- create_table("issue_assignees", {:id=>false, :force=>:cascade})
   -> 0.0061s
-- create_table("issue_links", {:id=>:serial, :force=>:cascade})
   -> 0.0108s
-- create_table("issue_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0137s
-- create_table("issue_tracker_data", {:force=>:cascade})
   -> 0.0092s
-- create_table("issue_user_mentions", {:force=>:cascade})
   -> 0.0130s
-- create_table("issues", {:id=>:serial, :force=>:cascade})
   -> 0.0806s
-- create_table("issues_prometheus_alert_events", {:id=>false, :force=>:cascade})
   -> 0.0060s
-- create_table("issues_self_managed_prometheus_alert_events", {:id=>false, :force=>:cascade})
   -> 0.0139s
-- create_table("jira_connect_installations", {:force=>:cascade})
   -> 0.0094s
-- create_table("jira_connect_subscriptions", {:force=>:cascade})
   -> 0.0113s
-- create_table("jira_tracker_data", {:force=>:cascade})
   -> 0.0065s
-- create_table("keys", {:id=>:serial, :force=>:cascade})
   -> 0.0272s
-- create_table("label_links", {:id=>:serial, :force=>:cascade})
   -> 0.0086s
-- create_table("label_priorities", {:id=>:serial, :force=>:cascade})
   -> 0.0145s
-- create_table("labels", {:id=>:serial, :force=>:cascade})
   -> 0.0275s
-- create_table("ldap_group_links", {:id=>:serial, :force=>:cascade})
   -> 0.0034s
-- create_table("lfs_file_locks", {:id=>:serial, :force=>:cascade})
   -> 0.0158s
-- create_table("lfs_objects", {:id=>:serial, :force=>:cascade})
   -> 0.0170s
-- create_table("lfs_objects_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0173s
-- create_table("licenses", {:id=>:serial, :force=>:cascade})
   -> 0.0054s
-- create_table("list_user_preferences", {:force=>:cascade})
   -> 0.0155s
-- create_table("lists", {:id=>:serial, :force=>:cascade})
   -> 0.0324s
-- create_table("members", {:id=>:serial, :force=>:cascade})
   -> 0.0314s
-- create_table("merge_request_assignees", {:force=>:cascade})
   -> 0.0140s
-- create_table("merge_request_blocks", {:force=>:cascade})
   -> 0.0086s
-- create_table("merge_request_diff_commits", {:id=>false, :force=>:cascade})
   -> 0.0085s
-- create_table("merge_request_diff_files", {:id=>false, :force=>:cascade})
   -> 0.0127s
-- create_table("merge_request_diffs", {:id=>:serial, :force=>:cascade})
   -> 0.0193s
-- create_table("merge_request_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0346s
-- create_table("merge_request_user_mentions", {:force=>:cascade})
   -> 0.0164s
-- create_table("merge_requests", {:id=>:serial, :force=>:cascade})
   -> 0.1091s
-- create_table("merge_requests_closing_issues", {:id=>:serial, :force=>:cascade})
   -> 0.0084s
-- create_table("merge_trains", {:force=>:cascade})
   -> 0.0197s
-- create_table("milestone_releases", {:id=>false, :force=>:cascade})
   -> 0.0133s
-- create_table("milestones", {:id=>:serial, :force=>:cascade})
   -> 0.0273s
-- create_table("namespace_aggregation_schedules", {:primary_key=>"namespace_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0071s
-- create_table("namespace_root_storage_statistics", {:primary_key=>"namespace_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0110s
-- create_table("namespace_statistics", {:id=>:serial, :force=>:cascade})
   -> 0.0062s
-- create_table("namespaces", {:id=>:serial, :force=>:cascade})
   -> 0.0895s
-- create_table("note_diff_files", {:id=>:serial, :force=>:cascade})
   -> 0.0143s
-- create_table("notes", {:id=>:serial, :force=>:cascade})
   -> 0.0550s
-- create_table("notification_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0196s
-- create_table("oauth_access_grants", {:id=>:serial, :force=>:cascade})
   -> 0.0150s
-- create_table("oauth_access_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0217s
-- create_table("oauth_applications", {:id=>:serial, :force=>:cascade})
   -> 0.0166s
-- create_table("oauth_openid_requests", {:id=>:serial, :force=>:cascade})
   -> 0.0122s
-- create_table("operations_feature_flag_scopes", {:force=>:cascade})
   -> 0.0104s
-- create_table("operations_feature_flags", {:force=>:cascade})
   -> 0.0191s
-- create_table("operations_feature_flags_clients", {:force=>:cascade})
   -> 0.0107s
-- create_table("packages_build_infos", {:force=>:cascade})
   -> 0.0099s
-- create_table("packages_conan_file_metadata", {:force=>:cascade})
   -> 0.0105s
-- create_table("packages_conan_metadata", {:force=>:cascade})
   -> 0.0114s
-- create_table("packages_dependencies", {:force=>:cascade})
   -> 0.0131s
-- create_table("packages_dependency_links", {:force=>:cascade})
   -> 0.0113s
-- create_table("packages_maven_metadata", {:force=>:cascade})
   -> 0.0128s
-- create_table("packages_package_files", {:force=>:cascade})
   -> 0.0175s
-- create_table("packages_package_tags", {:force=>:cascade})
   -> 0.0086s
-- create_table("packages_packages", {:force=>:cascade})
   -> 0.0210s
-- create_table("pages_domain_acme_orders", {:force=>:cascade})
   -> 0.0156s
-- create_table("pages_domains", {:id=>:serial, :force=>:cascade})
   -> 0.0638s
-- create_table("path_locks", {:id=>:serial, :force=>:cascade})
   -> 0.0247s
-- create_table("personal_access_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0391s
-- create_table("plan_limits", {:force=>:cascade})
   -> 0.0180s
-- create_table("plans", {:id=>:serial, :force=>:cascade})
   -> 0.0148s
-- create_table("pool_repositories", {:force=>:cascade})
   -> 0.0189s
-- create_table("programming_languages", {:id=>:serial, :force=>:cascade})
   -> 0.0143s
-- create_table("project_alerting_settings", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0070s
-- create_table("project_aliases", {:force=>:cascade})
   -> 0.0180s
-- create_table("project_authorizations", {:id=>false, :force=>:cascade})
   -> 0.0154s
-- create_table("project_auto_devops", {:id=>:serial, :force=>:cascade})
   -> 0.0120s
-- create_table("project_ci_cd_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0105s
-- create_table("project_custom_attributes", {:id=>:serial, :force=>:cascade})
   -> 0.0190s
-- create_table("project_daily_statistics", {:force=>:cascade})
   -> 0.0107s
-- create_table("project_deploy_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0129s
-- create_table("project_error_tracking_settings", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0077s
-- create_table("project_feature_usages", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0217s
-- create_table("project_features", {:id=>:serial, :force=>:cascade})
   -> 0.0116s
-- create_table("project_group_links", {:id=>:serial, :force=>:cascade})
   -> 0.0215s
-- create_table("project_import_data", {:id=>:serial, :force=>:cascade})
   -> 0.0122s
-- create_table("project_incident_management_settings", {:primary_key=>"project_id", :id=>:serial, :force=>:cascade})
   -> 0.0063s
-- create_table("project_metrics_settings", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0119s
-- create_table("project_mirror_data", {:id=>:serial, :force=>:cascade})
   -> 0.0391s
-- create_table("project_pages_metadata", {:id=>false, :force=>:cascade})
   -> 0.0146s
-- create_table("project_repositories", {:force=>:cascade})
   -> 0.0191s
-- create_table("project_repository_states", {:id=>:serial, :force=>:cascade})
   -> 0.0416s
-- create_table("project_statistics", {:id=>:serial, :force=>:cascade})
   -> 0.0299s
-- create_table("project_tracing_settings", {:force=>:cascade})
   -> 0.0108s
-- create_table("projects", {:id=>:serial, :force=>:cascade})
   -> 0.1689s
-- create_table("prometheus_alert_events", {:force=>:cascade})
   -> 0.0199s
-- create_table("prometheus_alerts", {:id=>:serial, :force=>:cascade})
   -> 0.0184s
-- create_table("prometheus_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0311s
-- create_table("protected_branch_merge_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0223s
-- create_table("protected_branch_push_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0260s
-- create_table("protected_branch_unprotect_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0238s
-- create_table("protected_branches", {:id=>:serial, :force=>:cascade})
   -> 0.0155s
-- create_table("protected_environment_deploy_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0209s
-- create_table("protected_environments", {:id=>:serial, :force=>:cascade})
   -> 0.0207s
-- create_table("protected_tag_create_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0287s
-- create_table("protected_tags", {:id=>:serial, :force=>:cascade})
   -> 0.0136s
-- create_table("push_event_payloads", {:id=>false, :force=>:cascade})
   -> 0.0104s
-- create_table("push_rules", {:id=>:serial, :force=>:cascade})
   -> 0.0201s
-- create_table("redirect_routes", {:id=>:serial, :force=>:cascade})
   -> 0.0201s
-- create_table("release_links", {:force=>:cascade})
   -> 0.0280s
-- create_table("releases", {:id=>:serial, :force=>:cascade})
   -> 0.0209s
-- create_table("remote_mirrors", {:id=>:serial, :force=>:cascade})
   -> 0.0217s
-- create_table("repository_languages", {:id=>false, :force=>:cascade})
   -> 0.0169s
-- create_table("resource_label_events", {:force=>:cascade})
   -> 0.0346s
-- create_table("resource_weight_events", {:force=>:cascade})
   -> 0.0174s
-- create_table("reviews", {:force=>:cascade})
   -> 0.0181s
-- create_table("routes", {:id=>:serial, :force=>:cascade})
   -> 0.0259s
-- create_table("saml_providers", {:id=>:serial, :force=>:cascade})
   -> 0.0110s
-- create_table("scim_oauth_access_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0175s
-- create_table("self_managed_prometheus_alert_events", {:force=>:cascade})
   -> 0.0193s
-- create_table("sent_notifications", {:id=>:serial, :force=>:cascade})
   -> 0.0106s
-- create_table("sentry_issues", {:force=>:cascade})
   -> 0.0119s
-- create_table("serverless_domain_cluster", {:primary_key=>"uuid", :id=>:string, :limit=>14, :force=>:cascade})
   -> 0.0192s
-- create_table("service_desk_settings", {:primary_key=>"project_id", :id=>:bigint, :default=>nil, :force=>:cascade})
   -> 0.0048s
-- create_table("services", {:id=>:serial, :force=>:cascade})
   -> 0.0400s
-- create_table("shards", {:id=>:serial, :force=>:cascade})
   -> 0.0115s
-- create_table("slack_integrations", {:id=>:serial, :force=>:cascade})
   -> 0.0219s
-- create_table("smartcard_identities", {:force=>:cascade})
   -> 0.0144s
-- create_table("snippet_user_mentions", {:force=>:cascade})
   -> 0.0270s
-- create_table("snippets", {:id=>:serial, :force=>:cascade})
   -> 0.0495s
-- create_table("software_license_policies", {:id=>:serial, :force=>:cascade})
   -> 0.0173s
-- create_table("software_licenses", {:id=>:serial, :force=>:cascade})
   -> 0.0184s
-- create_table("spam_logs", {:id=>:serial, :force=>:cascade})
   -> 0.0058s
-- create_table("subscriptions", {:id=>:serial, :force=>:cascade})
   -> 0.0154s
-- create_table("suggestions", {:force=>:cascade})
   -> 0.0139s
-- create_table("system_note_metadata", {:id=>:serial, :force=>:cascade})
   -> 0.0136s
-- create_table("taggings", {:id=>:serial, :force=>:cascade})
   -> 0.0317s
-- create_table("tags", {:id=>:serial, :force=>:cascade})
   -> 0.0103s
-- create_table("term_agreements", {:id=>:serial, :force=>:cascade})
   -> 0.0174s
-- create_table("timelogs", {:id=>:serial, :force=>:cascade})
   -> 0.0247s
-- create_table("todos", {:id=>:serial, :force=>:cascade})
   -> 0.0471s
-- create_table("trending_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0120s
-- create_table("u2f_registrations", {:id=>:serial, :force=>:cascade})
   -> 0.0166s
-- create_table("uploads", {:id=>:serial, :force=>:cascade})
   -> 0.0241s
-- create_table("user_agent_details", {:id=>:serial, :force=>:cascade})
   -> 0.0114s
-- create_table("user_callouts", {:id=>:serial, :force=>:cascade})
   -> 0.0124s
-- create_table("user_custom_attributes", {:id=>:serial, :force=>:cascade})
   -> 0.0167s
-- create_table("user_interacted_projects", {:id=>false, :force=>:cascade})
   -> 0.0113s
-- create_table("user_preferences", {:id=>:serial, :force=>:cascade})
   -> 0.0098s
-- create_table("user_statuses", {:primary_key=>"user_id", :id=>:serial, :force=>:cascade})
   -> 0.0085s
-- create_table("user_synced_attributes_metadata", {:id=>:serial, :force=>:cascade})
   -> 0.0132s
-- create_table("users", {:id=>:serial, :force=>:cascade})
   -> 0.1260s
-- create_table("users_ops_dashboard_projects", {:force=>:cascade})
   -> 0.0153s
-- create_table("users_security_dashboard_projects", {:id=>false, :force=>:cascade})
   -> 0.0091s
-- create_table("users_star_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0140s
-- create_table("vulnerabilities", {:force=>:cascade})
   -> 0.0486s
-- create_table("vulnerability_feedback", {:id=>:serial, :force=>:cascade})
   -> 0.0353s
-- create_table("vulnerability_identifiers", {:force=>:cascade})
   -> 0.0094s
-- create_table("vulnerability_issue_links", {:force=>:cascade})
   -> 0.0139s
-- create_table("vulnerability_occurrence_identifiers", {:force=>:cascade})
   -> 0.0202s
-- create_table("vulnerability_occurrence_pipelines", {:force=>:cascade})
   -> 0.0194s
-- create_table("vulnerability_occurrences", {:force=>:cascade})
   -> 0.1168s
-- create_table("vulnerability_scanners", {:force=>:cascade})
   -> 0.0086s
-- create_table("web_hook_logs", {:id=>:serial, :force=>:cascade})
   -> 0.0152s
-- create_table("web_hooks", {:id=>:serial, :force=>:cascade})
   -> 0.0197s
-- create_table("zoom_meetings", {:force=>:cascade})
   -> 0.0134s
-- add_foreign_key("alerts_service_data", "services", {:on_delete=>:cascade})
   -> 0.0110s
-- add_foreign_key("allowed_email_domains", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("analytics_cycle_analytics_group_stages", "labels", {:column=>"end_event_label_id", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("analytics_cycle_analytics_group_stages", "labels", {:column=>"start_event_label_id", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("analytics_cycle_analytics_group_stages", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("analytics_cycle_analytics_project_stages", "labels", {:column=>"end_event_label_id", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("analytics_cycle_analytics_project_stages", "labels", {:column=>"start_event_label_id", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("analytics_cycle_analytics_project_stages", "projects", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("analytics_language_trend_repository_languages", "programming_languages", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("analytics_language_trend_repository_languages", "projects", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("analytics_repository_file_commits", "analytics_repository_files", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("analytics_repository_file_commits", "projects", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("analytics_repository_file_edits", "analytics_repository_files", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("analytics_repository_file_edits", "projects", {:on_delete=>:cascade})
   -> 0.0048s
-- add_foreign_key("analytics_repository_files", "projects", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("application_settings", "namespaces", {:column=>"custom_project_templates_group_id", :on_delete=>:nullify})
   -> 0.0039s
-- add_foreign_key("application_settings", "projects", {:column=>"file_template_project_id", :name=>"fk_ec757bd087", :on_delete=>:nullify})
   -> 0.0030s
-- add_foreign_key("application_settings", "projects", {:column=>"instance_administration_project_id", :on_delete=>:nullify})
   -> 0.0031s
-- add_foreign_key("application_settings", "users", {:column=>"usage_stats_set_by_user_id", :name=>"fk_964370041d", :on_delete=>:nullify})
   -> 0.0053s
-- add_foreign_key("approval_merge_request_rule_sources", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("approval_merge_request_rule_sources", "approval_project_rules", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("approval_merge_request_rules", "merge_requests", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("approval_merge_request_rules_approved_approvers", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("approval_merge_request_rules_approved_approvers", "users", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("approval_merge_request_rules_groups", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("approval_merge_request_rules_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("approval_merge_request_rules_users", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("approval_merge_request_rules_users", "users", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("approval_project_rules", "projects", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("approval_project_rules_groups", "approval_project_rules", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("approval_project_rules_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("approval_project_rules_users", "approval_project_rules", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("approval_project_rules_users", "users", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("approvals", "merge_requests", {:name=>"fk_310d714958", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("approver_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("aws_roles", "users", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("badges", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("badges", "projects", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("board_assignees", "boards", {:on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("board_assignees", "users", {:column=>"assignee_id", :on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("board_group_recent_visits", "boards", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("board_group_recent_visits", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("board_group_recent_visits", "users", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("board_labels", "boards", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("board_labels", "labels", {:on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("board_project_recent_visits", "boards", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("board_project_recent_visits", "projects", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("board_project_recent_visits", "users", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("boards", "namespaces", {:column=>"group_id", :name=>"fk_1e9a074a35", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("boards", "projects", {:name=>"fk_f15266b5f9", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("chat_teams", "namespaces", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("ci_build_needs", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0088s
-- add_foreign_key("ci_build_trace_chunks", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("ci_build_trace_section_names", "projects", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("ci_build_trace_sections", "ci_build_trace_section_names", {:column=>"section_name_id", :name=>"fk_264e112c66", :on_delete=>:cascade})
   -> 0.0015s
-- add_foreign_key("ci_build_trace_sections", "ci_builds", {:column=>"build_id", :name=>"fk_4ebe41f502", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("ci_build_trace_sections", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("ci_builds", "ci_pipelines", {:column=>"auto_canceled_by_id", :name=>"fk_a2141b1522", :on_delete=>:nullify})
   -> 0.0035s
-- add_foreign_key("ci_builds", "ci_pipelines", {:column=>"commit_id", :name=>"fk_d3130c9a7f", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("ci_builds", "ci_pipelines", {:column=>"upstream_pipeline_id", :name=>"fk_87f4cefcda", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("ci_builds", "ci_resource_groups", {:column=>"resource_group_id", :name=>"fk_6661f4f0e8", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("ci_builds", "ci_stages", {:column=>"stage_id", :name=>"fk_3a9eaa254d", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("ci_builds", "projects", {:name=>"fk_befce0568a", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("ci_builds_metadata", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("ci_builds_metadata", "projects", {:on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("ci_builds_runner_session", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("ci_group_variables", "namespaces", {:column=>"group_id", :name=>"fk_33ae4d58d8", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("ci_job_artifacts", "ci_builds", {:column=>"job_id", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("ci_job_artifacts", "projects", {:on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("ci_job_variables", "ci_builds", {:column=>"job_id", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("ci_pipeline_chat_data", "chat_names", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("ci_pipeline_chat_data", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("ci_pipeline_schedule_variables", "ci_pipeline_schedules", {:column=>"pipeline_schedule_id", :name=>"fk_41c35fda51", :on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("ci_pipeline_schedules", "projects", {:name=>"fk_8ead60fcc4", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("ci_pipeline_schedules", "users", {:column=>"owner_id", :name=>"fk_9ea99f58d2", :on_delete=>:nullify})
   -> 0.0031s
-- add_foreign_key("ci_pipeline_variables", "ci_pipelines", {:column=>"pipeline_id", :name=>"fk_f29c5f4380", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("ci_pipelines", "ci_pipeline_schedules", {:column=>"pipeline_schedule_id", :name=>"fk_3d34ab2e06", :on_delete=>:nullify})
   -> 0.0018s
-- add_foreign_key("ci_pipelines", "ci_pipelines", {:column=>"auto_canceled_by_id", :name=>"fk_262d4c2d19", :on_delete=>:nullify})
   -> 0.0017s
-- add_foreign_key("ci_pipelines", "external_pull_requests", {:name=>"fk_190998ef09", :on_delete=>:nullify})
   -> 0.0020s
-- add_foreign_key("ci_pipelines", "merge_requests", {:name=>"fk_a23be95014", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("ci_pipelines", "projects", {:name=>"fk_86635dbd80", :on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("ci_pipelines_config", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("ci_resource_groups", "projects", {:name=>"fk_774722d144", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("ci_resources", "ci_builds", {:column=>"build_id", :name=>"fk_e169a8e3d5", :on_delete=>:nullify})
   -> 0.0033s
-- add_foreign_key("ci_resources", "ci_resource_groups", {:column=>"resource_group_id", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("ci_runner_namespaces", "ci_runners", {:column=>"runner_id", :on_delete=>:cascade})
   -> 0.0064s
-- add_foreign_key("ci_runner_namespaces", "namespaces", {:on_delete=>:cascade})
   -> 0.0402s
-- add_foreign_key("ci_runner_projects", "projects", {:name=>"fk_4478a6f1e4", :on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("ci_sources_pipelines", "ci_builds", {:column=>"source_job_id", :name=>"fk_be5624bf37", :on_delete=>:cascade})
   -> 0.0054s
-- add_foreign_key("ci_sources_pipelines", "ci_pipelines", {:column=>"pipeline_id", :name=>"fk_e1bad85861", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("ci_sources_pipelines", "ci_pipelines", {:column=>"source_pipeline_id", :name=>"fk_d4e29af7d7", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("ci_sources_pipelines", "projects", {:column=>"source_project_id", :name=>"fk_acd9737679", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("ci_sources_pipelines", "projects", {:name=>"fk_1e53c97c0a", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("ci_stages", "ci_pipelines", {:column=>"pipeline_id", :name=>"fk_fb57e6cc56", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("ci_stages", "projects", {:name=>"fk_2360681d1d", :on_delete=>:cascade})
   -> 0.0062s
-- add_foreign_key("ci_subscriptions_projects", "projects", {:column=>"downstream_project_id", :on_delete=>:cascade})
   -> 0.0046s
-- add_foreign_key("ci_subscriptions_projects", "projects", {:column=>"upstream_project_id", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("ci_trigger_requests", "ci_triggers", {:column=>"trigger_id", :name=>"fk_b8ec8b7245", :on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("ci_triggers", "projects", {:name=>"fk_e3e63f966e", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("ci_triggers", "users", {:column=>"owner_id", :name=>"fk_e8e10d1964", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("ci_variables", "projects", {:name=>"fk_ada5eb64b3", :on_delete=>:cascade})
   -> 0.0053s
-- add_foreign_key("cluster_groups", "clusters", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("cluster_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("cluster_platforms_kubernetes", "clusters", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("cluster_projects", "clusters", {:on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("cluster_projects", "projects", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("cluster_providers_aws", "clusters", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("cluster_providers_aws", "users", {:column=>"created_by_user_id", :on_delete=>:nullify})
   -> 0.0020s
-- add_foreign_key("cluster_providers_gcp", "clusters", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("clusters", "projects", {:column=>"management_project_id", :name=>"fk_f05c5e5a42", :on_delete=>:nullify})
   -> 0.0022s
-- add_foreign_key("clusters", "users", {:on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("clusters_applications_cert_managers", "clusters", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("clusters_applications_crossplane", "clusters", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("clusters_applications_elastic_stacks", "clusters", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("clusters_applications_helm", "clusters", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("clusters_applications_ingress", "clusters", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("clusters_applications_jupyter", "clusters", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("clusters_applications_jupyter", "oauth_applications", {:on_delete=>:nullify})
   -> 0.0027s
-- add_foreign_key("clusters_applications_knative", "clusters", {:on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("clusters_applications_prometheus", "clusters", {:name=>"fk_557e773639", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("clusters_applications_runners", "ci_runners", {:column=>"runner_id", :name=>"fk_02de2ded36", :on_delete=>:nullify})
   -> 0.0034s
-- add_foreign_key("clusters_applications_runners", "clusters", {:on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("clusters_kubernetes_namespaces", "cluster_projects", {:on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("clusters_kubernetes_namespaces", "clusters", {:on_delete=>:cascade})
   -> 0.0016s
-- add_foreign_key("clusters_kubernetes_namespaces", "environments", {:on_delete=>:nullify})
   -> 0.0022s
-- add_foreign_key("clusters_kubernetes_namespaces", "projects", {:on_delete=>:nullify})
   -> 0.0033s
-- add_foreign_key("commit_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0050s
-- add_foreign_key("container_expiration_policies", "projects", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("container_repositories", "projects")
   -> 0.0037s
-- add_foreign_key("dependency_proxy_blobs", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("dependency_proxy_group_settings", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("deploy_keys_projects", "projects", {:name=>"fk_58a901ca7e", :on_delete=>:cascade})
   -> 0.0058s
-- add_foreign_key("deployment_merge_requests", "deployments", {:on_delete=>:cascade})
   -> 0.0079s
-- add_foreign_key("deployment_merge_requests", "merge_requests", {:on_delete=>:cascade})
   -> 0.0016s
-- add_foreign_key("deployments", "clusters", {:name=>"fk_289bba3222", :on_delete=>:nullify})
   -> 0.0015s
-- add_foreign_key("deployments", "projects", {:name=>"fk_b9a3851b82", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("description_versions", "epics", {:on_delete=>:cascade})
   -> 0.0051s
-- add_foreign_key("description_versions", "issues", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("description_versions", "merge_requests", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("design_management_designs", "issues", {:on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("design_management_designs", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("design_management_designs_versions", "design_management_designs", {:column=>"design_id", :name=>"fk_03c671965c", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("design_management_designs_versions", "design_management_versions", {:column=>"version_id", :name=>"fk_f4d25ba00c", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("design_management_versions", "issues", {:on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("design_management_versions", "users", {:column=>"author_id", :name=>"fk_c1440b4896", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("design_user_mentions", "design_management_designs", {:column=>"design_id", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("design_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0016s
-- add_foreign_key("draft_notes", "merge_requests", {:on_delete=>:cascade})
   -> 0.0056s
-- add_foreign_key("draft_notes", "users", {:column=>"author_id", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("elasticsearch_indexed_namespaces", "namespaces", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("elasticsearch_indexed_projects", "projects", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("environments", "projects", {:name=>"fk_d1c8c1da6a", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("epic_issues", "epics", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("epic_issues", "issues", {:on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("epic_metrics", "epics", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("epic_user_mentions", "epics", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("epic_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("epics", "epics", {:column=>"due_date_sourcing_epic_id", :name=>"fk_013c9f36ca", :on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("epics", "epics", {:column=>"parent_id", :name=>"fk_25b99c1be3", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("epics", "epics", {:column=>"start_date_sourcing_epic_id", :name=>"fk_9d480c64b2", :on_delete=>:nullify})
   -> 0.0027s
-- add_foreign_key("epics", "milestones", {:on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("epics", "namespaces", {:column=>"group_id", :name=>"fk_f081aa4489", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("epics", "users", {:column=>"assignee_id", :name=>"fk_dccd3f98fc", :on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("epics", "users", {:column=>"author_id", :name=>"fk_3654b61b03", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("epics", "users", {:column=>"closed_by_id", :name=>"fk_aa5798e761", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("events", "namespaces", {:column=>"group_id", :name=>"fk_61fbf6ca48", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("events", "projects", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("events", "users", {:column=>"author_id", :name=>"fk_edfd187b6f", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("evidences", "releases", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("external_pull_requests", "projects", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("fork_network_members", "fork_networks", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("fork_network_members", "projects", {:column=>"forked_from_project_id", :name=>"fk_b01280dae4", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("fork_network_members", "projects", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("fork_networks", "projects", {:column=>"root_project_id", :name=>"fk_e7b436b2b5", :on_delete=>:nullify})
   -> 0.0071s
-- add_foreign_key("forked_project_links", "projects", {:column=>"forked_to_project_id", :name=>"fk_434510edb0", :on_delete=>:cascade})
   -> 0.0072s
-- add_foreign_key("geo_container_repository_updated_events", "container_repositories", {:name=>"fk_212c89c706", :on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("geo_event_log", "geo_cache_invalidation_events", {:column=>"cache_invalidation_event_id", :name=>"fk_42c3b54bed", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("geo_event_log", "geo_container_repository_updated_events", {:column=>"container_repository_updated_event_id", :name=>"fk_6ada82d42a", :on_delete=>:cascade})
   -> 0.0015s
-- add_foreign_key("geo_event_log", "geo_hashed_storage_migrated_events", {:column=>"hashed_storage_migrated_event_id", :name=>"fk_27548c6db3", :on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("geo_event_log", "geo_job_artifact_deleted_events", {:column=>"job_artifact_deleted_event_id", :name=>"fk_176d3fbb5d", :on_delete=>:cascade})
   -> 0.0049s
-- add_foreign_key("geo_event_log", "geo_lfs_object_deleted_events", {:column=>"lfs_object_deleted_event_id", :name=>"fk_d5af95fcd9", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("geo_event_log", "geo_repositories_changed_events", {:column=>"repositories_changed_event_id", :name=>"fk_4a99ebfd60", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("geo_event_log", "geo_repository_created_events", {:column=>"repository_created_event_id", :name=>"fk_9b9afb1916", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("geo_event_log", "geo_repository_deleted_events", {:column=>"repository_deleted_event_id", :name=>"fk_c4b1c1f66e", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("geo_event_log", "geo_repository_renamed_events", {:column=>"repository_renamed_event_id", :name=>"fk_86c84214ec", :on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("geo_event_log", "geo_repository_updated_events", {:column=>"repository_updated_event_id", :name=>"fk_78a6492f68", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("geo_event_log", "geo_reset_checksum_events", {:column=>"reset_checksum_event_id", :name=>"fk_cff7185ad2", :on_delete=>:cascade})
   -> 0.0042s
-- add_foreign_key("geo_event_log", "geo_upload_deleted_events", {:column=>"upload_deleted_event_id", :name=>"fk_c1f241c70d", :on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("geo_hashed_storage_attachments_events", "projects", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("geo_hashed_storage_migrated_events", "projects", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("geo_node_namespace_links", "geo_nodes", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("geo_node_namespace_links", "namespaces", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("geo_node_statuses", "geo_nodes", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("geo_repositories_changed_events", "geo_nodes", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("geo_repository_created_events", "projects", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("geo_repository_renamed_events", "projects", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("geo_repository_updated_events", "projects", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("geo_reset_checksum_events", "projects", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("gitlab_subscriptions", "namespaces", {:name=>"fk_e2595d00a1", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("gitlab_subscriptions", "plans", {:column=>"hosted_plan_id", :name=>"fk_bd0c4019c3", :on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("gpg_key_subkeys", "gpg_keys", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("gpg_keys", "users", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("gpg_signatures", "gpg_key_subkeys", {:on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("gpg_signatures", "gpg_keys", {:on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("gpg_signatures", "projects", {:on_delete=>:cascade})
   -> 0.0061s
-- add_foreign_key("grafana_integrations", "projects", {:on_delete=>:cascade})
   -> 0.0054s
-- add_foreign_key("group_custom_attributes", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("group_deletion_schedules", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("group_deletion_schedules", "users", {:name=>"fk_11e3ebfcdd", :on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("group_group_links", "namespaces", {:column=>"shared_group_id", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("group_group_links", "namespaces", {:column=>"shared_with_group_id", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("identities", "saml_providers", {:name=>"fk_aade90f0fc", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("import_export_uploads", "namespaces", {:column=>"group_id", :name=>"fk_83319d9721", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("import_export_uploads", "projects", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("index_statuses", "projects", {:name=>"fk_74b2492545", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("insights", "namespaces", {:on_delete=>:cascade})
   -> 0.0069s
-- add_foreign_key("insights", "projects", {:on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("internal_ids", "namespaces", {:name=>"fk_162941d509", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("internal_ids", "projects", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("ip_restrictions", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0066s
-- add_foreign_key("issue_assignees", "issues", {:name=>"fk_b7d881734a", :on_delete=>:cascade})
   -> 0.0042s
-- add_foreign_key("issue_assignees", "users", {:name=>"fk_5e0c8d9154", :on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("issue_links", "issues", {:column=>"source_id", :name=>"fk_c900194ff2", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("issue_links", "issues", {:column=>"target_id", :name=>"fk_e71bb44f1f", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("issue_metrics", "issues", {:on_delete=>:cascade})
   -> 0.0058s
-- add_foreign_key("issue_tracker_data", "services", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("issue_user_mentions", "issues", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("issue_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("issues", "epics", {:column=>"promoted_to_epic_id", :name=>"fk_df75a7c8b8", :on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("issues", "issues", {:column=>"duplicated_to_id", :name=>"fk_9c4516d665", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("issues", "issues", {:column=>"moved_to_id", :name=>"fk_a194299be1", :on_delete=>:nullify})
   -> 0.0018s
-- add_foreign_key("issues", "milestones", {:name=>"fk_96b1dd429c", :on_delete=>:nullify})
   -> 0.0055s
-- add_foreign_key("issues", "projects", {:name=>"fk_899c8f3231", :on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("issues", "users", {:column=>"author_id", :name=>"fk_05f1e72feb", :on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("issues", "users", {:column=>"closed_by_id", :name=>"fk_c63cbf6c25", :on_delete=>:nullify})
   -> 0.0030s
-- add_foreign_key("issues", "users", {:column=>"updated_by_id", :name=>"fk_ffed080f01", :on_delete=>:nullify})
   -> 0.0029s
-- add_foreign_key("issues_prometheus_alert_events", "issues", {:on_delete=>:cascade})
   -> 0.0049s
-- add_foreign_key("issues_prometheus_alert_events", "prometheus_alert_events", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("issues_self_managed_prometheus_alert_events", "issues", {:on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("issues_self_managed_prometheus_alert_events", "self_managed_prometheus_alert_events", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("jira_connect_subscriptions", "jira_connect_installations", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("jira_connect_subscriptions", "namespaces", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("jira_tracker_data", "services", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("label_links", "labels", {:name=>"fk_d97dd08678", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("label_priorities", "labels", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("label_priorities", "projects", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("labels", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("labels", "projects", {:name=>"fk_7de4989a69", :on_delete=>:cascade})
   -> 0.0067s
-- add_foreign_key("lfs_file_locks", "projects", {:on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("lfs_file_locks", "users", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("list_user_preferences", "lists", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("list_user_preferences", "users", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("lists", "boards", {:name=>"fk_0d3f677137", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("lists", "labels", {:name=>"fk_7a5553d60f", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("lists", "milestones", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("lists", "users", {:name=>"fk_d6cf4279f7", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("members", "users", {:name=>"fk_2e88fb7ce9", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("merge_request_assignees", "merge_requests", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("merge_request_assignees", "users", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("merge_request_blocks", "merge_requests", {:column=>"blocked_merge_request_id", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("merge_request_blocks", "merge_requests", {:column=>"blocking_merge_request_id", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("merge_request_diff_commits", "merge_request_diffs", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("merge_request_diff_files", "merge_request_diffs", {:on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("merge_request_diffs", "merge_requests", {:name=>"fk_8483f3258f", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("merge_request_metrics", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0082s
-- add_foreign_key("merge_request_metrics", "merge_requests", {:on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("merge_request_metrics", "users", {:column=>"latest_closed_by_id", :name=>"fk_ae440388cc", :on_delete=>:nullify})
   -> 0.0059s
-- add_foreign_key("merge_request_metrics", "users", {:column=>"merged_by_id", :name=>"fk_7f28d925f3", :on_delete=>:nullify})
   -> 0.0043s
-- add_foreign_key("merge_request_user_mentions", "merge_requests", {:on_delete=>:cascade})
   -> 0.0072s
-- add_foreign_key("merge_request_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("merge_requests", "ci_pipelines", {:column=>"head_pipeline_id", :name=>"fk_fd82eae0b9", :on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("merge_requests", "merge_request_diffs", {:column=>"latest_merge_request_diff_id", :name=>"fk_06067f5644", :on_delete=>:nullify})
   -> 0.0022s
-- add_foreign_key("merge_requests", "milestones", {:name=>"fk_6a5165a692", :on_delete=>:nullify})
   -> 0.0019s
-- add_foreign_key("merge_requests", "projects", {:column=>"source_project_id", :name=>"fk_3308fe130c", :on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("merge_requests", "projects", {:column=>"target_project_id", :name=>"fk_a6963e8447", :on_delete=>:cascade})
   -> 0.0065s
-- add_foreign_key("merge_requests", "users", {:column=>"assignee_id", :name=>"fk_6149611a04", :on_delete=>:nullify})
   -> 0.0042s
-- add_foreign_key("merge_requests", "users", {:column=>"author_id", :name=>"fk_e719a85f8a", :on_delete=>:nullify})
   -> 0.0033s
-- add_foreign_key("merge_requests", "users", {:column=>"merge_user_id", :name=>"fk_ad525e1f87", :on_delete=>:nullify})
   -> 0.0029s
-- add_foreign_key("merge_requests", "users", {:column=>"updated_by_id", :name=>"fk_641731faff", :on_delete=>:nullify})
   -> 0.0024s
-- add_foreign_key("merge_requests_closing_issues", "issues", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("merge_requests_closing_issues", "merge_requests", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("merge_trains", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("merge_trains", "merge_requests", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("merge_trains", "projects", {:column=>"target_project_id", :on_delete=>:cascade})
   -> 0.0095s
-- add_foreign_key("merge_trains", "users", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("milestone_releases", "milestones", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("milestone_releases", "releases", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("milestones", "namespaces", {:column=>"group_id", :name=>"fk_95650a40d4", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("milestones", "projects", {:name=>"fk_9bd0a0c791", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("namespace_aggregation_schedules", "namespaces", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("namespace_root_storage_statistics", "namespaces", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("namespace_statistics", "namespaces", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("namespaces", "namespaces", {:column=>"custom_project_templates_group_id", :name=>"fk_e7a0b20a6b", :on_delete=>:nullify})
   -> 0.0058s
-- add_foreign_key("namespaces", "plans", {:name=>"fk_fdd12e5b80", :on_delete=>:nullify})
   -> 0.0067s
-- add_foreign_key("namespaces", "projects", {:column=>"file_template_project_id", :name=>"fk_319256d87a", :on_delete=>:nullify})
   -> 0.0051s
-- add_foreign_key("note_diff_files", "notes", {:column=>"diff_note_id", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("notes", "projects", {:name=>"fk_99e097b079", :on_delete=>:cascade})
   -> 0.0060s
-- add_foreign_key("notes", "reviews", {:name=>"fk_2e82291620", :on_delete=>:nullify})
   -> 0.0028s
-- add_foreign_key("notification_settings", "users", {:name=>"fk_0c95e91db7", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("oauth_openid_requests", "oauth_access_grants", {:column=>"access_grant_id", :name=>"fk_77114b3b09", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("operations_feature_flag_scopes", "operations_feature_flags", {:column=>"feature_flag_id", :on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("operations_feature_flags", "projects", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("operations_feature_flags_clients", "projects", {:on_delete=>:cascade})
   -> 0.0082s
-- add_foreign_key("packages_build_infos", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("packages_build_infos", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("packages_conan_file_metadata", "packages_package_files", {:column=>"package_file_id", :on_delete=>:cascade})
   -> 0.0091s
-- add_foreign_key("packages_conan_metadata", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("packages_dependency_links", "packages_dependencies", {:column=>"dependency_id", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("packages_dependency_links", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("packages_maven_metadata", "packages_packages", {:column=>"package_id", :name=>"fk_be88aed360", :on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("packages_package_files", "packages_packages", {:column=>"package_id", :name=>"fk_86f0f182f8", :on_delete=>:cascade})
   -> 0.0046s
-- add_foreign_key("packages_package_tags", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("packages_packages", "projects", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("pages_domain_acme_orders", "pages_domains", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("pages_domains", "projects", {:name=>"fk_ea2f6dfc6f", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("path_locks", "projects", {:name=>"fk_5265c98f24", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("path_locks", "users")
   -> 0.0029s
-- add_foreign_key("personal_access_tokens", "users")
   -> 0.0088s
-- add_foreign_key("plan_limits", "plans", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("pool_repositories", "projects", {:column=>"source_project_id", :on_delete=>:nullify})
   -> 0.0034s
-- add_foreign_key("pool_repositories", "shards", {:on_delete=>:restrict})
   -> 0.0025s
-- add_foreign_key("project_alerting_settings", "projects", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("project_aliases", "projects", {:on_delete=>:cascade})
   -> 0.0050s
-- add_foreign_key("project_authorizations", "projects", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("project_authorizations", "users", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("project_auto_devops", "projects", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("project_ci_cd_settings", "projects", {:name=>"fk_24c15d2f2e", :on_delete=>:cascade})
   -> 0.0065s
-- add_foreign_key("project_custom_attributes", "projects", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("project_daily_statistics", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("project_deploy_tokens", "deploy_tokens", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("project_deploy_tokens", "projects", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("project_error_tracking_settings", "projects", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("project_feature_usages", "projects", {:on_delete=>:cascade})
   -> 0.0053s
-- add_foreign_key("project_features", "projects", {:name=>"fk_18513d9b92", :on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("project_group_links", "projects", {:name=>"fk_daa8cee94c", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("project_import_data", "projects", {:name=>"fk_ffb9ee3a10", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("project_incident_management_settings", "projects", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("project_metrics_settings", "projects", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("project_mirror_data", "projects", {:name=>"fk_d1aad367d7", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("project_pages_metadata", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("project_repositories", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("project_repositories", "shards", {:on_delete=>:restrict})
   -> 0.0017s
-- add_foreign_key("project_repository_states", "projects", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("project_statistics", "projects", {:on_delete=>:cascade})
   -> 0.0048s
-- add_foreign_key("project_tracing_settings", "projects", {:on_delete=>:cascade})
   -> 0.0038s
-- add_foreign_key("projects", "pool_repositories", {:name=>"fk_6e5c14658a", :on_delete=>:nullify})
   -> 0.0027s
-- add_foreign_key("projects", "users", {:column=>"marked_for_deletion_by_user_id", :name=>"fk_25d8780d11", :on_delete=>:nullify})
   -> 0.0034s
-- add_foreign_key("prometheus_alert_events", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("prometheus_alert_events", "prometheus_alerts", {:on_delete=>:cascade})
   -> 0.0058s
-- add_foreign_key("prometheus_alerts", "environments", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("prometheus_alerts", "projects", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("prometheus_alerts", "prometheus_metrics", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("prometheus_metrics", "projects", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("protected_branch_merge_access_levels", "namespaces", {:column=>"group_id", :name=>"fk_98f3d044fe", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("protected_branch_merge_access_levels", "protected_branches", {:name=>"fk_8a3072ccb3", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("protected_branch_merge_access_levels", "users")
   -> 0.0028s
-- add_foreign_key("protected_branch_push_access_levels", "namespaces", {:column=>"group_id", :name=>"fk_7111b68cdb", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("protected_branch_push_access_levels", "protected_branches", {:name=>"fk_9ffc86a3d9", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("protected_branch_push_access_levels", "users")
   -> 0.0019s
-- add_foreign_key("protected_branch_unprotect_access_levels", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("protected_branch_unprotect_access_levels", "protected_branches", {:on_delete=>:cascade})
   -> 0.0015s
-- add_foreign_key("protected_branch_unprotect_access_levels", "users", {:on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("protected_branches", "projects", {:name=>"fk_7a9c6d93e7", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("protected_environment_deploy_access_levels", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("protected_environment_deploy_access_levels", "protected_environments", {:on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("protected_environment_deploy_access_levels", "users", {:on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("protected_environments", "projects", {:on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("protected_tag_create_access_levels", "namespaces", {:column=>"group_id", :name=>"fk_b4eb82fe3c", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("protected_tag_create_access_levels", "protected_tags", {:name=>"fk_f7dfda8c51", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("protected_tag_create_access_levels", "users")
   -> 0.0056s
-- add_foreign_key("protected_tags", "projects", {:name=>"fk_8e4af87648", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("push_event_payloads", "events", {:name=>"fk_36c74129da", :on_delete=>:cascade})
   -> 0.0038s
-- add_foreign_key("push_rules", "projects", {:name=>"fk_83b29894de", :on_delete=>:cascade})
   -> 0.0048s
-- add_foreign_key("release_links", "releases", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("releases", "projects", {:name=>"fk_47fe2a0596", :on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("releases", "users", {:column=>"author_id", :name=>"fk_8e4456f90f", :on_delete=>:nullify})
   -> 0.0021s
-- add_foreign_key("remote_mirrors", "projects", {:name=>"fk_43a9aa4ca8", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("repository_languages", "projects", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("resource_label_events", "epics", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("resource_label_events", "issues", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("resource_label_events", "labels", {:on_delete=>:nullify})
   -> 0.0019s
-- add_foreign_key("resource_label_events", "merge_requests", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("resource_label_events", "users", {:on_delete=>:nullify})
   -> 0.0019s
-- add_foreign_key("resource_weight_events", "issues", {:on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("resource_weight_events", "users", {:on_delete=>:nullify})
   -> 0.0034s
-- add_foreign_key("reviews", "merge_requests", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("reviews", "projects", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("reviews", "users", {:column=>"author_id", :on_delete=>:nullify})
   -> 0.0033s
-- add_foreign_key("saml_providers", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("scim_oauth_access_tokens", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("self_managed_prometheus_alert_events", "environments", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("self_managed_prometheus_alert_events", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("sentry_issues", "issues", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("serverless_domain_cluster", "clusters_applications_knative", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("serverless_domain_cluster", "pages_domains", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("serverless_domain_cluster", "users", {:column=>"creator_id", :on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("service_desk_settings", "projects", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("services", "projects", {:name=>"fk_71cce407f9", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("slack_integrations", "services", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("smartcard_identities", "users", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("snippet_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("snippet_user_mentions", "snippets", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("snippets", "projects", {:name=>"fk_be41fd4bb7", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("software_license_policies", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("software_license_policies", "software_licenses", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("subscriptions", "projects", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("suggestions", "notes", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("system_note_metadata", "description_versions", {:name=>"fk_fbd87415c9", :on_delete=>:nullify})
   -> 0.0029s
-- add_foreign_key("system_note_metadata", "notes", {:name=>"fk_d83a918cb1", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("term_agreements", "application_setting_terms", {:column=>"term_id"})
   -> 0.0028s
-- add_foreign_key("term_agreements", "users", {:on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("timelogs", "issues", {:name=>"fk_timelogs_issues_issue_id", :on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("timelogs", "merge_requests", {:name=>"fk_timelogs_merge_requests_merge_request_id", :on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("todos", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("todos", "notes", {:name=>"fk_91d1f47b13", :on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("todos", "projects", {:name=>"fk_45054f9c45", :on_delete=>:cascade})
   -> 0.0050s
-- add_foreign_key("todos", "users", {:column=>"author_id", :name=>"fk_ccf0373936", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("todos", "users", {:name=>"fk_d94154aa95", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("trending_projects", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("u2f_registrations", "users")
   -> 0.0032s
-- add_foreign_key("user_callouts", "users", {:on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("user_custom_attributes", "users", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("user_interacted_projects", "projects", {:name=>"fk_722ceba4f7", :on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("user_interacted_projects", "users", {:name=>"fk_0894651f08", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("user_preferences", "users", {:on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("user_statuses", "users", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("user_synced_attributes_metadata", "users", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("users", "application_setting_terms", {:column=>"accepted_term_id", :name=>"fk_789cd90b35", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("users", "namespaces", {:column=>"managing_group_id", :name=>"fk_a4b8fefe3e", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("users_ops_dashboard_projects", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("users_ops_dashboard_projects", "users", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("users_security_dashboard_projects", "projects", {:on_delete=>:cascade})
   -> 0.0038s
-- add_foreign_key("users_security_dashboard_projects", "users", {:on_delete=>:cascade})
   -> 0.0042s
-- add_foreign_key("users_star_projects", "projects", {:name=>"fk_22cd27ddfc", :on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("vulnerabilities", "epics", {:name=>"fk_1d37cddf91", :on_delete=>:nullify})
   -> 0.0034s
-- add_foreign_key("vulnerabilities", "milestones", {:column=>"due_date_sourcing_milestone_id", :name=>"fk_7c5bb22a22", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("vulnerabilities", "milestones", {:column=>"start_date_sourcing_milestone_id", :name=>"fk_88b4d546ef", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("vulnerabilities", "milestones", {:name=>"fk_131d289c65", :on_delete=>:nullify})
   -> 0.0034s
-- add_foreign_key("vulnerabilities", "projects", {:name=>"fk_efb96ab1e2", :on_delete=>:cascade})
   -> 0.0046s
-- add_foreign_key("vulnerabilities", "users", {:column=>"author_id", :name=>"fk_b1de915a15", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("vulnerabilities", "users", {:column=>"closed_by_id", :name=>"fk_cf5c60acbf", :on_delete=>:nullify})
   -> 0.0036s
-- add_foreign_key("vulnerabilities", "users", {:column=>"last_edited_by_id", :name=>"fk_1302949740", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("vulnerabilities", "users", {:column=>"resolved_by_id", :name=>"fk_76bc5f5455", :on_delete=>:nullify})
   -> 0.0024s
-- add_foreign_key("vulnerabilities", "users", {:column=>"updated_by_id", :name=>"fk_7ac31eacb9", :on_delete=>:nullify})
   -> 0.0023s
-- add_foreign_key("vulnerability_feedback", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:nullify})
   -> 0.0028s
-- add_foreign_key("vulnerability_feedback", "issues", {:on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("vulnerability_feedback", "merge_requests", {:name=>"fk_563ff1912e", :on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("vulnerability_feedback", "projects", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("vulnerability_feedback", "users", {:column=>"author_id", :on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("vulnerability_feedback", "users", {:column=>"comment_author_id", :name=>"fk_94f7c8a81e", :on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("vulnerability_identifiers", "projects", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("vulnerability_issue_links", "issues", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("vulnerability_issue_links", "vulnerabilities", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("vulnerability_occurrence_identifiers", "vulnerability_identifiers", {:column=>"identifier_id", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("vulnerability_occurrence_identifiers", "vulnerability_occurrences", {:column=>"occurrence_id", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("vulnerability_occurrence_pipelines", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("vulnerability_occurrence_pipelines", "vulnerability_occurrences", {:column=>"occurrence_id", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("vulnerability_occurrences", "projects", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("vulnerability_occurrences", "vulnerabilities", {:name=>"fk_97ffe77653", :on_delete=>:nullify})
   -> 0.0030s
-- add_foreign_key("vulnerability_occurrences", "vulnerability_identifiers", {:column=>"primary_identifier_id", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("vulnerability_occurrences", "vulnerability_scanners", {:column=>"scanner_id", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("vulnerability_scanners", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("web_hook_logs", "web_hooks", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("web_hooks", "projects", {:name=>"fk_0c8ca6d9d1", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("zoom_meetings", "issues", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("zoom_meetings", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- enable_extension("pg_trgm")
   -> 0.0937s
-- enable_extension("plpgsql")
   -> 0.0020s
-- create_table("abuse_reports", {:id=>:serial, :force=>:cascade})
   -> 0.0285s
-- create_table("alerts_service_data", {:force=>:cascade})
   -> 0.0062s
-- create_table("allowed_email_domains", {:force=>:cascade})
   -> 0.0047s
-- create_table("analytics_cycle_analytics_group_stages", {:force=>:cascade})
   -> 0.0209s
-- create_table("analytics_cycle_analytics_project_stages", {:force=>:cascade})
   -> 0.0228s
-- create_table("analytics_language_trend_repository_languages", {:id=>false, :force=>:cascade})
   -> 0.0142s
-- create_table("analytics_repository_file_commits", {:force=>:cascade})
   -> 0.0143s
-- create_table("analytics_repository_file_edits", {:force=>:cascade})
   -> 0.0103s
-- create_table("analytics_repository_files", {:force=>:cascade})
   -> 0.0067s
-- create_table("appearances", {:id=>:serial, :force=>:cascade})
   -> 0.0104s
-- create_table("application_setting_terms", {:id=>:serial, :force=>:cascade})
   -> 0.0058s
-- create_table("application_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0998s
-- create_table("approval_merge_request_rule_sources", {:force=>:cascade})
   -> 0.0080s
-- create_table("approval_merge_request_rules", {:force=>:cascade})
   -> 0.0274s
-- create_table("approval_merge_request_rules_approved_approvers", {:force=>:cascade})
   -> 0.0100s
-- create_table("approval_merge_request_rules_groups", {:force=>:cascade})
   -> 0.0148s
-- create_table("approval_merge_request_rules_users", {:force=>:cascade})
   -> 0.0110s
-- create_table("approval_project_rules", {:force=>:cascade})
   -> 0.0175s
-- create_table("approval_project_rules_groups", {:force=>:cascade})
   -> 0.0147s
-- create_table("approval_project_rules_users", {:force=>:cascade})
   -> 0.0184s
-- create_table("approvals", {:id=>:serial, :force=>:cascade})
   -> 0.0082s
-- create_table("approver_groups", {:id=>:serial, :force=>:cascade})
   -> 0.0140s
-- create_table("approvers", {:id=>:serial, :force=>:cascade})
   -> 0.0132s
-- create_table("audit_events", {:id=>:serial, :force=>:cascade})
   -> 0.0106s
-- create_table("award_emoji", {:id=>:serial, :force=>:cascade})
   -> 0.0124s
-- create_table("aws_roles", {:primary_key=>"user_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0183s
-- create_table("badges", {:id=>:serial, :force=>:cascade})
   -> 0.0119s
-- create_table("board_assignees", {:id=>:serial, :force=>:cascade})
   -> 0.0121s
-- create_table("board_group_recent_visits", {:force=>:cascade})
   -> 0.0213s
-- create_table("board_labels", {:id=>:serial, :force=>:cascade})
   -> 0.0103s
-- create_table("board_project_recent_visits", {:force=>:cascade})
   -> 0.0222s
-- create_table("boards", {:id=>:serial, :force=>:cascade})
   -> 0.0210s
-- create_table("broadcast_messages", {:id=>:serial, :force=>:cascade})
   -> 0.0133s
-- create_table("chat_names", {:id=>:serial, :force=>:cascade})
   -> 0.0195s
-- create_table("chat_teams", {:id=>:serial, :force=>:cascade})
   -> 0.0073s
-- create_table("ci_build_needs", {:id=>:serial, :force=>:cascade})
   -> 0.0120s
-- create_table("ci_build_trace_chunks", {:force=>:cascade})
   -> 0.0083s
-- create_table("ci_build_trace_section_names", {:id=>:serial, :force=>:cascade})
   -> 0.0089s
-- create_table("ci_build_trace_sections", {:id=>false, :force=>:cascade})
   -> 0.0110s
-- create_table("ci_builds", {:id=>:serial, :force=>:cascade})
   -> 0.1150s
-- create_table("ci_builds_metadata", {:id=>:serial, :force=>:cascade})
   -> 0.0196s
-- create_table("ci_builds_runner_session", {:force=>:cascade})
   -> 0.0101s
-- create_table("ci_group_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0134s
-- create_table("ci_job_artifacts", {:id=>:serial, :force=>:cascade})
   -> 0.0240s
-- create_table("ci_job_variables", {:force=>:cascade})
   -> 0.0135s
-- create_table("ci_pipeline_chat_data", {:force=>:cascade})
   -> 0.0096s
-- create_table("ci_pipeline_schedule_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0073s
-- create_table("ci_pipeline_schedules", {:id=>:serial, :force=>:cascade})
   -> 0.0197s
-- create_table("ci_pipeline_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0149s
-- create_table("ci_pipelines", {:id=>:serial, :force=>:cascade})
   -> 0.0671s
-- create_table("ci_pipelines_config", {:primary_key=>"pipeline_id", :force=>:cascade})
   -> 0.0132s
-- create_table("ci_resource_groups", {:force=>:cascade})
   -> 0.0059s
-- create_table("ci_resources", {:force=>:cascade})
   -> 0.0172s
-- create_table("ci_runner_namespaces", {:id=>:serial, :force=>:cascade})
   -> 0.0157s
-- create_table("ci_runner_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0172s
-- create_table("ci_runners", {:id=>:serial, :force=>:cascade})
   -> 0.0356s
-- create_table("ci_sources_pipelines", {:id=>:serial, :force=>:cascade})
   -> 0.0308s
-- create_table("ci_stages", {:id=>:serial, :force=>:cascade})
   -> 0.0238s
-- create_table("ci_subscriptions_projects", {:force=>:cascade})
   -> 0.0123s
-- create_table("ci_trigger_requests", {:id=>:serial, :force=>:cascade})
   -> 0.0129s
-- create_table("ci_triggers", {:id=>:serial, :force=>:cascade})
   -> 0.0187s
-- create_table("ci_variables", {:id=>:serial, :force=>:cascade})
   -> 0.0153s
-- create_table("cluster_groups", {:id=>:serial, :force=>:cascade})
   -> 0.0083s
-- create_table("cluster_platforms_kubernetes", {:id=>:serial, :force=>:cascade})
   -> 0.0129s
-- create_table("cluster_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0164s
-- create_table("cluster_providers_aws", {:force=>:cascade})
   -> 0.0133s
-- create_table("cluster_providers_gcp", {:id=>:serial, :force=>:cascade})
   -> 0.0171s
-- create_table("clusters", {:id=>:serial, :force=>:cascade})
   -> 0.0194s
-- create_table("clusters_applications_cert_managers", {:id=>:serial, :force=>:cascade})
   -> 0.0156s
-- create_table("clusters_applications_crossplane", {:id=>:serial, :force=>:cascade})
   -> 0.0088s
-- create_table("clusters_applications_elastic_stacks", {:force=>:cascade})
   -> 0.0112s
-- create_table("clusters_applications_helm", {:id=>:serial, :force=>:cascade})
   -> 0.0079s
-- create_table("clusters_applications_ingress", {:id=>:serial, :force=>:cascade})
   -> 0.0108s
-- create_table("clusters_applications_jupyter", {:id=>:serial, :force=>:cascade})
   -> 0.0138s
-- create_table("clusters_applications_knative", {:id=>:serial, :force=>:cascade})
   -> 0.0105s
-- create_table("clusters_applications_prometheus", {:id=>:serial, :force=>:cascade})
   -> 0.0069s
-- create_table("clusters_applications_runners", {:id=>:serial, :force=>:cascade})
   -> 0.0140s
-- create_table("clusters_kubernetes_namespaces", {:force=>:cascade})
   -> 0.0279s
-- create_table("commit_user_mentions", {:force=>:cascade})
   -> 0.0182s
-- create_table("container_expiration_policies", {:primary_key=>"project_id", :id=>:bigint, :default=>nil, :force=>:cascade})
   -> 0.0073s
-- create_table("container_repositories", {:id=>:serial, :force=>:cascade})
   -> 0.0104s
-- create_table("conversational_development_index_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0056s
-- create_table("dependency_proxy_blobs", {:id=>:serial, :force=>:cascade})
   -> 0.0067s
-- create_table("dependency_proxy_group_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0112s
-- create_table("deploy_keys_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0103s
-- create_table("deploy_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0235s
-- create_table("deployment_merge_requests", {:id=>false, :force=>:cascade})
   -> 0.0101s
-- create_table("deployments", {:id=>:serial, :force=>:cascade})
   -> 0.0541s
-- create_table("description_versions", {:force=>:cascade})
   -> 0.0117s
-- create_table("design_management_designs", {:force=>:cascade})
   -> 0.0133s
-- create_table("design_management_designs_versions", {:id=>false, :force=>:cascade})
   -> 0.0160s
-- create_table("design_management_versions", {:force=>:cascade})
   -> 0.0109s
-- create_table("design_user_mentions", {:force=>:cascade})
   -> 0.0151s
-- create_table("draft_notes", {:force=>:cascade})
   -> 0.0175s
-- create_table("elasticsearch_indexed_namespaces", {:id=>false, :force=>:cascade})
   -> 0.0039s
-- create_table("elasticsearch_indexed_projects", {:id=>false, :force=>:cascade})
   -> 0.0038s
-- create_table("emails", {:id=>:serial, :force=>:cascade})
   -> 0.0233s
-- create_table("environments", {:id=>:serial, :force=>:cascade})
   -> 0.0282s
-- create_table("epic_issues", {:id=>:serial, :force=>:cascade})
   -> 0.0187s
-- create_table("epic_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0074s
-- create_table("epic_user_mentions", {:force=>:cascade})
   -> 0.0187s
-- create_table("epics", {:id=>:serial, :force=>:cascade})
   -> 0.0401s
-- create_table("events", {:id=>:serial, :force=>:cascade})
   -> 0.0253s
-- create_table("evidences", {:force=>:cascade})
   -> 0.0066s
-- create_table("external_pull_requests", {:force=>:cascade})
   -> 0.0103s
-- create_table("feature_gates", {:id=>:serial, :force=>:cascade})
   -> 0.0085s
-- create_table("features", {:id=>:serial, :force=>:cascade})
   -> 0.0085s
-- create_table("fork_network_members", {:id=>:serial, :force=>:cascade})
   -> 0.0110s
-- create_table("fork_networks", {:id=>:serial, :force=>:cascade})
   -> 0.0099s
-- create_table("forked_project_links", {:id=>:serial, :force=>:cascade})
   -> 0.0079s
-- create_table("geo_cache_invalidation_events", {:force=>:cascade})
   -> 0.0047s
-- create_table("geo_container_repository_updated_events", {:force=>:cascade})
   -> 0.0087s
-- create_table("geo_event_log", {:force=>:cascade})
   -> 0.0539s
-- create_table("geo_hashed_storage_attachments_events", {:force=>:cascade})
   -> 0.0135s
-- create_table("geo_hashed_storage_migrated_events", {:force=>:cascade})
   -> 0.0094s
-- create_table("geo_job_artifact_deleted_events", {:force=>:cascade})
   -> 0.0110s
-- create_table("geo_lfs_object_deleted_events", {:force=>:cascade})
   -> 0.0077s
-- create_table("geo_node_namespace_links", {:id=>:serial, :force=>:cascade})
   -> 0.0198s
-- create_table("geo_node_statuses", {:id=>:serial, :force=>:cascade})
   -> 0.0109s
-- create_table("geo_nodes", {:id=>:serial, :force=>:cascade})
   -> 0.0192s
-- create_table("geo_repositories_changed_events", {:force=>:cascade})
   -> 0.0080s
-- create_table("geo_repository_created_events", {:force=>:cascade})
   -> 0.0099s
-- create_table("geo_repository_deleted_events", {:force=>:cascade})
   -> 0.0075s
-- create_table("geo_repository_renamed_events", {:force=>:cascade})
   -> 0.0097s
-- create_table("geo_repository_updated_events", {:force=>:cascade})
   -> 0.0154s
-- create_table("geo_reset_checksum_events", {:force=>:cascade})
   -> 0.0080s
-- create_table("geo_upload_deleted_events", {:force=>:cascade})
   -> 0.0089s
-- create_table("gitlab_subscription_histories", {:force=>:cascade})
   -> 0.0061s
-- create_table("gitlab_subscriptions", {:force=>:cascade})
   -> 0.0150s
-- create_table("gpg_key_subkeys", {:id=>:serial, :force=>:cascade})
   -> 0.0151s
-- create_table("gpg_keys", {:id=>:serial, :force=>:cascade})
   -> 0.0130s
-- create_table("gpg_signatures", {:id=>:serial, :force=>:cascade})
   -> 0.0307s
-- create_table("grafana_integrations", {:force=>:cascade})
   -> 0.0104s
-- create_table("group_custom_attributes", {:id=>:serial, :force=>:cascade})
   -> 0.0222s
-- create_table("group_deletion_schedules", {:primary_key=>"group_id", :id=>:bigint, :default=>nil, :force=>:cascade})
   -> 0.0083s
-- create_table("group_group_links", {:force=>:cascade})
   -> 0.0092s
-- create_table("historical_data", {:id=>:serial, :force=>:cascade})
   -> 0.0030s
-- create_table("identities", {:id=>:serial, :force=>:cascade})
   -> 0.0230s
-- create_table("import_export_uploads", {:id=>:serial, :force=>:cascade})
   -> 0.0186s
-- create_table("import_failures", {:force=>:cascade})
   -> 0.0169s
-- create_table("index_statuses", {:id=>:serial, :force=>:cascade})
   -> 0.0121s
-- create_table("insights", {:id=>:serial, :force=>:cascade})
   -> 0.0113s
-- create_table("internal_ids", {:force=>:cascade})
   -> 0.0303s
-- create_table("ip_restrictions", {:force=>:cascade})
   -> 0.0075s
-- create_table("issue_assignees", {:id=>false, :force=>:cascade})
   -> 0.0105s
-- create_table("issue_links", {:id=>:serial, :force=>:cascade})
   -> 0.0208s
-- create_table("issue_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0091s
-- create_table("issue_tracker_data", {:force=>:cascade})
   -> 0.0064s
-- create_table("issue_user_mentions", {:force=>:cascade})
   -> 0.0210s
-- create_table("issues", {:id=>:serial, :force=>:cascade})
   -> 0.0909s
-- create_table("issues_prometheus_alert_events", {:id=>false, :force=>:cascade})
   -> 0.0074s
-- create_table("issues_self_managed_prometheus_alert_events", {:id=>false, :force=>:cascade})
   -> 0.0098s
-- create_table("jira_connect_installations", {:force=>:cascade})
   -> 0.0097s
-- create_table("jira_connect_subscriptions", {:force=>:cascade})
   -> 0.0142s
-- create_table("jira_tracker_data", {:force=>:cascade})
   -> 0.0099s
-- create_table("keys", {:id=>:serial, :force=>:cascade})
   -> 0.0300s
-- create_table("label_links", {:id=>:serial, :force=>:cascade})
   -> 0.0090s
-- create_table("label_priorities", {:id=>:serial, :force=>:cascade})
   -> 0.0193s
-- create_table("labels", {:id=>:serial, :force=>:cascade})
   -> 0.0307s
-- create_table("ldap_group_links", {:id=>:serial, :force=>:cascade})
   -> 0.0878s
-- create_table("lfs_file_locks", {:id=>:serial, :force=>:cascade})
   -> 0.0183s
-- create_table("lfs_objects", {:id=>:serial, :force=>:cascade})
   -> 0.0104s
-- create_table("lfs_objects_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0114s
-- create_table("licenses", {:id=>:serial, :force=>:cascade})
   -> 0.0063s
-- create_table("list_user_preferences", {:force=>:cascade})
   -> 0.0185s
-- create_table("lists", {:id=>:serial, :force=>:cascade})
   -> 0.0482s
-- create_table("members", {:id=>:serial, :force=>:cascade})
   -> 0.0752s
-- create_table("merge_request_assignees", {:force=>:cascade})
   -> 0.0173s
-- create_table("merge_request_blocks", {:force=>:cascade})
   -> 0.0174s
-- create_table("merge_request_diff_commits", {:id=>false, :force=>:cascade})
   -> 0.0111s
-- create_table("merge_request_diff_files", {:id=>false, :force=>:cascade})
   -> 0.0066s
-- create_table("merge_request_diffs", {:id=>:serial, :force=>:cascade})
   -> 0.0286s
-- create_table("merge_request_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0446s
-- create_table("merge_request_user_mentions", {:force=>:cascade})
   -> 0.0266s
-- create_table("merge_requests", {:id=>:serial, :force=>:cascade})
   -> 0.1309s
-- create_table("merge_requests_closing_issues", {:id=>:serial, :force=>:cascade})
   -> 0.0093s
-- create_table("merge_trains", {:force=>:cascade})
   -> 0.0197s
-- create_table("milestone_releases", {:id=>false, :force=>:cascade})
   -> 0.0092s
-- create_table("milestones", {:id=>:serial, :force=>:cascade})
   -> 0.0307s
-- create_table("namespace_aggregation_schedules", {:primary_key=>"namespace_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0067s
-- create_table("namespace_root_storage_statistics", {:primary_key=>"namespace_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0103s
-- create_table("namespace_statistics", {:id=>:serial, :force=>:cascade})
   -> 0.0065s
-- create_table("namespaces", {:id=>:serial, :force=>:cascade})
   -> 0.0782s
-- create_table("note_diff_files", {:id=>:serial, :force=>:cascade})
   -> 0.0072s
-- create_table("notes", {:id=>:serial, :force=>:cascade})
   -> 0.0447s
-- create_table("notification_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0181s
-- create_table("oauth_access_grants", {:id=>:serial, :force=>:cascade})
   -> 0.0095s
-- create_table("oauth_access_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0192s
-- create_table("oauth_applications", {:id=>:serial, :force=>:cascade})
   -> 0.0164s
-- create_table("oauth_openid_requests", {:id=>:serial, :force=>:cascade})
   -> 0.0099s
-- create_table("operations_feature_flag_scopes", {:force=>:cascade})
   -> 0.0083s
-- create_table("operations_feature_flags", {:force=>:cascade})
   -> 0.0087s
-- create_table("operations_feature_flags_clients", {:force=>:cascade})
   -> 0.0117s
-- create_table("packages_build_infos", {:force=>:cascade})
   -> 0.0125s
-- create_table("packages_conan_file_metadata", {:force=>:cascade})
   -> 0.0086s
-- create_table("packages_conan_metadata", {:force=>:cascade})
   -> 0.0094s
-- create_table("packages_dependencies", {:force=>:cascade})
   -> 0.0107s
-- create_table("packages_dependency_links", {:force=>:cascade})
   -> 0.0118s
-- create_table("packages_maven_metadata", {:force=>:cascade})
   -> 0.0071s
-- create_table("packages_package_files", {:force=>:cascade})
   -> 0.0098s
-- create_table("packages_package_tags", {:force=>:cascade})
   -> 0.0102s
-- create_table("packages_packages", {:force=>:cascade})
   -> 0.0177s
-- create_table("pages_domain_acme_orders", {:force=>:cascade})
   -> 0.0119s
-- create_table("pages_domains", {:id=>:serial, :force=>:cascade})
   -> 0.0512s
-- create_table("path_locks", {:id=>:serial, :force=>:cascade})
   -> 0.0165s
-- create_table("personal_access_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0154s
-- create_table("plan_limits", {:force=>:cascade})
   -> 0.0124s
-- create_table("plans", {:id=>:serial, :force=>:cascade})
   -> 0.0117s
-- create_table("pool_repositories", {:force=>:cascade})
   -> 0.0155s
-- create_table("programming_languages", {:id=>:serial, :force=>:cascade})
   -> 0.0121s
-- create_table("project_alerting_settings", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0040s
-- create_table("project_aliases", {:force=>:cascade})
   -> 0.0157s
-- create_table("project_authorizations", {:id=>false, :force=>:cascade})
   -> 0.0105s
-- create_table("project_auto_devops", {:id=>:serial, :force=>:cascade})
   -> 0.0153s
-- create_table("project_ci_cd_settings", {:id=>:serial, :force=>:cascade})
   -> 0.0103s
-- create_table("project_custom_attributes", {:id=>:serial, :force=>:cascade})
   -> 0.0137s
-- create_table("project_daily_statistics", {:force=>:cascade})
   -> 0.0152s
-- create_table("project_deploy_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0161s
-- create_table("project_error_tracking_settings", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0043s
-- create_table("project_feature_usages", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0216s
-- create_table("project_features", {:id=>:serial, :force=>:cascade})
   -> 0.0116s
-- create_table("project_group_links", {:id=>:serial, :force=>:cascade})
   -> 0.0099s
-- create_table("project_import_data", {:id=>:serial, :force=>:cascade})
   -> 0.0078s
-- create_table("project_incident_management_settings", {:primary_key=>"project_id", :id=>:serial, :force=>:cascade})
   -> 0.0122s
-- create_table("project_metrics_settings", {:primary_key=>"project_id", :id=>:integer, :default=>nil, :force=>:cascade})
   -> 0.0060s
-- create_table("project_mirror_data", {:id=>:serial, :force=>:cascade})
   -> 0.0250s
-- create_table("project_pages_metadata", {:id=>false, :force=>:cascade})
   -> 0.0150s
-- create_table("project_repositories", {:force=>:cascade})
   -> 0.0182s
-- create_table("project_repository_states", {:id=>:serial, :force=>:cascade})
   -> 0.0296s
-- create_table("project_statistics", {:id=>:serial, :force=>:cascade})
   -> 0.0119s
-- create_table("project_tracing_settings", {:force=>:cascade})
   -> 0.0093s
-- create_table("projects", {:id=>:serial, :force=>:cascade})
   -> 0.1211s
-- create_table("prometheus_alert_events", {:force=>:cascade})
   -> 0.0158s
-- create_table("prometheus_alerts", {:id=>:serial, :force=>:cascade})
   -> 0.0146s
-- create_table("prometheus_metrics", {:id=>:serial, :force=>:cascade})
   -> 0.0211s
-- create_table("protected_branch_merge_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0209s
-- create_table("protected_branch_push_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0201s
-- create_table("protected_branch_unprotect_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0193s
-- create_table("protected_branches", {:id=>:serial, :force=>:cascade})
   -> 0.0115s
-- create_table("protected_environment_deploy_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0180s
-- create_table("protected_environments", {:id=>:serial, :force=>:cascade})
   -> 0.0138s
-- create_table("protected_tag_create_access_levels", {:id=>:serial, :force=>:cascade})
   -> 0.0149s
-- create_table("protected_tags", {:id=>:serial, :force=>:cascade})
   -> 0.0163s
-- create_table("push_event_payloads", {:id=>false, :force=>:cascade})
   -> 0.0101s
-- create_table("push_rules", {:id=>:serial, :force=>:cascade})
   -> 0.0125s
-- create_table("redirect_routes", {:id=>:serial, :force=>:cascade})
   -> 0.0212s
-- create_table("release_links", {:force=>:cascade})
   -> 0.0122s
-- create_table("releases", {:id=>:serial, :force=>:cascade})
   -> 0.0131s
-- create_table("remote_mirrors", {:id=>:serial, :force=>:cascade})
   -> 0.0146s
-- create_table("repository_languages", {:id=>false, :force=>:cascade})
   -> 0.0090s
-- create_table("resource_label_events", {:force=>:cascade})
   -> 0.0232s
-- create_table("resource_weight_events", {:force=>:cascade})
   -> 0.0129s
-- create_table("reviews", {:force=>:cascade})
   -> 0.0134s
-- create_table("routes", {:id=>:serial, :force=>:cascade})
   -> 0.0177s
-- create_table("saml_providers", {:id=>:serial, :force=>:cascade})
   -> 0.0142s
-- create_table("scim_oauth_access_tokens", {:id=>:serial, :force=>:cascade})
   -> 0.0102s
-- create_table("self_managed_prometheus_alert_events", {:force=>:cascade})
   -> 0.0158s
-- create_table("sent_notifications", {:id=>:serial, :force=>:cascade})
   -> 0.0093s
-- create_table("sentry_issues", {:force=>:cascade})
   -> 0.0093s
-- create_table("serverless_domain_cluster", {:primary_key=>"uuid", :id=>:string, :limit=>14, :force=>:cascade})
   -> 0.0126s
-- create_table("service_desk_settings", {:primary_key=>"project_id", :id=>:bigint, :default=>nil, :force=>:cascade})
   -> 0.0067s
-- create_table("services", {:id=>:serial, :force=>:cascade})
   -> 0.0210s
-- create_table("shards", {:id=>:serial, :force=>:cascade})
   -> 0.0078s
-- create_table("slack_integrations", {:id=>:serial, :force=>:cascade})
   -> 0.0179s
-- create_table("smartcard_identities", {:force=>:cascade})
   -> 0.0137s
-- create_table("snippet_user_mentions", {:force=>:cascade})
   -> 0.0202s
-- create_table("snippets", {:id=>:serial, :force=>:cascade})
   -> 0.0329s
-- create_table("software_license_policies", {:id=>:serial, :force=>:cascade})
   -> 0.0143s
-- create_table("software_licenses", {:id=>:serial, :force=>:cascade})
   -> 0.0211s
-- create_table("spam_logs", {:id=>:serial, :force=>:cascade})
   -> 0.0058s
-- create_table("subscriptions", {:id=>:serial, :force=>:cascade})
   -> 0.0165s
-- create_table("suggestions", {:force=>:cascade})
   -> 0.0122s
-- create_table("system_note_metadata", {:id=>:serial, :force=>:cascade})
   -> 0.0101s
-- create_table("taggings", {:id=>:serial, :force=>:cascade})
   -> 0.0259s
-- create_table("tags", {:id=>:serial, :force=>:cascade})
   -> 0.0116s
-- create_table("term_agreements", {:id=>:serial, :force=>:cascade})
   -> 0.0172s
-- create_table("timelogs", {:id=>:serial, :force=>:cascade})
   -> 0.0207s
-- create_table("todos", {:id=>:serial, :force=>:cascade})
   -> 0.0432s
-- create_table("trending_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0066s
-- create_table("u2f_registrations", {:id=>:serial, :force=>:cascade})
   -> 0.0175s
-- create_table("uploads", {:id=>:serial, :force=>:cascade})
   -> 0.0255s
-- create_table("user_agent_details", {:id=>:serial, :force=>:cascade})
   -> 0.0140s
-- create_table("user_callouts", {:id=>:serial, :force=>:cascade})
   -> 0.0142s
-- create_table("user_custom_attributes", {:id=>:serial, :force=>:cascade})
   -> 0.0109s
-- create_table("user_interacted_projects", {:id=>false, :force=>:cascade})
   -> 0.0118s
-- create_table("user_preferences", {:id=>:serial, :force=>:cascade})
   -> 0.0189s
-- create_table("user_statuses", {:primary_key=>"user_id", :id=>:serial, :force=>:cascade})
   -> 0.0103s
-- create_table("user_synced_attributes_metadata", {:id=>:serial, :force=>:cascade})
   -> 0.0140s
-- create_table("users", {:id=>:serial, :force=>:cascade})
   -> 0.1343s
-- create_table("users_ops_dashboard_projects", {:force=>:cascade})
   -> 0.0131s
-- create_table("users_security_dashboard_projects", {:id=>false, :force=>:cascade})
   -> 0.0089s
-- create_table("users_star_projects", {:id=>:serial, :force=>:cascade})
   -> 0.0161s
-- create_table("vulnerabilities", {:force=>:cascade})
   -> 0.0531s
-- create_table("vulnerability_feedback", {:id=>:serial, :force=>:cascade})
   -> 0.0270s
-- create_table("vulnerability_identifiers", {:force=>:cascade})
   -> 0.0088s
-- create_table("vulnerability_issue_links", {:force=>:cascade})
   -> 0.0155s
-- create_table("vulnerability_occurrence_identifiers", {:force=>:cascade})
   -> 0.0221s
-- create_table("vulnerability_occurrence_pipelines", {:force=>:cascade})
   -> 0.0123s
-- create_table("vulnerability_occurrences", {:force=>:cascade})
   -> 0.0259s
-- create_table("vulnerability_scanners", {:force=>:cascade})
   -> 0.0107s
-- create_table("web_hook_logs", {:id=>:serial, :force=>:cascade})
   -> 0.0114s
-- create_table("web_hooks", {:id=>:serial, :force=>:cascade})
   -> 0.0211s
-- create_table("zoom_meetings", {:force=>:cascade})
   -> 0.0192s
-- add_foreign_key("alerts_service_data", "services", {:on_delete=>:cascade})
   -> 0.0057s
-- add_foreign_key("allowed_email_domains", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("analytics_cycle_analytics_group_stages", "labels", {:column=>"end_event_label_id", :on_delete=>:cascade})
   -> 0.0052s
-- add_foreign_key("analytics_cycle_analytics_group_stages", "labels", {:column=>"start_event_label_id", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("analytics_cycle_analytics_group_stages", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("analytics_cycle_analytics_project_stages", "labels", {:column=>"end_event_label_id", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("analytics_cycle_analytics_project_stages", "labels", {:column=>"start_event_label_id", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("analytics_cycle_analytics_project_stages", "projects", {:on_delete=>:cascade})
   -> 0.0080s
-- add_foreign_key("analytics_language_trend_repository_languages", "programming_languages", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("analytics_language_trend_repository_languages", "projects", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("analytics_repository_file_commits", "analytics_repository_files", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("analytics_repository_file_commits", "projects", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("analytics_repository_file_edits", "analytics_repository_files", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("analytics_repository_file_edits", "projects", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("analytics_repository_files", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("application_settings", "namespaces", {:column=>"custom_project_templates_group_id", :on_delete=>:nullify})
   -> 0.0058s
-- add_foreign_key("application_settings", "projects", {:column=>"file_template_project_id", :name=>"fk_ec757bd087", :on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("application_settings", "projects", {:column=>"instance_administration_project_id", :on_delete=>:nullify})
   -> 0.0032s
-- add_foreign_key("application_settings", "users", {:column=>"usage_stats_set_by_user_id", :name=>"fk_964370041d", :on_delete=>:nullify})
   -> 0.0078s
-- add_foreign_key("approval_merge_request_rule_sources", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0077s
-- add_foreign_key("approval_merge_request_rule_sources", "approval_project_rules", {:on_delete=>:cascade})
   -> 0.0042s
-- add_foreign_key("approval_merge_request_rules", "merge_requests", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("approval_merge_request_rules_approved_approvers", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("approval_merge_request_rules_approved_approvers", "users", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("approval_merge_request_rules_groups", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("approval_merge_request_rules_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("approval_merge_request_rules_users", "approval_merge_request_rules", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("approval_merge_request_rules_users", "users", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("approval_project_rules", "projects", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("approval_project_rules_groups", "approval_project_rules", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("approval_project_rules_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("approval_project_rules_users", "approval_project_rules", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("approval_project_rules_users", "users", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("approvals", "merge_requests", {:name=>"fk_310d714958", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("approver_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("aws_roles", "users", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("badges", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("badges", "projects", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("board_assignees", "boards", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("board_assignees", "users", {:column=>"assignee_id", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("board_group_recent_visits", "boards", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("board_group_recent_visits", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("board_group_recent_visits", "users", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("board_labels", "boards", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("board_labels", "labels", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("board_project_recent_visits", "boards", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("board_project_recent_visits", "projects", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("board_project_recent_visits", "users", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("boards", "namespaces", {:column=>"group_id", :name=>"fk_1e9a074a35", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("boards", "projects", {:name=>"fk_f15266b5f9", :on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("chat_teams", "namespaces", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("ci_build_needs", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0138s
-- add_foreign_key("ci_build_trace_chunks", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("ci_build_trace_section_names", "projects", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("ci_build_trace_sections", "ci_build_trace_section_names", {:column=>"section_name_id", :name=>"fk_264e112c66", :on_delete=>:cascade})
   -> 0.0038s
-- add_foreign_key("ci_build_trace_sections", "ci_builds", {:column=>"build_id", :name=>"fk_4ebe41f502", :on_delete=>:cascade})
   -> 0.0048s
-- add_foreign_key("ci_build_trace_sections", "projects", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("ci_builds", "ci_pipelines", {:column=>"auto_canceled_by_id", :name=>"fk_a2141b1522", :on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("ci_builds", "ci_pipelines", {:column=>"commit_id", :name=>"fk_d3130c9a7f", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("ci_builds", "ci_pipelines", {:column=>"upstream_pipeline_id", :name=>"fk_87f4cefcda", :on_delete=>:cascade})
   -> 0.0054s
-- add_foreign_key("ci_builds", "ci_resource_groups", {:column=>"resource_group_id", :name=>"fk_6661f4f0e8", :on_delete=>:nullify})
   -> 0.0060s
-- add_foreign_key("ci_builds", "ci_stages", {:column=>"stage_id", :name=>"fk_3a9eaa254d", :on_delete=>:cascade})
   -> 0.0049s
-- add_foreign_key("ci_builds", "projects", {:name=>"fk_befce0568a", :on_delete=>:cascade})
   -> 0.0071s
-- add_foreign_key("ci_builds_metadata", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("ci_builds_metadata", "projects", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("ci_builds_runner_session", "ci_builds", {:column=>"build_id", :on_delete=>:cascade})
   -> 0.0046s
-- add_foreign_key("ci_group_variables", "namespaces", {:column=>"group_id", :name=>"fk_33ae4d58d8", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("ci_job_artifacts", "ci_builds", {:column=>"job_id", :on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("ci_job_artifacts", "projects", {:on_delete=>:cascade})
   -> 0.0058s
-- add_foreign_key("ci_job_variables", "ci_builds", {:column=>"job_id", :on_delete=>:cascade})
   -> 0.0086s
-- add_foreign_key("ci_pipeline_chat_data", "chat_names", {:on_delete=>:cascade})
   -> 0.0048s
-- add_foreign_key("ci_pipeline_chat_data", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("ci_pipeline_schedule_variables", "ci_pipeline_schedules", {:column=>"pipeline_schedule_id", :name=>"fk_41c35fda51", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("ci_pipeline_schedules", "projects", {:name=>"fk_8ead60fcc4", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("ci_pipeline_schedules", "users", {:column=>"owner_id", :name=>"fk_9ea99f58d2", :on_delete=>:nullify})
   -> 0.0042s
-- add_foreign_key("ci_pipeline_variables", "ci_pipelines", {:column=>"pipeline_id", :name=>"fk_f29c5f4380", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("ci_pipelines", "ci_pipeline_schedules", {:column=>"pipeline_schedule_id", :name=>"fk_3d34ab2e06", :on_delete=>:nullify})
   -> 0.0018s
-- add_foreign_key("ci_pipelines", "ci_pipelines", {:column=>"auto_canceled_by_id", :name=>"fk_262d4c2d19", :on_delete=>:nullify})
   -> 0.0018s
-- add_foreign_key("ci_pipelines", "external_pull_requests", {:name=>"fk_190998ef09", :on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("ci_pipelines", "merge_requests", {:name=>"fk_a23be95014", :on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("ci_pipelines", "projects", {:name=>"fk_86635dbd80", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("ci_pipelines_config", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("ci_resource_groups", "projects", {:name=>"fk_774722d144", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("ci_resources", "ci_builds", {:column=>"build_id", :name=>"fk_e169a8e3d5", :on_delete=>:nullify})
   -> 0.0033s
-- add_foreign_key("ci_resources", "ci_resource_groups", {:column=>"resource_group_id", :on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("ci_runner_namespaces", "ci_runners", {:column=>"runner_id", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("ci_runner_namespaces", "namespaces", {:on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("ci_runner_projects", "projects", {:name=>"fk_4478a6f1e4", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("ci_sources_pipelines", "ci_builds", {:column=>"source_job_id", :name=>"fk_be5624bf37", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("ci_sources_pipelines", "ci_pipelines", {:column=>"pipeline_id", :name=>"fk_e1bad85861", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("ci_sources_pipelines", "ci_pipelines", {:column=>"source_pipeline_id", :name=>"fk_d4e29af7d7", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("ci_sources_pipelines", "projects", {:column=>"source_project_id", :name=>"fk_acd9737679", :on_delete=>:cascade})
   -> 0.0103s
-- add_foreign_key("ci_sources_pipelines", "projects", {:name=>"fk_1e53c97c0a", :on_delete=>:cascade})
   -> 0.0046s
-- add_foreign_key("ci_stages", "ci_pipelines", {:column=>"pipeline_id", :name=>"fk_fb57e6cc56", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("ci_stages", "projects", {:name=>"fk_2360681d1d", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("ci_subscriptions_projects", "projects", {:column=>"downstream_project_id", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("ci_subscriptions_projects", "projects", {:column=>"upstream_project_id", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("ci_trigger_requests", "ci_triggers", {:column=>"trigger_id", :name=>"fk_b8ec8b7245", :on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("ci_triggers", "projects", {:name=>"fk_e3e63f966e", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("ci_triggers", "users", {:column=>"owner_id", :name=>"fk_e8e10d1964", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("ci_variables", "projects", {:name=>"fk_ada5eb64b3", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("cluster_groups", "clusters", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("cluster_groups", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("cluster_platforms_kubernetes", "clusters", {:on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("cluster_projects", "clusters", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("cluster_projects", "projects", {:on_delete=>:cascade})
   -> 0.0084s
-- add_foreign_key("cluster_providers_aws", "clusters", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("cluster_providers_aws", "users", {:column=>"created_by_user_id", :on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("cluster_providers_gcp", "clusters", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("clusters", "projects", {:column=>"management_project_id", :name=>"fk_f05c5e5a42", :on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("clusters", "users", {:on_delete=>:nullify})
   -> 0.0029s
-- add_foreign_key("clusters_applications_cert_managers", "clusters", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("clusters_applications_crossplane", "clusters", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("clusters_applications_elastic_stacks", "clusters", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("clusters_applications_helm", "clusters", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("clusters_applications_ingress", "clusters", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("clusters_applications_jupyter", "clusters", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("clusters_applications_jupyter", "oauth_applications", {:on_delete=>:nullify})
   -> 0.0026s
-- add_foreign_key("clusters_applications_knative", "clusters", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("clusters_applications_prometheus", "clusters", {:name=>"fk_557e773639", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("clusters_applications_runners", "ci_runners", {:column=>"runner_id", :name=>"fk_02de2ded36", :on_delete=>:nullify})
   -> 0.0039s
-- add_foreign_key("clusters_applications_runners", "clusters", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("clusters_kubernetes_namespaces", "cluster_projects", {:on_delete=>:nullify})
   -> 0.0036s
-- add_foreign_key("clusters_kubernetes_namespaces", "clusters", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("clusters_kubernetes_namespaces", "environments", {:on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("clusters_kubernetes_namespaces", "projects", {:on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("commit_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("container_expiration_policies", "projects", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("container_repositories", "projects")
   -> 0.0030s
-- add_foreign_key("dependency_proxy_blobs", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("dependency_proxy_group_settings", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("deploy_keys_projects", "projects", {:name=>"fk_58a901ca7e", :on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("deployment_merge_requests", "deployments", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("deployment_merge_requests", "merge_requests", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("deployments", "clusters", {:name=>"fk_289bba3222", :on_delete=>:nullify})
   -> 0.0022s
-- add_foreign_key("deployments", "projects", {:name=>"fk_b9a3851b82", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("description_versions", "epics", {:on_delete=>:cascade})
   -> 0.0123s
-- add_foreign_key("description_versions", "issues", {:on_delete=>:cascade})
   -> 0.0111s
-- add_foreign_key("description_versions", "merge_requests", {:on_delete=>:cascade})
   -> 0.0072s
-- add_foreign_key("design_management_designs", "issues", {:on_delete=>:cascade})
   -> 0.0051s
-- add_foreign_key("design_management_designs", "projects", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("design_management_designs_versions", "design_management_designs", {:column=>"design_id", :name=>"fk_03c671965c", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("design_management_designs_versions", "design_management_versions", {:column=>"version_id", :name=>"fk_f4d25ba00c", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("design_management_versions", "issues", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("design_management_versions", "users", {:column=>"author_id", :name=>"fk_c1440b4896", :on_delete=>:nullify})
   -> 0.0036s
-- add_foreign_key("design_user_mentions", "design_management_designs", {:column=>"design_id", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("design_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("draft_notes", "merge_requests", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("draft_notes", "users", {:column=>"author_id", :on_delete=>:cascade})
   -> 0.0079s
-- add_foreign_key("elasticsearch_indexed_namespaces", "namespaces", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("elasticsearch_indexed_projects", "projects", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("environments", "projects", {:name=>"fk_d1c8c1da6a", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("epic_issues", "epics", {:on_delete=>:cascade})
   -> 0.0051s
-- add_foreign_key("epic_issues", "issues", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("epic_metrics", "epics", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("epic_user_mentions", "epics", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("epic_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("epics", "epics", {:column=>"due_date_sourcing_epic_id", :name=>"fk_013c9f36ca", :on_delete=>:nullify})
   -> 0.0020s
-- add_foreign_key("epics", "epics", {:column=>"parent_id", :name=>"fk_25b99c1be3", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("epics", "epics", {:column=>"start_date_sourcing_epic_id", :name=>"fk_9d480c64b2", :on_delete=>:nullify})
   -> 0.0033s
-- add_foreign_key("epics", "milestones", {:on_delete=>:nullify})
   -> 0.0045s
-- add_foreign_key("epics", "namespaces", {:column=>"group_id", :name=>"fk_f081aa4489", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("epics", "users", {:column=>"assignee_id", :name=>"fk_dccd3f98fc", :on_delete=>:nullify})
   -> 0.0022s
-- add_foreign_key("epics", "users", {:column=>"author_id", :name=>"fk_3654b61b03", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("epics", "users", {:column=>"closed_by_id", :name=>"fk_aa5798e761", :on_delete=>:nullify})
   -> 0.0052s
-- add_foreign_key("events", "namespaces", {:column=>"group_id", :name=>"fk_61fbf6ca48", :on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("events", "projects", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("events", "users", {:column=>"author_id", :name=>"fk_edfd187b6f", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("evidences", "releases", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("external_pull_requests", "projects", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("fork_network_members", "fork_networks", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("fork_network_members", "projects", {:column=>"forked_from_project_id", :name=>"fk_b01280dae4", :on_delete=>:nullify})
   -> 0.0019s
-- add_foreign_key("fork_network_members", "projects", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("fork_networks", "projects", {:column=>"root_project_id", :name=>"fk_e7b436b2b5", :on_delete=>:nullify})
   -> 0.0020s
-- add_foreign_key("forked_project_links", "projects", {:column=>"forked_to_project_id", :name=>"fk_434510edb0", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("geo_container_repository_updated_events", "container_repositories", {:name=>"fk_212c89c706", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("geo_event_log", "geo_cache_invalidation_events", {:column=>"cache_invalidation_event_id", :name=>"fk_42c3b54bed", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("geo_event_log", "geo_container_repository_updated_events", {:column=>"container_repository_updated_event_id", :name=>"fk_6ada82d42a", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("geo_event_log", "geo_hashed_storage_migrated_events", {:column=>"hashed_storage_migrated_event_id", :name=>"fk_27548c6db3", :on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("geo_event_log", "geo_job_artifact_deleted_events", {:column=>"job_artifact_deleted_event_id", :name=>"fk_176d3fbb5d", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("geo_event_log", "geo_lfs_object_deleted_events", {:column=>"lfs_object_deleted_event_id", :name=>"fk_d5af95fcd9", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("geo_event_log", "geo_repositories_changed_events", {:column=>"repositories_changed_event_id", :name=>"fk_4a99ebfd60", :on_delete=>:cascade})
   -> 0.0017s
-- add_foreign_key("geo_event_log", "geo_repository_created_events", {:column=>"repository_created_event_id", :name=>"fk_9b9afb1916", :on_delete=>:cascade})
   -> 0.0056s
-- add_foreign_key("geo_event_log", "geo_repository_deleted_events", {:column=>"repository_deleted_event_id", :name=>"fk_c4b1c1f66e", :on_delete=>:cascade})
   -> 0.0058s
-- add_foreign_key("geo_event_log", "geo_repository_renamed_events", {:column=>"repository_renamed_event_id", :name=>"fk_86c84214ec", :on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("geo_event_log", "geo_repository_updated_events", {:column=>"repository_updated_event_id", :name=>"fk_78a6492f68", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("geo_event_log", "geo_reset_checksum_events", {:column=>"reset_checksum_event_id", :name=>"fk_cff7185ad2", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("geo_event_log", "geo_upload_deleted_events", {:column=>"upload_deleted_event_id", :name=>"fk_c1f241c70d", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("geo_hashed_storage_attachments_events", "projects", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("geo_hashed_storage_migrated_events", "projects", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("geo_node_namespace_links", "geo_nodes", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("geo_node_namespace_links", "namespaces", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("geo_node_statuses", "geo_nodes", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("geo_repositories_changed_events", "geo_nodes", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("geo_repository_created_events", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("geo_repository_renamed_events", "projects", {:on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("geo_repository_updated_events", "projects", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("geo_reset_checksum_events", "projects", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("gitlab_subscriptions", "namespaces", {:name=>"fk_e2595d00a1", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("gitlab_subscriptions", "plans", {:column=>"hosted_plan_id", :name=>"fk_bd0c4019c3", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("gpg_key_subkeys", "gpg_keys", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("gpg_keys", "users", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("gpg_signatures", "gpg_key_subkeys", {:on_delete=>:nullify})
   -> 0.0034s
-- add_foreign_key("gpg_signatures", "gpg_keys", {:on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("gpg_signatures", "projects", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("grafana_integrations", "projects", {:on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("group_custom_attributes", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("group_deletion_schedules", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("group_deletion_schedules", "users", {:name=>"fk_11e3ebfcdd", :on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("group_group_links", "namespaces", {:column=>"shared_group_id", :on_delete=>:cascade})
   -> 0.0084s
-- add_foreign_key("group_group_links", "namespaces", {:column=>"shared_with_group_id", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("identities", "saml_providers", {:name=>"fk_aade90f0fc", :on_delete=>:cascade})
   -> 0.0054s
-- add_foreign_key("import_export_uploads", "namespaces", {:column=>"group_id", :name=>"fk_83319d9721", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("import_export_uploads", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("index_statuses", "projects", {:name=>"fk_74b2492545", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("insights", "namespaces", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("insights", "projects", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("internal_ids", "namespaces", {:name=>"fk_162941d509", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("internal_ids", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("ip_restrictions", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0077s
-- add_foreign_key("issue_assignees", "issues", {:name=>"fk_b7d881734a", :on_delete=>:cascade})
   -> 0.0061s
-- add_foreign_key("issue_assignees", "users", {:name=>"fk_5e0c8d9154", :on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("issue_links", "issues", {:column=>"source_id", :name=>"fk_c900194ff2", :on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("issue_links", "issues", {:column=>"target_id", :name=>"fk_e71bb44f1f", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("issue_metrics", "issues", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("issue_tracker_data", "services", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("issue_user_mentions", "issues", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("issue_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("issues", "epics", {:column=>"promoted_to_epic_id", :name=>"fk_df75a7c8b8", :on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("issues", "issues", {:column=>"duplicated_to_id", :name=>"fk_9c4516d665", :on_delete=>:nullify})
   -> 0.0018s
-- add_foreign_key("issues", "issues", {:column=>"moved_to_id", :name=>"fk_a194299be1", :on_delete=>:nullify})
   -> 0.0020s
-- add_foreign_key("issues", "milestones", {:name=>"fk_96b1dd429c", :on_delete=>:nullify})
   -> 0.0021s
-- add_foreign_key("issues", "projects", {:name=>"fk_899c8f3231", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("issues", "users", {:column=>"author_id", :name=>"fk_05f1e72feb", :on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("issues", "users", {:column=>"closed_by_id", :name=>"fk_c63cbf6c25", :on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("issues", "users", {:column=>"updated_by_id", :name=>"fk_ffed080f01", :on_delete=>:nullify})
   -> 0.0031s
-- add_foreign_key("issues_prometheus_alert_events", "issues", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("issues_prometheus_alert_events", "prometheus_alert_events", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("issues_self_managed_prometheus_alert_events", "issues", {:on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("issues_self_managed_prometheus_alert_events", "self_managed_prometheus_alert_events", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("jira_connect_subscriptions", "jira_connect_installations", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("jira_connect_subscriptions", "namespaces", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("jira_tracker_data", "services", {:on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("label_links", "labels", {:name=>"fk_d97dd08678", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("label_priorities", "labels", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("label_priorities", "projects", {:on_delete=>:cascade})
   -> 0.0051s
-- add_foreign_key("labels", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("labels", "projects", {:name=>"fk_7de4989a69", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("lfs_file_locks", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("lfs_file_locks", "users", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("list_user_preferences", "lists", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("list_user_preferences", "users", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("lists", "boards", {:name=>"fk_0d3f677137", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("lists", "labels", {:name=>"fk_7a5553d60f", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("lists", "milestones", {:on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("lists", "users", {:name=>"fk_d6cf4279f7", :on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("members", "users", {:name=>"fk_2e88fb7ce9", :on_delete=>:cascade})
   -> 0.0076s
-- add_foreign_key("merge_request_assignees", "merge_requests", {:on_delete=>:cascade})
   -> 0.0085s
-- add_foreign_key("merge_request_assignees", "users", {:on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("merge_request_blocks", "merge_requests", {:column=>"blocked_merge_request_id", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("merge_request_blocks", "merge_requests", {:column=>"blocking_merge_request_id", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("merge_request_diff_commits", "merge_request_diffs", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("merge_request_diff_files", "merge_request_diffs", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("merge_request_diffs", "merge_requests", {:name=>"fk_8483f3258f", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("merge_request_metrics", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("merge_request_metrics", "merge_requests", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("merge_request_metrics", "users", {:column=>"latest_closed_by_id", :name=>"fk_ae440388cc", :on_delete=>:nullify})
   -> 0.0032s
-- add_foreign_key("merge_request_metrics", "users", {:column=>"merged_by_id", :name=>"fk_7f28d925f3", :on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("merge_request_user_mentions", "merge_requests", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("merge_request_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("merge_requests", "ci_pipelines", {:column=>"head_pipeline_id", :name=>"fk_fd82eae0b9", :on_delete=>:nullify})
   -> 0.0024s
-- add_foreign_key("merge_requests", "merge_request_diffs", {:column=>"latest_merge_request_diff_id", :name=>"fk_06067f5644", :on_delete=>:nullify})
   -> 0.0021s
-- add_foreign_key("merge_requests", "milestones", {:name=>"fk_6a5165a692", :on_delete=>:nullify})
   -> 0.0024s
-- add_foreign_key("merge_requests", "projects", {:column=>"source_project_id", :name=>"fk_3308fe130c", :on_delete=>:nullify})
   -> 0.0029s
-- add_foreign_key("merge_requests", "projects", {:column=>"target_project_id", :name=>"fk_a6963e8447", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("merge_requests", "users", {:column=>"assignee_id", :name=>"fk_6149611a04", :on_delete=>:nullify})
   -> 0.0061s
-- add_foreign_key("merge_requests", "users", {:column=>"author_id", :name=>"fk_e719a85f8a", :on_delete=>:nullify})
   -> 0.0039s
-- add_foreign_key("merge_requests", "users", {:column=>"merge_user_id", :name=>"fk_ad525e1f87", :on_delete=>:nullify})
   -> 0.0029s
-- add_foreign_key("merge_requests", "users", {:column=>"updated_by_id", :name=>"fk_641731faff", :on_delete=>:nullify})
   -> 0.0031s
-- add_foreign_key("merge_requests_closing_issues", "issues", {:on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("merge_requests_closing_issues", "merge_requests", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("merge_trains", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:nullify})
   -> 0.0021s
-- add_foreign_key("merge_trains", "merge_requests", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("merge_trains", "projects", {:column=>"target_project_id", :on_delete=>:cascade})
   -> 0.0062s
-- add_foreign_key("merge_trains", "users", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("milestone_releases", "milestones", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("milestone_releases", "releases", {:on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("milestones", "namespaces", {:column=>"group_id", :name=>"fk_95650a40d4", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("milestones", "projects", {:name=>"fk_9bd0a0c791", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("namespace_aggregation_schedules", "namespaces", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("namespace_root_storage_statistics", "namespaces", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("namespace_statistics", "namespaces", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("namespaces", "namespaces", {:column=>"custom_project_templates_group_id", :name=>"fk_e7a0b20a6b", :on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("namespaces", "plans", {:name=>"fk_fdd12e5b80", :on_delete=>:nullify})
   -> 0.0055s
-- add_foreign_key("namespaces", "projects", {:column=>"file_template_project_id", :name=>"fk_319256d87a", :on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("note_diff_files", "notes", {:column=>"diff_note_id", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("notes", "projects", {:name=>"fk_99e097b079", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("notes", "reviews", {:name=>"fk_2e82291620", :on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("notification_settings", "users", {:name=>"fk_0c95e91db7", :on_delete=>:cascade})
   -> 0.0038s
-- add_foreign_key("oauth_openid_requests", "oauth_access_grants", {:column=>"access_grant_id", :name=>"fk_77114b3b09", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("operations_feature_flag_scopes", "operations_feature_flags", {:column=>"feature_flag_id", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("operations_feature_flags", "projects", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("operations_feature_flags_clients", "projects", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("packages_build_infos", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:nullify})
   -> 0.0035s
-- add_foreign_key("packages_build_infos", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("packages_conan_file_metadata", "packages_package_files", {:column=>"package_file_id", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("packages_conan_metadata", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0021s
-- add_foreign_key("packages_dependency_links", "packages_dependencies", {:column=>"dependency_id", :on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("packages_dependency_links", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("packages_maven_metadata", "packages_packages", {:column=>"package_id", :name=>"fk_be88aed360", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("packages_package_files", "packages_packages", {:column=>"package_id", :name=>"fk_86f0f182f8", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("packages_package_tags", "packages_packages", {:column=>"package_id", :on_delete=>:cascade})
   -> 0.0020s
-- add_foreign_key("packages_packages", "projects", {:on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("pages_domain_acme_orders", "pages_domains", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("pages_domains", "projects", {:name=>"fk_ea2f6dfc6f", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("path_locks", "projects", {:name=>"fk_5265c98f24", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("path_locks", "users")
   -> 0.0021s
-- add_foreign_key("personal_access_tokens", "users")
   -> 0.0022s
-- add_foreign_key("plan_limits", "plans", {:on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("pool_repositories", "projects", {:column=>"source_project_id", :on_delete=>:nullify})
   -> 0.0036s
-- add_foreign_key("pool_repositories", "shards", {:on_delete=>:restrict})
   -> 0.0029s
-- add_foreign_key("project_alerting_settings", "projects", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("project_aliases", "projects", {:on_delete=>:cascade})
   -> 0.0049s
-- add_foreign_key("project_authorizations", "projects", {:on_delete=>:cascade})
   -> 0.0051s
-- add_foreign_key("project_authorizations", "users", {:on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("project_auto_devops", "projects", {:on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("project_ci_cd_settings", "projects", {:name=>"fk_24c15d2f2e", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("project_custom_attributes", "projects", {:on_delete=>:cascade})
   -> 0.0076s
-- add_foreign_key("project_daily_statistics", "projects", {:on_delete=>:cascade})
   -> 0.0057s
-- add_foreign_key("project_deploy_tokens", "deploy_tokens", {:on_delete=>:cascade})
   -> 0.0052s
-- add_foreign_key("project_deploy_tokens", "projects", {:on_delete=>:cascade})
   -> 0.0107s
-- add_foreign_key("project_error_tracking_settings", "projects", {:on_delete=>:cascade})
   -> 0.0129s
-- add_foreign_key("project_feature_usages", "projects", {:on_delete=>:cascade})
   -> 0.0297s
-- add_foreign_key("project_features", "projects", {:name=>"fk_18513d9b92", :on_delete=>:cascade})
   -> 0.0186s
-- add_foreign_key("project_group_links", "projects", {:name=>"fk_daa8cee94c", :on_delete=>:cascade})
   -> 0.0053s
-- add_foreign_key("project_import_data", "projects", {:name=>"fk_ffb9ee3a10", :on_delete=>:cascade})
   -> 0.0049s
-- add_foreign_key("project_incident_management_settings", "projects", {:on_delete=>:cascade})
   -> 0.0071s
-- add_foreign_key("project_metrics_settings", "projects", {:on_delete=>:cascade})
   -> 0.0070s
-- add_foreign_key("project_mirror_data", "projects", {:name=>"fk_d1aad367d7", :on_delete=>:cascade})
   -> 0.0048s
-- add_foreign_key("project_pages_metadata", "projects", {:on_delete=>:cascade})
   -> 0.0051s
-- add_foreign_key("project_repositories", "projects", {:on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("project_repositories", "shards", {:on_delete=>:restrict})
   -> 0.0026s
-- add_foreign_key("project_repository_states", "projects", {:on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("project_statistics", "projects", {:on_delete=>:cascade})
   -> 0.0064s
-- add_foreign_key("project_tracing_settings", "projects", {:on_delete=>:cascade})
   -> 0.0082s
-- add_foreign_key("projects", "pool_repositories", {:name=>"fk_6e5c14658a", :on_delete=>:nullify})
   -> 0.0052s
-- add_foreign_key("projects", "users", {:column=>"marked_for_deletion_by_user_id", :name=>"fk_25d8780d11", :on_delete=>:nullify})
   -> 0.0084s
-- add_foreign_key("prometheus_alert_events", "projects", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("prometheus_alert_events", "prometheus_alerts", {:on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("prometheus_alerts", "environments", {:on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("prometheus_alerts", "projects", {:on_delete=>:cascade})
   -> 0.0035s
-- add_foreign_key("prometheus_alerts", "prometheus_metrics", {:on_delete=>:cascade})
   -> 0.0079s
-- add_foreign_key("prometheus_metrics", "projects", {:on_delete=>:cascade})
   -> 0.0065s
-- add_foreign_key("protected_branch_merge_access_levels", "namespaces", {:column=>"group_id", :name=>"fk_98f3d044fe", :on_delete=>:cascade})
   -> 0.0052s
-- add_foreign_key("protected_branch_merge_access_levels", "protected_branches", {:name=>"fk_8a3072ccb3", :on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("protected_branch_merge_access_levels", "users")
   -> 0.0066s
-- add_foreign_key("protected_branch_push_access_levels", "namespaces", {:column=>"group_id", :name=>"fk_7111b68cdb", :on_delete=>:cascade})
   -> 0.0051s
-- add_foreign_key("protected_branch_push_access_levels", "protected_branches", {:name=>"fk_9ffc86a3d9", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("protected_branch_push_access_levels", "users")
   -> 0.0041s
-- add_foreign_key("protected_branch_unprotect_access_levels", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("protected_branch_unprotect_access_levels", "protected_branches", {:on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("protected_branch_unprotect_access_levels", "users", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("protected_branches", "projects", {:name=>"fk_7a9c6d93e7", :on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("protected_environment_deploy_access_levels", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("protected_environment_deploy_access_levels", "protected_environments", {:on_delete=>:cascade})
   -> 0.0079s
-- add_foreign_key("protected_environment_deploy_access_levels", "users", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("protected_environments", "projects", {:on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("protected_tag_create_access_levels", "namespaces", {:column=>"group_id", :name=>"fk_b4eb82fe3c", :on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("protected_tag_create_access_levels", "protected_tags", {:name=>"fk_f7dfda8c51", :on_delete=>:cascade})
   -> 0.0049s
-- add_foreign_key("protected_tag_create_access_levels", "users")
   -> 0.0034s
-- add_foreign_key("protected_tags", "projects", {:name=>"fk_8e4af87648", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("push_event_payloads", "events", {:name=>"fk_36c74129da", :on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("push_rules", "projects", {:name=>"fk_83b29894de", :on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("release_links", "releases", {:on_delete=>:cascade})
   -> 0.0065s
-- add_foreign_key("releases", "projects", {:name=>"fk_47fe2a0596", :on_delete=>:cascade})
   -> 0.0100s
-- add_foreign_key("releases", "users", {:column=>"author_id", :name=>"fk_8e4456f90f", :on_delete=>:nullify})
   -> 0.0035s
-- add_foreign_key("remote_mirrors", "projects", {:name=>"fk_43a9aa4ca8", :on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("repository_languages", "projects", {:on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("resource_label_events", "epics", {:on_delete=>:cascade})
   -> 0.0064s
-- add_foreign_key("resource_label_events", "issues", {:on_delete=>:cascade})
   -> 0.0058s
-- add_foreign_key("resource_label_events", "labels", {:on_delete=>:nullify})
   -> 0.0028s
-- add_foreign_key("resource_label_events", "merge_requests", {:on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("resource_label_events", "users", {:on_delete=>:nullify})
   -> 0.0076s
-- add_foreign_key("resource_weight_events", "issues", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("resource_weight_events", "users", {:on_delete=>:nullify})
   -> 0.0041s
-- add_foreign_key("reviews", "merge_requests", {:on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("reviews", "projects", {:on_delete=>:cascade})
   -> 0.0068s
-- add_foreign_key("reviews", "users", {:column=>"author_id", :on_delete=>:nullify})
   -> 0.0043s
-- add_foreign_key("saml_providers", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0030s
-- add_foreign_key("scim_oauth_access_tokens", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0034s
-- add_foreign_key("self_managed_prometheus_alert_events", "environments", {:on_delete=>:cascade})
   -> 0.0028s
-- add_foreign_key("self_managed_prometheus_alert_events", "projects", {:on_delete=>:cascade})
   -> 0.0171s
-- add_foreign_key("sentry_issues", "issues", {:on_delete=>:cascade})
   -> 0.0056s
-- add_foreign_key("serverless_domain_cluster", "clusters_applications_knative", {:on_delete=>:cascade})
   -> 0.0038s
-- add_foreign_key("serverless_domain_cluster", "pages_domains", {:on_delete=>:cascade})
   -> 0.0069s
-- add_foreign_key("serverless_domain_cluster", "users", {:column=>"creator_id", :on_delete=>:nullify})
   -> 0.0057s
-- add_foreign_key("service_desk_settings", "projects", {:on_delete=>:cascade})
   -> 0.0084s
-- add_foreign_key("services", "projects", {:name=>"fk_71cce407f9", :on_delete=>:cascade})
   -> 0.0088s
-- add_foreign_key("slack_integrations", "services", {:on_delete=>:cascade})
   -> 0.0057s
-- add_foreign_key("smartcard_identities", "users", {:on_delete=>:cascade})
   -> 0.0044s
-- add_foreign_key("snippet_user_mentions", "notes", {:on_delete=>:cascade})
   -> 0.0064s
-- add_foreign_key("snippet_user_mentions", "snippets", {:on_delete=>:cascade})
   -> 0.0048s
-- add_foreign_key("snippets", "projects", {:name=>"fk_be41fd4bb7", :on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("software_license_policies", "projects", {:on_delete=>:cascade})
   -> 0.0036s
-- add_foreign_key("software_license_policies", "software_licenses", {:on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("subscriptions", "projects", {:on_delete=>:cascade})
   -> 0.0099s
-- add_foreign_key("suggestions", "notes", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("system_note_metadata", "description_versions", {:name=>"fk_fbd87415c9", :on_delete=>:nullify})
   -> 0.0022s
-- add_foreign_key("system_note_metadata", "notes", {:name=>"fk_d83a918cb1", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("term_agreements", "application_setting_terms", {:column=>"term_id"})
   -> 0.0039s
-- add_foreign_key("term_agreements", "users", {:on_delete=>:cascade})
   -> 0.0089s
-- add_foreign_key("timelogs", "issues", {:name=>"fk_timelogs_issues_issue_id", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("timelogs", "merge_requests", {:name=>"fk_timelogs_merge_requests_merge_request_id", :on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("todos", "namespaces", {:column=>"group_id", :on_delete=>:cascade})
   -> 0.0047s
-- add_foreign_key("todos", "notes", {:name=>"fk_91d1f47b13", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("todos", "projects", {:name=>"fk_45054f9c45", :on_delete=>:cascade})
   -> 0.0039s
-- add_foreign_key("todos", "users", {:column=>"author_id", :name=>"fk_ccf0373936", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("todos", "users", {:name=>"fk_d94154aa95", :on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("trending_projects", "projects", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("u2f_registrations", "users")
   -> 0.0025s
-- add_foreign_key("user_callouts", "users", {:on_delete=>:cascade})
   -> 0.0063s
-- add_foreign_key("user_custom_attributes", "users", {:on_delete=>:cascade})
   -> 0.0072s
-- add_foreign_key("user_interacted_projects", "projects", {:name=>"fk_722ceba4f7", :on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("user_interacted_projects", "users", {:name=>"fk_0894651f08", :on_delete=>:cascade})
   -> 0.0043s
-- add_foreign_key("user_preferences", "users", {:on_delete=>:cascade})
   -> 0.0049s
-- add_foreign_key("user_statuses", "users", {:on_delete=>:cascade})
   -> 0.0033s
-- add_foreign_key("user_synced_attributes_metadata", "users", {:on_delete=>:cascade})
   -> 0.0052s
-- add_foreign_key("users", "application_setting_terms", {:column=>"accepted_term_id", :name=>"fk_789cd90b35", :on_delete=>:cascade})
   -> 0.0057s
-- add_foreign_key("users", "namespaces", {:column=>"managing_group_id", :name=>"fk_a4b8fefe3e", :on_delete=>:nullify})
   -> 0.0042s
-- add_foreign_key("users_ops_dashboard_projects", "projects", {:on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("users_ops_dashboard_projects", "users", {:on_delete=>:cascade})
   -> 0.0023s
-- add_foreign_key("users_security_dashboard_projects", "projects", {:on_delete=>:cascade})
   -> 0.0025s
-- add_foreign_key("users_security_dashboard_projects", "users", {:on_delete=>:cascade})
   -> 0.0026s
-- add_foreign_key("users_star_projects", "projects", {:name=>"fk_22cd27ddfc", :on_delete=>:cascade})
   -> 0.0046s
-- add_foreign_key("vulnerabilities", "epics", {:name=>"fk_1d37cddf91", :on_delete=>:nullify})
   -> 0.0049s
-- add_foreign_key("vulnerabilities", "milestones", {:column=>"due_date_sourcing_milestone_id", :name=>"fk_7c5bb22a22", :on_delete=>:nullify})
   -> 0.0025s
-- add_foreign_key("vulnerabilities", "milestones", {:column=>"start_date_sourcing_milestone_id", :name=>"fk_88b4d546ef", :on_delete=>:nullify})
   -> 0.0021s
-- add_foreign_key("vulnerabilities", "milestones", {:name=>"fk_131d289c65", :on_delete=>:nullify})
   -> 0.0024s
-- add_foreign_key("vulnerabilities", "projects", {:name=>"fk_efb96ab1e2", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("vulnerabilities", "users", {:column=>"author_id", :name=>"fk_b1de915a15", :on_delete=>:nullify})
   -> 0.0057s
-- add_foreign_key("vulnerabilities", "users", {:column=>"closed_by_id", :name=>"fk_cf5c60acbf", :on_delete=>:nullify})
   -> 0.0043s
-- add_foreign_key("vulnerabilities", "users", {:column=>"last_edited_by_id", :name=>"fk_1302949740", :on_delete=>:nullify})
   -> 0.0040s
-- add_foreign_key("vulnerabilities", "users", {:column=>"resolved_by_id", :name=>"fk_76bc5f5455", :on_delete=>:nullify})
   -> 0.0037s
-- add_foreign_key("vulnerabilities", "users", {:column=>"updated_by_id", :name=>"fk_7ac31eacb9", :on_delete=>:nullify})
   -> 0.0024s
-- add_foreign_key("vulnerability_feedback", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:nullify})
   -> 0.0029s
-- add_foreign_key("vulnerability_feedback", "issues", {:on_delete=>:nullify})
   -> 0.0030s
-- add_foreign_key("vulnerability_feedback", "merge_requests", {:name=>"fk_563ff1912e", :on_delete=>:nullify})
   -> 0.0030s
-- add_foreign_key("vulnerability_feedback", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("vulnerability_feedback", "users", {:column=>"author_id", :on_delete=>:cascade})
   -> 0.0032s
-- add_foreign_key("vulnerability_feedback", "users", {:column=>"comment_author_id", :name=>"fk_94f7c8a81e", :on_delete=>:nullify})
   -> 0.0112s
-- add_foreign_key("vulnerability_identifiers", "projects", {:on_delete=>:cascade})
   -> 0.0029s
-- add_foreign_key("vulnerability_issue_links", "issues", {:on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("vulnerability_issue_links", "vulnerabilities", {:on_delete=>:cascade})
   -> 0.0037s
-- add_foreign_key("vulnerability_occurrence_identifiers", "vulnerability_identifiers", {:column=>"identifier_id", :on_delete=>:cascade})
   -> 0.0045s
-- add_foreign_key("vulnerability_occurrence_identifiers", "vulnerability_occurrences", {:column=>"occurrence_id", :on_delete=>:cascade})
   -> 0.0024s
-- add_foreign_key("vulnerability_occurrence_pipelines", "ci_pipelines", {:column=>"pipeline_id", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("vulnerability_occurrence_pipelines", "vulnerability_occurrences", {:column=>"occurrence_id", :on_delete=>:cascade})
   -> 0.0018s
-- add_foreign_key("vulnerability_occurrences", "projects", {:on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("vulnerability_occurrences", "vulnerabilities", {:name=>"fk_97ffe77653", :on_delete=>:nullify})
   -> 0.0022s
-- add_foreign_key("vulnerability_occurrences", "vulnerability_identifiers", {:column=>"primary_identifier_id", :on_delete=>:cascade})
   -> 0.0019s
-- add_foreign_key("vulnerability_occurrences", "vulnerability_scanners", {:column=>"scanner_id", :on_delete=>:cascade})
   -> 0.0040s
-- add_foreign_key("vulnerability_scanners", "projects", {:on_delete=>:cascade})
   -> 0.0041s
-- add_foreign_key("web_hook_logs", "web_hooks", {:on_delete=>:cascade})
   -> 0.0031s
-- add_foreign_key("web_hooks", "projects", {:name=>"fk_0c8ca6d9d1", :on_delete=>:cascade})
   -> 0.0027s
-- add_foreign_key("zoom_meetings", "issues", {:on_delete=>:cascade})
   -> 0.0022s
-- add_foreign_key("zoom_meetings", "projects", {:on_delete=>:cascade})
   -> 0.0022s

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/01_admin.rb
**************************************************
⛔️ WARNING: Sidekiq testing API enabled, but this is not the test environment.  Your jobs will not go to Redis.
**************************************************
.
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/02_application_settings.rb
Creating the default ApplicationSetting record.
Enable hashed storage for every new projects.
.
== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/02_users.rb

Skipping mass insertion for Users.
Consider running the seed with MASS_INSERT=1

Skipping mass insertion for Namespaces.
Consider running the seed with MASS_INSERT=1
....................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/03_project.rb
........
Skipping mass insertion for Projects and relations.
Consider running the seed with MASS_INSERT=1

OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/04_labels.rb

Generating group labels
......................................................................
Generating project labels
........................................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/06_teams.rb
............................................................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/07_milestones.rb
........................................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/09_issues.rb

Seeding issues for the 'gitlab-org/gitlab-test' project
..............
14 issues created!

Seeding issues for the 'gitlab-org/gitlab-shell' project
..........
10 issues created!

Seeding issues for the 'gnuwget/wget2' project
........
8 issues created!

Seeding issues for the 'Commit451/lab-coat' project
.........
9 issues created!

Seeding issues for the 'jashkenas/underscore' project
.......
7 issues created!

Seeding issues for the 'flightjs/flight' project
.......
7 issues created!

Seeding issues for the 'twitter/typeahead-js' project
.........
9 issues created!

Seeding issues for the 'h5bp/html5-boilerplate' project
............
12 issues created!

OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/10_merge_requests.rb
.................................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/11_keys.rb
..........
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/12_snippets.rb
..................................................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/13_comments.rb
................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/14_pipelines.rb

OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/15_award_emoji.rb
............................................................................................................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/16_protected_branches.rb
........
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/17_cycle_analytics.rb
Skipped. Use the `SEED_CYCLE_ANALYTICS` environment variable to enable.

OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/18_abuse_reports.rb
.......................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/19_environments.rb

OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/20_nested_groups.rb
Skipped. Use the `SEED_NESTED_GROUPS` environment variable to enable.

OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/21_dev_ops_score_metrics.rb
.
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/23_spam_logs.rb
.......................
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/24_forks.rb
..........
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/25_api_personal_access_token.rb
.
OK

== Seed from /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/db/fixtures/development/99_common_metrics.rb

== Seed from ee/db/fixtures/development/20_burndown.rb
..........................................................................................
OK

== Seed from ee/db/fixtures/development/20_vulnerabilities.rb

OK

== Seed from ee/db/fixtures/development/22_epics.rb
...................................
OK

== Seed from ee/db/fixtures/development/25_downstream_pipelines.rb

OK

== Seed from ee/db/fixtures/development/26_packages.rb

OK

== Seed from ee/db/fixtures/development/27_plans.rb
....
OK

== Seed from ee/db/fixtures/development/30_customizable_cycle_analytics.rb
Skipped. Use the `SEED_CUSTOMIZABLE_CYCLE_ANALYTICS` environment variable to enable.

OK

== Seed from ee/db/fixtures/development/90_productivity_analytics.rb
Skipped. Use the `SEED_PRODUCTIVITY_ANALYTICS` environment variable to enable.

OK
SELECT pg_catalog.set_config('search_path', '', false)
CREATE DATABASE praefect_development ENCODING 'UTF8' LC_COLLATE 'C' LC_CTYPE 'C';
Generating public/private rsa key pair.
Your identification has been saved in openssh/ssh_host_rsa_key.
Your public key has been saved in openssh/ssh_host_rsa_key.pub.
The key fingerprint is:
SHA256:5zVsS1gzHzPOVphxqLHMxaNtCotlxGFnyxqBYYyRGfA zain@Zains-MacBook-Pro.local
The key's randomart image is:
+---[RSA 2048]----+
|    ..oBo++.o....|
|     .+.o.o=..== |
|      E  ..o*B*..|
|          +***o= |
|        S++o*o=  |
|        .o.+.+   |
|          . .    |
|                 |
|                 |
+----[SHA256]-----+
if false; then \
    protocol='https' gitlab_host=127.0.0.1 gitlab_port=3000 registry_port=5000 \
    support/edit-registry-config.yml registry/config.yml; \
  else \
    gitlab_host=docker.for.mac.localhost gitlab_port=3000 registry_port=5000 \
    support/edit-registry-config.yml registry/config.yml; \
  fi
Generating a 2048 bit RSA private key
......................+++
..+++
writing new private key to 'localhost.key'
-----
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  108M  100  108M    0     0  8265k      0  0:00:13  0:00:13 --:--:-- 10.1M
elasticsearch-6.5.1.tar.gz.tmp: OK

-------------------------------------------------------
Setup finished!
-------------------------------------------------------

# GitLab Development Kit cheat sheet

gdk start                                 # Start everything
gdk start redis postgresql                # Start specific services
gdk stop                                  # Stop all services and unload Runit
gdk stop redis postgresql                 # Stop specific service
gdk status                                # See status of all services
gdk restart                               # Restart everything
gdk restart redis postgresql              # Restart specific services

gdk tail                                  # Tail all logs
gdk tail redis postgresql                 # Tail specific logs

gdk thin                                  # Run rails web server with thin in foreground

gdk install gitlab_repo=https://my-fork   # Install everything
gdk update                                # Pull application changes from Git
gdk reconfigure                           # Delete and regenerate all config files created by GDK
gdk psql -d gitlabhq_development          # Postgres console
gdk redis-cli                             # Redis console

gdk doctor                                # Run diagnostics on GDK

# Development admin account: root / 5iveL!fe

For more information about GitLab development see
https://docs.gitlab.com/ce/development/README.html.
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



$ support/set-gitlab-upstream
Remote origin is gitlab, adding remote upstream to gitlab
Fetching master from upstream...
remote: Enumerating objects: 36, done.
remote: Counting objects: 100% (36/36), done.
remote: Compressing objects: 100% (33/33), done.
remote: Total 36 (delta 13), reused 19 (delta 3), pack-reused 0
Unpacking objects: 100% (36/36), done.
From https://gitlab.com/gitlab-org/gitlab
 * branch                    master     -> FETCH_HEAD
 * [new branch]              master     -> upstream/master
Branch 'master' set up to track remote branch 'master' from 'upstream'.

# Verify upstream is set up correctly
$ cd gitlab
# blank
$ git remote -v
origin git@gitlab.com:zainfathoni/gitlab.git (fetch)
origin git@gitlab.com:zainfathoni/gitlab.git (push)
upstream https://gitlab.com/gitlab-org/gitlab.git (fetch)
upstream none (push)

```

</details>

<details><summary>Copy YAML configuration from the example then run GitLab locally</summary>

```bash
$ cp gdk.example.yml gdk.yml
# blank

$ gdk start
(in /Users/zain/Code/GitLab/gitlab-development-kit)
run: ./services/gitlab-pages: (pid 40346) 13s, normally down; run: log: (pid 40199) 25s
run: ./services/gitlab-workhorse: (pid 40351) 13s, normally down; run: log: (pid 40196) 25s
run: ./services/jaeger: (pid 40347) 13s, normally down; run: log: (pid 40197) 25s
run: ./services/postgresql: (pid 40349) 13s, normally down; run: log: (pid 40193) 25s
run: ./services/praefect: (pid 40348) 13s, normally down; run: log: (pid 40202) 25s
run: ./services/praefect-gitaly-0: (pid 40350) 13s, normally down; run: log: (pid 40195) 25s
run: ./services/rails-background-jobs: (pid 40353) 13s, normally down; run: log: (pid 40201) 25s
run: ./services/rails-web: (pid 40355) 13s, normally down; run: log: (pid 40194) 25s
run: ./services/redis: (pid 40352) 13s, normally down; run: log: (pid 40198) 25s
run: ./services/webpack: (pid 40354) 13s, normally down; run: log: (pid 40200) 25s
```

Open [http://localhost:3000](http://localhost:3000/) and you should see GitLab sign in page.
The development login credentials are `root` and `5iveL!fe`.

![GitLab Sign In page](images/gitlab-sign-in-page.png)

</details>

<details><summary>Generate frontend fixtures for running the unit tests</summary>

```bash
$ bundle install
Fetching gem metadata from https://rubygems.org/........
Using rake 12.3.3
Using RedCloth 4.3.2
Using multipart-post 2.0.0
Using ace-rails-ap 4.1.2
Using abstract_type 0.0.7
Using thread_safe 0.3.6
Using concurrent-ruby 1.1.5
Using erubi 1.9.0
Using mini_portile2 2.4.0
Using crass 1.0.5
Using rack 2.0.7
Using nio4r 2.5.2
Using websocket-extensions 0.1.3
Using mini_mime 1.0.2
Using arel 9.0.0
Using pg 1.1.4
Using mimemagic 0.3.2
Using ice_nine 0.11.2
Using public_suffix 3.1.1
Using aes_key_wrap 1.0.1
Using akismet 3.0.0
Using graphql 1.9.11
Using bundler 1.17.3
Fetching builder 3.2.4
Using minitest 5.11.3
Using thor 0.20.3
Using method_source 0.9.2
Using jwt 2.1.0
Using multi_xml 0.6.0
Using asciidoctor 2.0.10
Using multi_json 1.13.1
Using encryptor 3.0.0
Using ast 2.4.0
Using awesome_print 1.8.0
Using aws-eventstream 1.0.3
Using jmespath 1.4.0
Using babosa 1.0.2
Using base32 0.3.2
Using batch-loader 1.4.0
Using bcrypt 3.1.12
Using bcrypt_pbkdf 1.0.0
Using benchmark-ips 2.3.0
Using memory_profiler 0.9.13
Using coderay 1.1.2
Using bindata 2.4.3
Using binding_ninja 0.2.3
Using debug_inspector 0.0.3
Using msgpack 1.3.1
Using brakeman 4.2.1
Using browser 2.5.3
Using uniform_notifier 1.13.0
Using byebug 9.1.0
Using regexp_parser 1.5.1
Using mime-types-data 3.2019.0331
Using cause 0.1
Using character_set 1.1.2
Using charlock_holmes 0.7.6
Using childprocess 3.0.0
Using chunky_png 1.3.5
Using citrus 3.0.2
Using claide 1.0.3
Using colored2 3.1.2
Using nap 1.1.0
Using open4 1.3.4
Using equalizer 0.0.11
Using connection_pool 2.2.2
Using contracts 0.11.0
Using i18n_data 0.8.0
Using sixarm_ruby_unaccent 1.2.0
Using unicode_utils 1.4.0
Using safe_yaml 1.0.4
Using creole 0.5.0
Using daemons 1.2.6
Using git 1.5.0
Using kramdown 2.1.0
Using no_proxy_fix 0.1.2
Using unicode-display_width 1.6.0
Using attr_required 1.0.1
Using database_cleaner 1.7.0
Using debugger-ruby_core_source 1.3.8
Using declarative 0.0.10
Using declarative-option 0.1.0
Using get_process_mem 0.2.3
Using heapy 0.1.4
Using device_detector 1.0.0
Using orm_adapter 0.5.0
Using rotp 2.1.2
Using diff-lcs 1.3
Using diff_match_patch 0.1.0
Using diffy 3.1.0
Using unf_ext 0.0.7.5
Using netrc 0.11.0
Using docile 1.3.1
Using ed25519 1.2.4
Using hashie 3.5.7
Using elasticsearch-rails 0.1.9
Using htmlentities 4.3.4
Using email_reply_trimmer 0.1.6
Using eventmachine 1.2.7
Using excon 0.62.0
Using escape_utils 1.2.1
Using expression_parser 0.9.0
Using fast_blank 1.0.0
Using fast_gettext 1.6.0
Using ffaker 2.10.0
Using ffi 1.11.3
Using flipper 0.17.1
Using formatador 0.2.5
Using ipaddress 0.8.3
Using xml-simple 1.1.5
Using memoist 0.16.0
Using os 1.0.0
Using httpclient 2.8.3
Using uber 0.1.0
Using retriable 3.1.2
Using raabro 1.1.6
Using rspec-support 3.8.2
Using ruby-progressbar 1.10.1
Using gemoji 3.0.1
Using json 1.8.6
Using execjs 2.6.0
Using text 1.3.1
Using locale 2.1.2
Using google-protobuf 3.8.0 (universal-darwin)
Using github-markup 1.7.0
Using opentracing 0.5.0
Using numerizer 0.2.0
Using redis 4.1.3
Using thrift 0.11.0.0
Using gitlab-markup 1.7.0
Using gitlab-net-dns 0.9.1
Using jaro_winkler 1.5.4
Using parallel 1.19.1
Using rainbow 3.0.0
Using net-ldap 0.16.0
Using pyu-ruby-sasl 0.0.3.3
Using rubyntlm 0.6.2
Using request_store 1.3.1
Using mustermann 1.0.3
Using rb-fsevent 0.10.2
Using ruby_dep 1.5.0
Using lumberjack 1.0.13
Using nenv 0.3.0
Using shellany 0.0.1
Using guard-compat 1.2.1
Using temple 0.8.2
Using tilt 2.0.10
Using sysexits 1.2.0
Using hangouts-chat 0.0.5
Using hashdiff 0.3.8
Using http-form_data 2.1.1
Using http_parser.rb 0.6.0
Using icalendar 2.4.1
Using oauth 0.5.4
Using regexp_property_values 0.3.4
Using kaminari-core 1.0.1
Using kgio 2.11.2
Using knapsack 1.17.0
Using recursive-open-struct 1.1.0
Using rubyzip 1.3.0
Using parslet 1.8.2
Using with_env 1.1.0
Using rugged 0.28.4.1
Using liquid 4.0.3
Using mail_room 0.10.0
Using mini_magick 4.9.5
Using murmurhash3 0.1.6
Using nakayoshi_fork 0.0.4
Using net-ntp 2.1.3
Using net-ssh 5.2.0
Using timfel-krb5-auth 0.8.3
Using optimist 3.0.0
Using rubypants 0.2.0
Using procto 0.0.3
Using prometheus-client-mmap 0.9.10
Using rack-cors 1.0.2
Using rack-timeout 0.5.1
Using raindrops 0.19.0
Using rdoc 6.0.4
Using re2 1.1.1
Using rinku 2.0.0
Using rouge 3.11.0
Using rspec-set 0.1.3
Using sqlite3 1.3.13
Using ruby-prof 1.0.0
Using sexp_processor 4.12.0
Using settingslogic 2.0.9
Using simple_po_parser 1.1.2
Using gitlab-license 1.0.0
Using slack-notifier 1.5.1
Using simplecov-html 0.10.2
Using sshkey 2.0.0
Using state_machines 0.5.0
Using test-prof 0.10.0
Using timecop 0.8.1
Using u2f 0.2.1
Using version_sorter 2.2.4
Using vmstat 2.3.0
Using stackprof 0.2.13
Using i18n 1.7.0
Using tzinfo 1.2.5
Using nokogiri 1.10.7
Using rack-test 1.1.0
Using websocket-driver 0.7.0
Using mail 2.7.1
Using marcel 0.3.3
Using memoizable 0.4.2
Using addressable 2.5.2
Using sprockets 3.7.2
Using descendants_tracker 0.0.4
Using warden 1.2.8
Using gitlab-puma 4.3.1.gitlab.2
Using rack-protection 2.0.5
Using gpgme 2.0.19
Using rack-accept 0.4.5
Using rack-attack 6.2.0
Using rack-proxy 0.6.0
Using bundler-audit 0.5.0
Using atlassian-jwt 0.2.0
Using asciidoctor-include-ext 0.3.1
Using asciidoctor-plantuml 0.0.10
Using attr_encrypted 3.1.0
Using aws-sigv4 1.1.0
Using benchmark-memory 0.1.2
Using better_errors 2.5.0
Using binding_of_caller 0.8.0
Using bootsnap 1.4.5
Using mime-types 3.2.2
Using cork 0.3.0
Using countries 3.0.0
Using crack 0.4.3
Using kramdown-parser-gfm 1.1.0
Using elasticsearch-api 5.0.3
Using parser 2.6.5.0
Using pry 0.11.3
Using rqrcode 0.7.0
Using snowplow-tracker 0.6.1
Using toml-rb 1.0.0
Using terminal-table 1.8.0
Using rblineprof 0.3.6
Using faraday 0.12.2
Using unf 0.1.4
Using omniauth 1.9.0
Using hashie-forbidden_attributes 0.1.1
Using derailed_benchmarks 1.3.5
Using representable 3.0.4
Using rspec-core 3.8.2
Using gettext_i18n_rails 1.8.0
Using rb-inotify 0.9.10
Using gssapi 1.2.0
Using rspec-expectations 3.8.4
Using rspec-mocks 3.8.1
Using sassc 2.0.1
Using sys-filesystem 1.1.6
Using recaptcha 4.13.1
Using uglifier 2.7.2
Using gemojione 3.3.0
Using po_to_json 1.0.1
Using influxdb 0.2.3
Using gettext 3.2.9
Using googleapis-common-protos-types 1.0.4
Using gitlab-chronic 0.10.5
Using gitlab_chronic_duration 0.10.6.2
Using redis-store 1.8.1
Using redis-namespace 1.6.0
Using jaeger-client 0.10.0
Using mustermann-grape 1.0.0
Using notiffany 0.1.3
Using haml 5.1.2
Using hamlit 2.11.0
Using js_regex 3.1.1
Using toml 0.2.0
Using licensee 8.9.2
Using org-ruby 0.9.12
Using rbtrace 0.4.11
Using ruby_parser 3.13.1
Using selenium-webdriver 3.142.6
Using unicorn 5.4.1
Using unleash 0.1.5
Using simplecov 0.16.1
Using ruby-saml 1.7.2
Using truncato 0.7.11
Using activesupport 5.2.3
Using thin 1.7.2
Using adamantium 0.2.0
Fetching loofah 2.4.0
Using axiom-types 0.1.1
Using xpath 3.2.0
Using launchy 2.4.3
Using coercible 1.0.0
Using ruby-enum 0.7.2
Using css_parser 1.7.0
Using et-orbi 1.2.1
Using gitlab-puma_worker_killer 0.1.1.gitlab.1
Using sidekiq 5.2.7
Using html2text 0.2.0
Using json-schema 2.8.0
Using nokogumbo 1.5.0
Using pry-byebug 3.5.1
Using pry-rails 0.3.6
Using rqrcode-rails3 0.1.7
Using ruby-fogbugz 0.2.1
Using webmock 3.5.1
Using aws-sdk-core 2.11.374
Using claide-plugins 0.9.2
Using httparty 0.16.4
Using rubocop 0.74.0
Using sentry-raven 2.9.0
Using acme-client 2.0.2
Using faraday_middleware 0.12.2
Using oauth2 1.4.1
Using faraday-http-cache 2.0.0
Using sawyer 0.8.1
Using domain_name 0.5.20180417
Using elasticsearch-transport 5.0.3
Using signet 0.11.0
Using gitlab_omniauth-ldap 2.1.1
Using omniauth-cas3 1.1.4
Using omniauth-multipassword 0.4.2
Using omniauth-oauth 1.1.0
Using omniauth-shibboleth 1.3.0
Using fuubar 2.2.0
Using grpc 1.24.0 (universal-darwin)
Using grape-entity 0.7.1
Using sass-listen 4.0.0
Using listen 3.1.5
Using rspec 3.8.0
Using jira-ruby 1.7.1
Using license_finder 5.4.0
Using omniauth-saml 1.10.0
Using swd 1.1.2
Using webfinger 1.1.0
Using omniauth_crowd 2.2.3
Using redis-rack 2.0.6
Using redis-activesupport 5.2.0
Using rspec-retry 0.6.1
Using rspec_junit_formatter 0.4.1
Using shoulda-matchers 4.0.1
Using spring 2.0.2
Using unicorn-worker-killer 0.4.4
Using rails-dom-testing 2.0.3
Using globalid 0.4.2
Using activemodel 5.2.3
Using bullet 6.0.2
Using html-pipeline 2.12.2
Using json-jwt 1.9.4
Using factory_bot 5.1.0
Using flipper-active_support_cache_store 0.17.1
Using concord 0.1.5
Using capybara 3.22.0
Using commonmarker 0.20.1
Using email_spec 2.2.0
Using flowdock 0.7.1
Using fugit 1.2.1
Using gitlab-sidekiq-fetcher 0.5.2
Using rubocop-gitlab-security 0.1.1
Using rubocop-performance 1.4.1
Using rubocop-rails 2.4.0
Using rubocop-rspec 1.37.0
Using virtus 1.0.5
Using haml_lint 0.34.0
Using hipchat 1.5.2
Using letter_opener 1.7.0
Using omniauth-oauth2 1.6.0
Using premailer 1.11.1
Using sanitize 4.6.6
Using faraday_middleware-multi_json 0.0.6
Using aws-sdk-resources 2.11.374
Using octokit 4.9.0
Using http-cookie 1.0.3
Using elasticsearch 5.0.3
Using googleauth 0.6.6
Using gitaly 1.73.0
Using sass 3.5.5
Using guard 2.15.1
Using omniauth-kerberos 0.3.0
Using omniauth-twitter 1.4.0
Using spring-commands-rspec 1.0.4
Using activejob 5.2.3
Using rack-oauth2 1.9.3
Using validate_email 0.1.6
Using validate_url 1.0.8
Using unparser 0.4.5
Using state_machines-activemodel 0.7.1
Using activerecord 5.2.3
Using capybara-screenshot 1.0.22
Using carrierwave 1.3.1
Using deckar01-task_list 2.3.1
Using extended-markdown-filter 0.6.0
Using sidekiq-cron 1.0.4
Installing builder 3.2.4
Using activerecord-explain-analyze 0.1.0
Using acts-as-taggable-on 6.5.0
Using asana 0.9.3
Using aws-sdk 2.11.374
Using danger 6.0.9
Using default_value_for 3.3.0
Using rest-client 2.0.2
Using elasticsearch-model 0.1.9
Using faraday_middleware-aws-signers-v4 0.1.7
Using flipper-active_record 0.17.1
Using google-api-client 0.23.4
Using gitlab-styles 3.1.0
Using graphql-docs 1.6.0
Using guard-rspec 4.7.3
Using http 3.3.0
Using kaminari-activerecord 1.0.1
Using omniauth-auth0 2.0.0
Using omniauth-authentiq 0.3.3
Using omniauth-azure-oauth2 0.0.10
Using omniauth-facebook 4.0.0
Using omniauth-github 1.3.0
Using omniauth-gitlab 1.0.3
Using omniauth-google-oauth2 0.6.0
Using omniauth-oauth2-generic 0.2.2
Using omniauth-salesforce 1.0.5
Using openid_connect 1.1.8
Using proc_to_ast 0.1.0
Using scss_lint 0.56.0
Using seed-fu 2.3.7
Using state_machines-activerecord 0.6.0
Using validates_hostname 1.0.6
Using discordrb-webhooks-blackst0ne 3.3.0
Using kubeclient 4.4.0
Using omniauth_openid_connect 0.3.3
Using rspec-parameterized 0.4.2
Using omniauth-ultraauth 0.0.2
Installing loofah 2.4.0
Using fog-core 2.1.0
Using wikicloth 0.8.1
Using fog-json 1.2.0
Using fog-xml 0.1.3
Using fog-local 0.6.0
Using fog-aliyun 0.3.3
Using fog-openstack 1.0.8
Using fog-aws 3.5.2
Using fog-google 1.9.1
Using fog-rackspace 0.1.1
Using grape 1.1.0
Using grape-path-helpers 1.1.0
Using grape_logging 1.7.0
Using rails-html-sanitizer 1.3.0
Using actionview 5.2.3
Using actionpack 5.2.3
Using kaminari-actionview 1.0.1
Using actioncable 5.2.3
Using railties 5.2.3
Using sprockets-rails 3.2.1
Using actionmailer 5.2.3
Using activestorage 5.2.3
Using gon 6.2.0
Using bootstrap_form 4.2.0
Using kaminari 1.0.1
Using rails-controller-testing 1.0.4
Using redis-actionpack 5.1.0
Fetching gitlab-labkit 0.8.0
Using marginalia 1.8.0
Using doorkeeper 4.3.2
Using responders 3.0.0
Using font-awesome-rails 4.7.0.5
Using factory_bot_rails 5.1.0
Using lograge 0.10.0
Using letter_opener_web 1.3.4
Using premailer-rails 1.10.3
Using rails-i18n 5.1.1
Using rspec-rails 4.0.0.beta3
Using webpack-rails 0.9.11
Using rails 5.2.3
Using peek 1.1.0
Using graphiql-rails 1.4.10
Using sassc-rails 2.1.0
Using redis-rails 5.0.2
Using doorkeeper-openid_connect 1.5.0
Using devise 4.7.1
Using devise-two-factor 3.0.0
Using apollo_upload_server 2.0.0.beta.3
Using health_check 2.6.0
Using gettext_i18n_rails_js 1.3.0
Using rspec_profiling 0.0.5
Using invisible_captcha 0.12.1
Installing gitlab-labkit 0.8.0
Bundle complete! 250 Gemfile dependencies, 478 gems now installed.
Gems in the group production were not installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.

$ gdk start
(in /Users/zain/Code/GitLab/gitlab-development-kit)
ok: run: ./services/gitlab-pages: (pid 46182) 0s, normally down
ok: run: ./services/gitlab-workhorse: (pid 46181) 0s, normally down
ok: run: ./services/jaeger: (pid 46186) 0s, normally down
ok: run: ./services/postgresql: (pid 46183) 0s, normally down
ok: run: ./services/praefect: (pid 46184) 0s, normally down
ok: run: ./services/praefect-gitaly-0: (pid 46185) 0s, normally down
ok: run: ./services/rails-background-jobs: (pid 46188) 0s, normally down
ok: run: ./services/rails-web: (pid 46187) 0s, normally down
ok: run: ./services/redis: (pid 46189) 0s, normally down
ok: run: ./services/webpack: (pid 46190) 0s, normally down

$ gdk stop rails
(in /Users/zain/Code/GitLab/gitlab-development-kit)
ok: down: ./services/rails-background-jobs: 0s
ok: down: ./services/rails-web: 0s

$ gdk status
(in /Users/zain/Code/GitLab/gitlab-development-kit)
run: ./services/gitlab-pages: (pid 46182) 11s, normally down; run: log: (pid 46177) 12s
run: ./services/gitlab-workhorse: (pid 46181) 11s, normally down; run: log: (pid 46175) 12s
run: ./services/jaeger: (pid 46186) 11s, normally down; run: log: (pid 46174) 12s
run: ./services/postgresql: (pid 46183) 11s, normally down; run: log: (pid 46176) 12s
run: ./services/praefect: (pid 46184) 11s, normally down; run: log: (pid 46172) 12s
run: ./services/praefect-gitaly-0: (pid 46185) 11s, normally down; run: log: (pid 46179) 12s
down: ./services/rails-background-jobs: 5s; run: log: (pid 46170) 12s
down: ./services/rails-web: 5s; run: log: (pid 46171) 12s
run: ./services/redis: (pid 46189) 11s, normally down; run: log: (pid 46173) 12s
run: ./services/webpack: (pid 46190) 11s, normally down; run: log: (pid 46178) 12s

$ bin/rake frontend:fixtures
/Users/zain/.rvm/rubies/ruby-2.6.3/bin/ruby -I/Users/zain/.rvm/gems/ruby-2.6.3/gems/rspec-core-3.8.2/lib:/Users/zain/.rvm/gems/ruby-2.6.3/gems/rspec-support-3.8.2/lib /Users/zain/.rvm/gems/ruby-2.6.3/gems/rspec-core-3.8.2/exe/rspec --pattern \{spec,ee/spec\}/frontend/fixtures/\*.rb --format documentation
warning: parser/current is loading parser/ruby26, which recognizes
warning: 2.6.5-compliant syntax, but you are running 2.6.3.
warning: please see https://github.com/whitequark/parser#compatibility-with-ruby-mri.
Run options: include {:focus=>true}

All examples were filtered out; ignoring {:focus=>true}

==> Setting up Gitaly...
Checking gitaly-ruby Gemfile...
Checking gitaly-ruby bundle...
The Gemfile\'s dependencies are satisfied
Trying to connect to gitaly: ................ OK
    Gitaly set up in 48.521242 seconds...

==> Setting up GitLab Elasticsearch Indexer...
    GitLab Elasticsearch Indexer set up in 38.492915 seconds...

Analytics (JavaScript fixtures)
  Groups::CycleAnalytics::EventsController
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>3}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>4}
    cycle_analytics/events/issue.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>7}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>8}
    cycle_analytics/events/plan.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>11}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>12}
    cycle_analytics/events/review.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>15}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>16}
    cycle_analytics/events/code.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>19}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>20}
    cycle_analytics/events/test.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>23}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>24}
    cycle_analytics/events/staging.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>27}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>28}
    cycle_analytics/events/production.json
  Groups::CycleAnalyticsController
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>31}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>32}
    cycle_analytics/mock_data.json
  Analytics::CycleAnalytics::StagesController
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>35}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>36}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>42}
    analytics/cycle_analytics/stages.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>45}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>46}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>52}
    analytics/cycle_analytics/stages/issue/records.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>55}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>56}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>62}
    analytics/cycle_analytics/stages/issue/median.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>65}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>66}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>72}
    analytics/cycle_analytics/stages/plan/records.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>75}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>76}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>82}
    analytics/cycle_analytics/stages/plan/median.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>85}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>86}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>92}
    analytics/cycle_analytics/stages/code/records.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>95}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>96}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>102}
    analytics/cycle_analytics/stages/code/median.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>105}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>106}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>112}
    analytics/cycle_analytics/stages/test/records.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>115}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>116}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>122}
    analytics/cycle_analytics/stages/test/median.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>125}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>126}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>132}
    analytics/cycle_analytics/stages/review/records.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>135}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>136}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>142}
    analytics/cycle_analytics/stages/review/median.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>145}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>146}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>152}
    analytics/cycle_analytics/stages/staging/records.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>155}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>156}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>162}
    analytics/cycle_analytics/stages/staging/median.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>165}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>166}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>172}
    analytics/cycle_analytics/stages/production/records.json
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>175}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>176}
2015-07-03T10:00:00.000Z 46548 TID-ouyrltsaw WARN: {:class=>"ArchiveTraceWorker", :message=>"The job does not have live trace but going to be archived.", :job_id=>182}
    analytics/cycle_analytics/stages/production/median.json
  Analytics::TasksByTypeController
    analytics/type_of_work/tasks_by_type.json

Epics (JavaScript fixtures)
  EpicPresenter (JavaScript fixtures)
    epic/mock_meta.json
  IssuablesHelper (JavaScript fixtures)
    epic/mock_data.json

Groups::SamlProvidersController (JavaScript fixtures)
DEPRECATION WARNING: The success? predicate is deprecated and will be removed in Rails 6.0. Please use successful? as provided by Rack::Response::Helpers. (called from block (2 levels) in <main> at /Users/zain/Code/GitLab/gitlab-development-kit/gitlab/ee/spec/frontend/fixtures/saml_providers.rb:28)
  groups/saml_providers/show.html

Admin::AbuseReportsController (JavaScript fixtures)
  abuse_reports/abuse_reports_list.html

Admin::UsersController (JavaScript fixtures)
  admin/users/new_with_internal_user_regex.html

Admin::ApplicationSettingsController (JavaScript fixtures)
  application_settings/accounts_and_limit.html

Projects::AutocompleteSourcesController (JavaScript fixtures)
  autocomplete_sources/labels.json

Projects::BlobController (JavaScript fixtures)
  blob/show.html

Projects::BoardsController (JavaScript fixtures)
  boards/show.html

Projects::BranchesController (JavaScript fixtures)
  branches/new_branch.html

Projects::ClustersController (JavaScript fixtures)
  clusters/show_cluster.html

Projects::CommitController (JavaScript fixtures)
  commit/show.html

Projects::DeployKeysController (JavaScript fixtures)
  deploy_keys/keys.json

Groups (JavaScript fixtures)
  GroupsController (JavaScript fixtures)
    groups/edit.html
  Groups::Settings::CiCdController (JavaScript fixtures)
    groups/ci_cd_settings.html

Projects::IssuesController (JavaScript fixtures)
  issues/new-issue.html
  issues/open-issue.html
  issues/closed-issue.html
  issues/issue-with-task-list.html
  issues/issue_with_comment.html
  issues/issue_list.html

API::Issues (JavaScript fixtures)
  issues/related_merge_requests.json

Projects::JobsController (JavaScript fixtures)
  builds/build-with-artifacts.html
  jobs/delayed.json

Labels (JavaScript fixtures)
  Groups::LabelsController (JavaScript fixtures)
    labels/group_labels.json
  Projects::LabelsController (JavaScript fixtures)
    labels/project_labels.json

Projects::MergeRequestsController (JavaScript fixtures)
  merge_requests/merge_request_of_current_user.html
  merge_requests/merge_request_with_task_list.html
  merge_requests/merged_merge_request.html
  merge_requests/diff_comment.html
  merge_requests/merge_request_with_comment.html
  merge_requests/discussions.json
  merge_requests/diff_discussion.json
  merge_requests/resolved_diff_discussion.json
  with image diff
    merge_requests/image_diff_discussion.json

Projects::MergeRequests::DiffsController (JavaScript fixtures)
  merge_request_diffs/with_commit.json
  merge_request_diffs/inline_changes_tab_with_comments.json
  merge_request_diffs/parallel_changes_tab_with_comments.json

Projects::PipelineSchedulesController (JavaScript fixtures)
  pipeline_schedules/edit.html
  pipeline_schedules/edit_with_variables.html

Projects::PipelinesController (JavaScript fixtures)
  pipelines/pipelines.json

Projects (JavaScript fixtures)
  ProjectsController (JavaScript fixtures)
    projects/dashboard.html
/Users/zain/.rvm/rubies/ruby-2.6.3/lib/ruby/2.6.0/delegate.rb:100: warning: delegator does not forward private method #to_ary
    projects/overview.html
    projects/edit.html
  Projects::Settings::CiCdController (JavaScript fixtures)
    projects/ci_cd_settings.html
    projects/ci_cd_settings_with_variables.html

Projects::ServicesController (JavaScript fixtures)
  services/prometheus/prometheus_service.html

Raw files (JavaScript fixtures)
  blob/balsamiq/test.bmpr
  blob/notebook/basic.json
  blob/notebook/worksheets.json
  blob/notebook/math.json
  blob/pdf/test.pdf

SearchController (JavaScript fixtures)
  search/show.html

Projects::ServicesController (JavaScript fixtures)
  services/edit_service.html

Sessions (JavaScript fixtures)
  SessionsController (JavaScript fixtures)
    sessions/new.html

SnippetsController (JavaScript fixtures)
  snippets/show.html

Projects::PipelinesController (JavaScript fixtures)
  pipelines/test_report.json

Todos (JavaScript fixtures)
  Dashboard::TodosController (JavaScript fixtures)
    todos/todos.html
  Projects::TodosController (JavaScript fixtures)
    todos/todos.json

U2F
  SessionsController (JavaScript fixtures)
    u2f/authenticate.html
  Profiles::TwoFactorAuthsController (JavaScript fixtures)
    u2f/register.html

Finished in 10 minutes 13 seconds (files took 1 minute 20.9 seconds to load)
85 examples, 0 failures

$ yarn jest
Test Suites: 5 failed, 763 passed, 768 total
Tests:       8 failed, 6 skipped, 7604 passed, 7618 total
Snapshots:   176 passed, 176 total
Time:        149.243s

$ gdk stop
(in /Users/zain/Code/GitLab/gitlab-development-kit)
ok: down: ./services/rails-background-jobs: 27114s
ok: down: ./services/rails-web: 27114s
ok: down: ./services/gitlab-pages: 0s
ok: down: ./services/gitlab-workhorse: 0s
ok: down: ./services/jaeger: 0s
ok: down: ./services/postgresql: 0s
ok: down: ./services/praefect: 0s
ok: down: ./services/praefect-gitaly-0: 0s
ok: down: ./services/redis: 0s
ok: down: ./services/webpack: 0s
Shutting down runsvdir (pid 46159)
```

</details>
