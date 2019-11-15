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
$ gem list | grep gitlab-development-kit
gitlab-development-kit (0.2.5)
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
