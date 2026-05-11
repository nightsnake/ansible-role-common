# Ansible common role

Just a meta role for install all the needed roles

### Roles

This role import bunch of other roles via ansible.bulitin.import_role.
You need to add these roles to you `roles/requirements.yml` manually.

Example of requirements.yml
```
roles:
  - src: https://github.com/nightsnake/ansible-role-common
    name: common
  - src: ericsysmin.chrony
    name: chrony
  - src: ontic.hostname
    name: hostname
  - src: robertdebock.locale
    name: locale
  - src: yatesr.timezone
    name: timezone
  - src: https://github.com/nightsnake/ansible-role-inputrc
    name: inputrc
  - src: https://github.com/nightsnake/ansible-role-users.git
    name: users
  - src: weareinteractive.sudo
    name: sudoers
  - src: https://github.com/nightsnake/ansible-role-bash-profile
    name: bash-profile    

collections:
  - name: devsec.hardening

```

### Example playbook

```
- hosts: all
  become: true
  gather_facts: no
  roles:
    - { role: ansible-role-common }
```
