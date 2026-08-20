# Cursor Workflows

## Basic Usage

1. Install Cursor from [cursor.sh](https://cursor.sh)
2. Open your project
3. Open the agent chat (Cmd/Ctrl + L)
4. Type a task description
5. The agent will: read files, edit, run commands, ask for approval

## Workflow Patterns

### 1. Agent Mode (Autonomous)

```
You: Implement a health check endpoint. Add GET /health to
     src/server.js that returns { status: "ok" }. Run: npm test
```

### 2. Inline Edit

1. Select code
2. Press Cmd/Ctrl + K
3. Type instructions
4. Agent shows diff, you accept/reject

### 3. Multi-Step with Rules

Place `.cursor/rules/general.md`:

```markdown
# Project Rules
- Run npm test after all changes
- Use tabs for indentation
- Max line length: 100
```

Then:

```
You: Add a user registration endpoint with email validation
     and password hashing. Follow the project rules.
```

## CLI Mode

```bash
# Headless/non-interactive
cursor --cli -i "Fix the bug in src/parser.py"

# Specify model
cursor --cli --model claude-3-5-sonnet "task"
```

TODO: Verify CLI flag compatibility

## MCP Integration

Cursor supports MCP servers for extended tool access.

TODO: Verify MCP setup process

## See Also

- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Autonomous workflows](../../docs/workflows/autonomous.md)
