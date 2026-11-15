# Omarchy

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

An "omakase" Linux distribution based on Arch Linux, the Hyprland tiling compositor and the Quickshell desktop toolkit, created by David Heinemeier Hansson (DHH), MIT-licensed, funded by the nonprofit Omacom Foundation. New installs use the stable channel, which follows official releases and an Omarchy Arch mirror held one month behind the latest packages. Every update takes a Snapper snapshot on Btrfs that can be booted and restored from the Limine boot loader (root filesystem only, not `/home`); direct `pacman -Syu` is stopped in favour of `omarchy update`. LUKS full-disk encryption and a firewall are on by default; the installer requires Secure Boot and TPM to be turned off. Unattended installs read their configuration from a drive labelled `cidata`. 37signals has moved its whole technical team to Omarchy. Official site: [omarchy.org](https://omarchy.org/), source: [omacom/omarchy](https://github.com/omacom/omarchy).

## Why mess.systems uses it

Candidate target OS for 2027 for `eng` workstations, personal devices and the lab; today it runs only on lab and personal devices. It is a rolling Arch base, the same risk class as CachyOS (Hold), and it is assessed only because its safeguards (delayed stable mirror, snapshot on every update, fallback kernel, unattended install) can be tested and measured. Fleet lists Omarchy as a supported host OS and ships a `pkg.tar.zst` agent package; LUKS key escrow on Omarchy is not working yet (Fleet issue #55069, milestone 4.95.0) and the support validation issue #53002 is open.

Conditions for Adopt as the `eng` standard, all of them: Fleet support validated and LUKS key escrow working in a released Fleet version; snapshot rollback rehearsed and timed; rebuild with `cidata` install, the workstation role and chezmoi at 30 minutes or less on a VM and on hardware; the role updates only through `omarchy update`; a Secure Boot and TPM decision in `endpoint`; policy for the stable channel only, time-limited passwordless sudo and a fallback kernel; six months on lab machines without an update-caused hard reset.

## Alternatives considered

Ubuntu LTS: Adopt, current base of all profiles. CachyOS: Hold, performance-focused rolling release. Fedora Atomic Desktops: Assess, Fleet agent cannot be installed on rpm-ostree systems. NixOS: Assess, desktop risk for GUI, IDE and GPU.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint), [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

Fleet 4.95 with LUKS key escrow on Omarchy; closing of Fleet issue #53002; a measured rollback and rebuild drill; any update-caused hard reset on a lab machine.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Assess | Initial entry; candidate target OS for 2027. |
