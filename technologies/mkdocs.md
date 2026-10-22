# MkDocs

| Category | Ring | Kind |
|---|---|---|
| [`gov`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Static site generator for documentation written in Markdown (BSD-2-Clause), used with the Material for MkDocs theme (MIT). Official site: [mkdocs.org](https://www.mkdocs.org/).

## Why mess.systems uses it

Builds a readable site from Markdown kept in git: requirements, their register, ADRs and process documents of the `archrepo` and `adr` capabilities. Used by the [requirements](https://github.com/mess-systems/requirements) template.

## Alternatives considered

Docusaurus, Sphinx, Hugo. MkDocs builds from plain Markdown with one YAML file and a strict mode that fails on broken links.

## Where it applies

- [Capability codes: `archrepo`, `adr`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`adr`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains), [`archrepo`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change of MkDocs or its Material theme, including the move to MkDocs 2.0.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-22 | Trial | Initial entry, used by the requirements template. |
