# Roo Prompts

Roo takes natural language task descriptions in its panel. Different modes affect behavior.

## Prompt Patterns by Mode

### Code Mode (Autonomous)

```
Refactor the user authentication module to use JWT tokens. Update all
related files in src/auth/. Write tests. Run: npm test
```

### Debug Mode

```
Investigate why the memory usage grows over time in the worker pool.
Check src/workers/ and run: go test -race ./...
```

### Chat Mode (Conversational)

```
Explain how the CI/CD pipeline works in this project.
```

### Ask Mode

```
What are the dependencies defined in package.json? Which ones are
outdated?
```

## .roo/rules/ Integration

Place rule files in `.roo/rules/`:

```markdown
# Code Mode Rules

You are a senior TypeScript developer.
- Use ES modules
- Run `npm test` after all changes
- Use Tailwind CSS for styling
```

Then just prompt in Code mode:

```
Add a CSV export endpoint to the API at /api/export/csv
```

## Switching Modes

Use the dropdown in the Roo panel, or via command:

```
Cmd/Ctrl + Shift + P → "Roo: Switch Mode" → Select mode
```

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
- [Prompting guide](../../docs/concepts/prompting.md)
