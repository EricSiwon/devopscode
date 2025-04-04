
# Material Theme TEST !!!



## Text Formating




## ProgressBar

```markdown
[=55% "55%"]
```

[=55% "55%"]

```markdown
[=20% "20%"]{: .candystripe}
```

[=20% "20%"]{: .candystripe}

```markdown
[=55% "55%"]{: .candystripe}
```

[=55% "55%"]{: .candystripe}

```markdown
[=85% "85%"]{: .candystripe}
```

[=85% "85%"]{: .candystripe}

```markdown
[=100% "100%"]{: .candystripe .candystripe-animate}
```

[=100% "100%"]{: .candystripe .candystripe-animate}

```markdown
[=25%]{: .thin .candystripe}
```

[=25%]{: .thin .candystripe}

```markdown
[=45%]{: .thin}
```

[=45%]{: .thin}

## Touche clavier

```markdown
++ctrl+alt+delete++
```

++ctrl+alt+delete++

```markdown
++ctrl++
```

++ctrl++

```markdown
++shift++
```

++shift++

----

=== "Tab 1"
    Markdown **content**.

    Multiple paragraphs.

=== "Tab 2"
    More Markdown **content**.

    - list item a
    - list item b

===! "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```
----

!!! example ""

    === "Unordered List"

        ``` markdown
        * Sed sagittis eleifend rutrum
        * Donec vitae suscipit est
        * Nulla tempor lobortis orci
        ```

    === "Ordered List"

        ``` markdown
        1. Sed sagittis eleifend rutrum
        2. Donec vitae suscipit est
        3. Nulla tempor lobortis orci
        ```
----


!!! note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

??? note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

----

`Lorem ipsum dolor sit amet`

:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

`Cras arcu libero`

:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex. Proin
    ut eros sed sapien ullamcorper consequat. Nunc ligula ante.

    Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    Nam vulputate tincidunt fringilla.
    Nullam dignissim ultrices urna non auctor.

-----

> Code Sniper ...

``` title="Code To Be Sniped"
--8<-- "docs/codesniped.txt"
```

!!! note
    "--8<-- "docs/codesniped.txt""

----

:smile: :heart: :thumbsup:

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |

```text

td,th{
    border: 1px solid;
  }

th, td {
  border-bottom: 1px solid #ddd;
}

  .md-typeset__table{}

  tr:nth-child(even) {background-color: #f2f2f2;}

  tr:hover {background-color: coral;}

p {
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}


.md-typeset table:not([class]) {
  background-color: var(--md-default-bg-color);
  border: .05rem solid var(--md-typeset-table-color);
  border-radius: .1rem;
  display: inline-block;
  font-size: .64rem;
  max-width: 100%;
  overflow: auto;
  touch-action: auto;
}

.md-typeset table:not([class]) td {
  border-top: .05rem solid var(--md-typeset-table-color);
  padding: .9375em 1.25em;
  vertical-align: top;
}

  ```

### Decoration Link Actif

```
  .md-nav__link--active{
    border: solid;
    border-width: 1px 1px 1px 1px;
    border-radius: 5px;
    background-color: #54a2e66b;
  }
```
