# Claude Code Setup

## Installation

```bash
# macOS (Homebrew)
brew install anthropic/claude/claude

# npm (all platforms)
npm install -g @anthropic-ai/claude-code

# Verify
claude --version
```

TODO: Verify exact install methods from [github.com/anthropics/claude-code](https://github.com/anthropics/claude-code)

## Authentication

```bash
# Claude Code will prompt you to authenticate in the browser
claude
```

Or set your API key:

```bash
export ANTHROPIC_API_KEY="sk-ant-..."
```

TODO: Verify if Claude Code still supports API key auth or requires account login

## Verification

```bash
claude --help
claude --version
```

## First Run

1. Navigate to your project directory
2. Run `claude`
3. Claude Code auto-detects `CLAUDE.md` if present
4. Describe a task in natural language
