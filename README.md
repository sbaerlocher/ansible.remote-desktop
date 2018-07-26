# Ansible Role: remote-desktop

[![Build Status](https://travis-ci.org/sbaerlocher/ansible.remote-desktop.svg?branch=master)](https://travis-ci.org/sbaerlocher/ansible.remote-desktop) [![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://sbaerlo.ch/licence) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-remote-desktop-blue.svg)](https://galaxy.ansible.com/sbaerlocher/remote_desktop)

## Description

Enables Windows Remote Desktop Services on Windows.

## Installation

```bash
ansible-galaxy install sbaerlocher.remote-desktop
```

## Requirements

None

## Role Variables

| Variable             | Default     | Comments (type)                                   |
| :---                 | :---        | :---                                              |
| remote_desktop_enabled | false | |
| remote_desktop_port | 3389 | |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
     - sbaerlocher.remote-desktop
```

## Changelog

### 1.1.0

* Spport for change the Remote Desktop Connection port

### 1.0.0

* inital commit

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2018, Simon Bärlocher