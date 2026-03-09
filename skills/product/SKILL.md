---
description: Generate a comprehensive professional product report from GitChain data
---

# GitChain Product Report

Generate a **complete professional product report** from GitChain container data.

## Process

1. Parse `$ARGUMENTS` for the product (ID, article number, name, or description)
2. If not a container ID → `search` first, pick best match
3. Load the full container with `get`
4. If auto-skeletonized (large product) → drill into ALL sections:
   - `product_container.meta`
   - `product_container.dimensions`
   - `product_container.pricing`
   - `product_container.technical_attributes`
   - `product_container.media`
   - `product_container.sources`
   - `product_container.classifications`
   - For Lightnet: `identity`, `electrical`, `mechanical`, `photometric`, `logistics`, `pricing`
5. Generate the report below

## Output Format — Full Product Report

```
# [Product Name]
**[Manufacturer] | Art.-Nr. [Article Number] | GitChain Container: [ID]**

---

## 1. Produktübersicht
- Hersteller & Marke
- Produktfamilie / Serie
- Kurzbeschreibung (2-3 Sätze, was das Produkt macht und wofür)
- Zielgruppe / Einsatzbereich

## 2. Technische Daten

### Kerndaten
| Merkmal | Wert | Einheit |
|---------|------|---------|
(Alle wichtigen Leistungsdaten — Nennleistung, Spannung, Effizienz, COP, etc.)

### Abmessungen & Gewicht
| Merkmal | Wert |
|---------|------|
| Höhe | ... mm |
| Breite | ... mm |
| Tiefe | ... mm |
| Gewicht | ... kg |
| Verpackungsmaße | ... (falls vorhanden) |

### Klassifizierung
- ETIM-Klasse: [Code] — [Klartext-Bezeichnung]
- UNSPSC: [Code] — [Klartext-Bezeichnung]
- Energieeffizienzklasse: [Label]
- Schutzart: [IP-Rating]

## 3. ETIM-Attribute (vollständig)
Alle ETIM-Features interpretiert mit Klartextnamen:
| ETIM-Code | Attribut | Wert | Einheit |
|-----------|----------|------|---------|
| EFxxxxxx | [Klartext] | [Wert] | [Einheit] |
(ALLE Attribute auflisten, keine auslassen. ETIM-Codes aus Fachwissen übersetzen.)

## 4. Preise & Konditionen
- Werkslistenpreis (netto): [Preis] €
- UVP (brutto): [Preis] € (falls vorhanden)
- Preisbasis / Mengeneinheit
- Rabattgruppe (falls vorhanden)
- Gültig ab: [Datum]

## 5. Medien & Dokumentation
- Produktbilder: [URLs/Referenzen]
- Datenblätter: [PDFs]
- BIM/CAD-Daten: [falls vorhanden]
- Installationsanleitungen: [falls vorhanden]

## 6. Logistik
- EAN/GTIN: [Code]
- Zolltarifnummer: [Code]
- Verpackungseinheit
- Mindestbestellmenge
- Lieferstatus

## 7. Datenherkunft & Verifizierung
- GitChain Container ID: [full ID]
- Version: [v1/v2/...]
- Namespace: [namespace]
- Datenquelle: [Hersteller-Katalog / API / etc.]
- Letztes Update: [Datum]
- Blockchain-Verifizierung: ✅/❌
- Datenqualität: [Vollständigkeit in %]

---
*Bericht generiert aus GitChain | 0711 Intelligence | [Datum]*
```

## Rules
- **ALLE** verfügbaren Daten einfließen lassen — nichts auslassen
- ETIM-Codes IMMER in Klartext übersetzen (EF010933 = COP, EF009442 = Nennheizleistung, etc.)
- Preise immer als netto UND brutto angeben wenn möglich
- Abmessungen immer in mm
- Gewicht in kg
- Bei fehlenden Daten: explizit "Nicht verfügbar" schreiben
- Bericht ist auf DEUTSCH
- Professioneller Ton, kein Marketing-Blabla
- Am Ende: Datenqualität bewerten (wie vollständig sind die Daten im Container?)
