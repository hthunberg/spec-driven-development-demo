---
allowed-tools: Bash(cat:*), Bash(test:*), Bash(ls:*), Write
description: Create technical design specification
---

## Context

Current spec: !`cat spec/.current-spec 2>/dev/null`
Design template: !`cat ./templates/design.md 2>/dev/null || echo "No template found"`

## Your Task

First, validate the current spec:
1. Read the current spec from the context above
2. Use `ls` to verify the spec directory exists
3. If invalid, inform user to run `/spec:switch` or `/spec:new`
4. Only proceed if valid

Then continue with design phase:

1. Read requirements.md first to understand what needs to be designed
2. Verify requirements are approved (look for `.requirements-approved` file in the spec directory)
3. If not approved, inform user to complete requirements first with `/spec:approve requirements`
4. If template is available in context above, use it as the base structure
5. If approved, create/update design.md with:
   - Architecture overview (with diagrams)
   - Technology stack decisions
   - Data model and schema
   - Interface design:
      * API endpoints (if backend/service)
      * UI/UX design (if frontend/application)
      * CLI commands (if command-line tool)
   - Security considerations:
     * Authentication and authorization
     * Data protection and encryption
     * Input validation and sanitization
     * OWASP Top 10 vulnerabilities mitigation
     * Secure configuration management
   - Performance considerations
   - Deployment architecture
   - Technical risks and mitigations
6. Use ASCII art or mermaid diagrams where helpful

Use the Write tool to create the design document in the correct spec directory.