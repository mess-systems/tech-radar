# Nix and NixOS

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Nix is a package manager that builds packages and environments from declarative descriptions; flakes pin inputs in a lock file. NixOS is a Linux distribution built entirely with Nix; stable releases come out in May and November and each is supported for about seven months (26.05 until 2026-12-31). Images for Proxmox VE and other platforms are built with `nixos-rebuild build-image`. Official site: [nixos.org](https://nixos.org/).

## Why mess.systems uses it

Nix on top of the existing OS gives each project a reproducible environment (`flake.nix`, `flake.lock`, direnv) that can be removed without touching the system. NixOS is used for disposable, isolated VMs on Proxmox VE built from the same flake. NixOS as the desktop OS is out of scope: short release support, no disk encryption escrow in Fleet, and a high risk for GUI, IDE and GPU setups. A prototype with measurements is in progress.

## Alternatives considered

Dev Containers: Trial, the default where a remote IDE or CI needs a container. Devbox: Nix-based environments through its own file; flakes and direnv cover the same need without another tool. Fleet does not collect Nix packages installed on a distribution other than NixOS.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

The prototype has measurements against Dev Containers: promote Nix on top of the OS to Trial or drop it.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Assess | Initial entry. |
