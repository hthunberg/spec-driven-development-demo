---
allowed-tools: Bash(touch:*), Bash(test:*), Bash(cat:*), Bash(ls:*)
description: Approve a specification phase
argument-hint: requirements|design|tasks
---

## Context

Current spec: !`cat spec/.current-spec 2>/dev/null`

## Your Task

First, validate the current spec:
1. Read the current spec from the context above
2. Use `ls` to verify the spec directory exists
3. If invalid, inform user to run `/spec:switch` or `/spec:new`
4. Only proceed if valid

Then continue with phase "$ARGUMENTS":

1. Verify the phase file exists (requirements.md, design.md, or tasks.md) in the spec directory
2. Create approval marker file: `.${ARGUMENTS}-approved` in the spec directory
3. Inform user about next steps:
   - After requirements → design phase (`/spec:design`)
   - After design → tasks phase (`/spec:tasks`)
   - After tasks → implementation (`/spec:implement`)
4. If invalid phase name, show valid options: requirements, design, tasks

Use touch command to create approval markers in the correct spec directory path.