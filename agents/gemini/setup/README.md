# Gemini Setup

## Installation

### Gemini CLI

TODO: Verify installation steps. Based on limited info:

```bash
npm install -g @google/gemini-cli
```

or

```bash
curl -fsSL https://gemini-cli.sh | bash
```

TODO: Verify exact install method

## Authentication

```bash
# Authenticate with Google account
gemini auth

# Or set API key
export GOOGLE_API_KEY="..."
```

TODO: Verify auth flow

## Requirements

- Google account or API key
- TODO: Verify system requirements

## Verification

```bash
gemini --version
gemini --help
```

## First Run

```bash
# In a project directory
gemini chat

# Or in autonomous mode
gemini agent "task description"
```

TODO: Verify exact CLI commands
