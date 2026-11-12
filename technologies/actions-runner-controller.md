# Actions Runner Controller (ARC)

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Kubernetes operator for self-hosted GitHub Actions runners (Apache-2.0; the runner itself is MIT). Runner scale sets register with GitHub, scale on the job queue and start one ephemeral runner pod per job. Versions checked on 2026-11-11: gha-runner-scale-set 0.15.1, runner v2.338.2. Official repository: [actions/actions-runner-controller](https://github.com/actions/actions-runner-controller).

## Why mess.systems uses it

It is the proposed product for GitHub Actions runners in the [`sdlc-ci-runners`](https://github.com/mess-systems/blueprints/tree/main/sdlc-ci-runners) blueprint: ephemeral runner pods without docker, installed through GitOps, with the GitHub App key from the secrets manager. Images are built in a separate rootless BuildKit, not inside the runner.

Assess, not Trial:

- It has been through one evaluation only, not a pilot.
- The `dind` container mode needs privileged pods, and the `kubernetes` modes give the runner RBAC on pods; the blueprint uses neither unless a job needs `services:`.
- Forgejo Actions stays the CI default for internal repositories; ARC covers repositories that live on GitHub.

## Alternatives considered

GARM (ephemeral VMs or containers through providers), terraform-aws-github-runner and RunsOn (AWS only), actuated (commercial Firecracker microVMs), runners on KubeVirt (heavy for a small team), managed runner services such as Ubicloud, WarpBuild, Namespace or Depot (code, cache and secrets with the vendor). Assess: GitHub Actions runners in our own Kubernetes.

## Where it applies

- [Capability codes: `ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`sdlc-ci-runners`](https://github.com/mess-systems/blueprints/tree/main/sdlc-ci-runners) |

## Review trigger

After the pilot in the blueprint (cold and warm build time, network failures): move to Trial or remove.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-12 | Assess | Initial entry after the 2026-11-11 evaluation of self-hosted GitHub Actions runners. |
