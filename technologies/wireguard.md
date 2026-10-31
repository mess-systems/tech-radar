# WireGuard

| Category | Ring | Kind |
|---|---|---|
| [`net`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Layer 3 VPN protocol and implementation based on Noise-protocol key exchange, with one UDP port per peer. The Linux implementation is part of the kernel since 5.6 (GPL-2.0); implementations exist for other platforms. Official site: [wireguard.com](https://www.wireguard.com/).

## Why mess.systems uses it

Encrypted transport between mesh peers. mess.systems does not configure it directly: NetBird creates and manages the WireGuard interfaces and keys, and the direct WireGuard port is the only mesh port the host firewall must allow from the LAN.

## Alternatives considered

IPsec and OpenVPN: more configuration and a larger code base. Plain WireGuard without a control plane has no SSO, groups or policies; NetBird adds them.

## Where it applies

- [Capability codes: `mesh`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`mesh`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`net-mesh`](https://github.com/mess-systems/blueprints/tree/main/net-mesh), [`data-sql-access`](https://github.com/mess-systems/blueprints/tree/main/data-sql-access) |

## Review trigger

A NetBird release changes the transport, or the kernel module is unavailable on a supported platform.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-31 | Adopt | Initial entry. |
