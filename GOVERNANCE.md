# Governance

Governance describes how Akari AMTS itself is maintained.

It is not project management bureaucracy. In this repository, governance means answering practical questions:

- who can change the specification
- how changes are proposed
- how compatibility is considered
- how decisions are recorded
- how language and community material are maintained

## Current Model

Akari AMTS currently uses lightweight maintainer governance.

Specification changes should be:

- proposed in issues or pull requests
- written in English
- reviewed for implementation independence
- checked against the design principles
- recorded in the changelog when user-visible

This repository may use ODTS Epics, Items, and Tasks to organize the work. ODTS is the project-development framework for repository work; it does not define the AMTS specification.

## Decision Principles

Changes should preserve:

- specification before implementation
- implementation independence
- human readability
- assistant friendliness
- minimal complexity
- stable evolution

## Languages

The specification language is English.

Community-facing repository material may exist in German, English, and Japanese.

Japanese material should include a note that help is welcome, especially from Japanese Mac developers.

## Compatibility

Before version 1.0.0, compatibility is best-effort.

Breaking changes should be explicit and should explain migration impact for existing AMTS Spaces and implementations.
