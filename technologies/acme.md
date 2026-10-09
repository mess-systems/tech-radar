# ACME

| Category | Ring | Kind |
|---|---|---|
| [`iam`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Specification |

## What it is

Automatic Certificate Management Environment ([RFC 8555](https://www.rfc-editor.org/rfc/rfc8555)): a protocol for requesting, validating, and renewing X.509 certificates automatically. Official site: [www.rfc-editor.org/rfc/rfc8555](https://www.rfc-editor.org/rfc/rfc8555).

## Why mess.systems uses it

The naming standard makes per-name ACME issuance against the internal CA (`pki.iam.shared`) the default for internal TLS. Pre-issued wildcards are allowed only for endpoints that cannot use ACME. Public names use a public CA through the DNS-01 challenge.

## Alternatives considered

Manually issued or long-lived wildcard certificates. Chosen because it is an IETF standard and removes manual renewal.

## Where it applies

- [TLS](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#7-tls)
- [Certificates in the worked example](https://github.com/mess-systems/naming-standard/blob/main/02-worked-example.md#6-certificates)

## Review trigger

A change to the TLS rules of the naming standard, or an internal endpoint class that cannot use ACME at all.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
