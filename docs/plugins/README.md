# Plugins System

FARTBULL supports plugins for extending agent capabilities beyond built-in skills.

## Overview

Plugins are lightweight extensions that can:
- Add new tool functions to agents
- Intercept and modify agent behavior
- Provide custom MCP (Model Context Protocol) servers
- Extend the agent's tool palette

The original system had 4 core plugins.

## Core Plugin Types

| Plugin | Purpose |
|--------|---------|
| `skill-builder` | Build, package, and publish custom skills |
| `auth-manager` | Manage API keys and authentication tokens |
| `logger` | Structured logging with rotation |
| `scheduler` | Cron-based task execution |

TODO: Verify these plugin names and capabilities against the original codebase.

## MCP Integration

Plugins can expose MCP servers:

```yaml
# Plugin config
plugins:
  - name: "dexscreener"
    type: "mcp"
    command: "npx @modelcontextprotocol/server-dexscreener"
    env:
      - DEX_API_KEY: $DEX_API_KEY
```

## Writing a Plugin

1. Create a new package in `plugins/<plugin-name>/`
2. Define the plugin manifest (`plugin.json`)
3. Implement the plugin entry point
4. Export tool functions or MCP capabilities

```typescript
// Example plugin structure
export const pluginManifest = {
  name: "my-plugin",
  version: "0.1.0",
  tools: ["myTool"],
  mcp: false
};

export async function myTool(params: MyParams): Promise<MyResult> {
  // Implementation
}
```

TODO: Verify TypeScript plugin API format.

## See Also

- [Skills System](skills/README.md)
- [MCP Integration](../integrations/index.md#mcp-model-context-protocol)
- [Agent Templates](../../templates/agent/)
