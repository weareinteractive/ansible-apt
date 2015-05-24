# Ansible APT Role

[![Build Status](https://img.shields.io/travis/weareinteractive/ansible-apt.svg)](https://travis-ci.org/weareinteractive/ansible-apt)
[![Galaxy](http://img.shields.io/badge/galaxy-franklinkim.apt-blue.svg)](https://galaxy.ansible.com/list#/roles/1366)
[![GitHub Tags](https://img.shields.io/github/tag/weareinteractive/ansible-apt.svg)](https://github.com/weareinteractive/ansible-apt)
[![GitHub Stars](https://img.shields.io/github/stars/weareinteractive/ansible-apt.svg)](https://github.com/weareinteractive/ansible-apt)

> `apt` is an [ansible](http://www.ansible.com) role which:
>
> * updates apt
> * cleans up apt
> * configures apt
> * installs packages
> * add repositories
> * add keys
> * manages unattended upgrades

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.apt
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.apt
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-apt.git franklinkim.apt
```

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```
# apt_unattended_upgrades_blacklist:
#   - vim
#   - libc6
# apt_mails:
#   - root
#   - foo@dev.null
#

# sets the amount of time the cache is valid
apt_cache_valid_time: 3600
# upgrade system: safe | full | dist
apt_upgrade: no
# packages to install
apt_packages: []
# remove packages that are no longer needed for dependencies
apt_autoremove: yes
# remove .deb files for packages no longer on your system
apt_autoclean: yes

# whether or not suggested packages should be installed.
apt_install_suggests: no
# do not install Recommended packages by default
apt_install_recommends: no
# allow 'apt-get autoremove' to remove recommended packages
apt_remove_recommends: no

# enable unattended-upgrades
apt_unattended_upgrades: yes
# list of packages to not update (regexp are supported)
apt_unattended_upgrades_blacklist: []
# Split the upgrade into the smallest possible chunks so that
# they can be interrupted with SIGUSR1. This makes the upgrade
# a bit slower but it has the benefit that shutdown while a upgrade
# is running is possible (with a small delay)
apt_unattended_upgrades_minimal_steps: no
# Send email to this address for problems or packages upgrades
# If empty or unset then no email is sent, make sure that you
# have a working mail setup on your system. A package that provides
# 'mailx' must be installed. E.g. "user@example.com"
apt_mails: []
# Set this value to "true" to get emails only on errors. Default
# is to always send a mail if Unattended-Upgrade::Mail is set
apt_unattended_upgrades_notify_always: no
# do automatic removal of new unused dependencies after the upgrade
# (equivalent to apt-get autoremove)
apt_unattended_upgrades_autoremove: yes

# remount file system: rootfs | tmpfs
#   tmpfs:  remount tmp before running if mounted noexec
#   rootfs: remount root filesystem r/w before running if mounted r/o
apt_remount_filesystem:

# repositories to register
apt_repositories: []
# gpg keys for external repositories
apt_keys: []
```

## Example playbook

```
- hosts: all
  sudo: yes
  roles:
    - franklinkim.apt
  vars:
    apt_cache_valid_time: 7200
    apt_packages:
      - vim
      - tree
    apt_mails:
      - root
    apt_unattended_upgrades_notify_always: yes
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-apt.git
$ cd ansible-apt
$ vagrant up
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.
