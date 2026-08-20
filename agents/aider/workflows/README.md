# Aider Workflows

## Basic Usage

```bash
# Start Aider in a project
cd myproject
aider

# Add specific files to context
aider -- /path/to/file1.py /path/to/file2.py

# Use a specific model
aider --model gpt-4o

# Dry run (show changes without applying)
aider --dry-run
```

## Workflow Patterns

### 1. Bug Fix

```bash
aider

You: There's a memory leak in src/allocator.py. The leak happens when
     freeing null pointers. Fix it and run: python -m pytest
```

### 2. Feature with Tests

```bash
aider

You: Add a health check endpoint to the FastAPI app. Create
     src/routes/health.py with GET /health returning {"status": "ok"}.
     Write tests in tests/test_health.py. Run: python -m pytest
```

### 3. Refactor

```bash
aider

You: /add src/utils/
You: Refactor the utils to use modern Python patterns. Add type hints
     everywhere. Run: mypy src/
```

### 4. Exploration

```bash
# Ask questions without editing
You: /ask What does the validate_email function in src/utils.py do?
```

### 5. Commit

```bash
# Aider uses git for undo/redo
You: /run git add -A && git commit -m "Add health check endpoint"
```

## Safety

- Aider shows diffs before editing
- Use `/ask` for read-only questions
- `--dry-run` to preview changes
- Review all changes before committing

## See Also

- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Debugging workflows](../../docs/workflows/debugging.md)
- [Safety principles](../../docs/concepts/safety.md)
