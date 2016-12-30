Ansible iptables Role
=====================

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
     - { role: MichaelRigart.iptables, become: true }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>
