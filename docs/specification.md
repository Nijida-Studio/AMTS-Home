# Akari AMTS Specification

## Name

Akari Memory Transfer Specification.

Short name:

AMTS.

Preferred public name:

Akari AMTS.

## Status

Draft.

Current version:

0.1.0.

## Purpose

AMTS defines conventions for preserving, organizing, transferring, and reconstructing project knowledge across assistant working environments.

The specification exists so that a project can continue with coherent context even when the previous work happened in another conversation, another assistant environment, or another tool.

## Scope

AMTS defines:

- terminology
- AMTS Space concepts
- project knowledge structure
- directory layout conventions
- assistant startup and shutdown procedures
- handover documents
- conversation archive structure
- repository integration points

AMTS does not define:

- application architecture
- programming languages
- build systems
- version control strategy
- project management methodology
- user interface behavior
- any specific assistant implementation

Those remain the responsibility of each adopting project or implementation.

## Core Model

AMTS separates four concerns:

1. **Specification**
   The written AMTS standard.

2. **AMTS Space**
   A concrete knowledge space organized according to AMTS.

3. **Project Workspace**
   The project-specific working memory inside an AMTS Space.

4. **Archive**
   Immutable historical conversation records.

## Principles

AMTS follows these principles:

- the project owns the knowledge
- conversations are temporary
- archives preserve history
- project knowledge is maintained separately
- assistant environments are interchangeable
- implementations do not define the specification
- documentation is the primary artifact

## Conformance

This draft uses the following informal conformance levels:

- **must**: required for AMTS conformance
- **should**: strongly recommended
- **may**: optional

A project may adopt AMTS partially, but it should document any intentional deviations.

## Terminology

Normative terms are defined in [Glossary](glossary.md).

