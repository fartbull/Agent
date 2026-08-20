# Gemini Workflows

## Basic Usage

```bash
# Chat mode
gemini chat

# Agent mode (TODO: verify command)
gemini agent "task description"
```

## Workflow Patterns

### 1. Bug Fix

```
Fix the race condition in src/worker.go. Run: go test ./...
```

### 2. Feature

```
Add a health endpoint to the Express app. Run: npm test
```

## Notes

- Gemini CLI is a newer tool; workflows may evolve rapidly
- Sandbox is enabled by default for safety

TODO: Verify all workflow patterns and CLI flags

## See Also

- [Coding workflows](../../docs/workflows/coding-workflows.md)
