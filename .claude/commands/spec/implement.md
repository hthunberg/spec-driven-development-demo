---
allowed-tools: Bash(cat:*), Bash(test:*), Bash(grep:*), Bash(ls:*), Write
description: Start implementation from approved tasks
argument-hint: [phase-number]
---

## Context

Current spec: !`cat spec/.current-spec 2>/dev/null`

## Your Task

First, validate the current spec:
1. Read the current spec from the context above
2. Use `ls` to verify the spec directory exists
3. If invalid, inform user to run `/spec:switch` or `/spec:new`
4. Only proceed if valid

Then continue with implementation:

1. Verify all phases are approved (check for `.requirements-approved`, `.design-approved`, `.tasks-approved` files)
2. If phase number provided ($ARGUMENTS), focus on that phase
3. Read and display current incomplete tasks from tasks.md
4. Create an implementation session log
5. Guide user to:
   - Work on tasks sequentially
   - Update task checkboxes as completed
   - Commit changes regularly
6. Remind about using Write tool to update tasks.md

**CRITICAL - Version Control Rules:**
- ✅ ONLY commit files in `spec/` directory and application directories (`src/`, `apps/`, etc.)
- ⚠️ Ask before updating file `.claude/settings.local.json`
- ❌ NEVER commit `.template/` directory contents
- ❌ NEVER commit or modify files in `.claude/` directory
- ❌ NEVER commit or modify files in `.vscode/` directory  
- ❌ NEVER modify `.gitignore` in the root directory
- ❌ NEVER modify `LICENSE` in the root directory

Start implementing based on the task list!