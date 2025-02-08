# home-infra
Home infrastructure as a code

## Dependencies

1. Install `sshpass` on local machine
2. Install `NetworkManager-wifi` on remote machine if WiFi support is needed
3. [Fix the SUDO permission](https://access.redhat.com/solutions/6217761)
  `Defaults noexec`
  `chmod 4755 /usr/bin/sudo`

## Commands

### List inventory

```sh
ansible-inventory -i inventory/hosts.yaml --list
```

### Encrypt secrets

```sh
ansible-vault encrypt_string --vault-password-file vars/vault_password.txt "password" --name 'key'
```

### Running playbooks in syntax check mode

```sh
ansible-playbook -i inventory/hosts.yaml --vault-password-file vars/vault_password.txt --syntax-check init_infra.yaml
```

### Running playbooks

```sh
ansible-playbook -i inventory/hosts.yaml --vault-password-file vars/vault_password.txt init_infra.yaml
```