# Roo Workflows

## Basic Usage

1. Install the Roo Code extension
2. Open your project in VS Code
3. Open the Roo panel
4. Select a mode (Code, Chat, Debug, Ask)
5. Type your task
6. Approve or auto-approve actions

## Workflow Patterns

### 1. Code Mode (Autonomous)

Select "Code" mode, then:

```
You: Implement a user registration endpoint with email validation,
     password hashing, and database storage. Use existing patterns in
     src/. Write tests. Run: npm test
```

### 2. Debug Mode (Investigation)

Select "Debug" mode, then:

```
You: Find why the goroutine count grows unbounded. Check src/ for
     missing cleanup in background workers.
```

### 3. Ask Mode (Q&A)

Select "Ask" mode, then:

```
You: Show me all the API routes defined in src/routes/. Group by
     controller.
```

### 4. With Rules

`.roo/rules/code.md`:

```markdown
You are a Go developer. Follow these rules:
- Use Go modules
- Run `go vet` and `go test` after changes
- Follow effective Go patterns
```

Prompt (Code mode):

```
You: Add graceful shutdown to the HTTP server
```

### 5. MCP Integration

```
You: Search the web for recent Rust security advisories and check
     if our dependencies are affected.
```

(TODO: Verify MCP setup process)

## Auto-Approval

To enable auto-approval in Code mode:

(TODO: Verify exact setting path)

## See Also

- [Autonomous workflows](../../docs/workflows/autonomous.md)
- [Debugging workflows](../../docs/workflows/debugging.md)
- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Safety principles](../../docs/concepts/safety.md)
