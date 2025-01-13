# File

## stat.exists

``` yaml title="Check if path exists"
- name:
  hosts: localhost
  gather_facts: False

  tasks:
    - name: "Check if path exists"
      stat:
        path: "/path/to/something"
      register: result

    - name: "Do something if path exists"
      command: ...
      when: result.stat.exists

    - name: "Do something else if path doesn't exist"
      command: ...
      when: not result.stat.exists
```

## stat.isreg

```yaml title="Check if is a regular file"
- name: Check if is a regular file
  hosts: localhost
  gather_facts: False

  tasks:
   - name: "Check if file exists"
      stat:
        path: "/path/to/something"
      register: result

    - name: "Do something if file exists"
      command: ...
      when: (result.stat.isreg is defined) and (result.stat.isreg)

    - name: "Do something else if file doesn't exist"
      command: ...
      when: (result.stat.isreg is undefined) or (not result.stat.isreg)
```

## stat.isdir

```yaml title="Check if directory exists"
- name: Check if directory exists
  hosts: localhost
  gather_facts: False

  tasks:
  - name: "Check if directory exists"
    stat:
      path: "/path/to/something"
    register: result

  - name: "Do something if directory exists"
    command: ...
    when: (result.stat.isdir is defined) and (result.stat.isdir)

  - name: "Do something else if directory doesn't exist"
    command: ...
    when: (result.stat.isdir is undefined) or (not result.stat.isdir)
```

## stat.islnk

```yaml title="Check if symlink exists"
- name: "Check if symlink exists"
  hosts: localhost
  gather_facts: False

  tasks:
  - name: "Check if symlink exists"
    stat:
      path: "/path/to/something"
    register: result

  - name: "Do something if symlink exists"
    command: ...
    when: (result.stat.islnk is defined) and (result.stat.islnk)

  - name: "Do something else if symlink doesn't exist"
    command: ...
    when: (result.stat.islnk is undefined) or (not result.stat.islnk)
```

## Lecture CSV file

``` yaml
- name: Read CSV Zonning Configuration
    read_csv:
      path: "{{ FileCsv }}"
      fieldnames: alias_host,wwn_host,alias_array,wwn_array,cfgactv,vfid,switch_ip,zonename
      delimiter: ','
    register: CfgConfigZonning
```

-----

## Write Dictionary in JSON file

```yaml
- name: Write VRA dictionnary in json file
  copy:
    content: "{{ dictionnary | to_nice_json(indent=2)}}"
    dest: "filename.json"
```

## Read JSON file in Dictionary

```yaml
- set_fact:
     dict_config: "{{ lookup('file','filename.json') | from_json }}"

	 input: "{{ lookup('file','output.json') | from_json }}
```

## Liste des fichiers / list files

```yaml
- hosts: localhost
  gather_facts: False

  tasks:
    - find:
        paths: "~/prod-ansible/brocade/Files/PRD_BucketBrocade/refs/"
        patterns: "SRE-{{switch}}-{{scope}}*"
      register: find_stdout

    - debug:
        msg:
          - "{{ find_stdout.Files }}"

    - debug:
        msg: "{{ item }}"
      with_items: "{{ find_stdout.Files | map(attribute='path') | sort | list }}"

    - name: Build list Files
      set_fact:
        Files: "{{ Files | default([])+ [item.path] }}"
      with_items: "{{ find_stdout.Files }}"

    - debug: var=Files

    - name: Build list sorted Files
      set_fact:
        Files_sorted: "{{ Files_sorted | default([])+ [item] }}"
      with_items: "{{ find_stdout.Files | map(attribute='path') | sort | list }}"

    - debug: var=Files_sorted

    - debug:
        msg:
          - "Most recent"
          - "{{ Files_sorted[-1] }}"
          - "Other method"
          - "{{ find_stdout.Files | map(attribute='path') | sort | last }}"
```
