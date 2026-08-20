# Claude Code Configuration

## Two Levels of Configuration

| Location | Scope | Purpose |
|----------|-------|---------|
| `CLAUDE.md` (project root) | Project | Context, instructions, custom commands, memory |
| `~/.claude/settings.json` | Global | Preferences, model, feature flags |

### CLAUDE.md (Project)

The `CLAUDE.md` file in your project root is automatically loaded by Claude Code on startup.

```markdown
# Project Name

## Overview
{Brief project description}

## Commands
- Build: `make build`
- Test: `npm test`
- Lint: `npm run lint`

## Conventions
- Use tabs for indentation
- Max line length: 100 characters
- Follow existing patterns

## Important Files
- `src/main.ts` — entry point
- `README.md` — project docs
```

TODO: Verify exact fields supported in CLAUDE.md

### settings.json (Global)

```json
{
  "model": {
    "claude-sonnet-4-20250514": {},
    "claude-opus-4-20250516": {}
  },
  "features": {
    "file_operations": true,
    "shell_commands": true,
    "web_search": true
  }
}
```

TODO: Verify exact schema for `~/.claude/settings.json`

### Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `ANTHROPIC_API_KEY` | Optional | Alternative to browser auth |

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)
