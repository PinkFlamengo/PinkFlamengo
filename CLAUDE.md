# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working in this repository.

## Repository Overview

**PinkFlamengo** is a fresh repository currently in initial setup. No source code, framework, or build configuration has been committed yet. This document will be updated as the project evolves.

Current state:
- Empty repository (no commits on main/master)
- Development branch: `claude/add-claude-documentation-tfU5w`
- Remote: configured at origin

---

## Git Workflow

### Branching

- Feature branches must follow the pattern: `claude/<description>-<session-id>`
- Never push directly to `main` or `master`
- Always push to the designated feature branch for the current session

### Commit Messages

Use clear, imperative-style commit messages:

```
Add initial project structure
Fix authentication bug in login handler
Update CLAUDE.md with build instructions
```

Avoid vague messages like "fix stuff" or "WIP".

### Pushing Changes

Always set upstream tracking on first push:

```bash
git push -u origin <branch-name>
```

If a push fails due to a network error, retry with exponential backoff (2s, 4s, 8s, 16s — up to 4 retries).

---

## Development Conventions (to be updated as project grows)

Since this is an empty repository, conventions will be defined as the stack is chosen. When code is added, update this file with:

- Language and framework versions
- Code style and linting rules
- Test framework and how to run tests
- Build commands
- Environment variable requirements

### General Principles (apply regardless of stack)

- Prefer editing existing files over creating new ones
- Keep solutions simple — avoid over-engineering
- Do not add features beyond what is explicitly requested
- Validate inputs at system boundaries (user input, external APIs); trust internal code
- Write secure code: avoid SQL injection, XSS, command injection, and other OWASP Top 10 issues

---

## Working with This Repository

### Before Making Changes

1. Confirm the active branch matches the session's designated branch
2. Pull the latest changes: `git pull origin <branch-name>`
3. Read relevant files before modifying them

### After Making Changes

1. Stage specific files (avoid `git add -A` unless intentional)
2. Write a clear commit message
3. Push to the designated branch

### File Operations

- Use dedicated tools for file reads, edits, and searches rather than shell commands
- Do not create documentation files unless explicitly requested
- Do not add comments or docstrings to code you did not change

---

## CI/CD

No CI/CD pipeline is configured yet. Update this section when workflows are added (GitHub Actions, GitLab CI, CircleCI, etc.).

---

## Environment

- Platform: Linux
- Shell: bash/zsh
- Git remote: `http://local_proxy@127.0.0.1:36584/git/PinkFlamengo/PinkFlamengo`

---

*Last updated: 2026-02-28. Update this file whenever the project structure, stack, or conventions change.*
