# Trivy

| Category | Ring | Kind |
|---|---|---|
| [`sec`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source scanner for vulnerabilities, misconfigurations and SBOMs (Apache-2.0). Official site: [trivy.dev](https://trivy.dev/).

## Why mess.systems uses it

Carries image and config scanning in CI and the registry.

## Alternatives considered

Grype. Chosen for one tool across images, IaC and SBOM.

## Where it applies

- [Capability codes: `scan`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |
