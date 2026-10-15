# Proxmox VE

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source virtualisation platform (AGPL-3.0) for KVM VMs and LXC containers. Official site: [proxmox.com/en/products/proxmox-virtual-environment/overview](https://www.proxmox.com/en/products/proxmox-virtual-environment/overview).

## Why mess.systems uses it

Carries the `compute` capability on own hardware.

## Alternatives considered

VMware, plain KVM. Chosen for an open license and built-in clustering and backup.

## Where it applies

- [Capability codes: `compute`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`compute`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |
