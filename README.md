# GitChain Plugin for Claude

**Product data chain for AI agents.** Search, browse, compare, and manage 131K+ verified product containers.

## What's inside

| Skill | Command | Description |
|-------|---------|-------------|
| Search | `/gitchain:search` | Find products by name, spec, or category |
| Product | `/gitchain:product` | Detailed product lookup with drill-down |
| Compare | `/gitchain:compare` | Side-by-side product comparison |
| Catalog | `/gitchain:catalog` | Namespace stats and data overview |
| Push | `/gitchain:push` | Create or update containers |

Plus **5 MCP tools** (search, get, push, context, status) for programmatic access.

## Available Data

| Namespace | Count | Type |
|-----------|-------|------|
| Lightnet | 109,117 | LED Lighting (ETIM-classified) |
| Bosch | 22,435 | Heating & HVAC |
| Eaton | ~100 | Electrical Components |

All containers are **blockchain-verified** with full data provenance.

## Install

```bash
# From 0711 marketplace
/plugin marketplace add C-0711/0711-tools
/plugin install gitchain@0711-tools

# Or directly
/plugin install --plugin-dir ./0711-gitchain-plugin
```

## Requirements

- SSH access to REACTOR (192.168.145.10) — VPN required
- GitChain API running on port 3100
- Node.js on REACTOR for MCP server

## Examples

```
/gitchain:search Bosch heat pump CS7001i
/gitchain:product 0711:product:bosch:8738210257:v1
/gitchain:compare CS7001i AW 7 vs CS7001i AW 13
/gitchain:catalog bosch
/gitchain:push new product data
```

---

Built by **0711 Intelligence** 🔥
