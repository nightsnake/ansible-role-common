# Ansible common role

Just a meta role for install all the needed roles

### Roles
```
  - geerlingguy.pip
  - yatesr.timezone
  - https://github.com/nightsnake/ansible-role-inputrc
  - https://github.com/nightsnake/bash_smoothly_ps
  - ericsysmin.chrony
  - https://github.com/nightsnake/ansible-resolv
  - MichaelRigart.aliases
  - Oefenweb.postfix
  - dev-sec.ssh-hardening
  - weareinteractive.sudo
  - robertdebock.locale
  - ontic.hostname
```
### Example playbook

```
- hosts: all
  become: yes
  gather_facts: no
  roles:
    - { role: ansible-role-common }
```
