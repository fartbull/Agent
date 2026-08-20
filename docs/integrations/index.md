# Integrations

Guides for integrating agents with external tools and services.

## GitHub

### Authentication

```bash
# Using gh CLI
gh auth login

# Or with token
export GH_TOKEN="your_token_here"
```

### Common Operations

```bash
# Create a branch
git checkout -b feature/my-feature

# Open a PR
gh pr create --title "My feature" --body "Description"

# Merge a PR
gh pr merge --squash
```

### Automation Patterns

- Use GitHub Actions for CI/CD
- Use issue templates for incoming requests
- Use branch protection rules for code quality

## Docker

### Basic Workflow

```bash
# Build
docker build -t myapp .

# Run
docker run -p 8080:8080 myapp

# Stop
docker stop myapp
```

### Docker Compose

```bash
docker compose up -d
docker compose down
```

## Solana

### Setup

```bash
# Install
sh -c "$(curl -sSfL https://release.solana.com/stable/install)"

# Configure
solana config set --url https://api.mainnet-beta.solana.com
```

### Common Commands

```bash
solana balance
solana address
solana account <PUBKEY>
```

## X API (curl-based posting)

Agents can post tweets and reply to mentions via curl:
- [Full X API guide](x-api.md) — posting, replying, mentions, rate limits
- Uses `xurl`-style curl helpers for social engagement

## MCP (Model Context Protocol)

MCP allows connecting external tools to agents:

```bash
# Install an MCP server
npm install -g @modelcontextprotocol/server-<name>

# Use with compatible agents
```

## Webhooks

For agents that support webhooks:

```bash
# Start a webhook server
./scripts/webhook-server.sh --port 3000 --secret YOUR_SECRET

# Send a webhook
curl -X POST http://localhost:3000/webhook/post \
  -H "Authorization: Bearer YOUR_SECRET" \
  -H "Content-Type: application/json" \
  -d '{"text": "Hello from webhook!"}'
```

## See Also

- [Tool Usage](tools/tool-usage.md)
- [Agent-specific integrations](../../../agents/)
