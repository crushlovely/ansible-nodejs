# Ansible Role For A Base Linux System

[![Build Status](http://img.shields.io/travis/crushlovely/ansible-linux-base.svg?style=flat)](https://travis-ci.org/crushlovely/ansible-linux-base)
[![Current Version](http://img.shields.io/github/release/crushlovely/ansible-linux-base.svg?style=flat)](https://galaxy.ansible.com/list#/roles/1180)

This Ansible role that installs `nodejs` and `npm`.  After it installs node and npm it will clear npm cache then globally installs Grunt CLI and Bower.

We use this to install Node when required.

## Installation

``` bash
$ ansible-galaxy install crushlovely.nodjs
```

## Variables

``` yaml
node_version: 0.10.15
npm_version: 1.4.4
node_prefix: "node-v{{ node_version }}"
node_tarball: "{{ node_prefix }}.tar.gz"
node_path: /usr/local
```

## Usage

Once this role is installed on your system, include it in the roles list of your playbook.

``` yaml
---
- hosts: localhost
  roles:
    - { role: crushlovely.nodejs, node_version: 0.10.15, npm_version: 1.4.4 }
```

## Dependencies

None

## License

MIT