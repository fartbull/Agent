# Context Management

Keeping within context window limits while preserving task fidelity.

## Strategies

### Progressive Loading

Load only what's needed for the current step:

```text
Step 1: Read config files (100 tokens)
Step 2: Read module being changed (500 tokens)
Step 3: Make edit (50 tokens in)
Step 4: Read test file (200 tokens)
```

Don't load everything at once.

### Summary Buffers

For large files, read sections and summarize:

```text
File: large-module.ts (5000 lines)
Read lines 1-100: [summarize key exports and types]
Read lines 2000-2100: [summarize the function we need to change]
```

### Scratch Files

Write intermediate findings to a scratch file instead of holding in context:

```bash
# Before starting a refactor
echo "Findings: 15 callsites in 3 files" > .scratch/refactor-plan.md
echo "- src/a.ts:5 callsite" >> .scratch/refactor-plan.md
# ... more findings
# Now read the file when you need it, not before
```

### Token Budgeting

| Phase | Typical Budget |
|-------|---------------|
| Research | 20-30% |
| Planning | 5-10% |
| Implementation | 40-50% |
| Verification | 10-20% |

## Context Patterns

### Pre-loading Checklist

Before editing a file:
1. Have I read it recently? (if not, read the specific section)
2. Do I know the exact lines to change? (if not, find them)
3. Do I understand the patterns used? (if not, read related code)
4. Have I checked for callsites? (if not, search)

### Re-reading Policy

- Re-read after any edit (line numbers shift)
- Re-read when a tool fails (file may have changed)
- Don't re-read as routine validation (trust the tool result)

### Delegation

When delegating to a subagent:
- Pass shared context in `local://` files
- Define the contract clearly (formats, schemas, interfaces)
- Don't duplicate background into individual tasks

## See Also

- [Task Decomposition](task-decomposition.md)
- [Memory](memory.md)
- [Agent-specific context limits](../../../agents/)
