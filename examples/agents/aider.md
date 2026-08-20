# Aider Examples

## Example 1: Bug Fix

```bash
aider -- /path/to/src/parser.py
# Then: Fix the null pointer exception in parse()
```

## Example 2: Add to Context

```bash
aider -- src/utils.py src/models/user.py
# Then: Add a validate_email function to utils.py
```

## Example 3: Dry Run

```bash
aider --dry-run -- "refactor to use dataclasses"
```
