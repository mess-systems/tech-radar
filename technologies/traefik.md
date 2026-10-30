# Traefik

| Category | Ring | Kind |
|---|---|---|
| [`net`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source reverse proxy and ingress controller (MIT, written in Go, maintained by Traefik Labs). It discovers routes from providers such as Kubernetes (Ingress, its own CRDs, and the [Gateway API](https://doc.traefik.io/traefik/providers/kubernetes-gateway/)), Docker, and plain files, and issues certificates over [ACME](acme.md). Official site: [traefik.io](https://traefik.io/traefik/). Source and releases: [github.com/traefik/traefik](https://github.com/traefik/traefik).

## Why mess.systems uses it

It carries the `ingress` capability: routing of incoming HTTP traffic to services inside a cluster or on a host. Configuration is declarative (CRDs or files), so routes live in Git and are deployed like any other workload. Behind an edge proxy that terminates TLS, Traefik trusts forwarded headers only from listed addresses ([entrypoint `forwardedHeaders`](https://doc.traefik.io/traefik/routing/entrypoints/)), which keeps the original scheme and client address intact for services such as the AI gateway.

## Alternatives considered

- [ingress-nginx](https://github.com/kubernetes/ingress-nginx) (Apache-2.0): a widely used Ingress controller built on NGINX. Not chosen: Traefik covers Kubernetes, containers outside Kubernetes, and file-based routes with one product and one configuration model.
- [Envoy Gateway](https://gateway.envoyproxy.io/) (Apache-2.0): a Gateway API implementation on Envoy. A candidate if mess.systems moves all routing to the Gateway API; Traefik already implements the Gateway API provider.

## Where it applies

- [Capability codes: `ingress`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Single base URL](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#6-single-base-url)
- [TLS](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#7-tls)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`ingress`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`obs-mcp-readonly`](https://github.com/mess-systems/blueprints/tree/main/obs-mcp-readonly) |

## Review trigger

A license or governance change of the project, or a decision to route all traffic through the Kubernetes Gateway API with a different implementation.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-30 | Adopt | Initial entry: ingress controller in the `obs-mcp-readonly` blueprint. |
