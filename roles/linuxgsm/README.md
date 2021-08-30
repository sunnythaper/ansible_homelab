linuxgsm
========

Install and upgrade games via linuxgsm

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
linuxgsm:
  server: sdtdserver
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
    - linuxgsm
```