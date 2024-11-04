# Syntax Material

> THEME Material pour MKDOCS

## ==Annotations==

### Simple :material-plus-circle:

Visiter la documentation officielle  : [Annotations](https://squidfunk.github.io/mkdocs-material/reference/annotations/){ .md-button }

!!! tips
    Il est aussi possible d'imbriquer les annotations.

!!! note ""
    Je suis un texte avec une annotation, (1) (Clique sur le + ) Bla bla bla....
    { .annotate }

    1.  :man_raising_hand: Je suis l'annotation

```text title="Text avec annotation"
    Je suis un texte avec une annotation, (1) (Clique sur le + ) Bla bla bla....
    { .annotate }

    1.  :man_raising_hand: Je suis l'annotation
```

### Dossier

=== "Dossier 1"

    Je suis un texte avec une annotation, (1) Dans le dossier 1.
    { .annotate }

    1.  :man_raising_hand: Je suis l'annotation 1

=== "Dossier 2"

    Je suis un texte avec une annotation, (1) Dans le dossier 2.
    { .annotate }

    1.  :woman_raising_hand: Je suis l'annotation 2

```markdown title="Dossiers"
=== "Dossier 1"

    Je suis un texte avec une annotation, (1) Dans le dossier 1.
    { .annotate }

    1.  :man_raising_hand: Je suis l'annotation 1

=== "Dossier 2"

    Je suis un texte avec une annotation, (1) Dans le dossier 2.
    { .annotate }

    1.  :woman_raising_hand: Je suis l'annotation 2
```

## ==Icons==

Les icons se trouve dans le repertoire : [Icons](https://github.com/squidfunk/mkdocs-material/tree/master/material/templates/.icons){ .md-button }

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

Visiter la documentation officielle: [Avertissements](https://squidfunk.github.io/mkdocs-material/reference/admonitions/){ .md-button }

!!! note
    Je suis une note ..... bla bla  
    bla bla

```markdown

!!! note
    Je suis une note ..... bla bla  
    bla bla
```

[=0%]{: .thin}

!!! note ""
    Je suis une note sans titre ..... bla bla  
    bla bla

```markdown
!!! note ""
    Je suis une note sans titre ..... bla bla  
    bla bla
```

[=0%]{: .thin}

!!! note "mon titre"
    Je suis une note avec titre ..... bla bla  
    bla bla

```markdown
!!! note "mon titre"
    Je suis une note avec titre ..... bla bla  
    bla bla
```

[=0%]{: .thin}

??? note "Message non deployé"
    Je suis une note non deployée ..... bla bla  bla bla 
    bla bla

```markdown
??? note "Message non deployé"
    Je suis une note non deployée ..... bla bla  bla bla 
    bla bla
```

[=0%]{: .thin}

???+ note "Message deployé"
    Je suis une note deployée ..... bla bla  bla bla 
    bla bla

```markdown
???+ note "Message deployé"
    Je suis une note deployée ..... bla bla  bla bla 
    bla bla
```

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

## ==Boutons==

Visiter la documentation officielle: [Boutons](https://squidfunk.github.io/mkdocs-material/reference/buttons/){ .md-button }

[Simple](#){ .md-button }

```markdown title=""
[Simple](#){ .md-button }
```

[Simple Avec Icon :fontawesome-solid-paper-plane:](#){ .md-button }


```markdown title=""
[Simple Avec Icon :fontawesome-solid-paper-plane:](#){ .md-button }
```

[Inverse](#){ .md-button .md-button--primary }

```markdown title=""
[Inverse](#){ .md-button .md-button--primary }
```

[Inverse Avec Icon :fontawesome-solid-paper-plane:](#){ .md-button .md-button--primary }

```markdown title=""
[Inverse Avec Icon :fontawesome-solid-paper-plane:](#){ .md-button .md-button--primary }
```

## ==Bloc de codes==

Visiter la documentation officielle: [Bloc de codes](https://squidfunk.github.io/mkdocs-material/reference/code-blocks/){ .md-button }

## ==Content tabss==

Visiter la documentation officielle: [Content tabs](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/){ .md-button }

## ==Data tables==

Visiter la documentation officielle: [Data tables](https://squidfunk.github.io/mkdocs-material/reference/data-tables/){ .md-button }

## ==Diagrams==

Visiter la documentation officielle: [Diagrams](https://squidfunk.github.io/mkdocs-material/reference/diagrams/){ .md-button }

## ==Footnotes==

Visiter la documentation officielle: [Footnotes](https://squidfunk.github.io/mkdocs-material/reference/footnotes/){ .md-button }

## ==Formatting==

Visiter la documentation officielle: [Formatting](https://squidfunk.github.io/mkdocs-material/reference/formatting/){ .md-button }

## ==Grids==

Visiter la documentation officielle: [Grids](https://squidfunk.github.io/mkdocs-material/reference/grids/){ .md-button }

## ==Images==

Visiter la documentation officielle: [Images](https://squidfunk.github.io/mkdocs-material/reference/images/){ .md-button }

## ==Lists==

Visiter la documentation officielle: [Lists](https://squidfunk.github.io/mkdocs-material/reference/lists/){ .md-button }

## ==Tooltips==

Visiter la documentation officielle: [Tooltips](https://squidfunk.github.io/mkdocs-material/reference/tooltips/){ .md-button }
