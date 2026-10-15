# OpenBao

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source secrets manager: key/value secrets, dynamic credentials, PKI, and encryption as a service. It is a community fork of HashiCorp Vault, licensed under MPL-2.0, and keeps Vault's API and policy model. Official site: [openbao.org](https://openbao.org/).

## Why mess.systems uses it

The [secrets conventions](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md) are written for its KV v2 engine: mounts per plane, the path grammar, policies, and auth roles all use OpenBao concepts. It provides the `secrets` capability (`secrets.iam.shared`).

## Alternatives considered

HashiCorp Vault: same API and policy model, but no longer under an open-source license; removed from the radar. Cloud-provider secret stores tie secrets to one provider. Chosen because the standard's mount, path, and policy rules map onto it one to one under an open-source license.

## Where it applies

- [Mounts](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#2-mounts)
- [Path grammar](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#3-path-grammar)
- [Policies](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#5-policies)
- [Auth roles and tokens](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#6-auth-roles-and-tokens)
- [Secrets manager (OpenBao / Vault) in the identity conventions](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#7-secrets-manager-openbao--vault)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`secrets`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or governance change upstream, loss of API compatibility with the policy and KV v2 model the standard relies on, or a change to the secrets conventions.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
| 2026-10-15 | Adopt | HashiCorp Vault entry removed from the radar. |
