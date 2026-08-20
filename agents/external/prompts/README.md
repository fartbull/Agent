# External Agent Prompts

## Purpose

Template for documenting prompt patterns for any external agent.

## Prompt Template

For any new agent, document:

1. **Prompt format** (natural language, structured, slash commands)
2. **Common patterns** (bug fix, feature, refactor)
3. **Slash commands** (if applicable)
4. **Context injection** (rules files, CLAUDE.md equivalent)

## Basic Patterns

### Task Description

```
{description of what you want done}
```

### Bug Fix

```
Fix {issue} in {file}. Run: {command}
```

### Feature

```
Add {feature} to {module}. Run: {command}
```

## See Also

- [Universal prompts](../../docs/prompts/universal-prompts.md)
