# Skills System

The FARTBULL skills system provides composable capabilities that agents can use to interact with external services, analyze data, and extend their toolset.

## Overview

Skills are modular packages that define:
- A set of tool functions available to agents
- Input/output types (TypeScript interfaces)
- Authentication requirements
- Error handling patterns

Each skill maps to a specific domain — Binance trading, token research, Solana development, DeFi protocols, etc.

## Available Skills

> The original system had 16 core skills. The expanded catalog below includes all available skills.

### Trading & Finance

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `alpha` | Binance Alpha request | API key + secret |
| `assets` | Binance Assets request | API key + secret |
| `binance` | Binance Spot, Futures, Convert | API key + secret |
| `convert` | Binance Convert request | API key + secret |
| `margin-trading` | Binance Margin trading | API key |
| `simple-earn` | Binance Simple Earn | API key |
| `sub-account` | Binance Sub-account | API key |
| `vip-loan` | Binance VIP Loan | API key |

### Cryptocurrency Data & Research

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `crypto-market-rank` | Market rankings, trending tokens | None |
| `dexscreener-skill` | DEX data, charts | None |
| `gmgn-market` | Price charts, trending tokens | None |
| `gmgn-token` | Token research, security | None |
| `gmgn-portfolio` | Wallet analysis, P&L | None |
| `query-token-info` | Token details, metadata | None |
| `query-token-audit` | Security audit, honeypot check | None |
| `query-address-info` | Wallet balances, positions | None |
| `birdeye-skill` | Birdeye DEX data | None |
| `jupiter-skill` | Jupiter swap routes | None |
| `raydium-skill` | Raydium DEX data | None |
| `meteora-skill` | Meteora DEX data | None |

### Derivatives & DeFi

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `derivatives-trading-coin-futures` | Coin-M futures | API key |
| `derivatives-trading-options` | Options trading | API key |
| `derivatives-trading-portfolio-margin` | Portfolio margin | API key |
| `derivatives-trading-portfolio-margin-pro` | Pro portfolio margin | API key |
| `derivatives-trading-usds-futures` | USDS-margined futures | API key |

### Solana

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `solana-dev` | Solana development (Anchor, CPIs) | None |
| `solana-wallet-skill` | Wallet connection, signing | User wallet |
| `solana-security-checklist` | Security audit checklist | None |
| `solana-testing-strategy` | Testing with Mollusk/LiteSVM | None |
| `solana-idl-codegen` | IDL to client codegen | None |
| `solana-compatibility-matrix` | Version compatibility | None |
| `solana-common-errors` | Error resolution | None |
| `solana-confidential-transfers` | Confidential transfers | None |
| `solana-trading-skill` | Solana trading | None |
| `solana-frontend-kit` | Frontend components | None |
| `bnbchain-mcp-skill` | BNB Chain MCP | None |

### Social & Content

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `square-post` | Post to Binance Square | API key |
| `claude-mem` | Persistent memory | None |
| `trading-signal` | Smart money signals | None |

### Token Launch & Meme Trading

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `gmgn-cooking` | Create meme coins on launchpads | Wallet |
| `gmgn-swap` | Swap tokens | Wallet |
| `gmgn-track` | Track smart money | None |
| `meme-rush` | Meme token lists | None |
| `pumpfun-skill` | Pump.fun integration | None |
| `jelly-skill` | Jelly swap protocol | None |
| `helius-skill` | Helius Solana data | API key |

### Prediction Markets

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `prediction-skill` | Prediction market data | None |
| `polymarket-skill` | Polymarket queries | None |
| `kalshi-skill` | Kalshi market data | None |

### Design

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `impeccable` | Frontend design/audit | None |
| `ui-ux-pro-max` | UI/UX component library | None |

### Utility

| Skill | Purpose | Auth Required |
|-------|---------|---------------|
| `base-skill` | Base skill foundation | None |
| `binance-skills-hub` | Hub for Binance skills | API key |
| `find-skills` | Discover/install skills | None |
| `bnb-trading-skill` | BNB trading | None |
| `bnb-wallet-skill` | BNB wallet | None |

## Skill Lifecycle

1. **Discover** — use `find-skills` to search the catalog
2. **Install** — download and configure the skill
3. **Use** — agent loads skill tools into its context
4. **Extend** — build custom skills using `templates/`

## See Also

- [Plugins System](plugins/README.md)
- [Agent Templates](../../templates/agent/)
- [Configuration System](../../configs/)
- [Tool Usage](docs/tools/tool-usage.md)
