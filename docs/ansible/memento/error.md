# Error

[Ansible Error Playbook](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_error_handling.html)

## ignore_errors

```yaml
- name: Do not count this as a failure
  ansible.builtin.command: /bin/false
  ignore_errors: true
```

## ignore_unreachable

```yaml
- hosts: all
  ignore_unreachable: true
  tasks:
  - name: This executes, fails, and the failure is ignored
    ansible.builtin.command: /bin/true

  - name: This executes, fails, and ends the play for this host
    ansible.builtin.command: /bin/true
    ignore_unreachable: false
```

## failed_when

## changed_when
