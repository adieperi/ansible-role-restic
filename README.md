# ansible-role-restic
Ansible role for deploying the restic binary

## How to install
### requirements.yml
**Put the file in your roles directory**
```yaml
---
- src: https://github.com/adieperi/ansible-role-restic.git
  scm: git
  version: master
  name: ansible-role-restic
```
### Download the role
```Shell
ansible-galaxy install -f -r ./roles/requirements.yml --roles-path=./roles
```
## Exemple Playbook
```yaml
---
- hosts: all
  tasks:

    - name: Install restic
      include_role:
        name: ansible-role-restic
      vars:
        resticVersion: 0.12.0
```