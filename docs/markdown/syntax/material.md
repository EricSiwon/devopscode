# Syntax Material

> THEME Material pour MKDOCS

## ==Annotations==

Visiter la documentation officielle: [Annotations :fontawesome-solid-info:](https://squidfunk.github.io/mkdocs-material/reference/annotations/){ .md-button }

!!! tips
    Il est aussi possible d'imbriquer les annotations.

!!! note ""
    Je suis un texte avec annotation, (1) (Clique sur le + ) Bla bla bla....
    { .annotate }

    1.  :man_raising_hand: Je suis l'annotation

### Syntaxe

```text title="Text avec annotation"
    Je suis un texte avec annotation, (1) (Clique sur le + ) Bla bla bla....
    { .annotate }

    1.  :man_raising_hand: Je suis l'annotation
```

## ==Icons==

Les icons se trouve dans le repertoire : [Icons](https://github.com/squidfunk/mkdocs-material/tree/master/material/templates/.icons)

### Utilisation

!!! tip  ""
    Material Design --> :material-information-slab-box-outline:
    ``` title=""
    :material-information-slab-box-outline:  
    ```
    Octicons --> :octicons-rocket-24:  
    ``` title=""
    :octicons-rocket-24:
    ```
    FontAwesome --> :fontawesome-solid-info:  
    ``` title=""
    :fontawesome-solid-info:
    ```
    Simple Icons --> :simple-flux:  
    ``` title=""
    :simple-flux:
    ```

## ==Avertissements==

Visiter la documentation officielle: [Avertissements :octicons-rocket-16:](https://squidfunk.github.io/mkdocs-material/reference/admonitions/){ .md-button }

### Syntaxe

```markdown
!!! note
    Je suis une note ..... bla bla  
    bla bla
```

!!! note
    Je suis une note ..... bla bla  
    bla bla

```markdown
!!! note ""
    Je suis une note sans titre ..... bla bla  
    bla bla
```

!!! note ""
    Je suis une note sans titre ..... bla bla  
    bla bla

```markdown
!!! note "mon tire"
    Je suis une note avec titre ..... bla bla  
    bla bla
```
!!! note "mon tire"
    Je suis une note avec titre ..... bla bla  
    bla bla

### Type supportés

!!! note

```markdown
!!! note
```

!!! abstract

```markdown

!!! abstract
```

!!! info

```markdown
!!! info
```

!!! tip

```markdown
!!! tip
```

!!! success

```markdown
!!! success
```

!!! question

```markdown
!!! question
```

!!! warning

```markdown
!!! warning
```

!!! failure

```markdown
!!! failure
```

!!! danger

```markdown
!!! danger
```

!!! bug

```markdown
!!! bug
```

!!! exemple

```markdown
!!! exemple
```

!!! quote

```markdown
!!! quote
```