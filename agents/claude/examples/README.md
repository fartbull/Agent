# Claude Code Examples

## Example 1: Bug Fix

```bash
# In your project directory:
claude

# Then:
You: There's a memory leak in the worker pool. The goroutine count keeps
     growing. Check src/worker.go and fix it. Run: go test ./...
```

## Example 2: Feature Implementation

```bash
claude

You: I need a CLI tool that converts CSV to JSON. Use Go, package main.
     Accept input file via --input flag, output via --output flag.
     Write tests and run: go test
```

## Example 3: Refactor with CLAUDE.md

```bash
# CLAUDE.md contains:
# Commands: Build: npm run build, Test: npm test
# Style: Use tabs, max 100 chars

claude

You: Refactor the auth middleware to use a decorator pattern. Follow
     the existing code style. Run npm test.
```

## Example 4: Documentation

```bash
claude

You: Write API documentation for the endpoints in src/routes/api.py.
     Include parameter descriptions, response schemas, and examples.
     Place in docs/api.md.
```

## Example 5: Test Generation

```bash
claude

You: Write comprehensive tests for the UserService class in
     src/services/UserService.ts. Cover edge cases, error paths,
     and happy path. Use the test patterns already in test/.
```
