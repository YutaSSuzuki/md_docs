# Docs as Code Operation Policy

## Premise

This project treats the future maintainer as a different developer, even when it is a solo project.

Documentation must preserve current state, decision context, unfinished work, and completed changes.

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
├── architecture/
├── api/
├── database/
├── operations/
├── performance/
├── adr/
├── proposals/
├── roadmap/
└── changelog/
```

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

1. Check roadmap, proposals, architecture, database, and API docs before work.
2. Create or update a Proposal before large feature, design, database, or infrastructure changes.
3. Update Current State documents during implementation.
4. After implementation, update ADR, roadmap, and changelog when needed.
5. Move completed Proposals to `proposals/done/` or delete them when no longer useful.
