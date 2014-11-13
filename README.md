Ansible iptables Role
=====================

An ansible role for installing and configuring iptables.

Role Variables
--------------
firewall_allowed_services: Only supported on Ubuntu. List service names (ie, OpenSSH)
firewall_allowed_ports: Define a list of hashes that specify port and proto.

**Don't forget to allow port 22 for SSH, or your first run will lock you out of your servers!**
```
firewall_allowed_ports:
  - port: 22
    proto: tcp
```
or
```
firewall_allowed_services:
    - OpenSSH
```

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - { role: MichaelRigart.iptables }

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>