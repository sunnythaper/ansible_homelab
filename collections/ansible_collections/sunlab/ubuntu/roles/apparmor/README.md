apparmor
========

Install and enfore AppArmor profiles

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default packages are based on a security-forward approach and can be overwritten with the following:

```yaml
---
apparmor:
  apt:
    install:
      - apparmor
      - apparmor-profiles
      - apparmor-profiles-extra
      - apparmor-utils
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
    - apparmor
```