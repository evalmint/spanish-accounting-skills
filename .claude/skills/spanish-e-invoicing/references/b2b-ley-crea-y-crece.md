# Mandatory B2B E-Invoice (Ley Crea y Crece, RD 238/2026)

## Contents

- [1. Legal chain](#1-legal-chain)
- [2. Schedule](#2-schedule)
- [3. Who and what is in scope](#3-who-and-what-is-in-scope)
- [4. The Spanish e-invoicing system: platforms and the SPFE](#4-the-spanish-e-invoicing-system-platforms-and-the-spfe)
- [5. Formats, signature and unique code](#5-formats-signature-and-unique-code)
- [6. Copia fiel to the SPFE](#6-copia-fiel-to-the-spfe)
- [7. Invoice states and payment reporting](#7-invoice-states-and-payment-reporting)
- [8. Transitional rules](#8-transitional-rules)
- [9. Requirements for private platforms](#9-requirements-for-private-platforms)
- [10. Relation to Verifactu, SII and the RF](#10-relation-to-verifactu-sii-and-the-rf)
- [11. Penalties and open points](#11-penalties-and-open-points)
- [12. Readiness checklist](#12-readiness-checklist)

## 1. Legal chain

| Instrument | Content |
|---|---|
| Ley 18/2022, of 28 Sep, *de creación y crecimiento de empresas* ("Crea y Crece"), art. 12 and DF 7.ª-8.ª | Rewrote Ley 56/2007 art. 2 bis: all businesses must issue, send and receive e-invoices to other businesses and report invoice states. Effects 1 year (> 8 M€) / 2 years (others) after the implementing regulation |
| Ley 56/2007 art. 2 bis and DA 21.ª (added by Ley 7/2024 DF 12.ª, in force 22 Dec 2024) | Free interconnection and interoperability; recipient cannot impose a platform (2 bis.3 bis); free copy for 4 years (2 bis.3); AEAT's Solución Pública de Facturación Electrónica (SPFE) as universal repository; copia fiel; payment reporting; data kept ≤ 12 years |
| **RD 238/2026, of 25 Mar** (BOE 31 Mar 2026, BOE-A-2026-7295), in force 20 Apr 2026 | The implementing regulation. Also amended RD 1619/2012 art. 8, 8 bis, 9, 10 |
| **Orden HAC/1028/2026, of 2 Oct** (BOE 5 Oct 2026, BOE-A-2026-20587), in force 6 Oct 2026 | Technical rules of the SPFE (UBL, copia fiel, unique code, status and payment messages, access). Its entry into force **started the clock** for all deadlines |
| AEAT sede | XSD, validations, volumes, web services (Orden art. 3.1, 4.2, 7.3) |
| Directive (EU) 2025/516 (ViDA), in force 14 Apr 2025 | Lets Member States require domestic e-invoices without an EU derogation (cited in RD 238/2026 preamble) |

Ley 56/2007 still carries the note that art. 12 of Ley 18/2022 depended on an EU derogation from Directive 2006/112 art. 218 and 232; ViDA amended those articles, and no separate Spanish derogation decision was found (unverified).

## 2. Schedule

| Date | Who / what | Source |
|---|---|---|
| 20 Apr 2026 | RD 238/2026 in force (no effects yet for businesses) | RD 238/2026 DF 4.ª.1 |
| 6 Oct 2026 | Orden HAC/1028/2026 in force: counting starts | Orden DF única |
| ≈ 6 Aug 2027 | SPFE available at least 2 months before first application (date inferred, not published) | RD 238/2026 DA 5.ª; Orden DA 2.ª |
| **6 Oct 2027** | Businesses with VAT *volumen de operaciones* (LIVA art. 121) > 8 M€ in the prior calendar year: issue, send and receive e-invoices, report states and payments. Private platforms: copia fiel, interconnection and operating requirements | RD 238/2026 DF 4.ª.1.a and 4.ª.2 |
| 6 Oct 2027 – 6 Oct 2028 | > 8 M€ issuers attach a legible PDF unless the recipient accepts the original only | RD 238/2026 DT 2.ª |
| **6 Oct 2028** | All other businesses and professionals; legal persons ≤ 8 M€ also report states | RD 238/2026 DF 4.ª.1.b |
| **6 Oct 2029** | Personas físicas and entidades en atribución de rentas ≤ 8 M€ must report states (voluntary until then) | RD 238/2026 DT 3.ª |
| 6 Oct 2028 | Subcontractors of public contracts move from the LCSP registry to this system (24 months from the Orden) | RD 238/2026 DT 1.ª |

Dates as published by AEAT ("Facturación electrónica y solución pública de facturación electrónica. Comienza la cuenta atrás", 29 Oct 2026).

## 3. Who and what is in scope

- **Issuers**: every empresario or profesional (LIVA art. 5) obliged to invoice under RD 1619/2012 (RD 238/2026 art. 3.1). Includes self-billing and third-party issuing; the supplier remains responsible (art. 3.2).
- **Recipients**: businesses and professionals with seat, permanent establishment or domicile in Spain, for operations addressed to it (art. 3.1). Invoices to consumers, foreign businesses and public administrations (B2G, own regime) are outside.
- **Excluded**:
  - Facturas simplificadas (RF art. 4), **except** simplificadas cualificadas carrying buyer data (RF art. 7.2) (RD 238/2026 art. 4.1; RF art. 8 bis.1).
  - Electricity-market operator, organised gas market operator, and invoices settled through IATA CASS, BSP and SIS-ICH (DA 2.ª).
  - Further sectors the Ministry of Economy may exclude by order, normally temporarily (art. 4.2).
- **Territory**: all Spain, including foral territories (with SPFE arrangements, DA 3.ª) and Canarias / Ceuta / Melilla.

## 4. The Spanish e-invoicing system: platforms and the SPFE

The *sistema español de factura electrónica* = private exchange platforms meeting the RD requirements + the AEAT public solution (art. 5). Businesses may use either or both (art. 5.2, 6.1).

| Element | Rule | Source |
|---|---|---|
| Default channel | A recipient that has not expressly agreed private platforms with its supplier is deemed to receive through the SPFE | art. 6.1 |
| Entry point | A recipient using a private platform must publish its entry point(s) in all communications and on its website; otherwise the SPFE is its entry point | art. 6.3 |
| Directory | Platforms must offer a public lookup of which businesses chose them | art. 6.4 |
| Interconnection | Platforms must interconnect with any other on a client's request, within 1 month, free of charge; meanwhile invoices travel through the SPFE | art. 8-9 |
| SPFE services | Free AEAT web form to issue invoices individually; web services for interconnection, copia fiel, status/payment messages, retrieval and download; access with electronic certificate, or Cl@ve for the forms; third parties need an apoderamiento | RD 238/2026 art. 11, DA 1.ª; Orden art. 5, 8-11 |
| SPFE invoices | UBL only; no embedded attachments; may be cancelled (*baja*) only if the operation never existed, leaving a trace | Orden art. 3.5-3.6 |
| Cost | SPFE use is free | art. 11.10 |

## 5. Formats, signature and unique code

- Structured message compliant with the **EN 16931** semantic model in one of: **CII**, **UBL** (with B2B adaptations), **EDIFACT** invoice, **Facturae** (art. 7.1). Peppol BIS Billing (UBL) is valid among private platforms (preamble). The Ministry of Economy can add syntaxes by order (DF 3.ª.3).
- Platforms must transform between all admitted syntaxes, preserving authenticity and integrity (art. 7.2). Between two platforms, the parties' agreed syntax applies; without agreement, the SPFE syntax (UBL) (art. 7.4).
- Invoices sent through private platforms must carry an **advanced electronic signature** (directly or delegated) per RF art. 10.1.a (art. 7.3). Through the SPFE, integrity is guaranteed by AEAT procedures (art. 11.7).
- **Unique code**: issuer NIF + series and number + issue date, in one field or concatenated (art. 7.5; Orden art. 6).
- Extra content beyond the RF minimum only if contractually agreed; buyer-supplied data (e.g. PO number) may be required only if sent to the supplier before the operation (art. 7.6).
- Systems producing the invoices must be adapted to LGT 29.2.j (Verifactu) (art. 2.d). In practice, the Verifactu QR URL travels as a field in the e-invoice (Orden HAC/1177/2024 art. 20.2).

## 6. Copia fiel to the SPFE

- Platforms or systems that do not use the SPFE to issue must send a **copia fiel** in UBL to the SPFE **simultaneously with issue**, flagged as a copy ("indicador de copia") (art. 6.2; Orden art. 4).
- The copy contains all fields with equivalent semantics in the SPFE syntax and at least the RF art. 6 (or 7.2) content (art. 2.b). No embedded files.
- No copy when the SPFE itself was the issuing or interconnection channel (art. 11.9; Orden art. 3.4).
- With self-billing or third-party issuing, the copy comes from the system of whoever issues (Orden art. 4.1).
- Duplicates (same unique code) are rejected (Orden art. 5.5). A rejected copy must be fixed and resent; if the original invoice itself had syntax or content errors not covered by RF art. 15, issue a correct original and send its copy (Orden art. 5.6).
- SPFE outage > 24 h: send within 4 working days after the fix (Orden art. 5.7).

## 7. Invoice states and payment reporting

**Between the parties** (art. 10), through the platforms:

| State | Mandatory? |
|---|---|
| Commercial acceptance or rejection, with date | Yes |
| Full effective payment, with date | Yes |
| Partial acceptance/rejection; partial payment with amount; assignment (factoring) with assignee | Optional |

- Deadline: **4 calendar days, excluding Saturdays, Sundays and national holidays**, from the event (art. 10.3).
- Buyers authorised to issue debit/credit notes instead of booking supplier rectificativas report on the corrected original (art. 10.5).

**To the SPFE** (art. 12; Orden art. 7-8), by the recipient, whatever channel was used:

- Mandatory: rejection, or full effective payment with its date, plus the **due date** of the payment term; same 4-day limit from the payment date (art. 12.3).
- Optional: date of receipt of goods/services or of the invoice when relevant under Ley 3/2004 art. 4 (art. 12.3).
- No rejection and no later rectificativa → the invoice is **presumed accepted** (art. 12.1).
- Payment counts as reported if the invoice or copy already shows a payment date on or before issue that equals the operation date (Orden art. 7.4), e.g. paid at the counter.
- The recipient may authorise its platform to report (art. 12.2). Issuers may voluntarily report collection, non-payment or date discrepancies (art. 12.4).
- Payment term computed under Ley 3/2004 art. 4; without an operation date on the invoice, from the issue date (art. 15). Construction 5 % retentions under LOE art. 19.1.a are excluded from the term (DA 6.ª).
- Uses: monitoring payment periods by the Ministries and the Observatorio Estatal de la Morosidad Privada, which lists late payers (art. 14).

## 8. Transitional rules

- **PDF**: for 12 months from 6 Oct 2027, > 8 M€ issuers must attach a legible PDF to each e-invoice unless the recipient voluntarily and expressly accepts only the original; the PDF goes to the recipient by any means, never to the SPFE (DT 2.ª).
- Status reporting by personas físicas ≤ 8 M€ voluntary until 6 Oct 2029 (DT 3.ª).
- Public-sector subcontractors: 24 months from the Orden to move from the LCSP DA 32.ª registry (DT 1.ª).
- From the effective date, the recipient's consent to e-invoices is no longer needed (RF art. 9.2 as amended).

## 9. Requirements for private platforms

From 6 Oct 2027 (art. 13; DF 4.ª.2):

- Able to connect to the SPFE.
- ISO/IEC 27001 (or equivalent) certified.
- AS2 or AS4 secure transport.
- Advanced electronic signature and seal (eIDAS).
- Exchange and transform all admitted syntaxes.
- Business continuity plan; permanent availability and support.
- Data governance and confidentiality (e.g. UNE 0080 maturity level 2).
- Free interconnection and interoperability; no charges to the requesting platform (art. 9.6).
- Automated retrieval of invoices received via the SPFE and immediate availability to clients (Orden art. 9).

## 10. Relation to Verifactu, SII and the RF

| Topic | Rule |
|---|---|
| RF content | Still applies in full; the e-invoice is the factura (RF art. 8 bis, 9) |
| Verifactu | Separate obligation; the producing system must comply (RD 238/2026 art. 2.d). SPFE web-form invoices are verifiable (DA 1.ª.2) |
| SII filers | Excluded from Verifactu but fully in the B2B mandate |
| Rectificativas | Electronic as well, with copia fiel; they rebut the presumption of acceptance (art. 12.1) |
| Conservation | Parties keep their own copies (RF art. 19); SPFE keeps them for the LGT period, ≤ 12 years (Ley 56/2007 DA 21.ª.5) |
| Data protection | Issuers must tell recipients that a copy goes to the SPFE (Ley 56/2007 DA 21.ª.6) |

## 11. Penalties and open points

- Ley 56/2007 art. 2 bis.9 fines (warning or up to 10,000 €) target companies that must offer e-invoices to consumers (art. 2 bis.4) and large service providers. No specific fine for B2B breaches was found in Ley 56/2007 or RD 238/2026 (unverified); an invoice not meeting the RF can still be penalised under LGT art. 201.
- Open as of Nov 2026: the SPFE technical documents and sandbox on the AEAT sede; the foral arrangements (DA 3.ª); any sector exclusion orders (art. 4.2).

## 12. Readiness checklist

```
1. Prior-year volumen de operaciones (modelo 390) > 8 M€?  → 6 Oct 2027, else 6 Oct 2028
2. Channel: private platform(s), SPFE, or both? Publish the entry point if private.
3. Output EN 16931 in UBL/CII/Facturae/EDIFACT, signed (private platform)?
4. Unique code = NIF + series/number + issue date?
5. Copia fiel in UBL to the SPFE at issue (when not issuing via SPFE)?
6. Receiving: can we ingest all four syntaxes (via platform) and retrieve from SPFE?
7. AP side: acceptance/rejection and full-payment messages within 4 working days;
   payment + due date to the SPFE; who is authorised (apoderamiento)?
8. Simplificadas cualificadas included; plain simplificadas excluded.
9. Verifactu-compliant producing system (QR URL field) from 2027.
10. > 8 M€: PDF attachment for the first 12 months unless waived.
```
