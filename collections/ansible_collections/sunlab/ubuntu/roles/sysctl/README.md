sysctl
========

Apply system level configurations via sysctl

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default packages can be overwritten with the following:

```yaml
---
sysctl:
  conf:
    ct: # FOR CONTAINERIZED SYSTEMS SUCH AS LXC
      - net.ipv6.conf.all.disable_ipv6: 1
    vm: # FOR VIRTUAL MACHINES OR BARE METAL
      - vm.swappiness: 10
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
    - sysctl
```