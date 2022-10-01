aide
========

Install aide for filesystem monitoring

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default packages can be overwritten with the following:

```yaml
---
aide:
  apt:
    install:
      - aide
      - aide-common
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
    - aide
```