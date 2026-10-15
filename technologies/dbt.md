# dbt

| Category | Ring | Kind |
|---|---|---|
| [`data`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

SQL-based transformation framework: models, tests, and documentation for data in a warehouse. dbt Core is open source (Apache-2.0). Official site: [www.getdbt.com](https://www.getdbt.com/).

## Why mess.systems uses it

Runs with Elementary for data tests and observability.

The object forms name datasets and dbt marts `<plane>.<domain>.<table>`. It fits the `transform` capability.

## Alternatives considered

Hand-written SQL jobs in the orchestrator. Chosen because the standard already fixes its mart naming.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`transform`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license change of dbt Core, or a change to the dataset form.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
| 2026-10-15 | Adopt | Elementary noted as the companion for data observability. |
