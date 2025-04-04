# Array

## Append

> list_save: "{{ list_save | default([]) + [ save ] }}"


## Tableau de Dictionnaire ( Objet Json)

```yaml
"dict_switch",
        {
            "switch_address": "10.xxx.197.xxx",
            "switch_login": "xxxxx",
            "switch_name": "SANxxxxxxx101",
            "switch_password": "xxxxx"
        }
```

Array_switchs: "{{ Array_switchs | default([]) + [dict_switch] }}"
