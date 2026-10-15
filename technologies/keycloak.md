# Keycloak

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source identity and access management server (Apache-2.0, a CNCF project). It provides single sign-on over OpenID Connect and SAML, user federation, and fine-grained admin roles. Official site: [www.keycloak.org](https://www.keycloak.org/).

## Why mess.systems uses it

It is the reference identity provider in the naming standard's examples: the `sso` capability (`sso.iam.shared`) and the `jwt-keycloak` auth mount. The standard treats the IdP as interchangeable.

## Alternatives considered

Other IdPs whose objects the standard maps (Entra ID, Okta, and similar). Trial because the standard names it as an illustration, not a requirement.

## Where it applies

- [Worked encodings](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#11-worked-encodings)
- [IdP objects](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#6-idp-objects)
- [Mounts (`auth/jwt-<idp>`)](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#2-mounts)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

After it has run the `sso` capability in a limited scope: promote to Adopt or move to Hold. Earlier on a license or maintenance change upstream.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
