---
allowed-tools: Bash(ls:*), Bash(cat:*), Bash(grep:*), Bash(test:*)
description: Show all specifications and their status
---

## Gather Status Information

All specs: !`ls -d spec/*/ 2>/dev/null | sort`
Current spec: !`cat spec/.current-spec 2>/dev/null || echo "None"`

## Your Task

Present a clear status report showing:

1. **All specifications with their IDs and names**
   - List each directory from the "All specs" output above
   - Extract ID and feature name from directory names

2. **Current active spec (highlighted)**
   - Mark the current spec from the "Current spec" output above
   - Show it prominently (e.g., with → arrow or **bold**)

3. **Phase completion status for each spec**
   - For each spec directory, check for:
     - `requirements.md` and `.requirements-approved`
     - `design.md` and `.design-approved`
     - `tasks.md` and `.tasks-approved`
   - Show which phases exist and which are approved

4. **Task progress percentage**
   - For specs with `tasks.md`, count:
     - Total tasks: lines matching `^- \[`
     - Completed: lines matching `^- \[x\]`
   - Calculate and show percentage

5. **Recommended next action for active spec**
   - Based on approval status, suggest next command to run

Use the Bash tools to read individual files as needed to gather this information.