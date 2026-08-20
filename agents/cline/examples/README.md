# Cline Examples

## Example 1: Bug Fix (Ask Mode)

```
You: Fix the null pointer exception in src/parser.py. I want to
     review each change. Run: pytest after fixing.
```

## Example 2: Feature Implementation (Act Mode)

```
You: Add a CSV export function to the analytics module. Create
     src/analytics/export.py with export_csv(data, outfile).
     Write tests. Run: python -m pytest
```

## Example 3: With .clinerules

`.clinerules`:

```
You are a React developer. Use TypeScript. Follow the patterns
in src/components/. Run npm test after changes.
```

Prompt:

```
You: Create a DataTable component that supports sorting, filtering,
and pagination. Use Tailwind CSS for styling.
```

## Example 4: Codebase Exploration

```
You: Find all files in src/ that import the old auth module.
     List them and tell me which ones need to be updated to use
     the new JWT module.
```

## Example 5: MCP Tools

```
You: Search for "solana airdrop checklist 2024" and create a
     markdown checklist based on your findings. Save to
     docs/airdrop-checklist.md.
```
