---
allowed-tools: Bash(cat:*), Bash(test:*), Bash(ls:*), Write
description: Create or review requirements specification
---



## Context

Current spec: !`cat spec/.current-spec 2>/dev/null`
Requirements template: !`cat ./templates/requirements.md 2>/dev/null || echo "No template found"`

## Your Task

First, validate the current spec:
1. Read the current spec from the context above
2. Use `ls` to verify the spec directory exists
3. If invalid, inform user to run `/spec:switch` or `/spec:new`
4. Only proceed if valid

Then for the current active specification:

1. Check if requirements.md exists in the spec directory
2. If template is available in context above, use it as the base structure
3. If not, create a comprehensive requirements.md with:
   - Feature overview
   - User stories with acceptance criteria
   - Functional requirements (P0, P1, P2)
   - Non-functional requirements
   - Constraints and assumptions
   - Out of scope items
   - Success metrics
4. If it exists, display current content and suggest improvements
5. Remind user to use `/spec:approve requirements` when ready

Use the Write tool to create/update the requirements.md file in the correct spec directory.