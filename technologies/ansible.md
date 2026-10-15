# Ansible

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Agentless configuration management and automation tool (GPL-3.0) that applies playbooks to hosts over SSH. Official site: [www.ansible.com](https://www.ansible.com/).

## Why mess.systems uses it

The object forms define its inventory groups: `<plane>_<domain>` and `<application>`.

## Alternatives considered

Other configuration management tools. Chosen because the standard already fixes its inventory naming.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| not mapped yet | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |

## Review trigger

A change to the inventory form, or a decision to manage hosts only through images and GitOps.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |
