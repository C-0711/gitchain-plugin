---
description: Generate a full catalog analysis report for a namespace or the entire registry
---

# GitChain Catalog Analysis Report

Generate a **comprehensive catalog analysis** for a namespace or the full registry.

## Process

1. Use `status` for system health and totals
2. Use `search` with broad queries per namespace to sample products
3. If `$ARGUMENTS` names a specific namespace, deep-dive that one
4. For deep-dive: search multiple product families, load 3-5 example products, analyze data quality

## Output Format — Catalog Report

```
# GitChain Kataloganalyse: [Namespace / "Gesamtbestand"]
**Stand: [Datum] | [Anzahl] Container | Blockchain-verifiziert**

---

## 1. Bestandsübersicht

| Namespace | Container | Typ | Hersteller | Datenquelle |
|-----------|-----------|-----|------------|-------------|
| lightnet | 109.117 | LED Beleuchtung | Lightnet GmbH | Herstellerkatalog |
| bosch | 22.435 | Heizung/HVAC | Bosch Thermotechnik | BMEcat + ETIM |
| eaton | ~100 | Elektrotechnik | Eaton Corp. | Lakehouse Sync |
| Total | **131.567** | | | |

## 2. Namespace Deep-Dive: [Namespace]

### Produktfamilien
| Familie/Serie | Anzahl | Preisrange | Beispiel |
|---------------|--------|------------|----------|
| [Serie A] | X | XX - XX € | [Artikelnr.] |
| [Serie B] | X | XX - XX € | [Artikelnr.] |

### Datenstruktur
- Attribute pro Produkt: Ø [Zahl]
- ETIM-klassifiziert: [X]%
- Mit Preisdaten: [X]%
- Mit Abmessungen: [X]%
- Mit Medien/Bildern: [X]%

### Preisanalyse
- Günstigstes Produkt: [Name] — [Preis] €
- Teuerstes Produkt: [Name] — [Preis] €
- Durchschnittspreis: [Preis] €
- Median: [Preis] €

### Top-Kategorien (ETIM-Klassen)
| ETIM-Klasse | Bezeichnung | Anzahl Produkte |
|-------------|-------------|-----------------|
| ECxxxxxx | [Klartext] | X |

### Beispielprodukte (3-5 geladen)
Für jedes Beispiel: Kurzsteckbrief mit Name, Art.-Nr., Kernspecs, Preis.

## 3. Datenqualität

| Metrik | Wert | Bewertung |
|--------|------|-----------|
| Vollständigkeit | XX% | ⭐⭐⭐⭐⭐ |
| ETIM-Abdeckung | XX% | ⭐⭐⭐⭐ |
| Preisdaten | XX% | ⭐⭐⭐ |
| Medien | XX% | ⭐⭐ |
| Blockchain-Status | XX% | ⭐⭐⭐⭐⭐ |

## 4. Nutzungsempfehlung

Wofür eignet sich dieser Katalog:
- ✅ B2B Datenverteilung (BMEcat/ETIM Export)
- ✅ Produktvergleiche und Beratung
- ✅ ERP/PIM-Integration
- ❌/✅ Endkundenportal (Medien-Vollständigkeit?)

---
*Kataloganalyse aus GitChain | 0711 Intelligence | [Datum]*
```

## Rules
- Load real example products to show actual data depth
- Calculate real percentages where possible
- Be honest about data gaps
- Language: DEUTSCH
