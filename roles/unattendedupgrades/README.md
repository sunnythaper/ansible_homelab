unattendedupgrades
========

Install and schedule apt package updates via unattended upgrades

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
unattendedupgrades:
  conf:
    AutoFixInterruptedDpkg: "true"
    Automatic_Reboot_Time: "05:00"
    Automatic_Reboot_WithUsers: "false"
    Automatic_Reboot: "true"
    Debug: "false"
    InstallOnShutdown: "false"
    Mail: admin@example.com
    MailOnlyOnError: true
    MinimalSteps: "true"
    OnlyOnACPower: "true"
    Package_Blacklist: []
    Remove_New_Unused_Dependencies: "true"
    Remove_Unused_Dependencies: "true"
    Remove_Unused_Kernel_Packages: "true"
    Skip_Updates_On_Metered_Connections: "true"
    SyslogEnable: "true"
    SyslogFacility: "daemon"
    Verbose: "false"
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
    - unattendedupgrades
```