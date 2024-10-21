# Mkdocs & Plugins

## Mkdocs

### Installation mkdocs

```{bash linenums="1" .copy}
pip install mkdocs

mkdocs new my-project

cd my-project

mkdocs serve
```

## Plugin

### Extention  mkdocs-material

```{ .bash .copy }
pip install mkdocs-material
pip install mkdocs-glightbox
pip install mkdocs-table-reader-plugin
```

!!! note "mkdocs-glightbox"
    https://github.com/blueswen/mkdocs-glightbox#usage

!!! nore "table-reader-plugin (Read external CSV file and more [ json,yaml,...] )"
    https://timvink.github.io/mkdocs-table-reader-plugin/#documentation-and-how-to-guides

```{ .yaml title="Configuration plugin" .copy }
plugins:
  - glightbox
  - table-reader
```

### Extention  mkdocs-material mermaid

```{ .yaml title="Configuration mkdocs.yml" .copy }
markdown_extensions:
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format
```