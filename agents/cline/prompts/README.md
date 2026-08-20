# Cline Prompts

Cline takes natural language task descriptions in its chat interface.

## Prompt Patterns

### Basic Task

```
Add a health check endpoint to the Express app at src/server.js.
Return { status: "ok" } with a 200 response. Run: npm test
```

### Bug Fix

```
There's a race condition in src/worker.go around the shared counter.
Add a mutex. Run: go test ./...
```

### Multi-Step

```
I need to refactor the auth module to use JWT. Please:
1. Read src/middleware/auth.js
2. Add JWT implementation in src/utils/jwt.js
3. Update the middleware to use it
4. Write tests
5. Run: npm test
```

## .clinerules Integration

Place `.clinerules` in project root:

```
You are a Go developer working on a microservices project.
- Use Go modules for dependencies
- Follow idiomatic Go patterns
- Run go vet and go test after changes
```

Then just prompt:

```
Add graceful shutdown to the HTTP server in cmd/server/main.go
```

## Modes

| Mode | Use Case |
|------|----------|
| **Ask** | Review each action before it happens |
| **Act** | Fully autonomous execution |

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
