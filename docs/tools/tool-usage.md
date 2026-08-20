# Tool Usage

Universal guides for common AI agent tools.

## Terminal / Shell Tools

### Navigation

```bash
pwd           # current directory
ls            # list files (prefer `read` tool for directories)
cd            # not needed — set `cwd` on tool call
```

### File Operations

| Tool | Use Case |
|------|----------|
| `read` | Read files, directories, DBs, archives |
| `write` | Create or overwrite files |
| `edit` | Surgical edits to existing files |
| `grep` | Search code with regex |
| `glob` | Find files by pattern |

### Process Management

```bash
# Start a background process
hub start <name> <command>

# Check status
hub jobs

# View logs
hub logs <name>

# Stop
hub stop <name>
```

## Database Tools

### SQLite

```bash
# Read table schema and rows
read db.sqlite:table

# Read specific row by key
read db.sqlite:table:primary_key

# Query with SQL
eval "SELECT * FROM table WHERE condition"
```

## Web Tools

### Browser Automation

```bash
# Open a tab
browser open --url "https://example.com"

# Run JavaScript in the page
browser run --code "document.title"

# Take a screenshot
browser run --code "await tab.screenshot({path: 'page.png'})"
```

### Web Search

```bash
# Search the web
web_search "query" --num_results 10
```

## Language Intelligence

Use `lsp` for:
- Definitions, references, type info
- Code actions (fixups, refactors, quick fixes)
- Rename symbols across files
- File rename with import rewriting

```bash
# Find all references to a symbol
lsp references --file src/module.ts --symbol "functionName"

# Rename a symbol across the codebase
lsp rename --file src/module.ts --symbol "oldName" --new_name "newName"

# Get code actions (quick fixes, refactors)
lsp code_actions --file src/module.ts --line 10 --query "import"
```

## Agent Coordination

Use `task` for independent parallel work:
- Read-only scouts for unknown codebases
- Independent file edits in different modules
- Separate subsystem investigations

```text
tasks[0]: Investigate auth module — agent=scout
tasks[1]: Investigate payment module — agent=scout
```

Use `hub` for inter-agent communication:
- `send` — fire-and-forget message to a peer
- `wait` — block until a specific job finishes
- `jobs` — snapshot of all running tasks

## Shell vs Tool Decision Matrix

| Need | Use |
|------|-----|
| Read a file | `read` tool |
| Search code | `grep` tool |
| Find files | `glob` tool |
| Edit a file | `edit` tool |
| Run a command | `bash` tool |
| Start a service | `hub start` |
| Check references | `lsp references` |
| Rename a symbol | `lsp rename` |

## See Also

- [Safety](../concepts/safety.md)
- [Universal Workflows](../workflows/)
- [Agent-specific tool docs](../../../agents/)
