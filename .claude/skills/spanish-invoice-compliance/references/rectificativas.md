# Facturas Rectificativas

## Contents

- [1. When a rectificativa is mandatory](#1-when-a-rectificativa-is-mandatory)
- [2. When it is not a rectificativa](#2-when-it-is-not-a-rectificativa)
- [3. Content, series and form](#3-content-series-and-form)
- [4. Deadlines](#4-deadlines)
- [5. VAT effect for seller and buyer](#5-vat-effect-for-seller-and-buyer)
- [6. Bad debts: LIVA art. 80](#6-bad-debts-liva-art-80)
- [7. PGC entries](#7-pgc-entries)
- [8. Rectificativas under Verifactu, SII and the B2B mandate](#8-rectificativas-under-verifactu-sii-and-the-b2b-mandate)
- [9. Checklist](#9-checklist)

Spain has no "credit note" as a separate legal document: every correction of an issued invoice is a *factura rectificativa* (RF art. 15). The business word *abono* is used for a negative rectificativa.

## 1. When a rectificativa is mandatory

| Cause | Rule |
|---|---|
| Original misses an art. 6 or 7 requirement (e.g. buyer NIF, wrong address) | RF art. 15.1 |
| Cuotas repercutidas determined incorrectly (wrong rate, VAT charged on ISP or exempt supply, arithmetic) | RF art. 15.2; LIVA art. 89.Uno |
| A LIVA art. 80 event: return of goods or packaging, discounts after the supply, volume rebates, total or partial cancellation, price change, concurso of the customer, uncollectable debt | RF art. 15.2; LIVA art. 80 |

## 2. When it is not a rectificativa

- Returned goods or packaging netted on the next invoice to the same customer, same VAT rate, positive or negative result (RF art. 15.2 second para.).
- A completa issued in exchange for a simplificada that met art. 7.1 (RF art. 15.6). It goes in the completa series and references the simplificada.
- Corrections that are not for a cause in §1 are not rectificativas (art. 15.6); a document that only cancels a never-performed operation is handled by cancelling it (Verifactu anulación record; B2B baja in the SPFE, Orden HAC/1028/2026 art. 3.5).

## 3. Content, series and form

- A **new invoice** identifying the rectified invoice(s) by number and date (art. 15.4). One rectificativa may correct several invoices if all are identified.
- Volume discounts and AEAT-authorised cases: identifying the period is enough (art. 15.4).
- All art. 6 (or art. 7 for a simplificada rectificativa) requirements apply (art. 15.5). Letters f), g), h) show the correction, either:
  - **by difference**: only the amount of the correction, positive or negative; or
  - **by substitution**: the amounts as they stand after the correction, also stating the amount of the correction.
- **Own series**, always (art. 6.1.a.2.º, 7.1.a.4.º). Common practice: prefix "R" (e.g. R2027-0001).
- A simplificada may always be used to rectify (art. 4.1.b).
- State the cause (e.g. "Rectificativa por devolución, art. 80.Dos LIVA"). The RF does not require it in words, but the libro registro, SII and Verifactu records require the type of rectificativa (R1-R5 in SII/Verifactu coding; see §8).

## 4. Deadlines

- Issue as soon as the cause is known, within **4 years** from the devengo or from the LIVA 80 event (RF art. 15.3; LIVA art. 89.Uno).
- Send to the recipient before day 16 of the month after issue (RF art. 18).
- Increase of cuotas to a consumer is not allowed except for legal rate rises (in that month and the next) (LIVA art. 89.Tres.1.º).
- Increase of cuotas without a prior AEAT requirement: file a rectifying self-assessment with surcharges and interest (LGT 26-27), unless the cause is LIVA 80 or a well-founded legal error, which go into the current period (LIVA art. 89.Cinco).
- Decrease: either start the LGT 120.3 rectification procedure, or regularise in the period of the rectification within one year, refunding the buyer the VAT charged in excess (LIVA art. 89.Cinco a-b).

## 5. VAT effect for seller and buyer

| Party | Effect | Where |
|---|---|---|
| Seller | Reduces (or increases) output VAT in the period of the rectificativa | modelo 303, libro de facturas expedidas |
| Buyer (business) | Must reduce input VAT in the period it receives the rectificativa; in concurso cases, in the original deduction periods | modelo 303; RIVA art. 24.2.b |
| Buyer (consumer) | No VAT effect | — |

## 6. Bad debts: LIVA art. 80

| Requirement | Concurso (art. 80.Tres) | Uncollectable debt (art. 80.Cuatro) |
|---|---|---|
| Trigger | Auto de declaración de concurso after the devengo | Unpaid 1 year from devengo; 6 months or 1 year if seller's prior-year volume ≤ 6,010,121.04 € (LIVA 121) |
| Other conditions | — | Invoiced and booked in time; buyer is a business, or base > 50 € excl. VAT; claim by court, notarial requirement or any reliable means of demand |
| Deadline for the rectificativa | 2 months from the end of the period for creditors to report (Ley Concursal) | Within 6 months after the 6-month / 1-year period |
| Communication to AEAT | Electronic form in the AEAT sede within 1 month of issuing the rectificativa, with copies and evidence | Same (RIVA art. 24.2.a.2.º) |
| Copy to | Administración concursal | — |
| Excluded | Secured, guaranteed or insured debts, related parties, recipients not established in Spain/Canarias/Ceuta/Melilla (with exceptions) | Same (LIVA art. 80.Cinco) |
| Reversal | Concurso concluded by some art. 176 causes: rectificativa upwards | Claim withdrawn or payment agreed: rectificativa upwards within 1 month (art. 80.Cuatro.C) |

The buyer (if a business) must report receipt through the AEAT form and reduce deducted VAT in its return (RIVA art. 24.2.b).

## 7. PGC entries

Seller, by difference, return of goods (21 %):

| Account | Debit | Credit |
|---|---|---|
| **708** Devoluciones de ventas | base | |
| **477** HP IVA repercutido | cuota | |
| **430** Clientes | | total |

Seller, post-invoice volume rebate: **709** instead of **708**. Prompt-payment discount after invoicing: **706**.

Seller, bad debt recovered through VAT (LIVA 80.Cuatro), after reclassification to **436**:

| Account | Debit | Credit |
|---|---|---|
| **477** HP IVA repercutido | cuota | |
| **436** Clientes de dudoso cobro | | cuota |

The remaining base is a loss in **650** (or covered by an impairment in **490** / **694**) when final; see `spanish-year-end-closing`.

Buyer receiving a negative rectificativa:

| Account | Debit | Credit |
|---|---|---|
| **400** Proveedores | total | |
| **608** Devoluciones de compras (or **609** Rappels por compras) | | base |
| **472** HP IVA soportado | | cuota |

## 8. Rectificativas under Verifactu, SII and the B2B mandate

| System | How a correction is recorded |
|---|---|
| Verifactu / SIF (RD 1007/2023) | A rectificativa is a new invoice with its own *registro de alta*, invoice type R1-R5 and the identification of the rectified invoices (art. 10.1.g). An invoice issued in error is cancelled with a *registro de anulación* (art. 11) that does not delete the original record; both enter the hash chain. A rejected alta can be corrected with a *subsanación* (Orden HAC/1177/2024 annex) (unverified detail) |
| SII | Invoice types: R1 (error grounded in law and LIVA 80.Uno, Dos, Seis), R2 (80.Tres concurso), R3 (80.Cuatro bad debts), R4 (other), R5 (rectifying a simplificada); by difference ("I") or substitution ("S") (unverified against current SII validation document) |
| B2B mandatory e-invoice (from 6 Oct 2027 / 6 Oct 2028) | Rectificativas are electronic and need a copia fiel in the SPFE; a rectificativa after an invoice counts against the presumption of acceptance (RD 238/2026 art. 12.1). Buyers authorised to issue debit/credit notes report states on the corrected original (art. 10.5, 12.5). See `spanish-e-invoicing` |

## 9. Checklist

```
1. Cause is one of RF 15.1 / 15.2 (else: not a rectificativa)?
2. Own number in the rectificativa series, own issue date?
3. Identifies the rectified invoice(s) (number + date), or the period for volume rebates?
4. Shows the correction (by difference or substitution, stating the correction)?
5. VAT per original rate; base per rate if mixed?
6. Within 4 years of the devengo / LIVA 80 event?
7. Sent to the customer before day 16 of next month?
8. LIVA 80.Tres / 80.Cuatro: AEAT form within 1 month, evidence attached?
9. Recorded in libro registro / SII / Verifactu with the right rectificativa type?
```
