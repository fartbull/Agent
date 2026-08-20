# Universal Coding Patterns

These patterns work across all supported agents. Each agent may have its own prompt syntax, but the underlying approach is universal.

## Pattern 1: Bug Fix with Reproduction

```
BUG: {describe the bug}
REPRODUCE: {steps to reproduce}
FIX: {what needs to change}
VERIFY: {command to verify}
```

Example:

```
The worker pool in src/worker.go has a race condition. When multiple
goroutines call counter++ simultaneously, the count is inconsistent.

Steps to reproduce:
1. Run the app with 4+ workers
2. Monitor the task count
3. Observe inconsistent values

Fix: add a sync.Mutex around the counter.
Verify: go test -race ./...
```

## Pattern 2: Feature with Tests

```
Add {feature}. Files involved: {file paths}.
Write tests. Run: {test command}
```

Example:

```
Add a POST /api/users endpoint that creates a user with name, email,
and password fields. Validate email format and hash passwords.
Write tests for happy path and validation errors.
Run: python -m pytest tests/test_users.py
```

## Pattern 3: Refactoring

```
Refactor {what to refactor} to use {pattern}.
Follow existing code style. Run: {test/lint command}
```

Example:

```
Refactor src/utils.py to use dataclasses instead of plain dicts.
Maintain backward compatibility. Run: mypy src/ && pytest
```

## Pattern 4: Documentation Generation

```
Write documentation for {file/module}.
Include: overview, parameters, return values, examples.
Save to: {path}
```

## Pattern 5: Dependency Upgrade

```
Upgrade {package} from {version} to {version}.
Check for breaking changes in the migration guide.
Run all tests after. Run: npm test
```

## Best Practices

1. **Be specific** — include file paths, function names, exact commands
2. **Provide context** — explain why, not just what
3. **Include verification** — always specify a command to run
4. **Test boundaries** — mention edge cases to consider
5. **Follow existing patterns** — agents should match your codebase style
