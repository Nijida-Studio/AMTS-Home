# Glossary

## Akari AMTS

The public name of the Akari Memory Transfer Specification.

## AMTS

Akari Memory Transfer Specification.

AMTS is an implementation-independent specification for assistant initialization, project context, documentation, handover, and memory exchange.

## Specification

A documented set of concepts, conventions, structures, and workflows.

AMTS is the specification.

## AMTS Space

A concrete knowledge space organized according to AMTS.

An AMTS Space may be local, synced, hosted, repository-backed, or managed by tooling.

## AMTS Installation

A concrete physical or hosted instance of an AMTS Space.

Example:

- a local folder synced across devices
- a repository directory used as a team AMTS Space
- a hosted workspace managed by an AMTS implementation

## AMTS Implementation

Software, assistant behavior, automation, or tooling that adopts, supports, or manages AMTS.

Implementations follow AMTS. They do not define AMTS.

## Assistant

An AI system or agent participating in project work.

AMTS does not require a specific assistant identity, model, vendor, or runtime.

## Environment

The place where an assistant is operating.

Examples:

- a chat environment
- a coding agent
- an IDE assistant
- a local automation tool

## Project

A named area of work with its own context, decisions, current work, and handover state.

## Project Workspace

The project-specific knowledge area inside an AMTS Space.

## Repository

A version-controlled project source tree.

An AMTS Space may reference repositories, but AMTS does not require every project to be a software repository.

## AGENTS.md

An optional repository-level instruction file for AI assistants.

When present, it can explain how assistants should work inside the repository.

## Docs/

An optional repository documentation directory.

When present, it can contain project-owned documentation that should be read before or during assistant work.

## Handover

A document that transfers relevant project context from one assistant session to another.

## Startup

The process by which an assistant initializes itself for work on a project.

## Shutdown

The process by which an assistant closes a session and records useful state for future continuation.

## Session Summary

A dated record of what happened during a work session.

## Current Work

A document describing the active focus, open tasks, blockers, and immediate next steps.

## Decision

A documented choice that affects the direction, structure, interpretation, or compatibility of a project.

## Archive

An immutable historical record of a conversation or session.

Archives are historical sources. They are not the primary project knowledge base.

## Governance

The lightweight decision process for maintaining AMTS itself.

Governance answers questions such as who may change the specification, how decisions are recorded, and how compatibility is handled.

