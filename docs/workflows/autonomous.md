# Autonomous Workflows

How to run agents autonomously with proper safeguards.

## 1. The Autonomous Loop

```
Plan → Execute → Verify → Reflect → Repeat
```

### Plan

- Define clear success criteria
- Break into verifiable steps
- Set up monitoring/alerts

### Execute

- Run steps sequentially or in parallel where safe
- Log all actions
- Pause for user input on critical decisions

### Verify

- Check success criteria after each step
- Run tests or validation commands
- Log results

### Reflect

- What worked? What didn't?
- Update the plan based on findings
- Document lessons learned

## 2. Safety Guards

Always include:

- **Rate limiting** — don't hammer APIs
- **Confirmation gates** — ask before destructive actions
- **Rollback plan** — how to undo if something goes wrong
- **Health checks** — verify system state before and after

## 3. Cron and Scheduling

Scheduled autonomous tasks need extra care:

```yaml
# Example: daily report
schedule: "0 8 * * *"  # 8 AM daily
max_duration: "30m"    # timeout
retry: 2               # retry on failure
retry_delay: "5m"      # wait between retries
```

### Rate Limit Awareness

| Action | Typical Limit |
|--------|--------------|
| API calls | 300/min |
| Posts | 300/day |
| Follows | 1000/week |
| DMs | 500/day |

Check and respect the limits of any service you automate against.

## 4. Monitoring

Set up monitoring for autonomous agents:

- **Health check** — is the agent alive?
- **Task tracking** — what ran, when, what result?
- **Alert on failure** — notify on errors
- **Metrics** — success rate, latency, resource usage

```bash
# Example health check
curl -sf http://localhost:8080/health || alert "Agent is down"
```

## 5. Error Handling

### Retry Logic

```yaml
max_retries: 3
backoff: exponential  # 1s, 5s, 25s
retry_for: [timeout, network_error]
```

### Dead Letter Queue

Unrecoverable failures should be logged and set aside for manual review.

## 6. Multi-Account Coordination

When managing multiple accounts:

- Use separate auth tokens per account
- Don't cross-engage (Account A liking Account B's posts)
- Rotate accounts to avoid pattern detection
- Track actions per account

## See Also

- [Research Workflows](research.md)
- [Safety](../concepts/safety.md)
- [Agent-specific cron guides](../../../agents/)
- [X API Integration](../integrations/x-api.md) — curl-based posting and reply automation
