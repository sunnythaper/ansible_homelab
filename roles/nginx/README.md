nginx
====

Configure nginx in a security-forward approach

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
nginx:
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
    - nginx
```