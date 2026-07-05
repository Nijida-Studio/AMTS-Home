# Repository Integration

## Purpose

AMTS can be used with software repositories, documentation repositories, design repositories, or non-code projects.

When a project has a source repository, AMTS should respect that repository as the primary local source of truth for repository-specific instructions.

## AGENTS.md

`AGENTS.md` is an optional repository-level instruction file for AI assistants.

It can define:

- project overview
- build and test commands
- coding conventions
- architecture boundaries
- safety rules
- required startup reads
- known constraints

AMTS treats `AGENTS.md` as repository-owned guidance. It is not an AMTS Space replacement.

If `AGENTS.md` conflicts with maintained project workspace memory, the assistant should surface the conflict instead of silently choosing one source.

## Docs/

`Docs/` is an optional repository documentation directory.

It can contain:

- architecture notes
- feature plans
- design documents
- implementation history
- user-facing documentation
- project memory that belongs inside the repository

AMTS treats repository `Docs/` as project-owned documentation.

## Relationship to an AMTS Space

An AMTS Space may point to one or more repositories.

The repository should contain information needed to work safely in that repository.

The AMTS project workspace should contain broader handover, current work, decisions, and cross-environment memory.

## Recommended Startup Order

For repository work:

1. read AMTS startup guidance
2. read the project handover
3. read `current-work.md` and `decisions.md`
4. read repository `AGENTS.md`, if present
5. read relevant repository `Docs/`
6. inspect task-relevant source files

