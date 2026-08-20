# External Agent Configuration

## Purpose

Template for documenting configuration of any external agent.

## Configuration Template

For any new agent, document:

1. **Config file locations** (global, project)
2. **Config format** (YAML, JSON, TOML, etc.)
3. **Key settings** (model, timeout, etc.)
4. **Environment variables** (API keys, etc.)
5. **CLI flags** (if applicable)

## Template Structure

```markdown
## Config Locations

| File | Scope | Purpose |
|------|-------|---------|
| TODO | TODO | TODO |

## Key Settings

| Setting | Default | Description |
|---------|---------|-------------|
| TODO | TODO | TODO |

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| TODO | TODO | TODO |
```

## See Also

- [Shared config](../../configs/shared/base.yaml)
- [Safety config](../../configs/shared/safety.yaml)
