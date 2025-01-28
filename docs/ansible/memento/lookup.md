# lookup

[lookup](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_lookups.html)

## file

[ansible.builtin.file](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/file_lookup.html)

## vars

[ansible.builtin.vars](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/vars_lookup.html)

## template

[ansible.builtin.template](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/template_lookup.html)

## pipe

[ansible.builtin.pipe]([DeepSeek](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/pipe_lookup.html))

## env

[ansible.builtin.env](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/env_lookup.html)

``` yaml
msg: "Set User ACL : {{ lookup('ansible.builtin.file', './winrun/cifs_112_set_initial_acl_remove.ps1') }}"

ansible_async_dir: "{{ lookup('env', 'HOME') }}/.ansible_async_{{ tiny_prefix }}/"

    when: (lookup('env', 'HOME'))

msg: "{{ inventory_hostname }} start: {{ lookup('pipe','date') }}"

template_body: "{{ lookup('file','cf_template.json') }}"

policy: '{{ lookup("template", "s3-policy.j2") }}'

policy: "{{ lookup('template', 'sns-policy.j2') | to_json }}"

policy: "{{ lookup('template', 'console-policy.j2') }}"

now_time: '{{ lookup("pipe", "date -u +%Y-%m-%d\ %H:%M:%S") }}'

background:{{ lookup('vars',"jj2html_" ~ set_var ~ "_bgcolor_ko_over") | default('#f79256') }};

current_value: "{{ lookup('ansible.builtin.vars', check_var.name, default='NoValue') }}"

_msg2log_config_on:     "{{ lookup('ansible.builtin.vars', 'msg2log_config_' + _msg_mode + '_on') }}"

jj2html_custom_filetxt_1_input: "{{ lookup('file', '../templates/files/input_file_2.txt').splitlines() }}"

jj2html_custom_filejson_1_input: "{{ lookup('file', '../templates/files/input_file.json') | from_json }}"

jj2html_custom_filecsv_1_input: "{{ lookup('file', '../templates/files/input_file_1.csv').splitlines() }}"

```
