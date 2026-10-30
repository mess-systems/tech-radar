# Keycloak

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source identity and access management server (Apache-2.0, a CNCF project). It provides single sign-on over OpenID Connect and SAML, user federation, and fine-grained admin roles. Official site: [www.keycloak.org](https://www.keycloak.org/).

## Why mess.systems uses it

It carries the `sso` capability (`sso.iam.shared`) as the default identity provider (IdP), and it is the reference IdP in the naming standard's examples, including the `jwt-keycloak` auth mount. It covers what the blueprints need from an IdP: OpenID Connect for people and services, OAuth clients for agents behind the [AI gateway](agentgateway.md), and a dedicated provider option in agentgateway for its token checks. The standard still treats the IdP as interchangeable.

## Alternatives considered

- [Authentik](authentik.md): moved to Trial, limited to lab and learning environments, where its flows and built-in proxy and LDAP outposts are convenient.
- [Zitadel](zitadel.md) (Assess): considered only for multi-tenant product identity.
- Hosted IdPs whose objects the standard maps (Entra ID, Okta, and similar): mapped for compatibility, not chosen as the default.

## Where it applies

- [Worked encodings](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#11-worked-encodings)
- [IdP objects](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#6-idp-objects)
- [Mounts (`auth/jwt-<idp>`)](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#2-mounts)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`obs-mcp-readonly`](https://github.com/mess-systems/blueprints/tree/main/obs-mcp-readonly) |

## Review trigger

A license, governance, or maintenance change upstream; or a release that breaks OpenID Connect discovery or token validation for the gateway.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
| 2026-10-30 | Adopt | Default IdP for the `sso` capability; Authentik moves to Trial. |
