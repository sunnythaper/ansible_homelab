logindefs
========

Configure /etc/login.defs to be more security-forward in approach

Requirements
------------

Tested with Ansible 2.8.5

Role Variables
--------------

Default declarations are based on a security-forward approach and can be overwritten with the following:

```yaml
---
logindefs:
  conf:
    CHFN_RESTRICT: rwh
    DEFAULT_HOME: "no"
    ENCRYPT_METHOD: SHA512
    ENV_PATH: "PATH=/usr/local/bin:/usr/bin:/bin"
    ENV_SUPATH: "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
    ERASECHAR: 0177
    FAILLOG_ENAB: "yes"
    FTMP_FILE: /var/log/btmp
    GID_MAX: 60000
    GID_MIN: 1000
    HUSHLOGIN_FILE: .hushlogin
    KILLCHAR: 025
    LOG_OK_LOGINS: "yes"
    LOG_UNKFAIL_ENAB: "no"
    LOGIN_RETRIES: 5
    LOGIN_TIMEOUT: 30
    MAIL_DIR: /var/mail
    PASS_MAX_DAYS: 365
    PASS_MIN_DAYS: 1
    PASS_WARN_AGE: 7
    SHA_CRYPT_MAX_ROUNDS: 65536
    SHA_CRYPT_MIN_ROUNDS: 10000
    SU_NAME: su
    SYSLOG_SG_ENAB: "yes"
    SYSLOG_SU_ENAB: "yes"
    TTYGROUP: tty
    TTYPERM: 0600
    UID_MAX: 60000
    UID_MIN: 1000
    UMASK: 077
    USERGROUPS_ENAB: "no"
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
    - logindefs
```