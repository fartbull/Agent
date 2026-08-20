# Aider Examples

## Example 1: Fix a Bug

```bash
aider

You: The worker pool in src/worker.py has a race condition. The
     shared counter isn't protected by a mutex. Fix it and run:
     python -m pytest tests/
```

## Example 2: Add a Feature

```bash
aider

You: Add a CSV parser to src/utils/parser.py. It should:
     1. Accept a file path
     2. Return a list of dicts
     3. Handle empty files gracefully
     Write tests in tests/test_parser.py. Run: pytest
```

## Example 3: Refactoring with Specific Files

```bash
aider -- src/components/Button.tsx src/components/Card.tsx

You: Refactor these React components to use hooks instead of class
     components. Run: npm test
```

## Example 4: Configuration

`.aider.conf`:

```ini
model = claude-3-5-sonnet-20241022
auto_reload = true
warn_dangerous = true
```

Usage:

```bash
aider --no-approximate  # strict mode
```

## Example 5: Test Generation

```bash
aider

You: Write unit tests for the AuthMiddleware in src/middleware/auth.ts.
     Cover: valid token, expired token, missing token. Run: npm test
```
