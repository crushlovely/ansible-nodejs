# Ansible Role For Node.js

[![Build Status](https://img.shields.io/circleci/project/crushlovely/ansible-nodejs.svg?style=flat)](https://img.shields.io/circleci/project/crushlovely/ansible-nodejs.svg)
[![Current Version](http://img.shields.io/github/release/crushlovely/ansible-nodejs.svg?style=flat)](https://github.com/crushlovely/ansible-nodejs)

This Ansible role installs `nodejs` and `npm`.  After it installs node and npm it will clear npm cache then globally installs Grunt CLI and Bower.

We use this to install Node when required.

## Installation

``` bash
$ ansible-galaxy install crushlovely.nodejs,v1.0.0
```

## Variables

``` yaml
node:
  version: 0.10.15
  path: /usr/local
  user: ubuntu
  group: ubuntu
npm:
  version: 1.4.4
```

## Usage

Once this role is installed on your system, include it in the roles list of your playbook.

``` yaml
- hosts: localhost
  roles:
    - crushlovely.ansible-nodejs
```
You can also add a vars folder to your project folder and have your variables served by adding them to a file and calling it in your playbook.

```yaml
- hosts: localhost
...
  vars_files:
    - vars/default_vars.yml
...
```

## Dependencies

This role requires there to be a `deploy` user with sudo capabilities.  [Click here to view our users role](https://galaxy.ansible.com/list#/roles/1337).  This role was developed with the `hash_behaviour = merge` setting.  You can add it to your ansible config file.

## License

MIT