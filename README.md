Role Name
=========

A brief description of the role goes here.

REF
------------

* https://gist.github.com/Tosyn/fef6437dd3906ff200e471e478eaae95

* http://phalcon.io/phalconphp-and-php7

Requirements
------------

  - `php` (version 7.0+) should be installed and working (you can use the `geerlingguy.php` role to install).
  - `composer` should be installed and working (you can use the `geerlingguy.composer` role to install).
  - `git` should be installed and working (you can use the `geerlingguy.git` role to install).

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - role: geerlingguy.git
        - role: geerlingguy.php
          php_packages:
            - php7.1
            - php7.1-gd
            - php7.1-curl
        - role: geerlingguy.composer
        - role: vkill.php7-phalcon
          php7_phalcon_php_version: "7.1"

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
