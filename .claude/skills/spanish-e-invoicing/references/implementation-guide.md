# Implementation Guide: Which Regime Applies, Peppol, ViDA

## Contents

- [1. Compliance matrix per invoice](#1-compliance-matrix-per-invoice)
- [2. Data flow of one B2B invoice from Oct 2028](#2-data-flow-of-one-b2b-invoice-from-oct-2028)
- [3. Build or buy](#3-build-or-buy)
- [4. Peppol in Spain](#4-peppol-in-spain)
- [5. ViDA and the EU context](#5-vida-and-the-eu-context)
- [6. Mapping RF art. 6 to EN 16931](#6-mapping-rf-art-6-to-en-16931)
- [7. Common failures](#7-common-failures)

## 1. Compliance matrix per invoice

For an issuer with domicilio fiscal in territorio común, not on SII, after all start dates:

| Invoice | Verifactu record + QR | Structured EN 16931 e-invoice | Copia fiel to SPFE | Status / payment reporting | Channel |
|---|---|---|---|---|---|
| B2C simplificada (ticket) | Yes | No | No | No | Paper / PDF / email |
| B2C completa | Yes | No (only if consumer consents) | No | No | Any |
| B2B simplificada (plain) | Yes | No | No | No | Any |
| B2B simplificada cualificada | Yes | Yes | Yes (if not via SPFE) | Yes | Platform or SPFE |
| B2B completa, Spanish recipient | Yes | Yes | Yes (if not via SPFE) | Recipient reports | Platform or SPFE |
| B2B, foreign recipient | Yes | No (RF rules; Peppol if agreed) | No | No | Any |
| B2G | Yes | Yes (Facturae / EN 16931) | Not under RD 238/2026 (B2G recipients are administrations) (unverified) | FACe states | FACe / regional PGEFe |
| Rectificativa of any of the above | Same as the original type | Same | Same | Same | Same |

Variations: SII filer → no Verifactu, rest unchanged. Basque issuer → TicketBAI instead of Verifactu. Navarra issuer → no software-integrity regime yet.

Start dates: Verifactu 1 Jan 2027 (IS) / 1 Jul 2027 (others); B2B 6 Oct 2027 (> 8 M€) / 6 Oct 2028 (others); B2G in force since 2015.

## 2. Data flow of one B2B invoice from Oct 2028

```
1. User approves the invoice in the SIF.
2. SIF creates the Verifactu registro de alta (hash of previous record), and in
   VERI*FACTU mode queues it for AEAT (flow control, ≤ 1,000 per send).
3. SIF renders EN 16931 (e.g. UBL) including the Verifactu QR URL field and the
   unique code NIF+series/number+date; signs it (advanced signature) if it goes
   through a private platform.
4. Delivery: recipient's published entry point (private platform, interconnected)
   or, by default, the SPFE.
5. Same moment: copia fiel in UBL to the SPFE (skipped if the SPFE was the channel).
6. Recipient's platform returns acceptance/rejection (≤ 4 working days).
7. Recipient pays; reports full payment + date + due date to the SPFE and to the
   issuer (≤ 4 working days).
8. Issuer reconciles the payment in the bank feed (see spanish-bank-files) and may
   report collection or discrepancies to the SPFE.
```

## 3. Build or buy

| Component | Build | Buy / connect |
|---|---|---|
| Verifactu records, hash, QR, AEAT web service | Feasible: published XSD/WSDL, SHA-256, certificate auth. Producer must sign the declaración responsable and accept LGT 201 bis exposure | Most ERP/invoicing vendors ship it |
| EN 16931 generation (UBL/CII/Facturae) | Feasible with open libraries; validate against EN 16931 schematrons and the SPFE UBL rules | Platform APIs |
| Private platform (exchange) | Requires ISO 27001, AS2/AS4, interconnection duties, 24/7 support (RD 238/2026 art. 13) | Use an existing platform or the free SPFE |
| SPFE integration | Web services with electronic certificate; apoderamiento for third parties (Orden HAC/1028/2026 art. 11) | Platform may act as authorised intermediary (RD 238/2026 art. 11.5) |
| B2G | Facturae + XAdES + DIR3 + FACe web services | Providers connect to FACe |

Using only the SPFE (free AEAT form or web services) is a legitimate path for small businesses: no platform contract, no signature requirement on the issuer's side, no copia fiel.

## 4. Peppol in Spain

- RD 238/2026 does not mandate Peppol, but its preamble states that Peppol BIS messages are valid among private platforms because they use UBL and follow EN 16931. AS4 (Peppol's transport) is one of the two admitted protocols (art. 13.1.b).
- The SPFE accepts UBL under AEAT's own specifications (Orden HAC/1028/2026 art. 3.1); whether it is reachable as a Peppol participant was not published as of Nov 2026 (unverified).
- Spanish identifiers on Peppol: scheme 9920 (Spanish VAT number, ES:VAT) (unverified); the B2B unique code requires the issuer's NIF.
- Spain's Peppol Authority and B2G Peppol reachability through FACe: (unverified).
- Practical reading: a Peppol access point that also meets the RD 238/2026 platform requirements (ISO 27001, transformations to CII/Facturae/EDIFACT, SPFE connection, copia fiel) can serve as a Spanish private platform.

## 5. ViDA and the EU context

- **Directive (EU) 2025/516** ("VAT in the Digital Age"), adopted 11 Mar 2025, in force 14 Apr 2025:
  - Member States may impose domestic e-invoicing without recipient acceptance and without an EU derogation, provided cross-border flows stay possible.
  - From **1 Jul 2030**: intra-EU B2B supplies require EN 16931 e-invoices and near-real-time digital reporting to the Member State.
  - National real-time reporting systems must converge with the EU model by 1 Jan 2035.
- Spain's B2B mandate is a "decentralised with central repository" model: free choice of platform or the public solution, copia fiel to AEAT, and payment-status reporting, which is unusual in the EU and driven by late-payment policy (Ley 18/2022).
- Spain's SII (since 2017) already gives AEAT invoice-level data for large taxpayers; Verifactu extends real-time data (in VERI*FACTU mode) to the rest.

## 6. Mapping RF art. 6 to EN 16931

| RF art. 6.1 | EN 16931 business term (indicative) |
|---|---|
| a) number and series | BT-1 Invoice number |
| b) issue date | BT-2 Invoice issue date |
| c) names | BT-27 Seller name; BT-44 Buyer name |
| d) NIF | BT-31 Seller VAT identifier; BT-48 Buyer VAT identifier (or BT-30/BT-47 legal registration) |
| e) addresses | BG-5 Seller postal address; BG-8 Buyer postal address |
| f) description, unit price, discounts | BG-25 Invoice line (BT-153 item name, BT-146 net price, BT-147 discount) |
| g) rate | BT-152 / BT-119 VAT category rate |
| h) cuota in euros | BT-110 Total VAT; BT-111 in accounting currency when invoice currency ≠ EUR (BT-6 = EUR) |
| i) operation date | BT-72 Actual delivery date / BG-14 invoicing period |
| j) exemption reference | BT-120 / BT-121 VAT exemption reason (text / code), category E |
| m) inversión del sujeto pasivo | Category AE + BT-120 «inversión del sujeto pasivo» |
| Intra-EU supply | Category K + exemption reason |
| Rectificativa reference | BG-3 Preceding invoice reference (BT-25, BT-26); type code 381 or 384 |
| IRPF retention | No native EN 16931 term; handled as an allowance or in a Spanish extension (Facturae has native withholding fields). Check the SPFE UBL specification (unverified) |

The mapping is indicative; the binding mapping for the SPFE is the AEAT UBL specification under Orden HAC/1028/2026 annex I.

## 7. Common failures

| Failure | Consequence | Fix |
|---|---|---|
| Treating Verifactu as the e-invoice | No structured invoice delivered from 2027-2028 | Implement both layers |
| Deleting a draft that already produced a Verifactu alta | Chain gap; integrity warning | Use an anulación record |
| Same invoice number reused across series in the unique code | SPFE rejects duplicates | Include the series in the unique code |
| Copia fiel sent late or not at all | Platform non-compliance from 6 Oct 2027 | Send at issue; retry; outage rule 4 working days |
| Payment status not reported in 4 working days | Breach of RD 238/2026 art. 12 | Automate from the bank reconciliation |
| Rejecting an invoice by email only | Presumed accepted in the SPFE | Report rejection through the platform/SPFE |
| VAT in foreign currency only | Breach of RF art. 12.1 | Provide the euro VAT total (BT-111) |
