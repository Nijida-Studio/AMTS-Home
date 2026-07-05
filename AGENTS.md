# AGENTS.md

## Project

This repository contains Akari AMTS, the Akari Memory Transfer Specification.

AMTS is a documentation-first specification. It is not an application, framework, runtime, or assistant implementation.

## Language

The specification language is English.

Repository and community-facing material may also exist in German and Japanese.

Japanese material should invite help from Japanese Mac developers when appropriate.

## Project Management

This repository uses ODTS as its agile project-development framework.

ODTS organizes AMTS work through Epics, Items, and Tasks in GitHub Issues.

ODTS does not define AMTS. AMTS remains the specification being developed.

## Working Boundaries

- Keep specification text implementation-independent.
- Keep public specification files in `docs/`.
- Keep project templates in `templates/`.
- Keep examples in `examples/`.
- Do not copy local machine paths into public specification files.
- Do not treat any implementation as defining AMTS.
- Do not treat ODTS project-management artifacts as AMTS specification text.

## Important Terms

- AMTS: the specification.
- AMTS Space: a concrete knowledge space organized according to AMTS.
- AMTS installation: a local or hosted instance of an AMTS Space.
- AMTS implementation: software, tooling, or assistant behavior that adopts AMTS.

## Recommended Startup

Before making changes, read:

- `README.md`
- `docs/specification.md`
- `docs/glossary.md`
- `docs/principles.md`
- `docs/repository-integration.md`
- `PROJECT-MANAGEMENT.md`
- `GOVERNANCE.md`

## Verification

For documentation-only changes, at minimum check:

- no stale project names such as copied source-project references remain
- no local machine paths are introduced
- markdown links point to existing files
- `git diff --check` passes
