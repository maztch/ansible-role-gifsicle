# Ansible Role: gifsicle

[![Build Status](https://travis-ci.com/maztch/ansible-role-gifsicle.svg?branch=master)](https://travis-ci.com/maztch/ansible-role-gifsicle)

Installs gifsicle from source, on RedHat/CentOS and Debian/Ubuntu servers.

## Requirements

If you are using SSL/TLS, you will need to provide your own certificate and key files. You can generate a self-signed certificate with a command like `openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout example.key -out example.crt`.


## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    gifsicle_version: 1.91
    

Gifsicle version to install.

    gifsicle_options:
      - --disable-gifview
      - --disable-gifdiff

A list of extra options for build giflossy.


## Dependencies

None.

## Example Playbook

    - hosts: webservers
      vars_files:
        - vars/main.yml
      roles:
        - { role: maztch.gifsicle }

*Inside `vars/main.yml`*:

    giflossy_options:
      - --disable-gifview

## License

MIT / BSD

