# ClickHouse

| Category | Ring | Kind |
|---|---|---|
| [`data`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source column-oriented database (Apache-2.0) for analytical queries. Official site: [clickhouse.com](https://clickhouse.com/).

## Why mess.systems uses it

The standard defines its schemas (same form as Postgres databases) and its warehouse roles (`corp_data_warehouse_rw`, `_ro`), with the `default` user disabled.

## Alternatives considered

Other analytical databases. Chosen because the standard already fixes its schema and role naming.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Database roles](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#11-database-roles)

## Review trigger

A change to the database forms or role rules.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
