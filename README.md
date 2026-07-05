# Akari AMTS

Akari AMTS is the Akari Memory Transfer Specification.

AMTS defines lightweight conventions for assistant initialization, project knowledge, documentation, handover, and memory exchange across assistant environments.

AMTS is a specification. It is not an application, library, framework, runtime, or assistant implementation.

## Purpose

AMTS helps a project preserve useful working context beyond a single conversation, tool, or assistant environment.

The central idea is simple:

- the project owns the knowledge
- conversations are temporary working sessions
- archives preserve history
- project knowledge is maintained separately from archives
- different assistant environments can reconstruct the same project context

## Core Terms

- **AMTS**: the specification itself.
- **AMTS Space**: a concrete project knowledge space that follows AMTS.
- **AMTS installation**: a local or hosted instance of an AMTS Space.
- **AMTS implementation**: software, tooling, or assistant behavior that adopts or automates AMTS.

## Documentation

Start here:

- [Specification](docs/specification.md)
- [Glossary](docs/glossary.md)
- [Design Principles](docs/principles.md)
- [Directory Layout](docs/directory-layout.md)
- [Assistant Workflow](docs/assistant-workflow.md)
- [Startup Procedure](docs/startup.md)
- [Shutdown Procedure](docs/shutdown.md)
- [Repository Integration](docs/repository-integration.md)
- [Versioning](docs/versioning.md)

Project templates are available in [templates/project](templates/project).

## Project Management

This repository uses ODTS as its agile project-development framework.

ODTS organizes AMTS work through Epics, Items, and Tasks. ODTS does not define AMTS.

See [Project Management](PROJECT-MANAGEMENT.md).

## Languages

The AMTS specification is written in English.

This repository also carries community-facing material in German, English, and Japanese. Japanese language support is intentionally open for improvement, and help from Japanese Mac developers is welcome.

- [Deutsch](community/de/README.md)
- [Japanese / 日本語](community/ja/README.md)

## License

Akari AMTS is licensed under the Apache License, Version 2.0.
