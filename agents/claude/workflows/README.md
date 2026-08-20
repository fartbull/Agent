# Claude Code Workflows

## Basic Usage

```bash
# Start Claude Code in a project
cd myproject
claude

# Then type natural language tasks
# Or use slash commands
```

## Workflow Patterns

### 1. Agentic Mode

```
You: /agent Build a REST API with Express that has CRUD for posts.
     Use SQLite for storage. Write tests. Run them.
```

Claude Code will autonomously:
1. Create the project structure
2. Install dependencies
3. Write the code
4. Write tests
5. Run tests
6. Report results

### 2. Interactive Mode

```
You: Read src/utils.py and tell me what the validate_email function does.
```

Good for quick questions, code reading, explanations.

### 3. Resume Session

```bash
claude --continue
```

Resumes from the last session in this project.

### 4. Compact Conversation

```
You: /compact
```

Summarizes the conversation to save context, then continues.

## Built-in Tools

Claude Code has integrated tools equivalent to:

| FARTBULL Tool | Claude Code Equivalent |
|---------------|----------------------|
| File system | Built-in (read/write/edit) |
| Bash | Built-in (shell tool) |
| Web search | Built-in (web_search) |
| Browser | Built-in (browser tool) |
| Grep | Built-in (grep tool) |
| Glob | Built-in (glob tool) |
| LSP | Partial (code navigation) |

## Safety

- Claude Code asks for approval before destructive actions
- Review changes before committing
- Use `.clinerules` or `CLAUDE.md` to set guardrails

## See Also

- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Autonomous workflows](../../docs/workflows/autonomous.md)
- [Safety principles](../../docs/concepts/safety.md)
