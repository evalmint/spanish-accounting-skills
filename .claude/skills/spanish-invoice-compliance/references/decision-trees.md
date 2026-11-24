# Spanish Invoice Compliance: Decision Trees

## Contents

- [1. Must an invoice be issued at all?](#1-must-an-invoice-be-issued-at-all)
- [2. Completa or simplificada?](#2-completa-or-simplificada)
- [3. Is this factura completa valid? (RF art. 6)](#3-is-this-factura-completa-valid-rf-art-6)
- [4. Which special mention?](#4-which-special-mention)
- [5. IRPF retention on the invoice?](#5-irpf-retention-on-the-invoice)
- [6. Which deadline?](#6-which-deadline)
- [7. Which series?](#7-which-series)
- [8. Common errors](#8-common-errors)

All references are to RD 1619/2012 (RF) unless stated. Territorio común.

## 1. Must an invoice be issued at all?

```
Seller is an empresario/profesional acting as such?            no → RF art. 1 second para. only (rare)
Buyer is an empresario/profesional, a legal person, or a
  public administration (art. 2.2.a, f)?                        yes → INVOICE ALWAYS
Intra-EU supply of goods, export, distance sale, installed goods
  (art. 2.2.b-e)?                                               yes → INVOICE ALWAYS
Prepayment received before the supply (art. 2.1 second para.)?  yes → invoice the prepayment
Otherwise, to a consumer:
  Exempt under LIVA 20 except 20.Uno 2º-5º, 15º, 20º, 22º, 24º, 25º, 28º?   → no invoice needed (art. 3.1.a)
  Activity under recargo de equivalencia (retailer)?                       → no invoice needed (art. 3.1.b), except immovables
  Régimen simplificado (módulos) not based on income?                      → no invoice needed (art. 3.1.c)
  Consumer asks for one to exercise a tax right?                           → invoice (art. 2.2.a)
  Else                                                                      → invoice (simplificada is enough)
IRPF estimación directa or objetiva by income → invoice duty also under RF art. 26
```

## 2. Completa or simplificada?

```
Excluded supply (art. 4.4)?  intra-EU goods LIVA 25 / distance sale LIVA 68.Tres.a outside OSS /
  ISP where buyer self-bills / art. 2.3.b) b') supplies   → COMPLETA
Total ≤ 400 € IVA included?                                → simplificada allowed (art. 4.1.a)
Rectifying a simplificada?                                 → simplificada rectificativa allowed (art. 4.1.b)
Total ≤ 3,000 € IVA incl. AND sector in art. 4.2 list
  (retail to consumers, hostelería/restauración, transport of
  persons, hairdressing, parking, tolls, laundry, sports
  facilities, photo studios, discotecas, delivery to home,
  ambulant sales, film rental, phone cabins)?              → simplificada allowed
  Note: art. 4.2.e covers "hostelería y restauración" by restaurants, bars, cafés and
  similar; whether hotel accommodation falls under it is not clear from the text
  (unverified). For hotels above 400 € issue a completa unless AEAT confirms.
AEAT authorisation (art. 4.3)?                             → simplificada allowed
Else                                                       → COMPLETA
Business buyer asks for its NIF, address and separate cuota → add them (art. 7.2): "simplificada cualificada",
  which gives the right to deduct and is inside the B2B e-invoice mandate (RD 238/2026 art. 4.1)
Invoicing both types in one calendar year → separate series (art. 7.1.a last para.)
```

## 3. Is this factura completa valid? (RF art. 6)

```
a) Number, and series if used; correlative within the series          art. 6.1.a
b) Issue date                                                         art. 6.1.b
c) Full name / razón social of issuer AND recipient                   art. 6.1.c
d) Issuer's NIF (Spanish or EU VAT number used for the supply)        art. 6.1.d
   Recipient's NIF mandatory if: intra-EU exempt supply (NIF-IVA),
   recipient is sujeto pasivo (ISP), or supply in TAI by an
   established issuer (i.e. almost every domestic B2B invoice)
e) Domicilio of both; the establishment if relevant to taxation       art. 6.1.e
f) Description, all data for the base imponible, unit price excl.
   VAT, discounts not in the unit price                               art. 6.1.f
g) VAT rate(s)                                                        art. 6.1.g
h) Cuota repercutida, shown separately                                art. 6.1.h
i) Date of supply or prepayment, if different from issue date         art. 6.1.i
j)-p) Special mentions when applicable                                 → §4
Base per rate / exempt / ISP shown separately when mixed              art. 6.2
Issued with a Verifactu-scope system: QR code (or its URL in an
  e-invoice) and, if VERI*FACTU mode, the phrase                     art. 6.5 (from 1 Jan / 1 Jul 2027)
Recargo de equivalencia charged? → separate invoice with RE rate and amount   art. 16.4
```

Missing any applicable item: the document is not a *factura* for deduction purposes (art. 6.4, LIVA art. 97.Uno) and must be corrected with a rectificativa (art. 15.1).

## 4. Which special mention?

| Situation | Mention on the invoice | Rule |
|---|---|---|
| Exempt supply (any part) | Article of LIVA (e.g. "Exenta art. 20.Uno.3.º LIVA") or Directive 2006/112, or "operación exenta" | 6.1.j |
| Intra-EU supply of goods | Exemption reference "Entrega intracomunitaria exenta, art. 25 LIVA" + buyer's NIF-IVA | 6.1.j, 6.1.d.1.º |
| Buyer is sujeto pasivo: domestic ISP (LIVA 84.Uno.2.º) or B2B service to another EU country | «inversión del sujeto pasivo», no cuota charged | 6.1.m |
| New means of transport to another EU country | Characteristics, first-use date, km / hours | 6.1.k |
| Buyer issues the invoice (autofacturación) | «facturación por el destinatario» | 6.1.l |
| Travel agencies' special regime | «régimen especial de las agencias de viajes» | 6.1.n |
| Margin scheme | «régimen especial de los bienes usados» / «… de los objetos de arte» / «… de las antigüedades y objetos de colección» | 6.1.o |
| Cash accounting (RECC) | «régimen especial del criterio de caja» | 6.1.p |
| Non-subject (no sujeta) supply, e.g. B2B service located outside Spain | Not listed in art. 6; state the reason (e.g. "no sujeta, art. 69 LIVA") as good practice and because Verifactu records require the cause (RD 1007/2023 art. 10.1.n) | — |

Simplificadas need the same mentions (art. 7.1.i).

## 5. IRPF retention on the invoice?

```
Issuer is a persona física (autónomo) or an entidad en atribución de rentas?   no (SL/SA) → no retention
Income is from a PROFESSIONAL activity (IAE sections 2 and 3, e.g. lawyer,
  consultant, architect, artist), not a business one?                        no → generally none
  (exceptions: módulos activities at 1 %, RIRPF 95.6; urban rent at 19 %, RIRPF 100-101)
Payer is an empresario/profesional or entity obliged to withhold (RIRPF 76)?  no (consumer) → none
→ Retention 15 % of the base imponible excl. VAT (RIRPF 95.1)
→ 7 % if the year of starting or one of the next two, the professional did no
  professional activity in the prior year, and has told the payer in writing
→ 7 % also for recaudadores municipales, mediadores de seguros with external
  auxiliaries, delegados comerciales of Loterías, and low-income artists (RIRPF 95.1 a-d)
```

Show the retention as a line that reduces *Total a pagar*; it does not change the VAT base. Example: base 1,000; IVA 21 % 210; IRPF −150; total 1,060.

## 6. Which deadline?

| Case | Issue (expedición) | Send (remisión) |
|---|---|---|
| Consumer | At the supply (art. 11.1) | At issue (art. 18) |
| Business buyer | Before day 16 of month after devengo (art. 11.1) | Same (art. 18) |
| Intra-EU goods | Before day 16 of month after transport starts (art. 11.2) | Same |
| Recapitulativa, consumer | Last day of the month (art. 13.2) | At issue |
| Recapitulativa, business | Before day 16 of next month (art. 13.2) | Same |
| Criterio de caja, business buyer | Before day 16 of month after the supply (art. 11.3) | Same |
| Rectificativa | As soon as the cause is known, within 4 years (art. 15.3) | Before day 16 of month after issue (art. 18) |
| SII filers | Plus: record in SII within 4 calendar days of issue (RIVA art. 69 bis) | — |

## 7. Which series?

| Document | Series rule |
|---|---|
| Rectificativas | Own series, always (6.1.a.2.º; 7.1.a.4.º) |
| Issued by the buyer or a third party | One separate series per issuer (6.1.a.1.º) |
| ISP supplies of LIVA 84.Uno.2.º g) (phones, consoles, laptops, tablets, silver/platinum/palladium) | Special series (6.1.a.4.º, LIVA 84.Uno.2.º g last para.) |
| Simplificadas and completas in the same year | Separate series (7.1.a) |
| Several establishments or different kinds of operations | Separate series allowed (6.1.a) |
| New year | Restarting numbering is allowed if the series code changes (e.g. 2027-A); correlative inside each series is what matters (unverified practice; RF only requires correlative numbering within the series) |

## 8. Common errors

| Error | Consequence | Fix |
|---|---|---|
| VAT charged on an ISP supply | Buyer cannot deduct; seller owes the VAT it invoiced (LIVA 89) | Rectificativa to zero the cuota, reissue with «inversión del sujeto pasivo» |
| Missing recipient NIF on a B2B invoice | Not a valid factura for the buyer's deduction | Rectificativa adding the data (art. 15.1) |
| Corrected invoice reissued under the same number | Duplicate numbering; under Verifactu a second alta with the same key is rejected | Rectificativa in its own series |
| Simplificada above the limit | Not an allowed document | Issue a completa replacing it (not a rectificativa if the original met art. 7.1, art. 15.6) |
| Foreign-currency invoice with VAT only in that currency | Breach of art. 12.1 | Show the cuota in euros at the LIVA 79.Once rate |
| Retention computed on base + VAT | Wrong retention, payer's modelo 111 off | Base excl. VAT |
| RE on the same invoice as goods without RE | Breach of art. 16.4 | Separate invoice for RE supplies |
