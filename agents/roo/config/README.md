# Roo Configuration

## Two Levels of Configuration

| Location | Scope | Purpose |
|----------|-------|---------|
| `.roo/rules/*.md` (project) | Project | Per-mode instruction files |
| `.roo/settings.json` | Project | Permissions and settings |
| VS Code Settings | User/Workspace | API keys, default model |

## .roo/rules/ (Per-Mode Rules)

Roo uses a directory of rule files, each matched to a mode:

```
.roo/
├── rules/
│   ├── code.md      ← applies in Code mode
│   ├── chat.md      ← applies in Chat mode
│   ├── debug.md     ← applies in Debug mode
│   └── ask.md       ← applies in Ask mode
└── settings.json
```

### Example: code.md (Code Mode Rules)

```markdown
# Roo Code Mode Rules

You are an autonomous coding agent. Follow these rules:
- Always read files before editing them
- Run `npm test` after changes
- Use TypeScript strict mode
- Commit with clear messages
```

TODO: Verify if rules are per-mode or universal

## .roo/settings.json

```json
{
  "permissions": {
    "shell": {
      "allowedCommands": ["npm test", "npm run build"],
      "deniedCommands": ["rm -rf", "sudo"]
    },
    "browser": true,
    "mcp": true
  },
  "autoApproval": {
    "enabled": false,
    "delayMs": 0
  }
}
```

TODO: Verify exact schema for settings.json

## VS Code Settings

Configuration is done through VS Code settings.json:

```json
{
  "roo.apiProvider": "anthropic",
  "roo.apiModel": "claude-3-5-sonnet-20241022",
  "roo.mode": "code"
}
```

TODO: Verify exact setting names

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `ANTHROPIC_API_KEY` | If using Anthropic | Claude API key |
| `OPENAI_API_KEY` | If using OpenAI | GPT API key |
| `GOOGLE_API_KEY` | If using Google | Gemini API key |

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)
- [Safety principles](../../docs/concepts/safety.md)
