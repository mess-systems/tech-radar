# Ubuntu LTS

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Long-term support releases of Ubuntu, published every two years with five years of standard security maintenance; Ubuntu Pro extends security maintenance to ten years, with a Legacy add-on to fifteen. Ubuntu 26.04 LTS (April 2026) makes TPM-backed full-disk encryption generally available on Ubuntu Desktop. Official site: [ubuntu.com](https://ubuntu.com/about/release-cycle).

## Why mess.systems uses it

Base operating system for Linux workstations of all endpoint profiles. Longest support cycle among the evaluated desktop distributions, unattended installation with autoinstall, and one of the Linux distributions where Fleet can enforce disk encryption and escrow keys (with Kubuntu and Fedora).

## Alternatives considered

Fedora Workstation: about 13 months per release. Fedora Atomic Desktops: Assess, Fleet agent cannot be installed on rpm-ostree systems. NixOS: Assess, about 7 months per release. Debian: no disk encryption escrow in Fleet. CachyOS: Hold. Omarchy: Assess, candidate for 2027.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint), [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

A new LTS release (upgrade plan), a change in Ubuntu Pro terms, or Fleet support for an image-based OS that passes the pilot.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Adopt | Initial entry. |
