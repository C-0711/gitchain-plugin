---
description: Compare two or more products side by side
---

# Product Comparison

Compare products from GitChain side by side.

## What to do

1. Parse `$ARGUMENTS` for product identifiers (IDs, article numbers, or names)
2. Search and retrieve each product using `search` + `get`
3. For large products, fetch key sections with `path`:
   - Bosch: `product_container.meta`, `product_container.dimensions`, `product_container.pricing`
   - Lightnet: `identity`, `electrical`, `photometric`, `mechanical`, `pricing`
4. Build a comparison table

## Output format

Create a markdown table comparing the products:

| Attribute | Product A | Product B |
|-----------|-----------|-----------|
| Name | ... | ... |
| Article # | ... | ... |
| Price | ... | ... |
| Key Spec 1 | ... | ... |
| Key Spec 2 | ... | ... |

Then add:
- **Key differences** — what sets them apart
- **Recommendation** — which fits what use case

## Example
`/gitchain:compare CS7001i AW 7 vs CS7001i AW 13`
→ Fetch both, compare heating capacity, dimensions, price, COP.
