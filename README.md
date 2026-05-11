# Ansible common role

Just a meta role for install all the needed roles

### Roles
```
  - yatesr.timezone as "timezone"
  - https://github.com/nightsnake/ansible-role-inputrc as "inputrc"
  - https://github.com/nightsnake/ansible-role-bash-profile as "bash-profile"
  - https://github.com/nightsnake/bash_smoothly_ps as "bash_smoothly_ps"
  - https://github.com/nightsnake/ansible-role-users.git as "users"
  - ericsysmin.chrony as "chrony"
  - dev-sec.ssh-hardening as "ssh-hardening"
  - weareinteractive.sudo as "sudoers"
  - robertdebock.locale as "locale"
  - ontic.hostname as "hostname"
```
Please don't forget to add roles above in your roles/requirements.yml

### Example playbook

```
- hosts: all
  become: yes
  gather_facts: no
  roles:
    - { role: ansible-role-common }
```
