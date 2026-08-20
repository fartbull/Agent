# Shared Configuration

This directory contains universal default configurations that apply to all agents.

## Files

| File | Purpose |
|------|---------|
| `base.yaml` | Base configuration shared across all agents |
| `safety.yaml` | Safety defaults and guardrails |

## Override Pattern

```
configs/
├── shared/
│   ├── base.yaml      ← universal defaults
│   └── safety.yaml    ← universal safety rules
└── agents/
    ├── pi/            ← Pi-specific overrides
    ├── codex/         ← Codex-specific overrides
    └── claude/        ← Claude-specific overrides
```

## Usage

Each agent folder includes its own `config/README.md` with agent-specific settings. The shared configs provide the baseline defaults.

See `templates/config/config-template.yaml` for the template used to create agent-specific configs.
