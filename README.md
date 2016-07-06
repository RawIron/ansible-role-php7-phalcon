Role Name
=========

[![Build Status](https://travis-ci.org/vkill/ansible-role-php7-phalcon.svg?branch=master)](https://travis-ci.org/vkill/ansible-role-php7-phalcon)

PhalconPhp with PHP7 Installation.

Refer
------------

* https://gist.github.com/Tosyn/fef6437dd3906ff200e471e478eaae95

* http://phalcon.io/phalconphp-and-php7

Requirements
------------

  - `php` (version 7.0+) should be installed and working (you can use `apt-get` to install or use the `geerlingguy.php` role to install).
  - `composer` should be installed and working (you can `apt-get` to install or use the `geerlingguy.composer` role to install).
  - `git` should be installed and working (you can use `apt-get` to install or the `geerlingguy.git` role to install).

Role Variables
--------------

TODO

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  become: true

  pre_tasks:
    - name: Add repository for PHP 7
      apt_repository: repo='ppa:ondrej/php'
      tags: system

  roles:
    - role: geerlingguy.git
    - role: geerlingguy.php
      php_enable_php_fpm: False
      php_enable_webserver: False
      php_packages:
        - php7.0
        - php7.0-gd
        - php7.0-curl
    - role: geerlingguy.composer
    - role: vkill.php7-phalcon
      php7_phalcon_php_version: "7.0"
```

Local Testing with Vagrant
----------------

* Install some ansible galaxy in your local system

```shell
$ ansible-galaxy install geerlingguy.php
$ ansible-galaxy install geerlingguy.composer
$ ansible-galaxy install geerlingguy.git
```

* Run vagrant

```shell
$ vagrant up --no-provision
$ vagrant provision
```

License
-------

MIT / BSD

Author Information
------------------

vkill <vkill.net@gmail.com>

&copy; 2016
