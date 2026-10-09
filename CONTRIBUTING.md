# Contributing

Thanks for helping improve the tech radar. A ring is a decision; every decision here should be traceable to a short, public rationale.

## Where to talk

| You have… | Use |
|---|---|
| A question about an entry, or a proposal to discuss first | An **Issue** |
| A ring change, a new entry, or a removal | A **pull request** with a short rationale |
| A typo or obviously broken link | A pull request directly |

## Changing a ring

1. **Edit the card.** Update the ring in the card's header table, and adjust *Why mess.systems uses it* or *Alternatives considered* if the reasoning changed.
2. **Add a History row** to the card: date (`YYYY-MM-DD`), new ring, and one sentence of rationale.
3. **Update the README table** so the ring matches the card.
4. **Write the rationale in the PR description**: what changed, the evidence (license change, maintenance status, an incident, a successful trial), and what the review trigger is now.

One technology per pull request. The maintainer decides and the History row records the outcome.

## Adding or removing an entry

- A new entry is a technology the organisation actually uses or that the [naming standard](https://github.com/mess-systems/naming-standard) names. Copy the card template below to `technologies/<slug>.md` (lowercase, hyphenated) and add a README row.
- The category is a [domain code](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) of the naming standard. If no code fits, propose one in the naming standard first.
- An entry is removed only after it has been on Hold and is no longer used. Keep the card's History in the removal PR description.

## Card template

```markdown
# <Technology>

| Category | Ring | Kind |
|---|---|---|
| [`<domain>`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [<Ring>](../README.md#rings) | Product or Specification |

## What it is

Two or three lines. Official site: [example.org](https://example.org/).

## Why mess.systems uses it

The role it plays and the capability it serves.

## Alternatives considered

Comparable options and why this one.

## Where it applies

- [Section title](https://github.com/mess-systems/naming-standard/blob/main/<file>.md#<anchor>)

## Review trigger

The event that reopens the decision.

## History

| Date | Ring | Change |
|---|---|---|
| YYYY-MM-DD | <Ring> | Initial entry. |
```

## Editorial rules

- English, Markdown, short sentences. Tables for mappings.
- Link with descriptive text that names the target, for example `[object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)`; do not write bare section numbers or the section sign.
- Link each technology to its official site, and external standards to their canonical source, on first mention.
- State verifiable facts (license, governing body, protocol support). Do not describe internal deployments.

## Discussion rules

- Be specific and kind. Critique technologies and decisions, not people, vendors' staff, or employers.
- Argue from evidence: licenses, maintenance status, security record, interoperability, and real-world cases described in fictional terms.
- Disagreement is fine; the maintainer decides and records the reasoning in the card's History.
- Do not share anything confidential to your employer or clients.

## Publication checklist (every issue, PR, and card)

Before you post, confirm that the text contains **none** of:

- [ ] Real internal hostnames, domains, or zones (yours or anyone else's). Use `example.com`, `*.example`, `corp.lan`.
- [ ] IP addresses, CIDRs, ports, or VPN/mesh details of real networks. If you need addresses, use the documentation ranges from [RFC 5737](https://www.rfc-editor.org/rfc/rfc5737) (`192.0.2.0/24`) or [RFC 3849](https://www.rfc-editor.org/rfc/rfc3849).
- [ ] Secrets or anything that looks like one: tokens, API keys, passwords, private keys, connection strings, real secrets paths.
- [ ] Real usernames, account IDs, group names, or email addresses of people or systems.
- [ ] Versions, sizes, or topology of a real deployment, container/VM IDs, asset tags, ticket numbers, or internal decision-record IDs.
- [ ] Customer, employer, or vendor-contract details not already public, including prices and licence terms negotiated privately.
- [ ] Screenshots that show any of the above.

Maintainers will edit or remove content that fails this checklist. If you posted something sensitive by mistake, rotate it first, then ask a maintainer to purge it.

## License of contributions

By contributing you agree that your contribution is licensed under [CC BY 4.0](LICENSE), the same as the rest of the text.
