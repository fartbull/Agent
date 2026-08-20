# Copilot Workflows

## Basic Usage

### Editor Integration (Inline)

1. Open a file in VS Code
2. Start typing code
3. Copilot shows inline suggestions (ghost text)
4. Accept with `Tab`, reject with `Esc`

### Chat Mode

1. Open Copilot Chat (`Ctrl/Cmd + Shift + L`)
2. Type a natural language question or task
3. Copilot responds or takes action

### Agent Mode

1. Open Copilot Chat
2. Switch to "Agent" mode (dropdown)
3. Describe a multi-step task
4. Copilot works through it autonomously

## Workflow Patterns

### 1. Bug Fix (Agent Mode)

```
Fix the null pointer exception in src/parser.py. Run: pytest
```

### 2. Feature (Agent Mode)

```
Add a CSV export endpoint at /api/export. Use the existing patterns.
Write tests. Run: npm test
```

### 3. Code Explanation (Chat Mode)

Select a function and type:

```
Explain this function
```

### 4. CLI Usage

```bash
# Get command suggestions
gh copilot suggest "git"

# Get shell explanations
gh copilot explain "git reset --hard HEAD~1"
```

TODO: Verify CLI commands

## Safety

- Review all changes before committing
- Use Ask mode (Chat) for sensitive operations
- Copilot does not have explicit sandbox mode

## See Also

- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Debugging workflows](../../docs/workflows/debugging.md)
- [Safety principles](../../docs/concepts/safety.md)
