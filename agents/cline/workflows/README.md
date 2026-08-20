# Cline Workflows

## Basic Usage

1. Install Cline VS Code extension
2. Open your project in VS Code
3. Open the Cline panel in the sidebar
4. Select a model and API key
5. Type your task description
6. Approve or auto-approve Cline's actions

## Workflow Patterns

### 1. Act Mode (Autonomous)

Set mode to "Act" in the dropdown, then:

```
You: Implement a user registration endpoint with email validation,
     password hashing, and database storage. Use the existing patterns
     in src/. Write tests and run: npm test
```

### 2. Ask Mode (Interactive Approval)

Set mode to "Ask", then:

```
You: Fix the memory leak in the worker pool. I want to review each
     change before applying. The bug is in src/worker.go.
```

### 3. With .clinerules

Place `.clinerules` in project root, then:

```
You: Add tests for the payment processing module. Follow the project
     rules in .clinerules. Run: npm test
```

### 4. MCP Integration

```
You: Search the web for the latest security vulnerabilities in
     express.js, then audit our dependencies and update package.json.
```

(TODO: Verify MCP setup process)

## Safety

- Review `.cline/settings.json` for denied commands
- Use Ask mode for sensitive operations
- Check file diffs before saving

## See Also

- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Autonomous workflows](../../docs/workflows/autonomous.md)
- [Safety principles](../../docs/concepts/safety.md)
