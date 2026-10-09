# Headscale

| Category | Ring | Kind |
|---|---|---|
| [`net`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source, self-hosted implementation of the Tailscale control server (BSD-3-Clause). It coordinates a WireGuard-based mesh VPN. Official site: [headscale.net](https://headscale.net/).

## Why mess.systems uses it

It is the example product for the `mesh` capability in the worked encodings (`mesh.net.shared`), including the documented exception for a control plane reachable before the mesh is up. The standard's mesh rules are product-agnostic.

## Alternatives considered

Other mesh VPN control planes. Trial because the standard names it as an illustration.

## Where it applies

- [Worked encodings](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#11-worked-encodings)
- [Grammar B: public (mesh coordinator exception)](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#32-grammar-b-public)
- [Mesh VPN groups](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#4-mesh-vpn-groups)

## Review trigger

After it has carried the `mesh` capability in a limited scope: promote to Adopt or move to Hold. Earlier on a maintenance or compatibility change upstream.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
