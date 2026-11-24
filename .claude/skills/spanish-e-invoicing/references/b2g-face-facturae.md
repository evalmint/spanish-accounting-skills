# B2G: FACe and Facturae

## Contents

- [1. Legal basis](#1-legal-basis)
- [2. Who must send e-invoices to the administration](#2-who-must-send-e-invoices-to-the-administration)
- [3. Entry points (PGEFe) and FACe](#3-entry-points-pgefe-and-face)
- [4. DIR3 codes](#4-dir3-codes)
- [5. Formats and signature](#5-formats-and-signature)
- [6. Deadlines and payment](#6-deadlines-and-payment)
- [7. Processing states](#7-processing-states)
- [8. Checklist](#8-checklist)

## 1. Legal basis

| Instrument | Content |
|---|---|
| Ley 25/2013, of 27 Dec, *de impulso de la factura electrónica y creación del registro contable de facturas en el Sector Público* | Who must e-invoice the administration (art. 4), format and signature (art. 5), entry points (art. 6), registro contable de facturas (art. 8-10). Art. 4 in force 15 Jan 2015 (DF 8.ª) |
| Orden HAP/492/2014 and Orden HAP/1074/2014 | Functional and technical requirements of the registro contable de facturas and of the Punto General de Entrada de Facturas Electrónicas (PGEFe) (titles from memory; unverified) |
| Orden HAP/1650/2015 | Updated the Facturae format, adopting version 3.2.x (unverified) |
| Ley 9/2017, de Contratos del Sector Público (LCSP), art. 198.4 and DA 32.ª | Payment term; invoice data and the subcontractors' registry |
| Ley 3/2004 (late payment) | Statutory interest |

## 2. Who must send e-invoices to the administration

Mandatory e-invoice through the corresponding entry point for (Ley 25/2013 art. 4.1):

- Sociedades anónimas and sociedades de responsabilidad limitada.
- Legal persons and entities without legal personality lacking Spanish nationality.
- Permanent establishments and branches of non-residents.
- Uniones temporales de empresas (UTE).
- AIE, AEIE, pension, venture capital, investment, asset, mortgage-market regulation, securitisation and investment guarantee funds.

Personas físicas (autónomos) **may** e-invoice but are not obliged by Ley 25/2013. Each administration may exclude invoices up to **5,000 €** and those to services abroad (art. 4.1 last para.); the State administration used this option (unverified: check the receiving administration's rule).

## 3. Entry points (PGEFe) and FACe

- The State, each Comunidad Autónoma and each local entity has a Punto General de Entrada de Facturas Electrónicas; regions and municipalities may adhere to the State's (art. 6.1). If an administration has none, suppliers may use the State's, which stores the invoice in a repository (art. 6.7).
- **FACe** (face.gob.es) is the State's PGEFe, used by the AGE and by many regions and municipalities that adhered. Some regions run their own (e.g. Catalonia's e.FACT, Basque and Navarre portals) (unverified list).
- Submission gives an electronic receipt with date and time and an automatic entry in the administration's registry (art. 6.4). The invoice then flows to the registro contable de facturas of the competent accounting office (art. 9).
- Channels: web upload, web services for software, and connectors run by e-invoice providers; FACe also connects with Peppol (unverified).

## 4. DIR3 codes

Each invoice must identify the receiving units with their DIR3 codes (directory of the Spanish public administration units):

| Role | Facturae role code |
|---|---|
| Oficina contable | 01 |
| Órgano gestor | 02 |
| Unidad tramitadora | 03 |
| Órgano proponente (optional) | 04 |

The codes come from the contracting body (usually in the contract or order). A wrong DIR3 code is the most common rejection reason (practitioner experience; unverified as a statistic). LCSP DA 32.ª also requires the invoice to identify the accounting body, the contracting body and the recipient.

## 5. Formats and signature

- Structured format, signed with an advanced electronic signature based on a qualified certificate (RF art. 10.1.a), or an advanced electronic seal of the legal person (Ley 25/2013 art. 5).
- **Facturae** is the Spanish XML format; versions 3.2, 3.2.1 and 3.2.2 are in use, 3.2.2 being the latest (facturae.gob.es; unverified for current acceptance list). Signature: XAdES per the Facturae signature policy.
- Directive 2014/55/EU requires public contracting authorities to accept EN 16931 invoices (UBL or CII); FACe accepts them according to third-party sources (unverified).
- Facturae is also one of the four syntaxes allowed under the B2B mandate (RD 238/2026 art. 7.1.d), so one generator can serve both.
- Verifactu applies to B2G invoices as well: the producing system must comply from 2027, and the QR URL goes as a field in the structured invoice.

## 6. Deadlines and payment

| Rule | Value | Source |
|---|---|---|
| Present the invoice in the administrative registry | Within 30 days of delivery of goods or services | Ley 25/2013 art. 3 |
| Administration approves conformity | Within 30 days of delivery (unverified detail) | LCSP art. 198.4 |
| Administration pays | Within 30 days of approving the conformity documents; late-payment interest under Ley 3/2004 after that | LCSP art. 198.4 |
| Ordinary RF issue deadline | Before day 16 of the month after the devengo (B2B rule applies to administrations as business-like recipients) | RF art. 11.1 |

## 7. Processing states

FACe shows the processing state of each invoice to the supplier (Ley 25/2013 art. 6.3). Common states: registered, registered in the RCF, accounted (obligación reconocida), paid, rejected, cancelled; with numeric codes (e.g. 1200, 1300, 2400, 2500, 2600, 3100) (codes unverified). Cancellation requests go through FACe and must be accepted by the administration.

## 8. Checklist

```
1. Supplier is SA/SL/UTE/non-resident/listed fund? → e-invoice mandatory (unless ≤ 5,000 € and the administration excludes it)
2. DIR3 codes (01 oficina contable, 02 órgano gestor, 03 unidad tramitadora) from the contract?
3. Facturae 3.2.x (or EN 16931 if accepted), signed XAdES with qualified certificate or seal?
4. RF art. 6 content, contract/expedient number, and Verifactu QR URL field from 2027?
5. Submitted to the right PGEFe within 30 days of delivery?
6. Track the state; chase payment after 30 + 30 days; claim Ley 3/2004 interest if late.
```
