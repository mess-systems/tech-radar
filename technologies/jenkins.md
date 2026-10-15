# Jenkins

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Open-source automation server (MIT) for CI/CD pipelines, extended through plugins. Official site: [www.jenkins.io](https://www.jenkins.io/).

## Why mess.systems uses it

It is the example product for the `ci` capability and the example service account (`svc-eng-sdlc-jenkins`) in the identity and secrets conventions.

## Alternatives considered

CI built into the git forge (Forgejo Actions), or other CI servers. Assess: kept only where Forgejo Actions does not fit.

## Where it applies

- [Identity kinds](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#2-identity-kinds)
- [Tokens, robots, credentials IDs](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#12-tokens-robots-credentials-ids)
- [Policies (scoped read)](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#5-policies)

## Review trigger

After an evaluation: move back to Trial or to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
| 2026-10-15 | Assess | Moved to Assess: CI defaults to Forgejo Actions. |
