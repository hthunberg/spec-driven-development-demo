---
allowed-tools: Bash(cat:*), Bash(test:*), Bash(ls:*)
description: Review current specification phase or implementation
---

## Context

Current spec: !`cat spec/.current-spec 2>/dev/null`

## Your Task

First, validate the current spec:
1. Read the current spec from the context above
2. Use `ls` to verify the spec directory exists
3. If invalid, inform user to run `/spec:switch` or `/spec:new`
4. Only proceed if valid

Then determine review type based on approval status:

**Check approval files:**
- Use `test -f spec/[current-spec]/.requirements-approved` to check if requirements approved
- Use `test -f spec/[current-spec]/.design-approved` to check if design approved
- Use `test -f spec/[current-spec]/.tasks-approved` to check if tasks approved

### IF ALL THREE PHASES ARE APPROVED (Implementation Review):

All specification documents are approved. It's time to review the implementation against the spec.

**Your Task:**

1. **Analyze the Specification:**
   - Read and understand the full specification:
     - spec/[current-spec]/requirements.md
     - spec/[current-spec]/design.md
     - spec/[current-spec]/tasks.md

2. **Inspect the Code:**
   - Identify and review the code changes that implement this specification
   - Look in the application directory (e.g., /apps/)
   - Use tools to find the relevant commits or diffs if necessary

3. **Verify Compliance:**
   - **Requirements:** Create a checklist from requirements.md and verify that each requirement is met by the code
   - **Design:** Confirm the implementation adheres to the architecture, patterns, and component choices outlined in design.md
   - **Tasks:** Ensure every item in tasks.md is completed and correctly implemented

4. **Deliver Your Review:**
   - Summarize your findings
   - Highlight any deviations, bugs, or areas for improvement
   - If the implementation is solid, provide a confirmation

### IF NOT ALL PHASES ARE APPROVED (Specification Review):

Show approval status using checkmarks and crosses:
- Show which files are approved and which are not
- Display clearly which phase needs review next

**Your Task:**

1. Identify the next document to be reviewed (the first one not yet approved)
2. Display the content of that document
3. Provide a review checklist for the document:
   - Does it meet all criteria for its type?
   - Is it complete, clear, and unambiguous?
   - Are there any missing elements or potential issues?
4. After your review, remind the user how to approve the document if they are satisfied (e.g., `/spec:approve requirements`)