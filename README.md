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
$ git clone https://github.com/weareinteractive/ansible-apt.git
```

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```
# sets the amount of time the cache is valid
apt_cache_valid_time: 3600
# upgrade system: safe | full | dist
apt_upgrade:
# packages to install
apt_packages: []
# apt_packages state: present | latest
apt_package_state: present
# remove packages that are no longer needed for dependencies
apt_autoremove: yes
# remove .deb files for packages no longer on your system
apt_autoclean: yes
# whether or not suggested packages should be installed.
apt_install_suggests: false
# whether or not recommended packages should be installed.
apt_install_recommends: false
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
    apt_packages_state: latest
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
