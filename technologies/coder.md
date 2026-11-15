# Coder

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Self-hosted platform for cloud development environments and AI coding agents: workspaces are defined in Terraform, connected through a WireGuard tunnel and stopped automatically when idle (AGPL-3.0, enterprise features under a separate license). Official site: [coder.com](https://coder.com/docs).

## Why mess.systems uses it

Chosen for remote development environments at the target stage: heavy and risky work and AI agents run on company servers, the laptop becomes a thin client. The ring stays Assess until a pilot.

## Alternatives considered

Kasm Workspaces: Adopt for browser-based virtual desktops (`vdi`), stays for that use; Coder is preferred for development environments defined in code. Disposable NixOS VMs on Proxmox VE: for the simple and medium stages.

## Where it applies

- [Capability codes: `vdi`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`vdi`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

Developer onboarding longer than a working day or a permanent need for isolated agent environments: run a pilot.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Assess | Initial entry. |
