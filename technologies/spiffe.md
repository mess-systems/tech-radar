# SPIFFE

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Specification |

## What it is

Secure Production Identity Framework for Everyone: an open specification (CNCF graduated) for workload identity. It defines SPIFFE IDs (`spiffe://<trust-domain>/<path>`) and verifiable identity documents such as the X.509-SVID. Official site: [spiffe.io](https://spiffe.io/).

## Why mess.systems uses it

The identity conventions make it the workload identity format: the trust domain is the organisation (`spiffe://mess.systems`), and the path mirrors the capability (`/<plane>/<domain>/<capability>`).

## Alternatives considered

Per-host static credentials (AppRole secret-ids, API keys) remain the fallback for workloads without SPIFFE. Chosen because it is a vendor-neutral specification and its ID structure carries the same axes as the naming standard.

## Where it applies

- [Principles applied (rule I8)](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#1-principles-applied)
- [Identity kinds](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#2-identity-kinds)
- [SPIFFE / SPIRE](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#8-spiffe--spire)
- [Auth roles and tokens](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#6-auth-roles-and-tokens)

## Review trigger

A new major version of the SPIFFE ID or SVID specifications, or a change to the trust-domain rule in the identity conventions.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
