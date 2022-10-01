ufw
========

Install and setup ufw with default rules

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
ufw:
  applications: []
  conf:
    DEFAULT_APPLICATION_POLICY: SKIP
    DEFAULT_FORWARD_POLICY: DROP
    DEFAULT_INPUT_POLICY: DROP
    DEFAULT_OUTPUT_POLICY: ACCEPT
    IPV6: no
    MANAGE_BUILTINS: no
    IPT_SYSCTL: /etc/ufw/sysctl.conf
  rules:
    - port: 22
      proto: tcp
      rule: allow
    - port: 53
      proto: any
      rule: allow
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
    - ufw
```