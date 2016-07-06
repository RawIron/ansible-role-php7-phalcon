Role Name
=========

A brief description of the role goes here.

REF
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

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

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
            - php7.1
            - php7.1-gd
            - php7.1-curl
        - role: geerlingguy.composer
        - role: ..
          php7_phalcon_php_version: "7.1"

Vagrant
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

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
