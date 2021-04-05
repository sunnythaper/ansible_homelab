dns
========

Set hostname, dns, and basic network settings

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default is to setup most settings via magic variables or vault variables (since I'd like to keep this info consistent yet private) and can be overwritten with the following:

```yaml
---
vault:
  host:
    domain: example.com
    nameservers:
      - 1.1.1.1
      - 1.0.0.1
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
    - dns
```