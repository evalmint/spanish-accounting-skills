# Spanish Invoice Compliance: Rules

## Contents

- [1. Legal sources and status](#1-legal-sources-and-status)
- [2. Who must invoice (art. 1-3, 26)](#2-who-must-invoice-art-1-3-26)
- [3. Factura simplificada (art. 4, 7)](#3-factura-simplificada-art-4-7)
- [4. Contents of a factura completa (art. 6)](#4-contents-of-a-factura-completa-art-6)
- [5. Series and numbering](#5-series-and-numbering)
- [6. Deadlines: issue and send (art. 11, 17, 18)](#6-deadlines-issue-and-send-art-11-17-18)
- [7. Recapitulativas and duplicados (art. 13, 14)](#7-recapitulativas-and-duplicados-art-13-14)
- [8. Autofacturación and facturación por terceros (art. 5)](#8-autofacturación-and-facturación-por-terceros-art-5)
- [9. Paper vs electronic, consent (art. 8-10)](#9-paper-vs-electronic-consent-art-8-10)
- [10. Currency and language (art. 12)](#10-currency-and-language-art-12)
- [11. Special regimes on the invoice (art. 16)](#11-special-regimes-on-the-invoice-art-16)
- [12. IRPF retention on invoices](#12-irpf-retention-on-invoices)
- [13. Intra-EU and cross-border invoices](#13-intra-eu-and-cross-border-invoices)
- [14. Conservation (art. 19-23)](#14-conservation-art-19-23)
- [15. Penalties (LGT art. 201)](#15-penalties-lgt-art-201)
- [16. PGC postings](#16-pgc-postings)
- [17. Time-dependent parameters](#17-time-dependent-parameters)

## 1. Legal sources and status

| Source | What it governs |
|---|---|
| LIVA (Ley 37/1992) art. 164.Uno.3.º, 88, 89, 97 | Duty to invoice, repercusión, rectification of cuotas, invoice as the document for deduction |
| RD 1619/2012, Reglamento de facturación (RF) | Everything in this file. Consolidated text on BOE, last update published 31 Mar 2026 |
| RD 1007/2023 (Verifactu) DF 1.ª | Added art. 6.5, 7.5 and 8.4 RF: QR code and "VERI*FACTU" phrase, applicable once Verifactu applies |
| RD 238/2026, of 25 Mar (BOE-A-2026-7295) DF 1.ª | In force 20 Apr 2026. Rewrote art. 8.1, 9 and 10 RF and added art. 8 bis: mandatory B2B e-invoice, consent not required where it is mandatory. Effective application deferred (see `spanish-e-invoicing`) |
| LIRPF art. 101, RIRPF art. 95, 99 | Retention on professional income |
| LGT (Ley 58/2003) art. 29.2.j, 66, 70, 201, 201 bis | Formal duties, limitation, conservation, penalties |

Foral territories (Álava, Bizkaia, Gipuzkoa, Navarra) have their own reglamentos de facturación that mirror the RF; check them for foral taxpayers.

## 2. Who must invoice (art. 1-3, 26)

- Every *empresario o profesional* must issue and keep a copy of an invoice for every supply of goods and services in its activity, including non-subject and exempt supplies, and for prepayments received (art. 2.1). This applies in all VAT special regimes.
- **Always** required (art. 2.2): business or professional recipient; recipient who demands it for a tax right; intra-EU supplies of goods (LIVA 25); distance sales located in Spain; exports; goods installed or assembled; legal persons not acting as businesses; public administrations.
- **Exceptions** when none of art. 2.2 applies (art. 3): exempt supplies under LIVA 20 (except 20.Uno 2.º-5.º, 15.º, 20.º, 22.º, 24.º, 25.º, 28.º); recargo de equivalencia activities (except supplies of immovables); módulos (régimen simplificado) not determined by income; REAGP farmers; financial/insurance services of LIVA 20.Uno.16.º and 18.º a) to n) with conditions (art. 3.2); AEAT authorisations.
- IRPF taxpayers in estimación directa, and in estimación objetiva where the yield depends on income, must invoice under the RF regardless of VAT regime (art. 26).

## 3. Factura simplificada (art. 4, 7)

**When allowed** (art. 4): total ≤ 400 € IVA included; any rectificativa; ≤ 3,000 € IVA included in the art. 4.2 sectors (retail to final consumers, ambulant and home sales, passenger transport, hostelería y restauración, discotecas, public phones, hairdressing and beauty, sports facilities, photo development, parking, film rental, dry-cleaning and laundry, toll roads); other cases authorised by AEAT.

**Never** (art. 4.4): intra-EU goods (LIVA 25); distance sales of LIVA 68.Tres.a) outside the OSS; ISP supplies by non-established suppliers where the buyer issues the invoice under art. 5; art. 2.3.b) b') supplies (located in another Member State with reverse charge, or outside the EU).

**Contents** (art. 7.1): number and series; issue date; supply date if different; issuer's NIF and full name; type of goods or services; VAT rate, optionally "IVA incluido", and base per rate when several rates; total consideration; for rectificativas, explicit reference to the rectified invoice and what changes; the art. 6.1.j)-p) mentions.

**Simplificada cualificada** (art. 7.2): if the business buyer asks, add its NIF and domicilio and show the cuota separately; this lets the buyer deduct (LIVA 97). Same if a consumer asks for a tax right (art. 7.3). These are within the mandatory B2B e-invoice when it applies (RD 238/2026 art. 4.1).

**Exchanging a simplificada for a completa** is not a rectificativa if the simplificada met art. 7.1 (art. 15.6).

## 4. Contents of a factura completa (art. 6)

| Letter | Content | Notes |
|---|---|---|
| a) | Number and series | Correlative within each series; mandatory separate series in §5 |
| b) | Issue date | |
| c) | Full name or razón social of issuer and recipient | |
| d) | Issuer's NIF (Spanish, or the EU VAT number used) | Recipient's NIF also when: intra-EU exempt supply; recipient is sujeto pasivo; supply located in Spain by an established issuer |
| e) | Domicilio of both | Establishment when relevant for place of supply |
| f) | Description and all data for the base imponible (LIVA 78-79), unit price excl. VAT, discounts | |
| g) | VAT rate(s) | |
| h) | Cuota repercutida, separately | Not shown separately under REAV and REBU (art. 16.2-3) |
| i) | Supply or prepayment date, if different from issue date | Also starts the payment period count for B2B e-invoice reporting (RD 238/2026 art. 15) |
| j) | Exemption reference | LIVA or Directive article, or "exenta" |
| k) | New means of transport details | Intra-EU |
| l) | «facturación por el destinatario» | Self-billing |
| m) | «inversión del sujeto pasivo» | Buyer liable |
| n) | «régimen especial de las agencias de viajes» | |
| o) | «régimen especial de los bienes usados» / «… objetos de arte» / «… antigüedades y objetos de colección» | |
| p) | «régimen especial del criterio de caja» | |

