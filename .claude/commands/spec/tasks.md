---
allowed-tools: Bash(cat:*), Bash(test:*), Bash(ls:*), Write
description: Create implementation task list
---

## Context

Current spec: !`cat spec/.current-spec 2>/dev/null`
Tasks template: !`cat ./templates/tasks.md 2>/dev/null || echo "No template found"`

## Your Task

First, validate the current spec:
1. Read the current spec from the context above
2. Use `ls` to verify the spec directory exists
3. If invalid, inform user to run `/spec:switch` or `/spec:new`
4. Only proceed if valid

Then continue with tasks phase:

1. Verify design is approved (check for `.design-approved` file in the spec directory)
2. If not approved, inform user to complete design first with `/spec:approve design`
3. If approved, create tasks.md with:
   - Overview with time estimates
   - Phase breakdown (Foundation, Core, Testing, Deployment)
   - Detailed task list with checkboxes
   - Task dependencies
   - Risk mitigation tasks
4. Each task should be specific and actionable
5. If template is available in context above, use it as the base structure for tasks
6. Use markdown checkboxes: `- [ ] Task description`

Organize tasks to enable incremental development and testing.

Use the Write tool to create the tasks.md file in the correct spec directory.