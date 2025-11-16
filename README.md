# Spec-Driven Development with Claude Code

This project demonstrates a structured approach to AI-assisted software development using specifications as the primary driver. Instead of directly instructing an AI assistant on *how* to code, we describe *what* we want to achieve through structured specifications that guide the entire development workflow.

## About me

I'm a Software Engineer living in Sweden. I have worked with this craft for over 25 years and still think it is one of the most rewarding things there is, and I am passionate about learning new things.

In this project I'm exploring spec-driven development with AI assistants. This is part of my learning journey to understand how structured processes can improve AI-assisted development quality and maintainability.

You can find me at:
- [Callista profile](https://callistaenterprise.se/om/medarbetare/hansthunberg/)
- [GitHub](https://github.com/hthunberg/)

## Getting started

### Prerequisites
```bash
# Install Claude Code CLI
# Follow instructions at: https://docs.claude.com/en/docs/claude-code
```

## Workflow

### Create a new specification
```bash
/spec:new todo-list-api
```

### Generate requirements
```bash
/spec:requirements
/spec:review
/spec:approve requirements
```

### Create technical design
```bash
/spec:design
/spec:review
/spec:approve design
```

### Generate task list
```bash
/spec:tasks
/spec:review
/spec:approve tasks
```

### Start implementation
```bash
/spec:implement
/spec:update-task "Initialize project repository"
```

## Available commands

| Command | Description |
|---------|-------------|
| `/spec:new <name>` | Create a new feature specification |
| `/spec:requirements` | Generate requirements document |
| `/spec:design` | Generate technical design |
| `/spec:tasks` | Generate task breakdown |
| `/spec:review` | Review current phase or implementation |
| `/spec:approve <phase>` | Approve a phase to proceed |
| `/spec:implement` | Start implementing approved tasks |
| `/spec:update-task <name>` | Mark task as complete |
| `/spec:status` | Show all specs and their status |
| `/spec:switch <spec-id>` | Switch to different specification |

## Customizing templates

Edit templates in `./templates/` to match your project needs:

- `requirements.md` - Add your specific requirement sections
- `design.md` - Adjust architecture sections for your stack
- `tasks.md` - Modify phase breakdown structure

## Learn more

Read my [blog post about spec-driven development](https://callistaenterprise.se/blogg/teknik/) for a detailed walkthrough and lessons learned.