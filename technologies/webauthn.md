# WebAuthn

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Specification |

## What it is

Web Authentication: a W3C standard for public-key, phishing-resistant authentication with platform authenticators and security keys (the basis of passkeys). Official site: [www.w3.org/TR/webauthn](https://www.w3.org/TR/webauthn/).

## Why mess.systems uses it

The identity conventions require it: human accounts use a password plus WebAuthn, and separate admin accounts (`<handle>-adm`) use WebAuthn only.

## Alternatives considered

TOTP and push-based one-time codes are phishing-prone. Chosen because it is an open standard supported by browsers and common IdPs.

## Where it applies

- [Identity kinds](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#2-identity-kinds)
- [IdP objects (`flow-admin-webauthn`)](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#6-idp-objects)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`sso`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A new WebAuthn level that changes authenticator requirements, or a change to the admin-account rule.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
