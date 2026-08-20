# Cursor Configuration

## Two Levels of Rules

| Location | Scope | Purpose |
|----------|-------|---------|
| `.cursorrules` (project root) | Project | Legacy rules format (single file) |
| `.cursor/rules/*.md` | Project | Current rules format (multiple files) |
| Editor settings | User | Model, API keys, UI preferences |

## .cursor/rules/ (Current Format)

```text
.cursor/
├── rules/
│   ├── general.md          ← applies to all files
│   ├── python.md           ← applies to .py files
│   └── frontend.md         ← applies to frontend files
└── mcp.json                ← MCP server config
```

### Example: general.md

```markdown
# Project Rules

- Use TypeScript with strict mode
- Run `npm test` after all changes
- Follow existing patterns in src/
```

TODO: Verify the exact rule matching mechanism (file path patterns, etc.)

## .cursorrules (Legacy)

```
You are working on a TypeScript project. Use strict mode. Always run tests
after changes. Follow existing code patterns.
```

## MCP Configuration

TODO: Verify MCP config format and location

```json
// .cursor/mcp.json
{
  "mcpServers": {
    "brave-search": {
      "command": "npx",
      "args": ["-3", "@modelcontextprotocol/server-brave-search"],
      "env": {
        "BRAVE_API_KEY": "YOUR_KEY"
      }
    }
  }
}
```

## Editor Settings

Settings are managed through:
- VS Code Settings UI (Cmd/Ctrl + ,)
- `~/.cursor/settings.json` (TODO: verify location)

Key settings:
- Default model (Claude, GPT, etc.)
- API keys
- Auto-complete behavior
- Privacy settings

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)
