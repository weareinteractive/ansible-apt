# apt

[![Build Status](https://travis-ci.org/weareinteractive/ansible-role-apt.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-role-apt)

> `apt` is an [Ansible](http://www.ansible.com) role which configures apt and installs/updates packages

# Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install weareinteractive.ansible-role-apt
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install weareinteractive.ansible-role-apt
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-role-apt.git
```

# Variables

```yml
# file: defauls/main.yaml

# install packages
apt_packages: []
# upgrade all packages
apt_upgrade: 'yes'
# sets the amount of time the cache is valid (5m)
apt_cache_valid_time: 3600
```

# Usage

Here's an example playbook:

```yml
# file: playbook.yml

- host: all
  role: weareinteractive.apt
```

# Testing

To test this role run:

```
$ git clone https://github.com/weareinteractive/ansible-role-apt.git
$ cd ansible-role-apt
$ vagrant up
```

## Contributing
[![I Love Open Source](http://www.iloveopensource.io/images/logo-lightbg.png)](http://www.iloveopensource.io/projects/53da2bea87659fce66003fa9)

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.
