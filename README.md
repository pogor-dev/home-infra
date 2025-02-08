# home-infra
Home infrastructure as a code

## Dependencies

1. Install `sshpass`

## Commands

### List inventory

```sh
ansible-inventory -i inventory/hosts.yaml --list
```

### Encrypt secrets

```sh
ansible-vault encrypt_string --vault-password-file vars/vault_password.txt "password" --name 'key'
```

### Running playbooks in check mode

```sh
ansible-playbook -i inventory/hosts.yaml --vault-password-file vars/vault_password.txt --check playbooks/init_infra.yaml
```