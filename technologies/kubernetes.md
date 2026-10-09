# Kubernetes

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source container orchestration platform (Apache-2.0, CNCF graduated). Official site: [kubernetes.io](https://kubernetes.io/).

## Why mess.systems uses it

The standard defines dedicated Kubernetes forms: namespaces, workloads, `mess.systems/<key>` labels, RBAC objects, and the `kubernetes-<cluster>` auth role. Its object-name limits are one source of the character rules. It provides the `k8s` capability.

## Alternatives considered

Running containers directly on VMs needs no extra forms beyond hosts. Chosen because the standard already fixes its naming in full and its API is the common target of the GitOps and RBAC rules.

## Where it applies

- [Character rules](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#1-character-rules-apply-to-every-family)
- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Kubernetes RBAC](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#10-kubernetes-rbac)
- [Auth roles and tokens](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#6-auth-roles-and-tokens)

## Review trigger

A Kubernetes change to object-name or label rules, or a change to the Kubernetes forms of the standard.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
