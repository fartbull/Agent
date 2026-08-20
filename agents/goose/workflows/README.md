# Goose Workflows

## Basic Usage

```bash
# Interactive — chat with Goose
goose

# Non-interactive — run a single task
goose -i "Create a REST API with Flask"

# With specific config
goose -i --config my-config.yaml "task"
```

## Workflow Patterns

### 1. Bug Fix

```bash
goose -i "Fix the memory leak in the Go worker pool. The bug is in
src/worker.go. Run: go test ./..."
```

### 2. Feature Implementation

```bash
goose -i "Add a health check endpoint to the Express app at /health.
Return { status: 'ok' }. Run: npm test"
```

### 3. Codebase Exploration

```bash
goose -i "Find all TODO comments in the codebase and create a summary
report. Save to TODO_REPORT.md"
```

## Extensions

Goose extensions provide additional tools:

```bash
# Start with specific extensions
goose --config config-with-extensions.yaml
```

TODO: Verify extension management commands

## Docker Mode

```bash
docker run --rm -it block/goose \
  -i "fix the bug in src/calculator.py"
```

## See Also

- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Autonomous workflows](../../docs/workflows/autonomous.md)
