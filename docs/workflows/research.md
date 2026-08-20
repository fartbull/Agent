# Research Workflows

How to research, investigate, and gather information with any agent.

## 1. Codebase Investigation

### Mapping Structure

```bash
# Use glob for structure, not `find`
glob "src/**/*.ts"

# Use grep for symbol lookup
grep "function_name" src/

# Use LSP for references, definitions, type info
lsp references src/module.ts
lsp definition src/module.ts:10
```

### Reading Strategy

- Read only what's necessary — don't load entire files blindly
- Use `read` with offset/limit for large files
- Read sections, not entire files, when possible

### Pattern Identification

1. Find 2-3 existing examples of the pattern you need
2. Read the code around those examples
3. Identify the conventions (naming, imports, structure)
4. Follow the same patterns

## 2. External Research

Use web search to:
- Find primary sources (official docs, RFCs)
- Corroborate claims with multiple sources
- Check latest version numbers and API changes

```bash
web_search "typescript strict mode best practices 2024"
```

## 3. Investigation Pattern

```
Question: "How does the auth module work?"

1. glob "src/auth/**/*"          → find files
2. read src/auth/index.ts         → understand entry point
3. grep "AuthService" src/        → find callsites
4. lsp references AuthService     → find all usages
5. read tests/test_auth.py        → understand expected behavior
```

## 4. Data Investigation

For databases and data stores:
- Use `read` with selectors: `db.sqlite:users:42`
- Use direct SQL via `eval`: `read("SELECT * FROM users WHERE active = 1")`
- Check schema before querying data

## 5. When to Stop Researching

- You have enough context to implement the change
- You've identified the pattern and its callsites
- You know how to verify your work

Don't over-research. The 80/20 rule applies: 20% more research rarely fixes the remaining 20% of uncertainty.

## See Also

- [Debugging Workflows](debugging.md)
- [Tool Usage](../tools/tool-usage.md)
- [Agent Investigation Guides](../../../agents/)