- Separate base per operation when mixing exempt and taxed, ISP and non-ISP, or different rates (art. 6.2).
- For supplies located in another Member State with reverse charge, letters f), g), h) may be replaced by quantity/nature and the amount (art. 6.3).
- An invoice that meets art. 6 is a *factura* for the right to deduct (art. 6.4).
- **Verifactu content** (art. 6.5, 7.5; added by RD 1007/2023): invoices issued with an RD 1007/2023 system carry a QR code (in an e-invoice, its URL may replace the image) and, only if the system sends every record to AEAT, the phrase «Factura verificable en la sede electrónica de la AEAT» or «VERI*FACTU». Applies from 1 Jan 2027 (IS taxpayers) / 1 Jul 2027 (others); details in `spanish-e-invoicing`.
- Other law may add mentions (e.g. Ley 3/2004 payment terms, consumer law, Registro Mercantil data on company documents under RRM art. 24) (RF art. 6.1 opening words).

## 5. Series and numbering

- Numbering is correlative within each series (art. 6.1.a, 7.1.a). Separate series are allowed for justified reasons (several establishments, different kinds of operations).
- **Mandatory separate series**: invoices issued by the recipient or third parties, one per issuer; rectificativas; invoices under RIVA DA 5.ª (foreclosures); LIVA 84.Uno.2.º g) ISP supplies; RIVA art. 61 quinquies.2 (VAT group); simplificadas vs completas issued in the same calendar year.
- Gaps and duplicates are formal breaches (LGT art. 201.2.a). Under Verifactu, the alta record key is NIF + series/number + issue date; a repeated key is rejected, and the chain records every record in order (RD 1007/2023 art. 8, 10).

