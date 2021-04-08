fail2ban
========

Install & configure fail2ban with enforced profiles

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
fail2ban:
  apt:
    install:
      - fail2ban
  conf:
    backend: "auto"
    bantime: "10m"
    destemail: "admin@example.com"
    findtime: "10m"
    logencoding: "auto"
    maxretry: "5"
    mta: "sendmail"
    protocol: "tcp"
    sender: "fail2ban@example.com"
    usedns: "warn"
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
    - fail2ban
```