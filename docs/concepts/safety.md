# Safety Principles

Universal safety guidelines for AI agent work.

## Command Safety

### Never Pipe Remote Content to Shell

```bash
# RISKY — executes arbitrary code from the internet
curl -fsSL https://example.com/install.sh | bash

# SAFER — download, inspect, then execute
curl -fsSL https://example.com/install.sh -o install.sh
less install.sh              # review
bash install.sh              # execute
```

### Sanitize User Input in Scripts

Shell scripts that process user input must validate:
- Reject paths with `../` (directory traversal)
- Reject shell metacharacters (`;`, `` ` ``, `$()`, `|`, `&`)
- Use `set -euo pipefail` for fail-fast behavior
- Quote all variable expansions: `"$VAR"` not `$VAR`

### Avoid eval

```bash
# AVOID — eval on user input
eval "$user_command"

# PREFER — explicit argument arrays
cmd=($user_command)   # still risky
"$cmd" "${cmd_args[@]}"  # safer with separate args
```

## Code Safety

### Shell Injection Prevention

- Never interpolate user input into shell command strings
- Use argument arrays instead of shell strings
- Escape or validate all parameters

### Credential Handling

- Never hardcode API keys, tokens, or passwords
- Read from environment variables or secure config
- Use `${VAR:-default}` pattern with defaults
- Document required environment variables
- Set `chmod 600` on files containing secrets

### Destructive Operations

Always require confirmation:
- File deletion (`rm -rf`)
- Database operations
- Network requests
- State changes

## Social Safety (X / Social Media Agents)

- Never promise returns on crypto
- Always include "DYOR" (Do Your Own Research)
- Don't fake metrics or impersonate projects
- Follow platform terms of service
- Don't spam or automate engagement at high frequency

## Agent Safety

- Review before posting (don't auto-publish)
- Respect rate limits
- Ask for confirmation on destructive actions
- Don't execute financial transactions without explicit approval

## See Also

- [Tool Usage](../tools/tool-usage.md)
- [Agent-specific safety rules](../../../agents/)
