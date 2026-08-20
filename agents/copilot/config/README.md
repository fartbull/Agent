# Copilot Configuration

## Configuration Locations

| Location | Scope | Purpose |
|----------|-------|---------|
| VS Code Settings | User/Workspace | Model, features, privacy |
| `.vscode/settings.json` | Project | Project-specific overrides |
| GitHub Copilot web UI | Account | Subscription, preferences |

## VS Code Settings

Settings (JSON):

```json
{
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "markdown": true
  },
  "github.copilot.chat.model": "claude-3.5-sonnet",
  "github.copilot.advanced": {
    "options": {
      "copilot": true
    }
  }
}
```

TODO: Verify exact setting names

## .vscode/settings.json (Project)

```json
{
  "github.copilot.enable": {
    "*": true,
    "plaintext": false
  },
  "github.copilot.inlineSuggestions": {
    "enable": true,
    "showStatusBar": true
  }
}
```

TODO: Verify exact settings

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| N/A | No | Copilot authenticates via GitHub

## CLI Configuration

The CLI tool (`gh copilot`) configuration:

```bash
# Sign in
gh copilot auth login

# Configure proxy (if needed)
# Set in GitHub CLI config
```

TODO: Verify CLI configuration options

## Modes

Copilot has different modes in VS Code:

| Mode | Behavior |
|------|----------|
| **Inline** | Autocomplete suggestions in editor |
| **Chat** | Conversation panel (Chat view) |
| **Agent** | Autonomous coding agent mode |

TODO: Verify mode names

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)
