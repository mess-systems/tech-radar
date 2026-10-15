# OpenID Connect

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Specification |

## What it is

Identity layer on top of OAuth 2.0, maintained by the OpenID Foundation. Applications delegate sign-in to an identity provider and receive signed ID tokens with claims such as groups. Official site: [openid.net/developers/how-connect-works](https://openid.net/developers/how-connect-works/).

## Why mess.systems uses it

The standard uses it for every human and CI login: applications get an OIDC client (`oidc` secret item), humans and CI authenticate to the secrets manager through `jwt-<idp>` roles bound to group claims, and privileged human access uses an OIDC login plus a policy instead of a stored token.

## Alternatives considered

SAML 2.0 covers browser sign-in but not the JWT-based machine flows the standard relies on. Chosen because it is the common protocol across IdPs, git forges, dashboards, and secrets managers.

## Where it applies

- [Items and fields (`oidc`)](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#4-items-and-fields)
- [Auth roles and tokens](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#6-auth-roles-and-tokens)
- [Principles applied (rule S5)](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#1-principles-applied)
- [IdP objects](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#6-idp-objects)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A successor specification gaining broad IdP support, or a change to how the standard binds groups to roles.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
