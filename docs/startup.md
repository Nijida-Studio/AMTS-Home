# Startup Procedure

## Purpose

Startup reconstructs the current project context with minimal user interaction.

## Procedure

### Step 1: Identify the Target

Determine:

- target project
- target repository, if any
- relevant AMTS Space or AMTS installation
- current task

### Step 2: Read AMTS Context

Read the active AMTS specification or local AMTS installation notes needed for the task.

At minimum, an assistant should understand:

- directory layout
- assistant workflow
- startup and shutdown expectations

### Step 3: Read Project Handover

Read:

```text
Projects/<ProjectName>/handover.md
```

The handover document is the preferred project workspace entry point.

### Step 4: Read Project Knowledge

Read relevant project workspace documents:

- `current-work.md`
- `decisions.md`
- relevant `session-summaries/`
- relevant files in `references/` or `prompts/`

### Step 5: Read Repository Documentation

If the task involves a repository, read repository-level guidance:

- `AGENTS.md`, if present
- relevant repository `Docs/`
- task-relevant source files

### Step 6: Inspect Only What Is Needed

Inspect the repository or workspace narrowly enough to understand the task.

Avoid loading unrelated files only to create the appearance of completeness.

### Step 7: Consult Archives If Needed

Consult archives only when maintained project knowledge is missing, ambiguous, or needs historical verification.

## Result

After startup, the assistant should have enough reconstructed context to continue responsibly.

If important information is missing, the assistant should ask the user instead of inventing project state.

