# Agent Configuration Overrides

This directory contains agent-specific configuration overrides that inherit from the shared configs in `../shared/`.

## Structure

```
configs/agents/
├── README.md          ← This file
├── pi.yaml            ← Pi-specific overrides
├── codex.yaml         ← Codex-specific overrides
├── claude.yaml        ← Claude Code overrides
├── gemini.yaml        ← Gemini overrides (needs verification)
├── opencode.yaml      ← OpenCode overrides (needs verification)
├── cursor.yaml        ← Cursor overrides
├── aider.yaml         ← Aider overrides
├── cline.yaml         ← Cline overrides
├── roo.yaml           ← Roo Code overrides
├── goose.yaml         ← Goose overrides
├── copilot.yaml       ← Copilot overrides
└── external.yaml      ← External agent template
```

## Usage

Each agent folder (`agents/<name>/config/`) includes its own documentation. These YAML files provide machine-readable overrides for tooling integration.

## Override Pattern

Agent-specific configs inherit defaults from `configs/shared/base.yaml` and can override any value. Safety rules from `configs/shared/safety.yaml` always apply unless explicitly overridden.

## Brand

FARTBULL — [fartbull.xyz](https://fartbull.xyz)
