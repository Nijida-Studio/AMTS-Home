# Directory Layout

## Overview

An AMTS Space is a concrete knowledge space organized according to AMTS.

This specification recommends a simple top-level layout:

```text
<amts-space>/
  AMTS/
  Common/
  Projects/
  Archive/
```

An implementation may choose another physical layout if it preserves the same conceptual boundaries.

## AMTS/

The `AMTS/` directory may contain a local copy of the active specification or installation-specific AMTS workflow documents.

Public specification work should happen in the AMTS specification repository. A local `AMTS/` directory inside an AMTS Space is an installation artifact.

## Common/

The `Common/` directory contains shared knowledge used by multiple projects.

Examples:

- shared terminology
- common references
- organization-level conventions
- reusable prompts

## Projects/

Each project should have its own project workspace:

```text
Projects/
  <ProjectName>/
    README.md
    handover.md
    current-work.md
    decisions.md
    session-summaries/
    prompts/
    references/
```

### README.md

Introduces the project workspace.

### handover.md

Primary entry point for assistant sessions.

It should describe the current project state and the recommended starting point.

### current-work.md

Describes the active focus, open tasks, blockers, and next steps.

### decisions.md

Records important decisions together with their rationale.

### session-summaries/

Contains dated summaries of completed working sessions.

### prompts/

Contains reusable prompts for project-related assistant work.

### references/

Contains supporting material such as specifications, notes, screenshots, or external documents.

## Archive/

The `Archive/` directory stores immutable conversation or session archives:

```text
Archive/
  <Environment>/
    <Year>/
      <ProjectName>/
```

Examples:

```text
Archive/Codex/2026/ExampleProject/
Archive/Chat/2026/ExampleProject/
```

Archives should not be edited after creation.

Knowledge that remains relevant should be extracted into project workspace documents.

