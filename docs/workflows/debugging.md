# Debugging Workflows

How to debug issues efficiently with any agent.

## 1. The Debugging Loop

```
1. Observe — what's the actual error/behavior?
2. Reproduce — can you trigger it consistently?
3. Isolate — narrow down the cause
4. Hypothesize — what could be wrong?
5. Test — verify the hypothesis
6. Fix — apply the fix at the source
7. Verify — confirm the fix works
```

## 2. Log Analysis

### Finding Logs

```bash
# Application logs
tail -f logs/app.log

# System logs
journalctl -u <service-name> --no-pager -n 50

# Agent logs
<agent> --version  # Verify agent is working
```

### Log Patterns

- Look for timestamps around when the issue occurred
- Search for error-level entries: `grep -i "error\|fail" logs/`
- Look for patterns: repeated errors, specific user IDs, specific endpoints
- Check for rate limiting, timeouts, auth failures

## 3. Debugging with a Debugger

When a debugger is available:
- Set breakpoints at the suspected code path
- Inspect variable values at runtime
- Step through execution
- Use data breakpoints for state changes

### Debugger Setup

```bash
# Go (Delve)
dlv debug --headless --listen=:2345 --api-version=2

# Node
node --inspect-brk index.js

# Python
python -m pdb script.py
```

## 4. Common Debugging Patterns

### "It works locally but not in production"

- Check environment variables
- Check file paths (relative vs absolute)
- Check permissions
- Check network access
- Check resource limits

### "The test passes but the real call fails"

- Check staging vs production differences
- Check input data format
- Check error handling paths
- Check timeout values

### "It worked yesterday"

- Check for recent deploys
- Check for config changes
- Check for upstream API changes
- Check for rate limit changes

## 5. Verification

After fixing:
- Reproduce the original scenario
- Confirm the fix resolves it
- Run related tests
- Check for regressions

## See Also

- [Research Workflows](research.md)
- [Verification Principles](../concepts/principles.md#verify-your-work)
