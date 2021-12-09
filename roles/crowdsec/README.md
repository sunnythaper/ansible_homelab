crowdsec
========

Install & configure crowdsec

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
crowdsec:
  apt:
    prereqs:
      - curl
      - gnupg
      - apt-transport-https
    install:
      - crowdsec
      - crowdsec-firewall-bouncer-iptables
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
---
- hosts: all
  roles:
    - crowdsec
```