# Copilot Prompts

Copilot uses prompts in two contexts:

1. **Chat** — the Copilot Chat panel (Ctrl/Cmd + Shift + L)
2. **Agent** — the Copilot agent mode (autonomous)

## Prompt Patterns

### Chat Mode (Q&A)

```
What does the validate_email function in src/utils.py do?
```

### Agent Mode (Autonomous)

```
Add a health check endpoint to the Express app at /health.
Return { status: "ok" }. Run: npm test
```

### Inline Suggestions

Type code, and Copilot suggests the rest. Accept with Tab.

### Slash Commands (Chat)

```
/explain    Explain the selected code
/refactor   Refactor the selected code
/fix        Fix the selected code
/document   Add documentation to the selected code
/tests      Write tests for the selected code
```

TODO: Verify exact slash commands available

## Prompting Tips

- Select code for context before asking questions
- Include file paths for navigation: `@file src/routes/api.py`
- Use `#todo` to ask Copilot to complete TODO comments

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
