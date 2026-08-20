# Codex Examples

## Example 1: Single Task

```bash
codex -p "Fix the null pointer in src/parser.go. Run: go test ./..."
```

## Example 2: Feature Implementation

```bash
codex -p "Add a /health endpoint to the FastAPI app. Return
         { status: 'ok' }. Write tests. Run: python -m pytest"
```

## Example 3: Autonomous Mode

```bash
codex --auto  # Interactive session without approval prompts
```
