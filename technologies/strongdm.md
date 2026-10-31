# StrongDM

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Hold](../README.md#rings) | Product |

## What it is

Commercial access platform for databases, servers and Kubernetes with session recording. The control plane is a service hosted by the vendor and cannot be self-hosted; gateways and relays run in the customer network. Delinea completed the acquisition of StrongDM on 2026-03-05; the StrongDM pricing page now leads to Delinea Platform packages. Official site: [strongdm.com](https://www.strongdm.com/).

## Why mess.systems uses it

Not used. Users, policies and access logs would be held outside the organization boundary.

## Alternatives considered

Keycloak, OpenBao and NetBird: self-hosted, already in Adopt. Teleport: Hold.

## Where it applies

- [Capability codes: `sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

Self-hosting of the control plane becomes available: reassess; otherwise remove the entry when no question about it remains.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-31 | Hold | Initial entry. |
