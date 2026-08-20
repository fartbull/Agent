# Copilot Setup

## Installation

### VS Code Extension

1. Install the "GitHub Copilot" extension from the VS Code marketplace:
   - Extensions → Search "Copilot"
   - Or: `code --install-extension github.copilot`

### JetBrains

1. Install the "GitHub Copilot" plugin:
   - Settings → Plugins → Marketplace → Search "Copilot"

### CLI

```bash
gh extension install github/gh-copilot
```

TODO: Verify CLI installation steps

## Requirements

- GitHub account
- Copilot subscription (trial available)
- VS Code 1.80+ or compatible editor

TODO: Verify minimum VS Code version

## Authentication

### VS Code

1. Install the extension
2. Press Cmd/Ctrl + Shift + P
3. Run "Copilot: Sign in"
4. Follow the browser authentication flow

### CLI

```bash
gh auth login
gh copilot auth login
```

TODO: Verify CLI auth flow

## Verification

```bash
gh copilot --version
```

TODO: Verify VS Code verification command

## First Run

1. Install the extension
2. Authenticate with GitHub
3. Open a project
4. Start typing — Copilot will show suggestions
5. Accept suggestion with Tab, or use `Ctrl/Cmd + Enter` to open chat
