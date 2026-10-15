# Authentik

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source identity provider (OIDC, SAML, LDAP, proxy). Official site: [goauthentik.io](https://goauthentik.io/).

## Why mess.systems uses it

Carries the `sso` capability as the default IdP.

## Alternatives considered

Keycloak (Trial), Zitadel (Assess). Chosen for flows and a built-in proxy and LDAP outpost.

## Where it applies

- [Capability codes: `sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |
