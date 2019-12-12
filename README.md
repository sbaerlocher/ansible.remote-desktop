# Ansible Role: remote-desktop

[![Build Status](https://img.shields.io/travis/sbaerlocher/ansible.remote-desktop.svg?branch=master&style=popout-square)](https://travis-ci.org/sbaerlocher/ansible.remote-desktop) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-remote-desktop-blue.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/remote-desktop) [![Ansible Role](https://img.shields.io/ansible/role/d/27482.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/remote-desktop)

## Description

Enables Windows Remote Desktop Services on Windows.

## Installation

```bash
ansible-galaxy install sbaerlocher.remote-desktop
```

## Requirements

None

## Role Variables

| Variable                          | Default                 | Comments (type)                                                                                                                                                                       |
| :-------------------------------- | :---------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| remote_desktop_enabled            | false                   |                                                                                                                                                                                       |
| remote_desktop_minencryptionLevel | '3'                     | [![getadmx doc](https://img.shields.io/badge/getadmx-doc-blue.svg)](https://getadmx.com/?Category=Windows_10_2016&Policy=Microsoft.Policies.TerminalServer::TS_ENCRYPTION_POLICY)     |
| remote_desktop_port               | 3389                    |                                                                                                                                                                                       |
| remote_desktop_shutdown_disable   | false                   | Disables the ability to shut down the device.                                                                                                                                         |
| remote_desktop_securitylayer      | '1'                     | [![getadmx doc](https://img.shields.io/badge/getadmx-doc-blue.svg)](https://getadmx.com/?Category=Windows_10_2016&Policy=Microsoft.Policies.TerminalServer::TS_SECURITY_LAYER_POLICY) |
| remote_desktop_group              | 'Remotedesktopbenutzer' | Group for logging on to the Remote Desktop Service.                                                                                                                                   |
| remote_desktop_members            | []                      | Users or groups who are allowed to log on to the Remote Desktop.                                                                                                                      |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.remote-desktop
```

## Author

- [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2020, Simon Bärlocher
