modprobe
========

Remove filesystems & network protocols via modprobe

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
modprobe:
  filename: 50-local
  disable:
    filesystems:
      - cramfs
    networks:
      - dccp
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
    - modprobe
```