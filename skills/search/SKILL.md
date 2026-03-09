---
description: Search GitChain and present structured results with key specs and prices
---

# GitChain Search

Search the GitChain container registry and present rich, actionable results.

## Process

1. Use `search` MCP tool with user's query from `$ARGUMENTS`
2. If manufacturer mentioned (Bosch, Eaton, Lightnet) → set `namespace`
3. For each result in top 5-10: load key data with `get` using `path` parameter
4. Present as structured table

## Output Format

```
# Suchergebnisse: "[Query]"
**[X] Treffer in [Namespace] | GitChain Registry**

| # | Produkt | Art.-Nr. | Serie | Preis (netto) | Kernmerkmal | Container ID |
|---|---------|----------|-------|---------------|-------------|--------------|
| 1 | [Name] | [Nr] | [Serie] | [€] | [wichtigstes Spec] | `0711:...:v1` |
| 2 | ... | | | | | |

### Schnellübersicht
- **Preisrange:** [min] — [max] €
- **Serien:** [Liste der gefundenen Serien]
- **Verfügbare Daten:** Specs ✅ | Preise ✅ | Medien ✅/❌ | ETIM ✅

💡 *Für Detailbericht: `/gitchain:product [Art.-Nr.]`*
💡 *Für Vergleich: `/gitchain:compare [Nr. A] vs [Nr. B]`*
```

## Rules
- Load at least key specs + price for each result (use `get` with `path`)
- Always show prices when available
- Always include container ID for drill-down
- Suggest next actions (product detail, comparison)
- Language: DEUTSCH
- Max 10 results
