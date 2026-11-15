# Fleet

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source device management built on osquery (MIT core). Official site: [fleetdm.com](https://fleetdm.com/).

Disk encryption enforcement and key escrow are Fleet Premium features ($7 per host per month at the time of writing); on Linux they cover Ubuntu, Kubuntu and Fedora, the disk must be encrypted during OS setup and the end user enters the disk password for escrow. Linux settings are enforced with scripts. The Fleet agent cannot be installed on rpm-ostree systems (Fedora Atomic Desktops, Bluefin, Aurora, Bazzite; Fleet issue #48694). Nix packages are collected on NixOS only. Omarchy is listed as a supported host OS (`pkg.tar.zst` package); LUKS key escrow on Omarchy is tracked in Fleet issue #55069 (milestone 4.95.0) and support validation in #53002.

## Why mess.systems uses it

Device inventory and queries across operating systems.

## Alternatives considered

Other MDM tools. Trial: limited scope.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint), [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

After it has carried the capability in a limited scope: promote to Adopt or move to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Trial | Initial entry. |
| 2026-11-15 | Trial | Linux limits recorded; device-workstation-stages blueprint. |
