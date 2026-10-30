# Authentik

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source identity provider (OIDC, SAML, LDAP, proxy). Official site: [goauthentik.io](https://goauthentik.io/).

## Why mess.systems uses it

Serves the `sso` capability in a limited scope: lab and learning environments, where its flows and built-in proxy and LDAP outposts are convenient. [Keycloak](keycloak.md) is the default IdP.

## Alternatives considered

[Keycloak](keycloak.md) (Adopt) is the default for new work. [Zitadel](zitadel.md) (Assess) only for multi-tenant product identity.

## Where it applies

- [Capability codes: `sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a need outside lab and learning environments: then move to Hold or record a reason for wider use.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |
| 2026-10-30 | Trial | Keycloak becomes the default IdP; Authentik stays for lab and learning environments. |
