# Loops

[Official Ansible Loop](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#iterating-over-a-simple-list)

##  Loop named

```yaml
    loop: "{{ CfgConfigZonning.list }}"
    loop_control:
      loop_var: data
```

## Nested Loop

```yaml
---
- hosts: localhost
  gather_facts: False

  tasks:
  - name: Loop nested
    debug:
      msg: "{{ item[0] }} ::  {{ item[1] }}"
    with_nested:
      - [ 'alice', 'bob' ]
      - [ 'clientdb', 'employeedb', 'providerdb' ]
...
```

## Boucle for

```yaml
---
- hosts: localhost
  gather_facts: False

  tasks:

  - name: Transform la variable list[0] en integer
    set_fact:
      firstSeqList: "{{ list[0] | int }}

  - name: init pair / inpaire : InitRange = 0 / 1
    set_fact:
      initRange: "{{ firstSeqList | int % 2 }}"

  - name: boucle for de 2 en 2 : range([start, ]stop[, step])
    debug:
      msg:
        - "{{ item }}"
    loop: "{{ range( initRange | int , lastSeqList | int + 1, 2 ) | list }}"
...
```

## Double loop Ansible

``` yaml title="Double loop Ansible" linenums="1" hl_lines="17-18 22-25 29-30"
--8<-- "docs/playbooks/loop00.yml"
```

``` text title="" hl_lines="3 6 9 12 17 20 23 26"
TASK [1 Create files] *******************************************
ok: [localhost] => (item=[{'key1': 'directory1'}, 'file11']) => {
    "msg": "Create files : directory1/file11"
}
ok: [localhost] => (item=[{'key1': 'directory1'}, 'file12']) => {
    "msg": "Create files : directory1/file12"
}
ok: [localhost] => (item=[{'key1': 'directory2'}, 'file21']) => {
    "msg": "Create files : directory2/file21"
}
ok: [localhost] => (item=[{'key1': 'directory2'}, 'file22']) => {
    "msg": "Create files : directory2/file22"
}

TASK [2 Create files] *************************************************************************
ok: [localhost] => (item=[{'key1': 'directory1', 'key2': ['file11', 'file12']}, 'file11']) => {
    "msg": "Create files : directory1/file11"
}
ok: [localhost] => (item=[{'key1': 'directory1', 'key2': ['file11', 'file12']}, 'file12']) => {
    "msg": "Create files : directory1/file12"
}
ok: [localhost] => (item=[{'key1': 'directory2', 'key2': ['file21', 'file22']}, 'file21']) => {
    "msg": "Create files : directory2/file21"
}
ok: [localhost] => (item=[{'key1': 'directory2', 'key2': ['file21', 'file22']}, 'file22']) => {
    "msg": "Create files : directory2/file22"
}
```

## [Until and loop](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#until-and-loop)

## Migrating from with_X to loop

### [with_list](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-list)

### [with_items](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-items)

### [with_indexed_items](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-indexed-items)

### [with_flattened](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-flattened)

### [with_together](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-together)

### [with_dict](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-dict)

### [with_sequence](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-sequence)

### [with_subelements](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-subelements)

### [with_nested/with_cartesian](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-nested-with-cartesian)

### [with_random_choice](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html#with-random-choice)
