# DataGrip

| Category | Ring | Kind |
|---|---|---|
| [`data`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Commercial desktop database IDE from JetBrains. Since 2025-10-01 it is free for non-commercial use by individuals; organizations need a paid license. The third-party [datagrip-vault-plugin](https://github.com/premium-minds/datagrip-vault-plugin) (Apache-2.0) reads Vault dynamic database credentials; it does not perform the Vault login. Official site: [jetbrains.com/datagrip](https://www.jetbrains.com/datagrip/).

## Why mess.systems uses it

Evaluated as a client that requests a temporary user from OpenBao per connection instead of a pasted password.

## Alternatives considered

DBeaver Community: free, Adopt, no secret-manager integration.

## Where it applies

- [Capability codes: `sql`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sql`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`data-sql-access`](https://github.com/mess-systems/blueprints/tree/main/data-sql-access) |

## Review trigger

The plugin is tested against the OpenBao database engine and the license cost is accepted: move to Trial; otherwise remove the entry.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-31 | Assess | Initial entry. |
