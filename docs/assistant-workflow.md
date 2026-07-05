# Assistant Workflow

## Purpose

AMTS defines a workflow that helps an assistant reconstruct project context before acting and preserve useful state before ending a session.

## Information Priority

When working on a project, an assistant should consider information in this order:

1. Repository instructions and source of truth
   - `AGENTS.md`
   - repository `Docs/`
   - source files relevant to the task

2. Project workspace
   - `handover.md`
   - `current-work.md`
   - `decisions.md`
   - relevant `session-summaries/`

3. Shared AMTS Space knowledge
   - `Common/`

4. Conversation archives
   - `Archive/`

Archives should be used to reconstruct or verify history when needed. They should not replace maintained project documentation.

## Session Handover

Every working session should leave the project in a state that allows a later assistant session to continue with minimal additional context.

Whenever practical, update or recommend updates to:

- `current-work.md`
- `decisions.md`
- `handover.md`
- a dated session summary

## Assistant Identity

AMTS does not require a specific assistant name or identity.

An implementation may use its own assistant identity. Akari is the originating assistant identity for Akari AMTS, but AMTS remains implementation-independent.

