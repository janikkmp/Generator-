# CLAUDE.md — AI Assistant Guide for Generator-

This file provides context and conventions for AI assistants (Claude, Copilot, etc.)
working in this repository.

---

## Repository Overview

**Project:** Generator-
**Author:** janikkmp
**Status:** Initial / early-stage repository

The repository currently contains only a `README.md`. This file will be updated as
the codebase grows.

---

## Repository Structure

```
Generator-/
├── README.md       # Project title and description
└── CLAUDE.md       # This file — AI assistant guide
```

As new files are added (source code, configuration, tests, etc.), update this
section to reflect the actual layout.

---

## Git Workflow

### Branches

| Branch | Purpose |
|--------|---------|
| `main` / `master` | Stable, production-ready code |
| `claude/<description>-<id>` | AI-assisted feature branches |

### Branch Naming

- AI-generated branches follow the pattern: `claude/<short-description>-<session-id>`
- Human feature branches: `feature/<description>` or `fix/<description>`

### Commit Messages

Write short, imperative commit messages:

```
Add user authentication module
Fix off-by-one error in generator loop
Update README with usage examples
```

- First line: ≤72 characters, imperative mood
- Leave a blank line before any extended description
- Reference issues with `#<number>` when applicable

### Push Convention

Always push with upstream tracking:

```bash
git push -u origin <branch-name>
```

---

## Development Conventions

Because the project is in its initial stage, the following conventions are
placeholders to be confirmed or updated once a technology stack is chosen.

### General Principles

1. **Keep it simple** — prefer straightforward solutions over clever abstractions
2. **No premature optimization** — solve the actual problem first
3. **No dead code** — delete unused files and functions rather than commenting them out
4. **No backwards-compatibility hacks** — change code directly; don't add shims for
   removed functionality
5. **Minimal error handling** — only validate at true system boundaries (user input,
   external APIs), not internal code paths

### Code Style

- Follow the style of the surrounding code in any file you edit
- Do not add docstrings, comments, or type annotations to code you did not change
- Only add comments where the logic is not self-evident

---

## Working with This Repository

### Starting a Session

1. Check current branch: `git branch`
2. Pull latest changes: `git pull origin <branch>`
3. Read any open issues or PR descriptions for context before making changes

### Making Changes

1. Confirm you are on the correct development branch before editing files
2. Prefer editing existing files to creating new ones
3. Mark completed work in the commit message clearly

### Finishing a Session

1. Stage specific files (avoid `git add -A` to prevent accidentally including
   secrets or binaries)
2. Commit with a descriptive message
3. Push: `git push -u origin <branch-name>`

---

## What to Avoid

- **Do not push to `main`/`master` directly** without a pull request
- **Do not force-push** unless explicitly instructed
- **Do not commit secrets** (`.env` files, API keys, credentials)
- **Do not skip pre-commit hooks** (`--no-verify`)
- **Do not add features, refactors, or cleanup** beyond what was explicitly requested
- **Do not create helper utilities or abstractions** for one-time operations

---

## Updating This File

Update `CLAUDE.md` whenever:

- A technology stack or framework is chosen
- New tooling (linters, formatters, test runners) is added
- Directory structure changes significantly
- New team conventions are agreed upon

The goal is to keep this file accurate and useful as a first-read for any AI
assistant starting a session in this repository.
