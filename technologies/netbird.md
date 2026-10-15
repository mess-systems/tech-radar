# NetBird

| Category | Ring | Kind |
|---|---|---|
| [`net`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source WireGuard-based overlay network with SSO login, access policies and a self-hosted control plane. Official site: [netbird.io](https://netbird.io/).

## Why mess.systems uses it

Carries the `mesh` capability for private access between sites and devices; replaces Headscale.

## Alternatives considered

Headscale, Tailscale, plain WireGuard. Chosen for a self-hosted control plane with SSO and policies built in.

## Where it applies

- [Capability codes: `mesh`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`mesh`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |
