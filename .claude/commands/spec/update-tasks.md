---
allowed-tools: Bash(cat:*), Bash(grep:*), Bash(ls:*), Write
description: Mark a task as complete
argument-hint: <task-description-or-number>
---

## Context

Current spec: !`cat spec/.current-spec 2>/dev/null`

## Your Task

First, validate the current spec:
1. Read the current spec from the context above
2. Use `ls` to verify the spec directory exists
3. If invalid, inform user to run `/spec:switch` or `/spec:new`
4. Only proceed if valid

Then update the task status for: "$ARGUMENTS"

1. Read the tasks.md file from the spec directory
2. Find the matching task (by description or line number)
3. Change `- [ ]` to `- [x]` for that task
4. Show updated progress statistics:
   - Total tasks
   - Completed tasks
   - Percentage complete
5. Suggest next task to work on

Use the Write tool to update the tasks.md file in the correct spec directory.