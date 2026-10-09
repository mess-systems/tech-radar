# HashiCorp Vault

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Hold](../README.md#rings) | Product |

## What it is

Secrets manager from HashiCorp with the same KV v2, policy, AppRole, and PKI model as OpenBao. Releases since August 2023 are under the Business Source License 1.1, not an open-source license. Official site: [developer.hashicorp.com/vault](https://developer.hashicorp.com/vault).

## Why mess.systems uses it

It is not used for new installs. The [secrets conventions](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md) stay compatible with it, so an existing Vault deployment can follow the same mounts, paths, and policies.

## Alternatives considered

[OpenBao](openbao.md) is the open-source fork with the same API and is the default choice. Hold, not removal, because the standard explicitly supports both.

## Where it applies

- [Secrets conventions](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md)
- [Secrets manager (OpenBao / Vault) in the identity conventions](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#7-secrets-manager-openbao--vault)

## Review trigger

A change in Vault's license, or a divergence between Vault and OpenBao that affects the secrets conventions.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Hold | Initial entry. |
