# Goose Setup

## Installation

### Option 1: Install Script (Recommended)

```bash
curl -fsSL https://github.com/block/goose/releases/latest/download/goose-installer.sh | bash
```

TODO: Verify exact URL — this may be outdated. Check [github.com/block/goose/releases](https://github.com/block/goose/releases)

### Option 2: Homebrew (macOS)

```bash
brew install goose
```

TODO: Verify this formula exists

### Option 3: Docker

```bash
docker pull block/goose
```

TODO: Verify Docker image name

### Option 4: Build from Source

```bash
git clone https://github.com/block/goose.git
cd goose
cargo build --release
```

## Requirements

- An API key from a supported provider (Anthropic, OpenAI, Google, etc.)

## Authentication

Set your API key as an environment variable:

```bash
export ANTHROPIC_API_KEY="sk-ant-..."
# or
export OPENAI_API_KEY="sk-..."
# or
export GOOGLE_API_KEY="..."
```

## Verification

```bash
goose --version
goose --help
```

## First Run

```bash
# Interactive mode
goose

# Non-interactive (single task)
goose -i "Create a Python script that parses a CSV file"

# With extensions
goose --config ~/.config/goose/config.yaml
```
