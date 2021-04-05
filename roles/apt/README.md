apt
========

Install and remove desired system packages via aptitude

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default packages are based on a security-forward approach and can be overwritten with the following:

```yaml
---
apt:
  install:
    - nano
  remove:
    - vim
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
    - apt
```