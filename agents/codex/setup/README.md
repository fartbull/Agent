# Codex Setup

## Installation

```bash
# Via pip (recommended)
pip install codex

# Or from GitHub releases
curl -fsSL https://github.com/openai/codex/releases/latest/download/codex-installer.sh | bash
```

TODO: Verify exact installation method from [github.com/openai/codex](https://github.com/openai/codex)

## Requirements

- Docker (for sandbox execution)
- OpenAI API key (OPENAI_API_KEY)

## Authentication

Set your OpenAI API key as an environment variable:

```bash
export OPENAI_API_KEY="sk-..."
```

TODO: Verify if Codex has its own auth flow or relies solely on OPENAI_API_KEY

## Verification

```bash
codex --version
codex --help
```

## First Run

```bash
# Interactive mode (confirms each step)
codex

# Autonomous mode (runs without confirmation)
codex --auto

# Single task
codex -p "Fix the typo in README.md"
```
