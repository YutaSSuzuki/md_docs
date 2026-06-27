---
name: docs-as-code-developer
description: Use this skill when developing or planning work in a repository based on the md_docs Docs as Code template. It guides Codex to read only the minimum safe documentation, place code in the existing app/config/scripts/tests structure, update Markdown docs for code and non-code decisions, and keep architecture, API, database, operations, performance, ADR, proposals, roadmap, and changelog consistent.
---

# Docs as Code Developer

## Core Rule

Documentation is part of the deliverable.

Update docs when code changes, and also when no code changes but the task produces a decision, plan, investigation result, or new current-state understanding.

## Reading Scope Rule

Do not read all documentation by default. Choose the smallest reading scope that is safe for the task.

### Full Orientation

Use when starting a new session, resuming unclear work, handling broad changes, or when current state is uncertain.

Read:

- `docs/index.md`
- `docs/documentation-policy.md`
- `docs/roadmap/current-roadmap.md`
- related category `index.md` files
- relevant Current State documents

### Focused Read

Use when the conversation context is fresh and the task scope is clear.

Read:

- related category `index.md`
- directly relevant docs
- directly relevant code, config, scripts, or tests

### Minimal Read

Use for small edits with clear scope.

Read:

- target file
- directly linked docs only when needed

### Reuse Conversation Context

If the current conversation already contains the needed context, do not reread unchanged docs.

Reread a document only when it may have changed, exact wording matters, previous context is incomplete, or there is uncertainty about current state.

## Task Classification

Before acting, classify the work and update the matching documents.

| Task Type | Required Action |
| --- | --- |
| Code change | Update code and related docs |
| Documentation-only decision | Update ADR, Proposal, Roadmap, or Current State docs |
| Investigation | Record findings in the relevant docs when the findings affect future work |
| Planning | Create or update Proposal and Roadmap |
| Review | Record accepted follow-up work in Proposal or Roadmap when requested |
| Small wording fix | Update only the target file unless broader docs are affected |

## Code Placement Rule

Use the existing project structure.

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

## Proposal Rule

Create or update a Proposal before large feature, architecture, database, infrastructure, API contract, or performance-design changes.

Do not create a Proposal for small bug fixes, small documentation edits, or mechanical cleanup unless the change needs user approval or future tracking.

After implementation, move completed Proposals to `docs/proposals/done/` or remove them when no longer useful.

## ADR Rule

Create or update an ADR when a durable decision is made.

Use ADRs for decisions involving architecture, database design policy, external services, cost, performance, operations, or anything likely to raise a future "why?" question.

ADRs are history. Do not delete accepted ADRs; supersede them with a new ADR when needed.

## Documentation-Only Work Rule

Do not skip documentation updates just because implementation was not performed.

Examples:

- A plan was chosen but code was not written: update `docs/proposals/` and `docs/roadmap/current-roadmap.md`.
- A design decision was made: update `docs/adr/`.
- A performance investigation found something useful: update `docs/performance/`.
- An operation procedure was clarified: update `docs/operations/`.
- Current system understanding changed: update the relevant Current State document.

## Current State Rule

Current State documents describe only the current system.

Do not preserve old architecture, old API behavior, old DB shape, or old operating procedures in Current State documents. Put history in ADRs and Changelog.

## Final Response Rule

When finishing, report:

- code changed
- docs changed
- tests or validation run
- remaining risks or follow-up work
