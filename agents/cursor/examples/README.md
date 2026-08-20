# Cursor Examples

## Example 1: Bug Fix via Agent Chat

```
You: There's a memory leak in the worker pool. The goroutine count
     keeps growing. Check src/worker.go and fix it.
     Run: go test ./...
```

## Example 2: Inline Edit

1. Select the code you want to refactor
2. Press Cmd/Ctrl + K
3. Type: `Refactor to use a switch statement`

## Example 3: Test Generation

```
You: Write unit tests for the AuthMiddleware class in
     src/middleware/auth.ts. Cover: valid token, expired token,
     missing token, malformed token. Run: npm test
```

## Example 4: Using Rules

`.cursor/rules/python.md`:

```markdown
- Use type hints
- Follow PEP 8
- Run pytest after changes
```

Prompt:

```
You: Implement a CSV parser in src/utils/parser.py.
     It should read a CSV file and return a list of dicts.
     Write tests and run: python -m pytest
```

## Example 5: CLI Mode

```bash
cursor --cli -i "Add a /api/health endpoint to the Flask app.
  Return { status: 'ok' }. Run: python -m pytest"
```
