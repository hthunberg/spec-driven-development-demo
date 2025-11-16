# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Spec-Driven Development Implementation Guide for Claude Code - a methodology framework providing custom slash commands for structured development workflows. It's not a traditional software project but a process framework.

## Commands

This project uses custom Claude Code slash commands located in `.claude/commands/spec/`:

~~~
/spec:new - Create a new feature specification
/spec:switch - Switch to a different specification
/spec:rename - Rename a specification
/spec:status - Show all specifications and their status
/spec:requirements - Create or review requirements specification
/spec:design - Create technical design specification
/spec:tasks - Create implementation task list
/spec:review - Review current specification phase
/spec:approve - Approve a specification phase
/spec:implement - Start implementation from approved tasks
/spec:update-task - Mark a task as complete
~~~

## Development Workflow

The project enforces a four-phase sequential workflow:

1. Requirements
2. Design 
3. Tasks
4. Implementation

Each phase must be approved before proceeding to the next. Approval creates marker files (e.g., `.requirements-approved`).

## Project Structure

```
spec/                     # All specifications stored here
  001-<name>/            # Each spec has its own directory
    README.md            # Current phase document
    .requirements-approved
    .design-approved
    .tasks-approved
  .current-spec          # Tracks active specification
```

## Key Implementation Notes

- Specs are numbered sequentially (001, 002, etc.)
- Active spec is tracked in `spec/.current-spec`
- Each command has specific tool permissions in its frontmatter
- Custom permissions configured in read only `.claude/settings.local.json`
- Custom templates for requirements, tasks, design etc in `.templates/`
- No build/test commands - this is a methodology project

## Working with Specifications

When implementing features based on a spec:
1. Check current status with `/spec:status`
2. Review the current phase document in `spec/XXX-name/README.md`
3. Follow the approved requirements, design, and task list
4. Update task completion using checkboxes or `/spec:update-task`

## Git Conventions

- Use descriptive commits: `spec(001): complete requirements phase`
- Each phase completion should be committed
- Keep spec documents under version control