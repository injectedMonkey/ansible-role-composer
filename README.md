COMPOSER
========

[![Build Status](https://travis-ci.org/injectedMonkey/ansible-role-composer.svg?branch=master)](https://travis-ci.org/injectedMonkey/ansible-role-composer)
[![License](https://img.shields.io/badge/License-BSD%202--Clause-orange.svg)](https://opensource.org/licenses/BSD-2-Clause)
[![GitHub release](https://img.shields.io/github/release/injectedMonkey/ansible-role-composer.svg?style=flat)](https://github.com/injectedMonkey/ansible-role-composer/releases)

Ansible role for composer. It's designed for my development environment
but might reach sometimes production ready state.

Supported distributions:
- Debian
- Ubuntu

Requirements
------------

This role requires ansible >= 2.4.

Dictionaries are used for configuration. Partially overriding defaults needs

      hash_behaviour = merge

to be set in your ansible.cfg or

      ANSIBLE_HASH_BEHAVIOUR=merge

for your environment.

Role Variables
--------------

      composer:
        path: /usr/local/bin
        self_update: true



Dependencies
------------

Make sure php is installed, but there are no dependencies on other roles.


Example Playbook
----------------

    - hosts: servers
    - include_role:
        name: injectedMonkey.composer
      vars:
        composer:
          path: /usr/local/bin
          self_update: true


License
-------

BSD

Author Information
------------------

injectedMonkey.wtf
