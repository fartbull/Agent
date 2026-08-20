# Aider Prompts

Aider works through a chat interface in the terminal. You describe what you want, and Aider proposes edits.

## Prompt Patterns

### Basic Task

```
Add input validation to the login endpoint in src/auth.py
```

### Bug Fix

```
There's a null pointer exception in the parser. It happens when the
input is an empty string. Fix it in src/parser.py.
```

### Feature Implementation

```
Add a CSV export function to the analytics module. Create
src/analytics/export.py with a function export_csv(data, outfile).
Run: python -m pytest
```

### Refactoring

```
Refactor src/utils.py to use type hints and dataclasses.
Update all callers. Run: mypy src/
```

## Slash Commands

| Command | Description |
|---------|-------------|
| `/add` | Add files to context |
| `/drop` | Remove files from context |
| `/ask` | Ask a question (no editing) |
| `/run` | Run a shell command |
| `/model` | Switch model |
| `/help` | Show all commands |
| `/exit` | Quit Aider |

## Example Session

```bash
aider
# Adding files: src/main.py src/utils.py
# You: Fix the type annotation in main.py
# Aider: Shows diff → you accept or reject
# You: /run python -m pytest tests/
```

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
