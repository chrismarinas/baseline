# Baseline

A basic dev environment setup that includes the following:

- CentOS 6.5
- Apache 2.2.15
- PHP 5.5.34
- MySQL 5.5.48

## Setup

1. Rename `build/ansible/group_vars/all.example` to `build/ansible/group_vars/all.yml`.

2. Update values in `group_vars/all.yml` as needed.

3. Run _vagrant up_ from docroot.

4. Add the following to your `/etc/hosts` file:

    ```
    192.168.200.10 vagrant.dev
    ```

## Todo

In the future I want to create a bunch of different playbooks for different LAMP combinations.