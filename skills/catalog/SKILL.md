---
description: Show catalog statistics, namespaces, and data overview
---

# Catalog Overview

Show what's in the GitChain container registry.

## What to do

1. Use `status` to get system health
2. Use `search` with broad queries per namespace to show what's available
3. If `$ARGUMENTS` specifies a namespace, focus on that one

## Known namespaces and content

| Namespace | Products | Type | Description |
|-----------|----------|------|-------------|
| `lightnet` | 109,117 | LED Lighting | Luminaires, controls, accessories. ETIM-classified. Full provenance. |
| `bosch` | 22,435 | Heating/HVAC | Heat pumps, controllers, boilers, accessories. Rich technical data. |
| `eaton` | ~100 | Electrical | UPS, circuit protection, switchgear. Via Lakehouse sync. |
| `bombas` | 7 | Memory | Agent memory containers. |
| `ctax` | 4 | Knowledge | Knowledge base entries. |

**Total: 131,567 containers** — all blockchain-verified.

## Output format

- System status (healthy/unhealthy, uptime)
- Namespace breakdown with counts
- Example products from requested namespace
- Available data fields per product type

If the user asks about a specific namespace, show 5 example products with `search`.
