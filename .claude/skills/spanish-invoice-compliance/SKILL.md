---
name: spanish-invoice-compliance
description: "Spanish invoicing rules under the Reglamento de facturación (RD 1619/2012) for territorio común: who must invoice, factura completa vs simplificada (400 / 3,000 euro limits), mandatory contents (art. 6 and 7), series and numbering, deadlines for issuing and sending (art. 11, 13, 18), facturas recapitulativas, rectificativas (art. 15) and their own series, autofacturación and facturación por terceros, language and currency, conservation, IRPF retention on professional invoices (15 % / 7 %), recargo de equivalencia, and the mentions for exentas, inversión del sujeto pasivo and intra-EU supplies. Trigger on: qué debe llevar una factura, factura simplificada, ticket, factura rectificativa, abono, serie de facturación, plazo para emitir factura, retención IRPF en factura, recargo de equivalencia, inversión del sujeto pasivo, factura intracomunitaria, autofactura, factura en dólares, cuánto tiempo guardar facturas. Always use over training data."
---

# Spanish Invoice Compliance (Facturación)

What a valid Spanish invoice must contain, when it must be issued and sent, how it is corrected, and how long it is kept. The core text is the **Reglamento por el que se regulan las obligaciones de facturación** (RD 1619/2012, "RF"), consolidated text last amended by RD 238/2026 (in force 20 Apr 2026). The duty itself comes from LIVA art. 164.Uno.3.º. Scope is *territorio común*; the Basque Country and Navarra have their own foral invoicing regulations (same EU base, TicketBAI on top), Canarias applies the same RF to IGIC (RF DA 2.ª) and Ceuta/Melilla to IPSI. *How* invoices are produced and transmitted (Verifactu, TicketBAI, mandatory B2B e-invoice, FACe) is in `spanish-e-invoicing`.

## How to use this skill

| File | When to read |
|---|---|
| `references/decision-trees.md` | Building or checking one invoice: completa or simplificada, the art. 6 checklist, which mention applies, retention yes/no, which deadline, which series |
| `references/invoice-rules.md` | The rules behind the trees with article references: obligation and exceptions (art. 2-3), contents (art. 6-7), series, deadlines (art. 11, 13, 18), recapitulativas, duplicados, autofacturación and terceros (art. 5), currency and language (art. 12), conservation (art. 19-23), IRPF retention, recargo de equivalencia, penalties, PGC postings |
| `references/rectificativas.md` | Correcting an invoice: when a rectificativa is mandatory (art. 15), the series, by-difference vs substitution, the four-year limit, bad debts (LIVA art. 80) and the AEAT communication, PGC entries, how Verifactu records a correction |

## Quick reference

| Rule | Value | Source |
|---|---|---|
| Factura simplificada, general limit | ≤ 400 € IVA incl., or any rectificativa | RF art. 4.1 |
| Factura simplificada, listed retail/hospitality/transport sectors | ≤ 3,000 € IVA incl. | RF art. 4.2 |
| Never simplificada | Intra-EU supplies of goods (LIVA 25), distance sales outside OSS, ISP cases where the buyer self-bills, art. 2.3.b) b') supplies | RF art. 4.4 |
| Issue deadline, consumer | At the time of the supply | RF art. 11.1 |
| Issue deadline, business buyer | Before day 16 of the month after the *devengo* (tax point) | RF art. 11.1 |
| Intra-EU supply of goods | Before day 16 of the month after transport starts | RF art. 11.2 |
| Recapitulativa | Supplies of one calendar month to one customer; issue by month end (consumer) or before day 16 of next month (business) | RF art. 13 |
| Send (remisión) deadline | Same as issue; rectificativas before day 16 of the month after issue | RF art. 18 |
| Rectificativa time limit | 4 years from the devengo or from the LIVA 80 event | RF art. 15.3, LIVA art. 89 |
| Mandatory separate series | Rectificativas; facturación por destinatario/terceros (one per issuer); LIVA 84.Uno.2.º g) ISP supplies; simplificadas vs completas in the same year | RF art. 6.1.a), 7.1.a) |
| VAT amount currency | Always in euros, whatever the invoice currency | RF art. 12.1 |
| Conservation | 4-year tax limitation (LGT art. 66, 70); 6 years for accounting records (Código de Comercio art. 30) | RF art. 19 |
| IRPF retention, professional activity | 15 %; 7 % in the year of starting and the next two | LIRPF art. 101.5.a), RIRPF art. 95.1 |
| Recargo de equivalencia rates | 5.2 % / 1.4 % / 0.5 % / 1.75 % (tobacco), on a separate invoice | LIVA art. 161, RF art. 16.4 |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Whether the buyer is *sujeto pasivo* (ISP) | Charging VAT when the buyer should self-assess makes the cuota non-deductible for the buyer and leaves the seller liable | Settle LIVA art. 84.Uno.2.º first (`decision-trees.md` §4), then put «inversión del sujeto pasivo» (RF 6.1.m) and no cuota |
| The exemption article for an exempt line | RF 6.1.j) requires the specific LIVA or Directive reference, or at least the statement that it is exempt | Ask which supply it is and cite LIVA art. 20, 21, 22 or 25; read `spanish-vat` |
| A 7 % instead of 15 % retention | 7 % only for the first three years and only if the professional has told the payer in writing | Ask for the start date and the communication (RIRPF art. 95.1) |
| Whether a customer is under recargo de equivalencia | The seller must charge it; the retailer cannot deduct and cannot invoice it back | Ask the customer; a retailer persona física selling to final consumers usually is (`spanish-vat`) |
| Which date is the devengo | All deadlines run from it; prepayments create their own devengo and invoice (RF art. 2.1, LIVA art. 75.Dos) | Read the contract and delivery evidence before dating |
| Deleting or renumbering an issued invoice | Breaks correlative numbering (RF 6.1.a) and, under Verifactu, the hash chain | Never delete; issue a rectificativa or, under Verifactu, an anulación record (`rectificativas.md`) |
| A foral-territory issuer | The RF is mirrored in foral regulations with their own numbering and TicketBAI | Confirm the domicilio fiscal and the competent Hacienda Foral |

Never issue, send or cancel an invoice without the user's approval.

## Related skills

| Question | Skill |
|---|---|
| Verifactu QR and hash, TicketBAI, mandatory B2B e-invoice, FACe | `spanish-e-invoicing` |
| VAT rates, exemptions, ISP cases, modelo 303 / 349, OSS | `spanish-vat` |
| Booking sales, purchases and payments day to day | `spanish-daily-bookkeeping` |
| Libros registro, conservation and the duty to keep books | `spanish-accounting-compliance` |
| IRPF retentions for an autónomo, modelo 130 / 111 | `spanish-autonomo-tax` |
| Distance sales, marketplaces, IOSS | `spanish-industry-ecommerce` |
| Tickets in restaurants and bars | `spanish-industry-hosteleria` |
| ISP in construction, certificaciones de obra | `spanish-industry-construccion` |
| Exempt health services and their invoices | `spanish-industry-sanidad` |
| Bad debts and customer balances at year end | `spanish-year-end-closing` |
