# Cursor Prompts

Cursor uses natural language prompts in its agent chat interface.

## Prompt Patterns

### Agent Mode

```
Open src/api/handlers.py and find the user auth logic. I need to add
JWT token refresh. Create a refresh endpoint, update the middleware,
and write tests. Run: python -m pytest
```

### Inline Editing

```
# Select code and press Cmd/Ctrl + K
Refactor this to use a dataclass
```

### Chat-Based

```
Can you explain how the rate limiter works in src/middleware/rate_limit.go?
```

## Rule System

Cursor supports two ways to inject persistent context:

1. **`.cursor/rules/` directory** — multiple rule files that match by pattern
2. **`.cursorrules`** — single rule file (legacy)

### Example Rule File

```markdown
# Python Rules

- Use type hints everywhere
- Follow PEP 8
- Run `pytest` after any Python changes
```

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