## 6. Deadlines: issue and send (art. 11, 17, 18)

- Issue at the time of the supply (art. 11.1). If the recipient is a business acting as such: before day 16 of the month after the month of devengo.
- Intra-EU supplies of goods (LIVA 75.Uno.8.º): before day 16 of the month after the month transport starts (art. 11.2).
- Criterio de caja: at the supply, or before day 16 of the following month for business recipients (art. 11.3).
- Originals must be sent to the recipient (art. 17), at issue or, for business recipients, by the same day-16 limit; rectificativas before day 16 of the month after issue (art. 18).
- SII filers (monthly VAT period, RIVA art. 62.6): record issued invoices within 4 calendar days of issue (8 for self-billed), and always before day 16 of the month after devengo (RIVA art. 69 bis).

## 7. Recapitulativas and duplicados (art. 13, 14)

- One invoice may cover several supplies to the same recipient within one calendar month (art. 13.1). Issue by the last day of that month, or before day 16 of the next month for business recipients; intra-EU goods follow art. 11.2.
- Only one original per invoice (art. 14.1). A duplicate is allowed only for several recipients of one supply (each share shown) or loss of the original, and carries «duplicado» (art. 14.2-4).

## 8. Autofacturación and facturación por terceros (art. 5)

- The duty can be met materially by the recipient or a third party; the supplier stays responsible (art. 5.1).
- **Self-billing** needs (art. 5.2): a prior written agreement listing the operations; an acceptance procedure for each invoice; a copy sent to the supplier; issue in the supplier's name. Mention «facturación por el destinatario» (art. 6.1.l) and a separate series per issuer.
- **Third-party issuing** (art. 5.3): any provider (software, gestoría, platform). If the recipient or third party is established outside the EU and outside a mutual-assistance country, AEAT must be told first (art. 5.4). SII filers using this option file a censal declaration (art. 5.1 second para.).
- Under Verifactu the obligation can also be met by the recipient or third party (RD 1007/2023 art. 6); under the B2B mandate, the copia fiel is sent by the system of whoever issues (Orden HAC/1028/2026 art. 4.1).

## 9. Paper vs electronic, consent (art. 8-10)

- Any medium is allowed if authenticity of origin, integrity and legibility are ensured for the whole conservation period; business controls with a reliable audit trail suffice (art. 8.1-3). An RD 1007/2023-compliant system is presumed to ensure them (art. 8.4).
- *Factura electrónica* = issued, transmitted and received electronically (art. 9.1). A PDF by email is a factura electrónica in the RF sense if the recipient accepts it; it is **not** the structured EN 16931 invoice required under the B2B mandate (RD 238/2026 art. 7).
- Electronic invoicing requires the recipient's consent, except where it is mandatory under art. 8 bis (art. 9.2, as rewritten by RD 238/2026).
- Authenticity and integrity are guaranteed by qualified electronic signature or seal, EDI with agreed controls, or AEAT-validated means (art. 10.1); for mandatory B2B e-invoices by the RD 238/2026 procedures (art. 10.2).

## 10. Currency and language (art. 12)

- Amounts may be in any currency, but the **VAT cuota must be in euros**, converted at the selling rate fixed by the Banco de España in force at the devengo (LIVA art. 79.Once) (art. 12.1).
- Any language is allowed; AEAT may require a translation into Castilian or another official language (art. 12.2).
- Verifactu records carry all amounts in euros (RD 1007/2023 art. 10.2).

## 11. Special regimes on the invoice (art. 16)

