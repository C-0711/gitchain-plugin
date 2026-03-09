---
description: Push data into GitChain as a new or updated container
---

# Push to GitChain

Create or update a container in the GitChain registry.

## What to do

1. Parse `$ARGUMENTS` for what to push
2. Determine the container type:
   - `product` — product data with specs, pricing, media
   - `memory` — conversation context, decisions, notes
   - `knowledge` — knowledge base entries, documentation
   - `agent` — agent state, capabilities, config
3. Ask for namespace if not obvious
4. Use the `push` MCP tool

## Guidelines

- **Identifier** should be unique within the namespace (article number, slug, etc.)
- **Data** is free-form JSON — structure it logically
- Every push is versioned and blockchain-anchored
- Include a meaningful `message` (like a git commit message)

## Examples

Push a product:
```
push({
  type: "product",
  namespace: "eaton",
  identifier: "5SC750",
  data: { name: "Eaton 5SC 750VA UPS", specs: { ... } },
  message: "Initial product data from catalog"
})
```

Save context:
```
push({
  type: "memory",
  namespace: "pope",
  identifier: "eaton-analysis-2026-03",
  data: { summary: "...", decisions: [...] },
  message: "Session notes from Eaton vault analysis"
})
```
