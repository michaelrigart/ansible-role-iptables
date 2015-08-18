Ansible iptables Role
=====================
[![Build Status](https://semaphoreci.com/api/v1/projects/1e3346f0-e00a-42a5-b9c9-8b1faafd271c/459459/badge.svg)](https://semaphoreci.com/michaelrigart/ansible-role-iptables)

An ansible role for installing and configuring iptables.

Role Variables
--------------

```yaml
firewall_allowed_ports: Define a list of cits that specify all different rules. Every item in the dict stands for a parameter of the ufw module. Default rule value is allow
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
