# Aider Setup

## Installation

```bash
pip install aider-chat
```

TODO: Verify if package name is still `aider-chat` (was previously `aider`)

## Requirements

- Python 3.10+
- An API key from a supported provider (Anthropic, OpenAI, Google)
- git (for version control integration)

## Authentication

Set your API key as an environment variable:

```bash
# Anthropic (default)
export ANTHROPIC_API_KEY="sk-ant-..."

# Or OpenAI
export OPENAI_API_KEY="sk-..."

# Or Google
export GOOGLE_API_KEY="..."
```

## Verification

```bash
aider --version
aiter --help
```

## First Run

```bash
# Navigate to your project
cd myproject

# Start Aider
aider

# Or with a specific model file
aider --model sonnet --no-approximate
```

Aider will:
1. Detect git repo (recommended)
2. Show you the list of files to add to context
3. Wait for your prompt
