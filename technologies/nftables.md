# nftables

| Category | Ring | Kind |
|---|---|---|
| [`net`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Linux packet-filtering framework of the netfilter project that replaces iptables, ip6tables, arptables and ebtables, with the `nft` command-line tool (GPL). In the kernel since 3.13. Official site: [netfilter.org](https://www.netfilter.org/projects/nftables/).

## Why mess.systems uses it

Host firewall on Linux servers: one table filters the LAN and the direct WireGuard port, managed by an Ansible role. The NetBird client also uses nftables for its own table, so the host table leaves the mesh interface to the mesh policies.

## Alternatives considered

iptables: legacy interface, translated to nftables on current distributions. firewalld and ufw: front ends that hide the rule set and conflict with tables written by other programs.

## Where it applies

- [Capability codes: `firewall`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- Example: [`net-mesh/examples/nftables-hostfw.example.nft`](https://github.com/mess-systems/blueprints/tree/main/net-mesh/examples)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`firewall`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`net-mesh`](https://github.com/mess-systems/blueprints/tree/main/net-mesh), [`data-sql-access`](https://github.com/mess-systems/blueprints/tree/main/data-sql-access) |

## Review trigger

A NetBird client release changes how it inserts rules into other tables, or a host distribution stops shipping nftables.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-31 | Adopt | Initial entry. |
