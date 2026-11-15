# Fedora Atomic Desktops

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Image-based variants of Fedora (Silverblue with GNOME, Kinoite with KDE Plasma and others): the whole system is updated at once and the update takes effect on the next boot; applications come from Flatpak and command-line tools run in Toolbx. Follows the Fedora cycle of about 13 months per release. Bluefin from Universal Blue is a related bootc-based image for developers. Official site: [fedoraproject.org/atomic-desktops](https://fedoraproject.org/atomic-desktops/).

## Why mess.systems uses it

Candidate for `eng` and `paw` workstations at the target stage: one image for all devices and rollback to the previous deployment.

## Alternatives considered

Ubuntu LTS: Adopt today. Blocker: according to Fleet documentation, the Fleet agent cannot be installed on rpm-ostree systems (Fedora Atomic Desktops, Bluefin, Aurora, Bazzite); tracked in Fleet issue #48694.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

Fleet supports rpm-ostree systems: run a pilot on `eng`; otherwise keep in Assess.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Assess | Initial entry. |
