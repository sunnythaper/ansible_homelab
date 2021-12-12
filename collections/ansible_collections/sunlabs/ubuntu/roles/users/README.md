users
========

Add & remove normal, system, and sudo users

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
users:
  add: []
  sudo: []
  system: []
  remove:
    - games
    - gnats
    - irc
    - list
    - news
    - sync
    - uucp
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
    - users
```