# Verifactu: Requirements for Invoicing Software (SIF)

## Contents

- [1. Legal chain](#1-legal-chain)
- [2. Timeline](#2-timeline)
- [3. Who is in scope](#3-who-is-in-scope)
- [4. What counts as an invoicing system](#4-what-counts-as-an-invoicing-system)
- [5. The two modes: VERI*FACTU and no-verifactu](#5-the-two-modes-verifactu-and-no-verifactu)
- [6. Billing records (registros de facturación)](#6-billing-records-registros-de-facturación)
- [7. Hash chain and signature](#7-hash-chain-and-signature)
- [8. QR code and phrase on the invoice](#8-qr-code-and-phrase-on-the-invoice)
- [9. Event log, conservation, AEAT access](#9-event-log-conservation-aeat-access)
- [10. Sending records to AEAT](#10-sending-records-to-aeat)
- [11. Declaración responsable of the producer](#11-declaración-responsable-of-the-producer)
- [12. Penalties](#12-penalties)
- [13. Practical decisions](#13-practical-decisions)

## 1. Legal chain

| Level | Instrument | Content |
|---|---|---|
| Law | Ley 11/2021 (*Ley antifraude*), art. 13 → LGT art. 29.2.j and 201 bis | Software that supports accounting, invoicing or management must guarantee integrity, conservation, accessibility, legibility, traceability and inalterability of records; penalties for producing and possessing non-compliant software |
| Regulation | RD 1007/2023, of 5 Dec (BOE-A-2023-24840), "Reglamento SIF" | Scope, records, hash, signature, declaración responsable, VERI*FACTU option. Amended by RD 254/2025 (dates, art. 4, 6) and RD-ley 15/2025 (dates) |
| Technical order | Orden HAC/1177/2024, of 17 Oct (BOE-A-2024-22138), in force 29 Oct 2024 | Technical, functional and content specifications; XML annex; QR specs. Not amended as of Nov 2026 (consolidated text last updated 28 Oct 2024) |
| AEAT sede | Technical documents (XSD/WSDL, hash algorithm, QR URL format, validations, FAQs) | Published under Orden HAC/1177/2024 DA 1.ª |
| Invoice rules | RD 1619/2012 art. 6.5, 7.5, 8.4 (added by RD 1007/2023) | QR and phrase on invoices; presumption of authenticity and integrity |

## 2. Timeline

| Date | Event | Source |
|---|---|---|
| 7 Dec 2023 | RD 1007/2023 in force | DF 4.ª |
| 29 Oct 2024 | Orden HAC/1177/2024 in force | Orden DF única |
| 29 Jul 2025 | Producers must offer adapted products; AEAT reception service available (9 months after the Orden) | RD 1007/2023 DF 4.ª |
| ~~1 Jul 2025~~ | Original user deadline | RD 1007/2023 original DF 4.ª |
| ~~1 Jan 2026 / 1 Jul 2026~~ | First postponement | RD 254/2025, of 1 Apr |
| **1 Jan 2027** | Users that are IS taxpayers (art. 3.1.a) must have adapted systems | DF 4.ª as amended by RD-ley 15/2025, of 2 Dec (BOE 3 Dec 2025, in force 4 Dec 2025, validated by Congress 11 Dec 2025) |
| **1 Jul 2027** | All other users of art. 3.1 | Same |

Systems under multi-year maintenance contracts must be adapted by those same user dates (DF 4.ª third para.). No further change was published in BOE up to 24 Nov 2026 (consolidated text last updated 3 Dec 2025).

## 3. Who is in scope

In scope, if they use an invoicing system for any part of their activity (art. 3.1):

- IS taxpayers (*contribuyentes del Impuesto sobre Sociedades*); partially exempt entities only for taxable income.
- IRPF taxpayers with economic activities.
- IRNR taxpayers with a permanent establishment.
- Entidades en atribución de rentas with economic activities.
- Producers and sellers of invoicing systems, for their products (art. 3.2).

Out of scope:

| Exclusion | Source |
|---|---|
| Taxpayers keeping VAT books through the SII (RIVA art. 62.6: monthly VAT period, i.e. grandes empresas > 6,010,121.04 €, REDEME, VAT groups, voluntary SII) | RD 1007/2023 art. 3.3 |
| Domicilio fiscal in the Basque Country or Navarra (foral systems apply) | art. 1.3 |
| Fully exempt IS entities (LIS art. 9.1) | art. 3.1.a |
| Electricity-market and CNE invoices (RF DA 3.ª and 6.ª) | art. 4.1 |
| Invoices of permanent establishments abroad | art. 4.2 |
| Invoices issued by the recipient or a mandatory third party, where those keep books through SII | art. 4.3 |
| Individual AEAT exemption on request | art. 5 |

Canarias, Ceuta and Melilla are in scope; VAT references read as IGIC / IPSI (art. 1.3).

## 4. What counts as an invoicing system

A *sistema informático de facturación* is the hardware and software used to issue invoices by admitting invoicing data, keeping it (inside or by export), and processing it to produce other results (art. 1.2). "Factura" covers completas and simplificadas.

- A taxpayer can use any compliant commercial system, its own development, or the free AEAT application if available (art. 7.b; Orden art. 19: individual issuing in own name or by an apoderado, recipient mandatory, PDF output) (availability of the AEAT app: unverified).
- One system may serve several taxpayers if records are kept separate per taxpayer and VERI*FACTU can be switched per taxpayer (art. 7.a; Orden art. 2).
- Invoices written by hand are outside the reglamento. Whether generic office tools (word processor, spreadsheet) count depends on how they are used; AEAT FAQs address it (unverified: check the current FAQ before advising).

## 5. The two modes: VERI*FACTU and no-verifactu

| | VERI*FACTU ("sistema de emisión de facturas verificables") | No-verifactu |
|---|---|---|
| Records sent to AEAT | Every record, automatically and continuously as generated (art. 16.1) | Kept locally; sent only on AEAT requirement (art. 14.2; Orden art. 18) |
| Electronic signature of records | Not required; the hash is enough (art. 16.3) | Required: XAdES Enveloped with a qualified certificate (art. 12; Orden art. 14) |
| Presumption of compliance with art. 8 | Yes, by design (art. 16.2) | Must prove it |
| Event log | Not required (Orden art. 3) | Required (Orden art. 9) |
| Phrase on invoice | «Factura verificable en la sede electrónica de la AEAT» or «VERI*FACTU» (RF art. 6.5.b) | None |
| QR on invoice | Yes | Yes (different URL) |
| Option | Starts by systematically sending; lasts at least until 31 Dec of that year (art. 16.5; Orden art. 17); waiver signalled in the submission message | — |

The free AEAT application, if used, is always VERI*FACTU (art. 16.4).

## 6. Billing records (registros de facturación)

**Registro de alta** (art. 9-10), generated simultaneously with or just before issuing each invoice. Content:

- Issuer NIF and name; recipient NIF and name when the RF requires them.
- Whether issued by the supplier, the recipient or a third party (art. 5 RF), with their identification.
- Series and number; issue date; supply date if different.
- Invoice type (completa / simplificada, and detail); rectificativa type and rectified invoices; simplificadas replaced.
- General description; total amount.
- VAT regime(s); ISP flag (LIVA 84.Uno.2.º and 3.º); base, rates, cuota, RE rates and cuota; whether issued under régimen simplificado or RE; exempt base and cause; non-subject amount and cause.
- Previous record reference (series, number, date of the previous record) and part of its hash; system identification code and producer data; timestamp to the second; generation circumstances.
- All amounts in euros, converted if the invoice is in another currency (art. 10.2).

**Registro de anulación** (art. 11): when an invoice was issued in error. NIF and name, issuer type, series/number and date of the cancelled invoice, previous record link and hash, system data, timestamp. The original alta stays; cancellation never deletes.

Corrections are always new records (art. 8.2.a). A rectificativa invoice is a new alta with rectificativa type, not an anulación.

## 7. Hash chain and signature

- Every alta, anulación and event record carries a *huella* (hash) and points to the previous record's hash (art. 12; Orden art. 7, 13).
- Hash input fields (Orden art. 13.1): alta = issuer NIF, series and number, issue date, invoice type, total cuota, total amount, previous hash, generation timestamp with time zone; anulación = issuer NIF, series and number, issue date, previous hash, timestamp; event = producer ID, system ID, version, installation number, issuer NIF, event type, previous hash, timestamp.
- Algorithm: **SHA-256** for all record types, per AEAT FAQ "Huella o hash" and the AEAT technical document on hash generation (Orden art. 13.2 delegates to AEAT). Exact concatenation and encoding: follow the AEAT document.
- Signature (no-verifactu only): ETSI EN 319 132, XAdES Enveloped, private key of a qualified certificate from an EU Trusted List provider (Orden art. 14).
- The system must detect and warn about any break in integrity or chaining and log it (Orden art. 6-7).

## 8. QR code and phrase on the invoice

- Every invoice from a SIF, paper or image, carries a QR code (RF art. 6.5.a, 7.5; Orden art. 20-21):
  - Size 30x30 mm to 40x40 mm; ISO/IEC 18004; error correction level M.
  - Content: the AEAT verification URL with issuer NIF, series and number, issue date and total amount.
  - The URL differs between VERI*FACTU and no-verifactu systems; exact URL, encoding and placement are in the AEAT technical document (Orden art. 21.2). Do not hard-code a URL from memory.
- Structured e-invoices (e.g. the B2B mandate) carry the URL as a separate field instead of the image (Orden art. 20.2).
- VERI*FACTU invoices also carry the phrase in a visible font similar to the rest of the invoice (Orden art. 20.1.b).
- Recipients can scan the QR and send the data to AEAT; for VERI*FACTU invoices this confirms that the issuer reported the invoice (RD 1007/2023 art. 17).

## 9. Event log, conservation, AEAT access

- No-verifactu systems keep an event log (Orden art. 9): start and end of no-verifactu operation; launch and findings of anomaly checks on billing and event records; backup restoration; exports of billing or event records. Plus a summary event record at least every 6 hours of operation and before shutdown. Events are chained and protected like billing records.
- Records are kept for the LGT limitation period, exportable to external storage in a legible electronic format (art. 8.2.c; Orden art. 8).
- AEAT may inspect on site and demand immediate access, downloads and passwords (art. 14.1), or request the records electronically (art. 14.2; Orden art. 18).
- Access to tax data must be separated from non-tax confidential data (art. 8.4).

## 10. Sending records to AEAT

- Web service in the AEAT sede, identification with an electronic certificate (own, representative or colaborador social) (Orden art. 5).
- Up to 1,000 records per submission; flow control with a waiting time "t", initially 60 seconds, updated in each response; the next submission waits t seconds or until 1,000 records accumulate, whichever comes first (Orden art. 16.2; annex 2.2).
- Failed submissions: resend in generation order as soon as possible, flag the incident, retry at least hourly and show a warning with the count pending (Orden art. 16.4).
- The response gives a CSV (código seguro de verificación) if at least one record is accepted and lists rejected records with error codes (Orden art. 16.5). Acceptance does not preclude later checks.

## 11. Declaración responsable of the producer

- The producer certifies in writing that the system complies with LGT 29.2.j, the reglamento and the Orden (art. 13).
- Visible in the system for every version, and given to clients and resellers at purchase; kept for all versions; available on request.
- Content (Orden art. 15): system name, ID and version; components and functions; whether it can run only as VERI*FACTU; signature types used in no-verifactu; producer identification; date and place of signature.
- There is no AEAT certification or approval ("homologación"); the declaración is self-certification.

## 12. Penalties

| Infringement | Penalty | Source |
|---|---|---|
| Producing or selling software that allows double books, hidden or altered records, or misses the specifications | 150,000 € per financial year with sales and per type of system | LGT art. 201 bis.1, .4 |
| Selling without the declaración responsable (certification) | 1,000 € per system sold | LGT art. 201 bis.4 |
| Possessing (using) non-certified or altered systems | 50,000 € per financial year | LGT art. 201 bis.2, .4 |
| Invoice-content breaches (e.g. missing QR) | 1 % of the operations | LGT art. 201.2.a |

## 13. Practical decisions

| Question | Answer |
|---|---|
| Company on SII | Out of Verifactu; continue SII (4-day reporting). Still in the B2B mandate |
| Company leaves SII during the year | Comes into scope from then (unverified: check AEAT FAQ on transitions) |
| Autónomo using a marketplace that self-bills them | Excluded only if the marketplace keeps books through SII (art. 4.3); otherwise the issuer's system must comply |
| Should we choose VERI*FACTU? | Fewer requirements (no signature, no event log, presumed compliance) in exchange for real-time reporting; most SME software defaults to it |
| Multi-company SaaS | Separate records and chain per taxpayer; per-taxpayer VERI*FACTU switch |
| Offline POS | Allowed; records generated at issue and sent when the connection returns, in order, with the incident flag (VERI*FACTU) |