| Regime | Invoice rule |
|---|---|
| Recargo de equivalencia (supplier side) | Separate invoices for supplies subject to RE, showing the RE rate and amount (art. 16.4). Rates: 5.2 % (21 % goods), 1.4 % (10 %), 0.5 % (4 %), 1.75 % tobacco (LIVA art. 161). The retailer keeps purchase invoices for RE and non-RE activities separate |
| Recargo de equivalencia (retailer side) | No duty to invoice consumers (art. 3.1.b); must invoice if the buyer is a business or asks; never shows RE on its own sales |
| REBU (margin scheme) | Mention per art. 6.1.o; cuota not shown separately (art. 16.2.c); signed purchase document when buying from non-businesses |
| REAV (travel agencies) | Mention per art. 6.1.n; cuota not required separately (art. 16.3) |
| REAGP | Buyer issues a signed receipt for the compensation (art. 16.1) |
| Criterio de caja | Mention per art. 6.1.p |
| Franquicia / small business VAT exemption | Spain had not transposed Directive (EU) 2020/285 as of Nov 2026 (unverified); do not issue invoices without VAT on that basis |

## 12. IRPF retention on invoices

| Payee | Rate | Source |
|---|---|---|
| Professional activity (persona física), general | 15 % | LIRPF art. 101.5.a; RIRPF art. 95.1 |
| New professional: year of start and next two, no professional activity in the prior year, written communication to payer | 7 % | RIRPF art. 95.1 |
| Recaudadores municipales; mediadores de seguros using external auxiliaries; delegados comerciales of Loterías y Apuestas del Estado | 7 % | RIRPF art. 95.1 a)-c) |
| Artists and related technicians (IAE groups 851-869 listed, sección 3.ª agrupaciones 01-03, 05) whose prior-year income from these activities was < 15,000 € and > 75 % of their work plus business income, with written communication | 7 % | RIRPF art. 95.1 d), added by RD 31/2023 |
| Business activities in estimación objetiva listed in RIRPF 95.6 | 1 % (2 % for some farming activities) | RIRPF art. 95.6 |
| Rent of urban property (landlord persona física or entity) | 19 % | RIRPF art. 100-101 |
| Courses, conferences, literary/artistic works (rendimientos del trabajo / capital mobiliario) | 15 % / 19 % | RIRPF art. 80, 101 (check case) |

- Base: the *ingresos íntegros* paid, i.e. the fee excluding VAT (RIRPF art. 95.1). Rates are cut by 60 % for income entitled to the Ceuta/Melilla deduction (LIRPF art. 68.4; RIRPF art. 95.1 last para.). Shown on the invoice as a negative line; VAT is still computed on the full base.
- The payer withholds only if it is an obliged retainer (businesses, professionals, entities; RIRPF art. 76). No retention on invoices to consumers or between companies (SL/SA, including SLP).
- Payer books the retention to **4751** and pays it with modelo 111 (annual summary modelo 190); the professional books it to **473** as a prepayment of IRPF. See `spanish-autonomo-tax`.
- Foral territories set their own rates.

## 13. Intra-EU and cross-border invoices

