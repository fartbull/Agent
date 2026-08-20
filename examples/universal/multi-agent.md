# Multi-Agent Workflows

Using multiple AI coding agents together can be more effective than relying on one.

## When to Chain Agents

- Agent A can't do the task alone (needs different model strengths)
- Agent A did the work but you want Agent B to review
- Different agents excel at different tasks (exploration vs. implementation vs. testing)

## Pattern 1: Exploration → Implementation

```
Step 1 (Agent: Claude Code or Pi):
  "Explore the codebase and tell me how the auth middleware works."

Step 2 (Agent: Aider or Codex):
  "Now implement JWT refresh based on the existing auth in src/auth/"
```

## Pattern 2: Implementation → Review

```
Step 1 (Agent: Cursor or Cline):
  "Implement the health check endpoint in src/app.py"

Step 2 (Agent: Claude Code or Pi):
  "Review the health check endpoint implementation for security issues"
```

## Pattern 3: Bug Fix → Test

```
Step 1 (Agent: Codex or Roo):
  "Fix the memory leak in src/allocator.c"

Step 2 (Agent: Aider):
  "Write a test that reproduces the memory leak, then verify the fix"
```

## Agent Comparison for Tasks

| Task | Best Agents | Reason |
|------|-------------|--------|
| Exploration/reading | Pi, Claude Code | Strong reasoning, good questions |
| Implementation | Aider, Codex, Cline | Strong editing, test running |
| Refactoring | Aider, Cursor | Good at structural changes |
| Review/QA | Pi, Claude Code | Good at catching issues |
| Speed/autonomy | Codex (--auto), Goose | Designed for autonomous execution |

## See Also

- [Agent matrix](docs/agents.md) for agent capabilities
- [Workflow templates](../../templates/workflow/workflow-template.yaml)
