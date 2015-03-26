Ansible iptables Role
=====================
[![Build Status](https://travis-ci.org/michaelrigart/ansible-role-iptables.svg?branch=master)](https://travis-ci.org/michaelrigart/ansible-role-iptables)

An ansible role for installing and configuring iptables.

Role Variables
--------------

```yaml
firewall_allowed_services: Only supported on Ubuntu. List service names (ie, OpenSSH)
firewall_allowed_ports: Define a list of hashes that specify port and proto.
```

**Don't forget to allow port 22 for SSH, or your first run will lock you out of your servers!**

```yaml
firewall_allowed_ports:
  - port: 22
    proto: tcp
```
or

```yaml
firewall_allowed_services:
    - OpenSSH
```

Example Playbook
-------------------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.iptables, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>