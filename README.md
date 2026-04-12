# archetect-catalog

The top-level Archetect master catalog. This is the default catalog that
`archetect` points at when you run `archetect render` (via `default`
action) with no explicit source.

## Structure

```
common/
  gitignore          → dot-gitignore-archetype
  starters/
    archetype-starter → archetype-starter-archetype
```

More categories and entries will be added as the ecosystem matures
(per-language ecosystems get their own master catalogs and are
referenced here as nested groups).

## Usage

```sh
# Interactive menu navigation
archetect render https://github.com/archetect/archetect-catalog.git

# Direct path navigation
archetect render https://github.com/archetect/archetect-catalog.git common/gitignore
```

## Versioning

This repository uses the
[`archetect-actions/repository-release`](https://github.com/archetect-actions/repository-release)
action. Major versions are tracked via `.version-line`. Once
[version-aware source resolution](https://github.com/archetect/archetect-3/blob/main/docs/specs/version-aware-source-resolution.md)
lands, clients will automatically resolve to the highest matching
major tag.
