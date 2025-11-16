# Spec-Driven Development with Claude Code

This project investigates a structured approach to AI-assisted software development using specifications as the primary driver. Instead of directly instructing an AI assistant on *how* to code, we describe *what* we want to achieve through structured specifications that guide the entire development workflow.

## Sample specifications included

The `spec/` directory contains a complete example specification for a todo-list API that has been generated through all workflow phases and is ready for implementation:
```
spec/001-todo-app/
├── requirements.md         # Complete requirements with user stories
├── design.md               # Technical design and architecture
└── tasks.md                # Detailed implementation task list
```

This serves as an example showing what a generated specification looks like before the implementation phase begins.

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
/spec:new todo-app
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

## Customizing templates

Edit templates in `./templates/` to match your project needs:

- `requirements.md` - Add your specific requirement sections
- `design.md` - Adjust architecture sections for your stack
- `tasks.md` - Modify phase breakdown structure