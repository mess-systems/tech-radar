# Kata Containers

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Open-source container runtime that runs each pod in a lightweight virtual machine with its own kernel (Apache-2.0). It plugs into Kubernetes as a RuntimeClass. Version checked on 2026-11-11: 4.3.1. Official site: [katacontainers.io](https://katacontainers.io/).

## Why mess.systems uses it

Kernel isolation for the pull request runner pool in the [`sdlc-ci-runners`](https://github.com/mess-systems/blueprints/tree/main/sdlc-ci-runners) blueprint, where untrusted code runs. Where Kata is not available, the blueprint falls back to user namespaces (`hostUsers: false`, GA in Kubernetes 1.36).

Assess: depends on what the Kubernetes provider offers; not piloted.

## Alternatives considered

gVisor (also a RuntimeClass), Firecracker microVMs, user namespaces only. Agent sandboxes such as CubeSandbox and OpenSandbox are not CI runners. Assess: isolation of untrusted CI jobs.

## Where it applies

- [Capability codes: `k8s`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`k8s`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`sdlc-ci-runners`](https://github.com/mess-systems/blueprints/tree/main/sdlc-ci-runners) |

## Review trigger

When the pull request pool of the blueprint is piloted: move to Trial or remove.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-12 | Assess | Initial entry after the 2026-11-11 evaluation of self-hosted GitHub Actions runners. |
