# Codex Prompts

Codex takes a **task description** as its prompt. It's designed for autonomous coding tasks.

## Prompt Patterns

### Single Task

```
Fix the memory leak in src/allocator.c that occurs when freeing null pointers.
```

### Multi-Step Task

```
Refactor the authentication module to add JWT support. Create a new file
src/auth/jwt.go, update the routes in src/routes/auth.go, and write tests
in src/auth/jwt_test.go. Run the tests after.
```

### Bug Fix with Verification

```
The /api/users endpoint returns 500 for users with no avatar. Steps to reproduce:
1. GET /api/users/123 (test user has no avatar)
2. See 500 Internal Server Error

Fix the issue and run: go test ./src/handlers/...
```

## What Works

- Concise, specific task descriptions
- File paths and line numbers
- Expected vs actual behavior for bugs
- Acceptance criteria

## What to Avoid

- Vague descriptions ("improve the code")
- Assumptions about file structure (specify paths)
- Multi-language tasks in a single prompt

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