| Supply | Invoice requirements |
|---|---|
| Intra-EU supply of goods, exempt LIVA 25 | Completa, buyer's NIF-IVA (validated in VIES), exemption reference, before day 16 of next month (art. 11.2); declare in modelo 349 |
| B2B service to a business in another Member State (LIVA 69.Uno.1.º) | Spanish RF applies (art. 2.3.b.b'.a''): completa, buyer's VAT number, «inversión del sujeto pasivo» (6.1.m); f)-h) may be simplified (6.3); modelo 349 |
| Export of goods outside the EU | Completa, exemption reference (LIVA 21) |
| Service located outside the EU | RF applies (art. 2.3.b.b'.b''); mention non-subjection as good practice |
| Purchase from a non-established supplier with ISP in Spain | The buyer self-assesses; supplier's foreign invoice is valid; the buyer may issue the invoice under art. 5 |
| OSS / IOSS sales | Invoice rules of the Member State of identification (art. 2.3.a; `spanish-industry-ecommerce`) |

## 14. Conservation (art. 19-23)

- Keep received invoices, copies of issued invoices, import documents, accounting justificantes and REAGP receipts for the LGT period (art. 19.1): the 4-year limitation (LGT art. 66) counted from the end of the filing period, longer where LGT art. 66 bis and 70 apply (e.g. 10 years to verify tax losses or deductions being used).
- Commercial law: 6 years from the last entry for books, correspondence and justificantes (Código de Comercio art. 30). In practice keep 6 years, longer for open tax credits.
- Original content, in order, any medium guaranteeing authenticity, integrity and legibility (art. 20). Electronic conservation must allow online access, search, copy, download and print by AEAT (art. 21).
- Conservation outside Spain only by electronic means with online access, after notifying AEAT (art. 22.2). A non-EU third party custodian needs prior notification (art. 19.4).
- The Solución Pública de Facturación Electrónica keeps B2B e-invoices for the LGT period, never more than 12 years (Ley 56/2007 DA 21.ª.5); this does not replace the parties' own conservation duty.

## 15. Penalties (LGT art. 201)

| Breach | Penalty |
|---|---|
| Requirements of invoices not met (contents, issue, sending, rectification, conservation) | 1 % of the operations concerned (art. 201.2.a) |
| Invoice not issued or not kept | 2 % of the operations, or 300 € per operation when the amount is unknown (art. 201.2.b) |
| Invoices with false or falsified data | 75 % of the operations (art. 201.3) |
| Substantial breach | +100 % (art. 201.5) |
| Possessing invoicing software that does not meet LGT 29.2.j / RD 1007/2023 | 50,000 € per financial year (LGT art. 201 bis.4) |
| Producing or selling such software | 150,000 € per year and type of system; 1,000 € per sale without the declaración responsable (art. 201 bis.4) |

## 16. PGC postings

| Event | Debit | Credit |
|---|---|---|
| Sale to customer with VAT | **430** total | **700** / **705** base; **477** cuota |
| Professional invoice with retention (issuer) | **430** net + **473** retention | **705** base; **477** cuota |
| Purchase of professional service with retention (payer) | **623** base; **472** cuota | **410** net; **4751** retention |
| Sale with recargo de equivalencia | **430** | **700**; **477** (VAT + RE) |
| Prepayment received | **572** | **438** advance; **477** cuota |
| ISP purchase (domestic or intra-EU service) | **600** / **629** base; **472** self-assessed cuota | **400** / **410** base; **477** self-assessed cuota |
| Volume rebate given | **709** base; **477** cuota (negative) | **430** |
| Return of goods | **708** base; **477** cuota (negative) | **430** |

Rectificativa entries: `rectificativas.md` §6.

## 17. Time-dependent parameters

| Parameter | Value | Valid from | Source |
|---|---|---|---|
| Simplificada limits | 400 € / 3,000 € | 1 Jan 2013 | RF art. 4 |
| Verifactu QR and phrase on invoices | Applies | 1 Jan 2027 (IS taxpayers); 1 Jul 2027 (others) | RD 1007/2023 DF 4.ª as amended by RD-ley 15/2025 |
| Consent for e-invoice not needed where mandatory | Applies | 20 Apr 2026 (text in force; mandate itself starts 6 Oct 2027 / 6 Oct 2028) | RF art. 9.2 as amended by RD 238/2026 |
| LIVA 80.Cuatro: consumer bad debts | Base > 50 € | 1 Jan 2023 | LIVA art. 80.Cuatro.A.3.ª |
| IRPF professional retention | 15 % / 7 % | 2016 onwards | RIRPF art. 95.1 |
| RE rates | 5.2 / 1.4 / 0.5 / 1.75 % | 1 Sep 2012 | LIVA art. 161 |
| VAT on furnished short-term lets (LIVA 20.Uno.23.º e') and some rates in LIVA 91 (hostelería-related, renovation works on homes) | Amended by RD-ley 29/2026, of 6 Oct, with effect 1 Dec 2026 (an earlier RD-ley 26/2026 with the same content was repealed by Congress on 2 Oct 2026). Invoices dated from 1 Dec 2026 must use the new treatment and its exemption or rate mention; content not read for this skill | 1 Dec 2026 | BOE-A-2026-20823; read `spanish-vat` |
