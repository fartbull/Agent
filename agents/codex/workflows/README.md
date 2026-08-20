# Codex Workflows

## Basic Usage

```bash
# Interactive mode — Codex asks for confirmation on each step
codex

# Autonomous mode — runs without asking
codex --auto

# Single task (non-interactive)
codex -p "task description here"
```

## Workflow Patterns

### 1. Bug Fix

```bash
codex -p "Fix the race condition in the worker pool. The bug is in src/worker.go.
Add a mutex around the shared state. Run: go test ./..."
```

### 2. Feature Implementation

```bash
codex -p "Add a /health endpoint to the Express server. Return { status: 'ok' }
with a 200 status code. Add it in src/server.js. Run: npm test"
```

### 3. Codebase Exploration

```bash
codex -p "Find all database queries in the user service and identify any
that are missing indexes. Check src/services/user.go."
```

## Approval Modes

| Mode | Behavior |
|------|----------|
| Default | Confirm each tool call |
| `--auto` | Execute without confirmation |

Use `--auto` with caution. Review the [safety principles](../../docs/concepts/safety.md).

## Docker Sandbox

Codex runs tasks in a Docker container by default:

- Isolated file system (mounted project directory)
- No network access by default (unless needed)
- Sandboxed execution environment

TODO: Verify network access configuration options
