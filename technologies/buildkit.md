# BuildKit

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Open-source container image builder behind `docker buildx` (Apache-2.0). It runs rootless in Kubernetes from the official `rootless` and `userns` manifests, and keeps layer cache in a registry (`type=registry,mode=max`), on a local volume or in S3. Version checked on 2026-11-11: v0.34.2. Official repository: [moby/buildkit](https://github.com/moby/buildkit).

## Why mess.systems uses it

It is the proposed image builder in the [`sdlc-ci-runners`](https://github.com/mess-systems/blueprints/tree/main/sdlc-ci-runners) blueprint: one rootless `buildkitd` as a shared service (StatefulSet with a volume), reached by `buildx` through the `remote` driver over mTLS, so runner pods need no docker and no privileged mode.

Assess: one evaluation so far, no pilot.

## Alternatives considered

kaniko (the Google repository was archived in June 2025; the Chainguard fork gets security fixes only), buildah rootless (works, more friction with fuse and seccomp in Kubernetes), docker-in-docker (needs privileged pods), Depot (vendor cloud). Assess: image builds for CI.

## Where it applies

- [Capability codes: `ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`sdlc-ci-runners`](https://github.com/mess-systems/blueprints/tree/main/sdlc-ci-runners) |

## Review trigger

After the pilot in the blueprint: move to Trial or remove.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-12 | Assess | Initial entry after the 2026-11-11 evaluation of self-hosted GitHub Actions runners. |
