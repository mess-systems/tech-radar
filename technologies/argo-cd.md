# Argo CD

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Declarative GitOps continuous delivery tool for Kubernetes (Apache-2.0, part of the CNCF-graduated Argo project). Official site: [argo-cd.readthedocs.io](https://argo-cd.readthedocs.io/).

## Why mess.systems uses it

It is the example for GitOps projects (`<plane>` or `<product>`) and for moving product-named IdP slugs to the application form (`eng-sdlc-argocd`).

## Alternatives considered

Other GitOps controllers. Adopt: target product for GitOps.

## Where it applies

- [Kubernetes RBAC](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#10-kubernetes-rbac)
- [IdP objects](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#6-idp-objects)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`gitops`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
| 2026-10-15 | Adopt | Target product for the `gitops` capability. |
