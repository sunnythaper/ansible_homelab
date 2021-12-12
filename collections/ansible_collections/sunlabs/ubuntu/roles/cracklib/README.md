cracklib
========

Harden password requirements with cracklib for pam

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
cracklib:
  conf:
    dcredit: -2
    difok: 3
    lcredit: -2
    minlen: 16
    ocredit: -1
    retry: 3
    ucredit: -1
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
    - cracklib
```