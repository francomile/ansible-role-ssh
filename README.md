# Ansible SSH Role

## Actions of the Role

* Setup SSH and enforce security

## Common Usage

```yaml
roles:
- { role: francomile.ssh,
    ssh_port: 22,
    ssh_authorized_keys_file: false,
    ssh_permit_root_login: "no",
    ssh_password_authentication: "no",
    ssh_pubkey_authentication: "yes",
    ssh_use_pam: "yes",
    # If you want to set allowed users and groups, set first ro true the switches and define the users and groups:
    # ssh_allow_users: true,
    # ssh_allow_users_list: ["johndoe", "batman"],
    # ssh_allow_groups: true,
    # ssh_allow_groups_list: ["adm", "sudo"],
    tags: ["ssh"]
  }
```

## Run the playbook

```shell
ansible-playbook -i inventory playbook.yaml --tags "ssh"
```
