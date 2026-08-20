# Goose Prompts

Goose supports both interactive and non-interactive prompting modes.

## Non-Interactive Mode

```bash
# Single task
goose -i "task description"

# With config file
goose -i --config config.yaml "task description"
```

## Prompt Patterns

### Single Task

```
"Fix the null pointer exception in src/parser.py"
```

### Multi-Step Task

```
"Refactor the authentication module to use JWT. Update src/auth.py,
create tests in test/test_auth.py, and run: python -m pytest"
```

### With Developer Instructions

Goose supports a developer prompt (system-level instructions):

```yaml
# In config.yaml
developer: "You are a senior Python developer. Follow PEP 8.
Always run tests after changes."
```

## Interactive Mode

```bash
goose
# Then type natural language
```

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
