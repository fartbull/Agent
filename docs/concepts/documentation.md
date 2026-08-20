# Documentation Conventions

How to write docs that work for both humans and AI agents.

## Writing Style

- **Be concise.** Cut filler. Lead with the conclusion.
- **Be technical.** Use exact paths, line numbers, API names.
- **Be direct.** No marketing language. No hedging.
- **Be specific.** "Use `pip install`" not "Install the package".

## Structure

Every doc should follow this pattern:

```markdown
# Title

One-line summary of what this covers.

## Section 1

## Section 2

## See Also
- [Link](relative-path.md)
```

## Code Blocks

Always specify the language:

```bash
pip install requests
```

```yaml
model: gpt-4
temperature: 0.7
```

Don't use bare ``` blocks — AI agents can't tell if they're code or prose.

## Links

- Use **relative links** for internal references
- Use **absolute links** for external URLs
- Test all links before committing
- Link to the most specific anchor, not the document root

## Tables

Use tables for:

- Comparisons (`\| Agent | Setup | Config \|`)
- Configurations (`\| Key | Default | Description \|`)
- Reference material (`\| Command | Action \|`)

## Examples

Every abstract concept should have a concrete example:

```text
Bad: "Use environment variables for secrets"
Good:
export DATABASE_URL="postgres://user:pass@localhost/db"
# In code: process.env.DATABASE_URL
```

## TODO Markers

When something is unknown or unverified:

```markdown
TODO: Verify the exact command for `openai api models`
Needs verification: Whether `goose config` reads from ~/.config/goose/
```

Never fake a working example. A TODO is better than a broken command.

## Internal Navigation

Add a "See Also" section at the end of every doc linking to related content.

## Versioning

Note version requirements where relevant:

> Requires Node.js 18+ and npm 9+

## See Also

- [Project Structure](project-structure.md)
- [Safety](safety.md)
- [Agent Documentation Style](../../../agents/)
