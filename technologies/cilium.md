# Cilium

| Category | Ring | Kind |
|---|---|---|
| [`net`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

eBPF-based networking, security and observability for Kubernetes (Apache-2.0, CNCF graduated). Official site: [cilium.io](https://cilium.io/).

## Why mess.systems uses it

Kubernetes network and policy layer.

## Alternatives considered

Calico, Flannel. Chosen for eBPF policies and built-in visibility.

## Where it applies

- [Capability codes: `firewall`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`firewall`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |
