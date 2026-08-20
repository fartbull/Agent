# Roo Setup

## Installation

### VS Code Extension

1. Install the "Roo Code" extension from the VS Code marketplace:
   - Extensions → Search "Roo Code"
   - Or visit: [marketplace.visualstudio.com/items?itemName=RooCode.roo-code](https://marketplace.visualstudio.com/items?itemName=RooCode.roo-code)

TODO: Verify exact extension ID and marketplace URL

### Requirements

- VS Code 1.96+ (TODO: verify minimum version)
- An API key from a supported provider

## Authentication

1. Install the extension
2. Open VS Code Command Palette (Cmd/Ctrl + Shift + P)
3. Run "Roo: Open" to open the Roo panel
4. Click on profile/settings icon
5. Select your API provider and enter your API key

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
3. Open Roo panel (activity bar icon)
4. Select a model
5. Choose a mode (Chat, Code, Debug, Ask)
6. Start typing tasks

## Modes

Roo has four built-in modes:

| Mode | Purpose |
|------|---------|
| **Chat** | Conversational, no file edits |
| **Code** | Full autonomous coding agent |
| **Debug** | Debugging and investigation |
| **Ask** | Answers questions, can also edit files |

See [workflows](workflows/README.md) for how to use each mode effectively.
