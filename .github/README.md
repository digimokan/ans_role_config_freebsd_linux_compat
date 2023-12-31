# ans_role_config_freebsd_linux_compat

Install and configure the FreeBSD Linux Binary-Compatibility Layer.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_freebsd_linux_compat.svg?label=release)](https://github.com/digimokan/ans_role_config_freebsd_linux_compat/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install the [FreeBSD Linux Binary-Compatibility Layer](https://docs.freebsd.org/en/books/handbook/linuxemu/#linuxemu-lbc-install).
* Configure the Linux Binary-Compatibility Layer service.

## Supported Operating Systems

* FreeBSD

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_freebsd_linux_compat
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure the FreeBSD Linux Binary-Compat Layer"
         ansible.builtin.include_role:
           name: ans_role_config_freebsd_linux_compat
           public: true
   ```

## Role Options

See the role `defaults` files for main role vars listings:

  * [defaults](../defaults/main/)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_freebsd_linux_compat/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

