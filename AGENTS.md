# AGENTS.md

This repository uses Docs as Code.

When working in this repository, follow the bundled Codex skill:

```text
skills/docs-as-code-developer/
```

The skill is the detailed source of truth for docs-aware development. This file provides the default rules that should apply even when the user does not explicitly mention the skill.

## Core Rules

- Documentation is part of the deliverable.
- Do not read all docs by default.
- Read the smallest safe set of files for the task.
- Reuse reliable conversation context instead of rereading unchanged docs.
- Update docs when code changes.
- Update docs even when no code changes, if the task creates a decision, plan, investigation result, or new current-state understanding.
- Keep Current State documents focused on the current system only.

## Reading Scope

Choose one scope before starting work.

| Scope | Use When | Read |
| --- | --- | --- |
| Full Orientation | New session, unclear context, broad change, or uncertain current state | `docs/index.md`, `docs/documentation-policy.md`, roadmap, related category indexes, relevant Current State docs |
| Focused Read | Conversation context is fresh and task scope is clear | Related category index, directly relevant docs, directly relevant code |
| Minimal Read | Small edit with clear target | Target file and directly linked docs only when needed |

Reread a document only when it may have changed, exact wording matters, previous context is incomplete, or current state is uncertain.

## Code Placement

Use the existing top-level structure.

| Target | Place |
| --- | --- |
| Application code | `app/` |
| Configuration | `config/` |
| Development or operation scripts | `scripts/` |
| Automated tests | `tests/` |
| Markdown documentation | `docs/` |

Do not create alternative top-level source or docs directories unless the project already uses them or the user explicitly asks.

## Documentation Update Map

| Change | Update |
| --- | --- |
| System architecture | `docs/architecture/` |
| API contract or flow | `docs/api/` |
| Database schema or migration | `docs/database/` |
| Run, deploy, backup, monitor, troubleshoot | `docs/operations/` |
| Performance test, metric, bottleneck, improvement | `docs/performance/` |
| Durable design decision | `docs/adr/` |
| Future implementation plan | `docs/proposals/` |
| Current development status | `docs/roadmap/current-roadmap.md` |
| Completed meaningful change | `docs/changelog/CHANGELOG.md` |

## Finish Rule

When finishing work, report:

- code changed
- docs changed
- tests or validation run
- remaining risks or follow-up work
