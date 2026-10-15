# SPIRE

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

The SPIFFE Runtime Environment: the reference implementation of SPIFFE (Apache-2.0, CNCF graduated). It attests nodes and workloads and issues them SVIDs. Official site: [spiffe.io/docs/latest/spire-about](https://spiffe.io/docs/latest/spire-about/).

## Why mess.systems uses it

The identity conventions place workloads and nodes in SPIRE, and the secrets conventions list `auth/jwt-spire` as the target auth method that replaces AppRole for workloads.

## Alternatives considered

Other SPIFFE-compatible issuers or a service mesh's built-in identity. Trial because the standard marks SPIRE-based auth as the target, with AppRole still in place.

## Where it applies

- [SPIFFE / SPIRE](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#8-spiffe--spire)
- [Identity kinds](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#2-identity-kinds)
- [Mounts (`auth/jwt-spire`, target)](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#2-mounts)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`spiffe`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |

## Review trigger

When `jwt-spire` replaces AppRole for a first group of workloads: promote to Adopt or move to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
