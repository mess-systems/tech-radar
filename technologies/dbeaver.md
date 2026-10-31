# DBeaver Community

| Category | Ring | Kind |
|---|---|---|
| [`data`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Desktop database client for PostgreSQL and other JDBC databases (Apache-2.0). The paid editions (Lite, Enterprise, Ultimate) add secret management, including reading connection settings from HashiCorp Vault. Official site: [dbeaver.io](https://dbeaver.io/).

## Why mess.systems uses it

Client for people who work with PostgreSQL: TLS with `sslmode=verify-full`, connection by service name. People paste the user name and password issued by OpenBao; the Community edition has no secret-manager integration.

## Alternatives considered

DataGrip: commercial, with a third-party plugin for Vault dynamic credentials. pgAdmin and `psql`: allowed, no recorded objection. DBeaver paid editions: their Vault integration reads stored secrets; reading dynamic credentials of the OpenBao database engine is not confirmed.

## Where it applies

- [Capability codes: `sql`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sql`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`data-sql-access`](https://github.com/mess-systems/blueprints/tree/main/data-sql-access) |

## Review trigger

The Community edition gains or loses PostgreSQL TLS settings, or a paid edition is confirmed to read dynamic credentials from OpenBao.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-31 | Adopt | Initial entry. |
