# Builtin

## ==meta==

[ansible.builtin.meta](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/meta_module.html)

- clear_facts
- clear_host_errors
- end_host
- end_play
- flush_handlers
- noop
- refresh_inventory
- reset_connection
- end_batch

## ==include_role==

- name
- tasks_from

``` yaml
  - name: Init Role Vars | ZONING BULK
    ansible.builtin.include_role:
      name: zoning
      tasks_from: zoning-bulk-0-init-playbook-vars.yml
    vars:
      step: 0
```
