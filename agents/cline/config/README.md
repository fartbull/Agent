# Cline Configuration

## Two Levels of Configuration

| Location | Scope | Purpose |
|----------|-------|---------|
| `.clinerules` (project root) | Project | Custom instructions for this project |
| `.cline/settings.json` | Project | Cline settings including allowed commands |
| VS Code Settings | User/Workspace | API keys, default model |

## .clinerules (Project Instructions)

```markdown
# Project Rules for Cline

You are working on a TypeScript project with strict mode enabled.
- Follow existing patterns in src/
- Run `npm test` after all changes
- Max line length: 100 characters
- Use tabs for indentation
```

TODO: Verify exact format — is it markdown or plain text?

## .cline/settings.json (Allowed Commands)

```json
{
  "permissions": {
    "shell": {
      "allowedCommands": ["npm test", "npm run build"],
      "deniedCommands": ["rm -rf", "sudo"]
    },
    "browser": true,
    "mcp": true
  }
}
```

TODO: Verify exact schema for settings.json

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `ANTHROPIC_API_KEY` | If using Anthropic | Claude API key |
| `OPENAI_API_KEY` | If using OpenAI | GPT API key |
| `GOOGLE_API_KEY` | If using Google | Gemini API key |

## VS Code Settings

Settings (JSON):

```json
{
  "cline.apiProvider": "anthropic",
  "cline.apiModel": "claude-3-5-sonnet-20241022",
  "cline.autoApprove": false,
  "cline.allowedCommands": ["npm test"]
}
```

TODO: Verify exact setting names

## Modes

- **Ask mode** — Cline asks for approval on each tool call
- **Act mode** — Cline executes autonomously

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)
