# Docs as Code Operation Policy

## Premise

This project treats the future maintainer as a different developer, even when it is a solo project.

Documentation must preserve current state, decision context, unfinished work, and completed changes.

AI is expected to read these documents before work, update them after work, and leave enough context for a human to understand the current state and give the next instruction.

When using Codex, apply the bundled `skills/docs-as-code-developer/` skill.

## Basic Policy

- Use Markdown for all project documentation.
- Manage documentation in Git with the code.
- Prefer Mermaid for diagrams.
- Keep Current State documents up to date.
- Do not keep historical architecture in Current State documents.
- Preserve decision history in ADRs.
- Preserve future ideas in Proposals.
- Preserve completed changes in Changelog.

## Directory Structure

```text
docs/
├── index.md
├── documentation-policy.md
├── architecture/     current state, context, runtime, deployment
├── api/              endpoints and feature flows
├── database/         schema, ER diagram, migration
├── operations/       runbook, deployment, backup, monitoring
├── performance/      current state, plans, results, analysis
├── adr/              permanent decision records
├── proposals/        changes under consideration
├── roadmap/          current development status
└── changelog/        completed changes
```

Each directory must have an `index.md` that explains why the directory exists, what to write there, which files exist, and how to read them.

## Update Rules

| Change | Update |
| --- | --- |
| System architecture | `architecture/` |
| API | `api/` |
| Database | `database/` |
| Operation procedure | `operations/` |
| Performance | `performance/` |
| Design decision | `adr/` |
| Future plan | `proposals/` |
| Development status | `roadmap/` |
| Completed change | `changelog/` |

## Workflow

1. Choose the smallest safe reading scope before work.
2. Check only the docs needed for the current task.
3. Create or update a Proposal before large feature, design, database, or infrastructure changes.
4. Update Current State documents during implementation.
5. After implementation, update ADR, roadmap, and changelog when needed.
6. Move completed Proposals to `proposals/done/` or delete them when no longer useful.

## Reading Scope

Do not read all documentation by default.

| Scope | Use When | Read |
| --- | --- | --- |
| Full Orientation | New session, unclear context, broad change, or uncertain current state | `docs/index.md`, this policy, roadmap, related category indexes, relevant Current State documents |
| Focused Read | Conversation context is fresh and task scope is clear | Related category index, directly relevant docs, directly relevant code |
| Minimal Read | Small edit with clear target | Target file and directly linked docs only when needed |

Reuse conversation context when it is still reliable. Reread documents when they may have changed, exact wording matters, or the previous context is incomplete.

## Documentation Update Rule

Documentation must be updated even when no code is changed.

| Situation | Update |
| --- | --- |
| Design decision was made | `adr/` |
| Future implementation plan was proposed | `proposals/` |
| Next work changed | `roadmap/current-roadmap.md` |
| Completed meaningful non-code change | `changelog/CHANGELOG.md` |
| Architecture understanding changed | `architecture/` |
| API understanding changed | `api/` |
| Database understanding changed | `database/` |
| Operation procedure changed | `operations/` |
| Performance finding changed | `performance/` |

## Human and AI Workflow

1. AI chooses Full Orientation, Focused Read, or Minimal Read.
2. AI reads only the documents needed for the selected scope.
3. AI performs the requested work.
4. AI updates the relevant documents.
5. Human reads the updated documents and understands the current state.
6. Human gives the next instruction based on the updated documents.

Documentation is part of the deliverable. Work is not complete when the code changed but the related docs are stale.

## Initial Setup Rule

The repository already contains the standard application and documentation structure.

- Do not create alternative top-level source or docs directories without a recorded reason.
- Update existing Current State files before adding another document.
- Split a feature into a new document only when the existing document becomes difficult to navigate.
- Add new ADR and Proposal files when a new decision or proposal must have its own lifecycle.
