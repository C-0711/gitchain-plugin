---
description: Search GitChain for products, knowledge, or saved contexts
---

# GitChain Search

Search the GitChain container registry for products, knowledge, or saved conversation contexts.

## What to do

1. Use the `search` MCP tool with the user's query: `$ARGUMENTS`
2. If the user mentions a specific manufacturer (Bosch, Eaton, Lightnet), set `namespace` accordingly
3. Show results as a clean list with: **Name**, namespace, type, and container ID
4. If results look relevant, ask if the user wants to drill into a specific product

## Available namespaces
- `bosch` — 22,435 heating/HVAC products (heat pumps, controllers, accessories)
- `lightnet` — 109,117 lighting products (LED luminaires, controls, accessories)
- `eaton` — Electrical components (UPS, circuit protection, switchgear)

## Example queries
- "Bosch heat pump CS7001i" → `search({ query: "CS7001i", namespace: "bosch" })`
- "LED pendant 3000K" → `search({ query: "LED pendant 3000K", namespace: "lightnet" })`
- "UPS 750VA" → `search({ query: "UPS 750VA", namespace: "eaton" })`

Keep output concise. Show max 10 results. Always include the container ID so the user can drill in.
