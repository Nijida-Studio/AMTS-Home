# Shutdown Procedure

## Purpose

Shutdown preserves project knowledge so that a later assistant session can reconstruct the same context.

## Procedure

### Step 1: Review the Session

Identify:

- completed tasks
- changed files
- new decisions
- open tasks
- blockers
- important context
- relevant links or references

### Step 2: Update Project Knowledge

Update or recommend updates to:

```text
Projects/<ProjectName>/current-work.md
Projects/<ProjectName>/decisions.md
Projects/<ProjectName>/handover.md
```

Only record durable project knowledge. Do not turn every transient conversation detail into project memory.

### Step 3: Create a Session Summary

Store session summaries under:

```text
Projects/<ProjectName>/session-summaries/
```

Recommended file name:

```text
YYYY-MM-DD_short-topic.md
```

The summary should include:

- date
- environment
- project
- repository and branch, if relevant
- completed work
- decisions
- open tasks
- relevant files
- archive reference, if available

### Step 4: Archive the Conversation If Possible

Store full conversation archives under:

```text
Archive/<Environment>/<Year>/<ProjectName>/
```

Archives are immutable and should not be edited after creation.

### Step 5: Leave a Clear Next Step

The handover document should tell the next assistant session where to continue.

