# Calcul

## Addition

> Convertion implicite avec la commande **`int`**

``` yaml title="Calcul" linenums="1" hl_lines="10"
--8<-- "docs/playbooks/calcul.yml"
```

``` text title="" hl_lines="3"
TASK [Display] ***************************
ok: [localhost] => {
    "new_number": "2"
}
```

## Exemples

```yaml
--8<-- "docs/playbooks/calcul_full.yml"
```

``` text title=""
TASK [Ansible addition 7] ***************************************
    "msg": "addition7"
}

TASK [Ansible arithmetic substraction 1] ***************************************
ok: [localhost] => {
    "msg": "substraction 1"
}

TASK [Multiplication 12] ***************************************
ok: [localhost] => {
    "msg": "multiplication 12"
}

TASK [Ansible Modulo operation - find remainder 3] ***************************************
ok: [localhost] => {
    "msg": "Modulo operation 3"
}

TASK [Ansible floating division 1.33333333333] ***************************************
ok: [localhost] => {
    "msg": "floating division 1.3333333333333333"
}

TASK [Ansible arithmetic cube root 3.0] ***************************************
ok: [localhost] => {
    "msg": "cube root 3.0"
}

TASK [Ansible arithmetic cube root 3.0] ***************************************
ok: [localhost] => {
    "msg": "square root 4.0"
}

TASK [Ansible arithmetic power of a number 27] ***************************************
ok: [localhost] => {
    "msg": "power 27.0"
}

TASK [Absolute value of a number 16.7] ***************************************
ok: [localhost] => {
    "msg": "Absolute value 16.7"
}

TASK [Int conversion of a float value -19] ***************************************
ok: [localhost] => {
    "msg": "Int conversion of float value -19"
}

TASK [Absolute value of a number 43] ***************************************
ok: [localhost] => {
    "msg": "Multiple filters for getting absolute integer value of negative number 43"
}

TASK [39.7 Round 40] ***************************************
ok: [localhost] => {
    "msg": "Common Ansible round of a number 40.0"
}

TASK [39.4 Round 39] ***************************************
ok: [localhost] => {
    "msg": "Common Rounding of a number 39.0"
}

TASK [39.5 Round 40] ***************************************
ok: [localhost] => {
    "msg": "Common Rounding of a number 40.0"
}

TASK [39.779 'common' Round 40] ***************************************
ok: [localhost] => {
    "msg": "Another way of Common Rounding of a number40.0"
}

TASK [39.779 (0, 'floor')  Round 39.0 - - still a float. Use integer filter to convert to integer] ***************************************
ok: [localhost] => {
    "msg": "floor Rounding of a number 39.0"
}

TASK [39.779 (1, 'floor') Round 39.7] ***************************************
ok: [localhost] => {
    "msg": "Ansible floor Rounding of a number 39.7"
}

TASK [39.779 (2,' floor') Round 39.77] ***************************************
ok: [localhost] => {
    "msg": "floor Rounding of a number 39.77"
}

TASK [39.779 (0, 'floor') Round 40.0 - still a float. Use integer filter to convert to integer] ***************************************
ok: [localhost] => {
    "msg": "Ceiling Rounding of a number 39.0"
}

TASK [39.779 (1, 'floor') Round 39.8] ***************************************
ok: [localhost] => {
    "msg": "Ceiling Rounding of a number 39.7"
}

TASK [39.779 (2, 'ceil') Round 39.78] ***************************************
ok: [localhost] => {
    "msg": "Ceiling Rounding of a number 39.78"
}

TASK [Log 4] ***************************************
ok: [localhost] => {
    "msg": "log of a number 2.0"
}
```
