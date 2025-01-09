# Configuration

## ansible.cfg

``` ini title="ansible.cfg"
--8<-- "docs/files/ansible.cfg"
```

## Launch Playbook with vaulted files

```bash
ansible-playbook playbook.yml  --ask-vault-password
```

## Launch Playbook with configured vault password file

> Need to put the password in user home directory in file

``` bash
export ANSIBLE_VAULT_PASSWORD_FILE=~/.vault_password
ansible-playbook playbook.yml
```
