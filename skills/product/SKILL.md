---
description: Look up a specific product by ID, name, or article number
---

# Product Lookup

Get detailed product information from GitChain.

## What to do

1. Parse `$ARGUMENTS` — could be a container ID, article number, or product name
2. If it's a full container ID (starts with `0711:`), use `get` directly
3. If it's a name or article number, `search` first, then `get` the best match
4. Products are typically large (100-700KB). The `get` tool auto-skeletons big data.
5. Use the `path` parameter to drill into specific sections:
   - `product_container.meta` — basic info (name, family, manufacturer)
   - `product_container.dimensions` — physical dimensions
   - `product_container.pricing` — prices and conditions
   - `product_container.technical_attributes` — specs
   - `product_container.media` — images and documents
   - `product_container.sources` — data provenance chain
   - For Lightnet: `identity`, `electrical`, `mechanical`, `photometric`, `logistics`

## Output format

Present the product as a structured summary:
- **Name** and article number
- **Manufacturer** and product family
- **Key specs** (most relevant 5-8 attributes)
- **Price** if available
- **Verification status** (blockchain-anchored or not)

If the user asks for more detail on a section, drill in with `path`.
