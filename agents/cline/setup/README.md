# Cline Setup

## Installation

### VS Code Extension

1. Install the Cline extension from the VS Code marketplace:
   - Extensions → Search "Cline"
   - Or: `code --install-extension cline.cline`

TODO: Verify exact extension ID

### Requirements

- VS Code 1.99+ (TODO: verify minimum version)
- An API key from a supported provider

## Authentication

1. Open VS Code
2. Open the Cline panel (View → Command Palette → "Cline: Open")
3. Click "Settings" (gear icon)
4. Select your API provider and enter your API key

Supported providers:
- Anthropic (Claude)
- OpenAI (GPT)
- Google (Gemini)
- Ollama (local)
- And more

TODO: Verify all supported providers

## First Run

1. Install the extension
2. Open a project folder in VS Code
3. Open Cline panel (bottom sidebar icon)
4. Select a model
5. Start typing tasks

## Modes

| Mode | Behavior |
|------|----------|
| **Ask** | Cline proposes actions, you approve |
| **Act** | Cline executes autonomously |

Switch modes with the dropdown in the Cline panel.
