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

## Requirements

- Ansible >= 2.9 **(No tests has been realized before this version)**

## Role Variables

All variables which can be overridden are stored in [default/main.yml](default/main.yml) file as well as in table below.

| Name           | Default Value | Choices | Description                        |
| -------------- | ------------- | ------- | -----------------------------------|
| `restic_version` | "latest" | [version](https://github.com/restic/restic/tags) | Choice of the restic version. |

## Example Playbook

```yaml
---
- hosts: all
  tasks:
    - name: Install restic backup
      include_role:
        name: ansible-role-restic
      vars:
        restic_version: 0.11.0
```
## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.

## Maintainers and Contributors

- [Anthony Dieperink](https://github.com/adieperi)
