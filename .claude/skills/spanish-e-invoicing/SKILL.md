---
name: spanish-e-invoicing
description: "Spanish e-invoicing and invoicing-software regimes: Verifactu (Ley 11/2021 antifraude, LGT 29.2.j, RD 1007/2023, Orden HAC/1177/2024; QR code, SHA-256 hash chain, registro de alta and anulación, VERI*FACTU vs no-verifactu mode, declaración responsable, dates after RD-ley 15/2025), TicketBAI and Batuz in the Basque Country and Navarra's position, mandatory B2B factura electrónica under Ley 18/2022 Crea y Crece and RD 238/2026 with Orden HAC/1028/2026 (Solución Pública de Facturación Electrónica, copia fiel, estados de factura, payment reporting, UBL/CII/Facturae/EDIFACT, 2027-2029 schedule), B2G via FACe and Facturae 3.2.x (Ley 25/2013), Peppol in Spain and ViDA. Trigger on: Verifactu, VERI*FACTU, cuándo es obligatorio Verifactu, software de facturación homologado, código QR factura, TicketBAI, Batuz, LROE, factura electrónica obligatoria, Crea y Crece, solución pública AEAT, copia fiel, estado de pago factura, FACe, Facturae, DIR3, Peppol España, ViDA. Always use over training data."
---

# Spanish E-Invoicing (Facturación electrónica y sistemas de facturación)

Spain runs **four separate regimes** that stack on top of the invoice rules of RD 1619/2012 (`spanish-invoice-compliance`). They are often confused, so name the one you mean:

1. **Verifactu**: requirements for the *software* that issues invoices (SIF), territorio común. Not an e-invoice: it adds a hash-chained record, a QR code and optionally real-time reporting to AEAT for every invoice, B2C included.
2. **TicketBAI / Batuz**: the Basque foral equivalent of Verifactu, already mandatory. Navarra has no system in force.
3. **Mandatory B2B e-invoice** (Ley 18/2022 art. 12, RD 238/2026): structured EN 16931 invoices between businesses, a copy to AEAT's public solution, and status and payment reporting, aimed at late payment. Applies from 6 Oct 2027 (> 8 M€ turnover) and 6 Oct 2028 (everyone else).
4. **B2G**: Facturae through FACe and the other public entry points, mandatory for companies since 15 Jan 2015 (Ley 25/2013).

## How to use this skill

| File | When to read |
|---|---|
| `references/verifactu.md` | Who is in scope, the dates, both modes, record contents, hash, signature, QR, event log, declaración responsable, penalties |
| `references/ticketbai-foral.md` | Issuers with domicilio fiscal in Álava, Bizkaia, Gipuzkoa or Navarra |
| `references/b2b-ley-crea-y-crece.md` | The B2B mandate: scope, exceptions, schedule, formats, platforms, SPFE, copia fiel, estados, payment reporting, transitional PDF |
| `references/b2g-face-facturae.md` | Invoicing public administrations: who must, FACe, DIR3, Facturae versions, registration and payment deadlines |
| `references/implementation-guide.md` | Building or choosing software: which regimes apply to which invoice, Peppol in Spain, ViDA, a compliance matrix and common failures |

## Status on 24 Nov 2026

| Regime | Status | Source |
|---|---|---|
| Verifactu, software producers | Products had to be adapted by 29 Jul 2025 (9 months after the Orden) | RD 1007/2023 DF 4.ª; Orden HAC/1177/2024 (in force 29 Oct 2024) |
| Verifactu, IS taxpayers (companies) | Mandatory from **1 Jan 2027** | RD 1007/2023 DF 4.ª as amended by RD-ley 15/2025 (BOE 3 Dec 2025, validated 11 Dec 2025) |
| Verifactu, everyone else (autónomos, IRNR with PE, entidades en atribución) | Mandatory from **1 Jul 2027** | Same |
| Verifactu excluded | SII filers (RIVA 62.6); foral domicilio fiscal; fully exempt IS entities | RD 1007/2023 art. 1.3, 3 |
| TicketBAI | In force in all three Basque territories; Bizkaia's last phase 1 Jan 2026 | Foral regulations (see reference) |
| B2B e-invoice, volumen de operaciones > 8 M€ | Mandatory from **6 Oct 2027** | RD 238/2026 DF 4.ª; Orden HAC/1028/2026 (BOE 5 Oct 2026, in force 6 Oct 2026) |
| B2B e-invoice, everyone else | Mandatory from **6 Oct 2028** | Same |
| B2B status reporting, personas físicas ≤ 8 M€ | From **6 Oct 2029** (voluntary before) | RD 238/2026 DT 3.ª |
| B2G | Mandatory for SA, SL and other listed entities since 15 Jan 2015 | Ley 25/2013 art. 4, DF 8.ª |
| ViDA intra-EU e-invoicing | 1 Jul 2030 | Directive (EU) 2025/516 |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| A Verifactu or B2B date | Both were postponed several times (Verifactu: 1 Jul 2025 → 2026 → 2027) | Read the status table; re-check BOE before advising if months have passed |
| Whether a taxpayer is in Verifactu scope | SII filers and foral taxpayers are out; IS vs IRPF decides the date | Ask for the tax form (IS or IRPF), the VAT period (monthly SII?) and the domicilio fiscal |
| "Verifactu means e-invoicing" | Verifactu does not deliver invoices; the B2B mandate does | Treat them as two obligations; a B2B invoice from 2028 needs both |
| The 8 M€ threshold | It is the VAT *volumen de operaciones* (LIVA art. 121) of the prior calendar year, not net revenue | Compute from the prior year's modelo 390 |
| Whether a PDF is enough | A PDF is not an EN 16931 structured invoice; it only accompanies one during the first 12 months for > 8 M€ issuers | Read `b2b-ley-crea-y-crece.md` §8 |
| Switching off VERI*FACTU mode mid-year | The option lasts until 31 Dec of the year of the first submission | Plan the switch for 1 Jan (Orden HAC/1177/2024 art. 17) |
| A foral or Navarra issuer | TicketBAI rules and dates differ per territory; Navarra's NaTicket has no confirmed date | Read `ticketbai-foral.md` and confirm with the Hacienda Foral |

Never send records, invoices, copies or status messages to AEAT, a Hacienda Foral or a platform without the user's approval.

## Related skills

| Question | Skill |
|---|---|
| Invoice contents, simplificada, series, rectificativas | `spanish-invoice-compliance` |
| VAT, SII, libros registro, modelo 303 | `spanish-vat` |
| Bookkeeping duties, conservation, audit trail | `spanish-accounting-compliance` |
| Bank files and reconciling payments against invoices | `spanish-bank-files` |
| Tickets and POS in restaurants | `spanish-industry-hosteleria` |
| Marketplaces, OSS, B2C online invoices | `spanish-industry-ecommerce` |
| Subscription billing and SaaS invoicing | `spanish-industry-saas` |
| Public-works contracts, certificaciones, FACe in construction | `spanish-industry-construccion` |
| Corporate tax status that sets the Verifactu date | `spanish-corporate-tax` |
| Autónomo obligations and dates | `spanish-autonomo-tax` |
