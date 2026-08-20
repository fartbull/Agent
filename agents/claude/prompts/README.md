# Claude Code Prompts

Claude Code uses natural language prompts in the terminal. It also supports slash commands.

## Slash Commands

| Command | Description |
|---------|-------------|
| `/agent` | Enter agentic mode (multi-step autonomous) |
| `/login` | Authenticate |
| `/model` | Select model (e.g., `claude-3-5-sonnet`) |
| `/help` | Show available commands |
| `/continue` | Resume a previous session |
| `/compact` | Summarize and compact the conversation |

## Prompt Patterns

### Task Description

```
Implement a health check endpoint in the Express app.
Add GET /health to src/routes/api.js that returns { status: "ok" }.
Run the tests after: npm test
```

### With Context

```
I'm working on the user authentication module. I need to add JWT refresh
token rotation. The current auth is in src/middleware/auth.js.

Please:
1. Read the current implementation
2. Add a refresh token endpoint
3. Add token rotation logic
4. Write tests
5. Run: npm test
```

### Chain of Thought

```
Let's build a rate limiter for the API. First, explore the existing
middleware. Then implement a token bucket algorithm. Test it
against the existing test suite.
```

## CLAUDE.md Integration

Use `CLAUDE.md` to set context once:

```markdown
# My Project

I use TypeScript with Express. My test runner is jest.
Standard patterns: dependency injection, async/await.

## Tasks
Always run `npm test` after changes.
```

Then just prompt:

```
Add a user registration endpoint with email validation and password hashing.
```

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
