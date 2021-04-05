coredump
========

Disable / restrict system coredumps

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
coredump:
  apt:
    install:
      - systemd-coredump
  conf:
    ProcessSizeMax: 0
    Storage: none
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
    - coredump
```