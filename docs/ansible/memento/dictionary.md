# Dictionary

## Append

[ansible.builtin.combine](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/combine_filter.html)

``` yaml title="Append" linenums="1" hl_lines="11-16"
--8<-- "docs/playbooks/dict1.yml"
```

``` text title="" hl_lines="3-5"
TASK [Display Append] *************************
ok: [localhost] => {
    "dict1": {
        "key1": "value",
        "key2": "MyValue"
    }
}
```

## Recursive

``` yaml title="Append" linenums="1" hl_lines="13-18"
--8<-- "docs/playbooks/dict2.yml"
```

``` text title="" hl_lines="3-8"
TASK [Display Recursive] ***********************
ok: [localhost] => {
    "dict2": {
        "date_of_day": {
            "jour": "monday",
            "seq": "11"
        }
    }
}
```

## {++List++}

[ansible.builtin.dict2items](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/dict2items_filter.html)

[ansible.builtin.items2dict](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/items2dict_filter.html#ansible-collections-ansible-builtin-items2dict-filter)

## {++Longueur++}

> (Nombre de keys) d'un dictionnaire

``` yaml title=""
{{ dict.keys() | list | length | int }}
```

## {++Extraction (selectattr)++}

[selectattr](https://www.middlewareinventory.com/blog/ansible-selectattr-example/)

``` json
"success_nodes": [
    {
        "identifier": "47301d67-9e86-4ef1-bba3-b4511d3f72ac",
                  "type": "workflow_job_template_node",
                  "workflow_job_template": {
                      "name": "I_WFL_DEPLOY_double",
                    "organization": {
                        "name": "ATOM-Stockage",
                      "type": "organization"
                    },
                    "type": "workflow_job_template"
                  }
                },
                {
                    "identifier": "d25ed6f2-7eef-4ca1-80c6-b45ae87e99e0",
                  "type": "workflow_job_template_node",
                  "workflow_job_template": {
                      "name": "I_WFL_DEPLOY_double",
                    "organization": {
                      "name": "ATOM-Stockage",
                      "type": "organization"
                    },
                    "type": "workflow_job_template"
                  }
                }
              ]

```

## Extraction (selectattr / attribute)

```yaml
ListId : "{{ success_nodes | default([], true) | selectattr('identifier', 'defined') | map(attribute='identifier')) | list }}"
```

```text
ListId: [ "47301d67-9e86-4ef1-bba3-b4511d3f72ac", "d25ed6f2-7eef-4ca1-80c6-b45ae87e99e0" ]
 ou si vide
 ListId: []
```

## Combine
