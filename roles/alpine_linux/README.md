# Alpine Linux Setup

- First run thru initial setup by entering `setup-alpine`
- Check if root login is disabled (for Ansible setup playbook) by entering `grep -i "rootlogin" /etc/ssh/sshd_config`
- If root login is disabled, edit SSH config by entering `vi /etc/ssh/sshd_config` and editing the line for PermitRootLogin to `PermitRootLogin prohibit-password`
- If SSH config was changed, restart the SSH service by entering `rc-service sshd restart`

