postfix
========

Configure postfix in a security-forward approach

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
postfix:
  conf:

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
    - postfix
```