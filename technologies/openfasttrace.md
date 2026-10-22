# OpenFastTrace

| Category | Ring | Kind |
|---|---|---|
| [`gov`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Requirements tracing tool (GPL-3.0) that links requirement markers in Markdown to tags in code and tests and reports what is not covered. Runs as a single Java jar. Official site: [github.com/itsallcode/openfasttrace](https://github.com/itsallcode/openfasttrace).

## Why mess.systems uses it

Traces requirements kept as code in the `archrepo` capability to their implementation and tests, and runs the trace in CI. Used by the [requirements](https://github.com/mess-systems/requirements) template.

## Alternatives considered

StrictDoc, Sphinx-needs, Doorstop. OpenFastTrace keeps markers in plain comments of any language and needs no database or server.

## Where it applies

- [Capability codes: `archrepo`, `ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`archrepo`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains), [`ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a need for ReqIF exchange that the tool cannot cover.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-22 | Trial | Initial entry, used by the requirements template. |
