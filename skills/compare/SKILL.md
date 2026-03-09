---
description: Generate a comprehensive side-by-side product comparison report
---

# GitChain Product Comparison Report

Generate a **full professional comparison report** for two or more products.

## Process

1. Parse `$ARGUMENTS` for products (IDs, names, article numbers)
2. Search and retrieve EACH product fully — drill into all sections with `path`
3. Identify all comparable attributes across products
4. Generate the mega-report below

## Output Format — Comparison Report

```
# Produktvergleich: [Product Family/Category]
**Generiert aus GitChain | [Anzahl] Produkte | [Namespace(s)]**

---

## Zusammenfassung
(3-5 Sätze: Was wird verglichen? Für wen? Kernunterschied in einem Satz.)

## Vergleichstabelle — Kerndaten

| Merkmal | [Produkt A] | [Produkt B] | [Produkt C...] |
|---------|-------------|-------------|-----------------|
| **Art.-Nr.** | | | |
| **Produktfamilie** | | | |
| **Bauart** | | | |

### Leistungsdaten
| Merkmal | [A] | [B] | [C...] | Vorteil |
|---------|-----|-----|--------|---------|
| Nennleistung | | | | ✅ [wer gewinnt] |
| COP / Effizienz | | | | ✅ |
| Max. Vorlauftemp. | | | | ✅ |
| Energielabel | | | | |
(ALLE verfügbaren Leistungsattribute)

### Abmessungen & Installation
| Merkmal | [A] | [B] | [C...] | Vorteil |
|---------|-----|-----|--------|---------|
| Höhe (mm) | | | | |
| Breite (mm) | | | | ✅ kompakter |
| Tiefe (mm) | | | | |
| Gewicht (kg) | | | | ✅ leichter |
| Stellfläche (m²) | | | | |

### Preisvergleich
| | [A] | [B] | [C...] |
|---------|-----|-----|--------|
| Listenpreis netto | | | |
| Preisdifferenz | — | +X € | +X € |
| Preis pro kW | | | |

## ETIM-Attribute im Detail

Vollständiger Vergleich ALLER ETIM-Features:
| ETIM-Code | Attribut | [A] | [B] | [C...] |
|-----------|----------|-----|-----|--------|
(ALLE Features beider/aller Produkte. ETIM-Codes in Klartext.)

## Analyse & Empfehlung

### Stärken pro Produkt
**[Produkt A]:**
- ✅ ...
- ✅ ...

**[Produkt B]:**
- ✅ ...
- ✅ ...

### Schwächen pro Produkt
**[Produkt A]:**
- ❌ ...

**[Produkt B]:**
- ❌ ...

### Einsatzempfehlung
| Anwendungsfall | Empfehlung | Begründung |
|----------------|------------|------------|
| Einfamilienhaus <100m² | [Produkt] | ... |
| Einfamilienhaus >120m² | [Produkt] | ... |
| Altbau mit Radiatoren | [Produkt] | ... |
| Neubau Fußbodenheizung | [Produkt] | ... |

### Preis-Leistungs-Sieger
[Klare Aussage mit Begründung]

### Gesamtsieger
[Klare Aussage mit Begründung]

## Datenqualität
| Produkt | Container ID | Attribute | Vollständigkeit |
|---------|-------------|-----------|-----------------|
| [A] | [ID] | X von Y | XX% |
| [B] | [ID] | X von Y | XX% |

---
*Vergleichsbericht generiert aus GitChain | 0711 Intelligence | [Datum]*
```

## Rules
- **Drill into EVERY section** of each product — don't just use the skeleton
- ETIM codes → Klartext (IMMER)
- Calculate derived metrics: Preis pro kW, Stellfläche (H×B), Leistungsdichte
- "Vorteil" column: mark the winner for each row with ✅
- Empfehlung MUSS konkrete Einsatzfälle nennen — keine leeren Phrasen
- Language: DEUTSCH
- Be opinionated — recommend clearly, don't hedge
