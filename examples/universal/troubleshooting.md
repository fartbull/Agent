# Troubleshooting

Common issues when using AI coding agents.

## Agent Won't Start

| Symptom | Likely Cause | Fix |
|---------|-------------|-----|
| "command not found" | Agent not in PATH | Reinstall or add to PATH |
| "No model selected" | API key not configured | Set environment variable |
| "Permission denied" | File system restrictions | Check working directory permissions |

## Agent Doesn't Find Files

| Symptom | Likely Cause | Fix |
|---------|-------------|-----|
| "File not found" | Wrong path | Use `pwd` to check working directory |
| "Cannot read file" | Permissions | Check file is readable: `chmod +r <file>` |
| "Wrong project" | Opened wrong directory | Restart agent in correct project |

## Agent Makes Wrong Changes

| Symptom | Likely Cause | Fix |
|---------|-------------|-----|
| Edits wrong file | Task description unclear | Use explicit file paths |
| Changes too much | Task too vague | Narrow scope: "only change file X" |
| Breaks tests | Didn't run verification | Always specify: "Run: npm test" |

## Agent Runs Forever

| Symptom | Likely Cause | Fix |
|---------|-------------|-----|
| No response | Context limit hit | Use `/compact` (Claude Code) or restart |
| Infinite loop | Vague instructions | Set a timeout, stop and restart |
| Too many turns | Task too open-ended | Use `--max-turns` flag (if available) |

## Model/API Issues

| Error | Meaning | Fix |
|-------|---------|-----|
| `401 Unauthorized` | Invalid API key | Check key is correct and has access |
| `429 Too Many Requests` | Rate limited | Wait, or use a lower-rate model |
| `context_length_exceeded` | Input too long | Reduce context, remove files |

## Getting Help

- Check the agent's [reference docs](../agents/<name>/reference/README.md)
- Run `<agent> --help` for CLI options
- See [FARTBULL docs](../docs/) for universal guidance
