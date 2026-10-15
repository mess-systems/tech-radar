# PostgreSQL

| Category | Ring | Kind |
|---|---|---|
| [`data`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source relational database (PostgreSQL License). Official site: [www.postgresql.org](https://www.postgresql.org/).

## Why mess.systems uses it

Runs with the pgvector extension for embeddings and the CloudNativePG operator on Kubernetes.

The standard defines dedicated Postgres forms: databases and schemas `<plane>_<domain>_<capability>_<env>` and roles `svc_<plane>_<domain>_<product>`. It provides the `sql` capability in the worked example.

## Alternatives considered

Other relational databases. Chosen because the standard already fixes its database, schema, and role naming.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Database roles](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#11-database-roles)
- [Services: intake and encoding](https://github.com/mess-systems/naming-standard/blob/main/02-worked-example.md#3-services-intake-and-encoding)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| not mapped yet | none yet |

## Review trigger

A change to the database forms or role rules.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
| 2026-10-15 | Adopt | pgvector and CloudNativePG noted as the standard setup. |
