timedatectl
========

Set system timezones via timedatectl.

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default is to setup timezone as `America/Phoenix` and can be overwritten with the following:

```yaml
---
local:
  timedatectl:
    timezone: America/Phoenix
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
    - timedatectl
```