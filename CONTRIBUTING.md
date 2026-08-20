# Contributing to FARTBULL Agent

Thanks for your interest in contributing to the FARTBULL universal agent knowledge base.

## How to Contribute

### Reporting Issues

Use the GitHub issue templates:

- **Bug Report** — errors in documentation, broken links, incorrect commands
- **Agent Request** — request support for a new agent
- **Documentation Update** — corrections or additions to existing docs
- **Guide Request** — request a new guide or documentation section

Search existing issues before creating a new one.

### Submitting Changes

1. Fork the repository
2. Create a feature branch: `git checkout -b my-change`
3. Make your changes
4. Validate markdown links (see below)
5. Commit with a clear message
6. Push and open a pull request

### Documentation Standards

- **Tone:** Technical, concise, direct. No marketing fluff.
- **Links:** Use relative links. Verify they resolve.
- **Code blocks:** Always specify the language (`yaml`, `bash`, `json`).
- **Tables:** Use for comparisons, matrices, configs.
- **TODOs:** Write `TODO` or `Needs verification` for unverified claims. Never fabricate.
- **File names:** `kebab-case.md` for docs, `UPPERCASE` for configs.

### When Something Is Unknown

If you're adding docs for a new agent and don't know a detail:

1. **Do not fabricate.**
2. Write: `TODO: Verify [specific claim]` or `Needs verification: [specific detail].`
3. Link to the agent's official documentation if available.

### Adding a New Agent

1. Copy `templates/agent/` to `agents/<new-agent>/`
2. Follow the structure in [AGENTS.md](AGENTS.md)
3. Document what you know; TODO everything else
4. Update `docs/agents.md` (support matrix)
5. Add TODO items to `TODO.md`

## Testing Locally

This is a documentation repository. Validate your changes:

```bash
# Check markdown links (requires markdown-link-check or lychee)
lychee --no-progress --verbose docs/ agents/

# Check for TODO markers
grep -r "TODO" . --include="*.md" | head -20
```

## License

By contributing, you agree that your contributions will be licensed under the license specified in [LICENSE.md](LICENSE.md). The repository owner must select a license — see [LICENSE.md](LICENSE.md) for the current status.
