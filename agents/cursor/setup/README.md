# Cursor Setup

## Installation

```bash
# macOS
brew install cursor

# Or download from cursor.sh
# https://www.cursor.com/downloads
```

TODO: Verify exact install command

## CLI Mode

```bash
# Install cursor CLI in PATH
cursor --cli install

# Run cursor in headless mode (non-interactive)
cursor --cli -i "task description"
```

TODO: Verify CLI flags and headless mode capabilities

## Authentication

- Create a Cursor account at [cursor.sh](https://cursor.sh)
- Or use your own API keys (Anthropic, OpenAI) in settings:
  - `~/.cursor/settings.json` (TODO: verify)
  - Or through the editor UI: Settings → Cursor → Models

## Verification

```bash
cursor --version
cursor --cli --help
```

## First Run

1. Install Cursor
2. Open your project directory in Cursor
3. Configure your AI model in Settings
4. Open the agent chat (Cmd/Ctrl + L or click the agent icon)
5. Type a task description
