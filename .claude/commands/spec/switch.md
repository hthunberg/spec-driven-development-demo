---
allowed-tools: Bash(ls:*), Bash(echo:*), Bash(test:*), Bash(cat:*)
description: Switch to a different specification
argument-hint: <spec-id>
---

## Available Specifications

!`ls -d spec/*/ 2>/dev/null | sort`

## Your Task

Switch the active specification to: $ARGUMENTS

1. If no argument provided, list all available specs from above and prompt user to choose one
2. Verify the requested spec directory exists (spec/$ARGUMENTS/)
3. Update `spec/.current-spec` with the new spec directory name (just the directory name, e.g., "001-feature-name")
4. Show the status of the newly active spec:
   - List files present
   - Show which phases are approved
   - Show task progress if tasks.md exists
5. Display next recommended action based on the spec's current state

Use the echo command to write to the `.current-spec` file.