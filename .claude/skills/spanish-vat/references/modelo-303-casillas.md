# Modelo 303: casillas, PGC mapping and settlement entries

Which casilla each operation goes into, how the casillas tie to the PGC accounts **472** and **477**, and how the period result is booked to **4750** or **4700**. Rules behind each case are in `vat-reference.md` and `intracomunitario-e-importacion.md`.

Source: AEAT, *Modelo 303. Instrucciones 2026* (sede.agenciatributaria.gob.es, checked 2026-11-24); RIVA arts. 71-74 bis. Casilla numbers are those of the 2026 form.

## Contents

1. [PGC structure for IVA](#1-pgc-structure-for-iva)
2. [IVA devengado (output)](#2-iva-devengado-output)
3. [IVA deducible (input)](#3-iva-deducible-input)
4. [Información adicional](#4-información-adicional)
5. [Resultado](#5-resultado)
6. [Mapping table: operation to casilla to account](#6-mapping-table-operation-to-casilla-to-account)
7. [Period-end settlement entries](#7-period-end-settlement-entries)
8. [Last period of the year and modelo 390](#8-last-period-of-the-year-and-modelo-390)
9. [Reconciliation checks](#9-reconciliation-checks)

## 1. PGC structure for IVA

The PGC 2007 gives only the three-digit accounts; companies open sub-accounts so that each casilla can be read from the ledger.

| PGC account | Name | Suggested company sub-accounts (not PGC, examples) |
|---|---|---|
| **472** | Hacienda Pública, IVA soportado | 472.21 / 472.10 / 472.04 interior corrientes by rate; 472.BI bienes de inversión; 472.IM importaciones; 472.AI adquisiciones intracomunitarias; 472.ISP inversión del sujeto pasivo |
| **477** | Hacienda Pública, IVA repercutido | 477.21 / 477.10 / 477.04 / 477.00 by rate; 477.AI intra-EU acquisitions self-assessed; 477.ISP reverse charge self-assessed; 477.RE recargo de equivalencia |
| **4750** | H.P., acreedora por IVA | Result payable |
| **4700** | H.P., deudora por IVA | Result to compensate or refund |
| **634** / **639** | Ajustes negativos / positivos en la imposición indirecta | Prorrata and regularisation adjustments |

Write sub-accounts with a dot or extra digits as the company's chart does; do not invent new PGC three-digit accounts.

## 2. IVA devengado (output)

| Casillas | Content |
|---|---|
| 150-152 | Base, rate and cuota at 0 % (art. 91.Cuatro donations; old temporary food rates) |
| 01-03 | Base, rate, cuota at 4 % |
| 04-06 | Base, rate, cuota at 10 % (including the temporary 10 % on energy in 2026) |
| 07-09 | Base, rate, cuota at 21 % |
| 153-155, 165-167 | Other rates listed by the form (used for the 2 %, 5 % and 7.5 % temporary rates in earlier years; mapping of each block unverified) |
| 10-11 | Intra-EU acquisitions of goods and services: base and self-assessed cuota (all rates, including 0 %) |
| 12-13 | Other reverse charge (art. 84.Uno.2º and 4º): non-EU services, domestic construction, scrap, gold, phones etc. |
| 14-15 | Modification of bases and cuotas (art. 80 credit notes, bad debts, tax-free refunds), with sign; not split by rate |
| 156-158 | Recargo de equivalencia 1.75 % |
| 168-170 | Recargo 0.5 % |
| 19-21 | Recargo 1.4 % |
| 22-24 | Recargo 5.2 % |
| 16-18 | Other recargo rates listed by the form (unverified use in 2026) |
| 25-26 | Modification of recargo bases and amounts |
| 27 | Total cuota devengada |

## 3. IVA deducible (input)

Bases are shown without applying prorrata; cuotas after prorrata. Purchases at 0 % or exempt are not declared.

| Casillas | Content |
|---|---|
| 28-29 | Domestic current goods and services (including domestic and non-EU reverse charge deductible) |
| 30-31 | Domestic capital goods (art. 108) |
| 32-33 | Imports of current goods (DUA) |
| 34-35 | Imports of capital goods |
| 36-37 | Intra-EU acquisitions of current goods and services |
| 38-39 | Intra-EU acquisitions of capital goods |
| 40-41 | Rectification of deductions (credit notes received, bad debts of suppliers), with sign |
| 42 | Compensations paid to REAGP farmers |
| 43 | Regularisation of capital goods (last period) |
| 44 | Regularisation by definitive prorrata (only 4T or month 12, or on cessation) |
| 45 | Total to deduct |
| 46 | Result of the general regime (27 − 45) |

## 4. Información adicional

| Casilla | Content |
|---|---|
| 59 | Exempt intra-EU supplies of goods (art. 25) and intra-EU services (art. 69 B2B to EU businesses) |
| 60 | Exports and assimilated: exports outside the EU including Canarias, Ceuta, Melilla; tax-free (viajeros) refunds; arts. 22-24 and 64 exemptions; exempt travel agency operations |
| 120 | Not subject by place-of-supply rules, other than OSS: B2B services to non-EU businesses, distance sales below the threshold of other countries, goods installed in another member state, other not-subject supplies |
| 122 | Domestic supplies with reverse charge where the company is the seller (art. 84.Uno.2º a, c-g; gold) |
| 123 | Not subject in Spain and declared via OSS/IOSS (Union, non-Union and import schemes) |
| 124 | Subject in Spain and declared via IOSS |
| 62-63 | RECC: base and cuota of supplies that would have been due under the general devengo rule |
| 74-75 | RECC: base and cuota of purchases under RECC by the general rule |

## 5. Resultado

| Casilla | Content |
|---|---|
| 46 | Result general regime |
| 58 | Result simplificado (simplificado filers) |
| 76 | Regularisation art. 80.Cinco.5ª (buyer with prorrata whose supplier reduced the base for non-payment) |
| 64 | Sum of results (46 + 58 + 76) |
| 65 | Percentage attributable to the State (100 % unless the company files also to the Basque or Navarre administrations) |
| 66 | Attributable to the State (64 × 65) |
| 77 | Import IVA liquidated by customs and deferred (only RIVA art. 74.1 option holders) |
| 110 | Compensation balance pending from earlier periods |
| 78 | Compensation balance applied in this period (max 66 + 77) |
| 87 | Compensation balance still pending for later periods (110 − 78) |
| 68 | Annual regularisation for Concierto/Convenio (last period) |
| 108 | Corrective return for discrepancy with administrative criteria |
| 69 | Result: 66 + 77 − 78 + 68 + 108 |
| 70, 109, 111 | Only in an autoliquidación rectificativa (previous result, refunds already agreed, part of a negative result offset against the rectified positive result) |
| 71 | Result of the self-assessment: 69 − 70 + 109 |
| 72 | Amount to compensate (negative result, no refund requested) |

A negative result can be refunded only in the last period of the year unless the company is in REDEME.

## 6. Mapping table: operation to casilla to account

| Operation | Casillas | Entry |
|---|---|---|
| Domestic sale at 21 % | 07-09 | Debit **430**; credit **700**/**705**, credit **477** |
| Domestic purchase at 21 %, fully deductible | 28-29 | Debit **600**/**62x**, debit **472**; credit **400**/**410** |
| Purchase of capital good | 30-31 | Debit **21x**, debit **472**; credit **523** |
| Sale to retailer in recargo de equivalencia, 21 % | 07-09 and 22-24 | Debit **430**; credit **700**, credit **477** (IVA and recargo sub-accounts) |
| Intra-EU purchase of goods | 10-11 and 36-37 | Debit **600**, debit **472**; credit **400**, credit **477** |
| EU service bought (Google Ireland, Meta, Shopify) | 10-11 and 28-29 | Debit **627**/**629**, debit **472**; credit **410**, credit **477** |
| Non-EU service bought | 12-13 and 28-29 | Same as above |
| Domestic construction reverse charge received | 12-13 and 28-29 (or 30-31) | Same, with the asset or cost account |
| Domestic reverse charge supplied (seller) | 122 | Debit **430**; credit **700** (no IVA) |
| Import with DUA, VAT paid via forwarder | 32-33 | Debit **472**; credit **410** (forwarder) or **572** |
| Import with deferred VAT | 32-33 and 77 | Debit **472**; credit **4750** |
| Intra-EU supply of goods | 59 | Debit **430**; credit **700** |
| B2B service to EU business | 59 | Debit **430**; credit **705** |
| B2B service to non-EU business | 120 | Debit **430**; credit **705** |
| Export, including Canarias | 60 | Debit **430**; credit **700** |
| Credit note issued, 21 % | 14-15 (negative) | Debit **708** (returns) or **706**/**709**, debit **477**; credit **430** |
| Credit note received | 40-41 (negative) | Debit **400**; credit **608**/**609**, credit **472** |
| Distance sale to EU consumer via OSS | 123 | Debit **430**/**572**; credit **700**, credit destination-VAT liability (sub-account of **4750** or **477** kept outside the 303 totals) |
| Exempt sale (art. 20), e.g. residential rent | Not in 01-09; affects prorrata | Debit **430**; credit **752** |
| Non-deductible IVA (gift, client meal, 50 % car) | Not in 28-29 for the non-deductible part | Add to the cost or asset account |

OSS VAT is never in **477**'s Spanish totals for the 303: if the company uses an **477** sub-account for OSS, exclude it from the 303 reconciliation and settle it against the modelo 369.

## 7. Period-end settlement entries

Clear every **472** and **477** sub-account included in the 303 into the result account.

**Result payable** (output 12,000, deductible input 7,500):

| Account | Debit | Credit |
|---|---|---|
| **477** | 12,000 | |
| **472** | | 7,500 |
| **4750** | | 4,500 |

Payment on filing: debit **4750** 4,500; credit **572** 4,500.

**Result negative, to compensate** (output 3,000, input 5,000):

| Account | Debit | Credit |
|---|---|---|
| **477** | 3,000 | |
| **4700** | 2,000 | |
| **472** | | 5,000 |

The **4700** balance is applied in a later 303 (casilla 78): debit **477**; credit **472** and **4700**. Refund requested in the last period: **4700** stays until the money arrives (debit **572**, credit **4700**).

**Deferred import VAT** (casilla 77, 2,100 on a DUA): during the period debit **472** 2,100, credit **4750** 2,100. At settlement the **472** amount is cleared with the rest; the 2,100 in **4750** is paid with the 303.

**Late filing surcharge (recargo LGT art. 27)**: debit **678** (gastos excepcionales) or the account the company uses for tax surcharges; late interest to **669**. Sanctions are not tax-deductible for IS (see `spanish-corporate-tax`).

## 8. Last period of the year and modelo 390

In the 303 of 4T (quarterly) or December (monthly):

1. Compute the definitive prorrata and fill casilla 44; regularise capital goods in casilla 43.
2. Opt for or revoke prorrata especial (check box), effective for the whole year.
3. Choose compensation or refund for a negative result.
4. If exempt from modelo 390 (SII filers; quarterly filers in territorio común with only simplificado and/or urban letting), complete the extra annual pages of the 303: activities (CNAE/IAE), prorrata, sectores diferenciados (casillas 700-805), volume of operations.
5. Others file modelo 390 by 30 January. Its totals must match the four (or twelve) 303s plus any rectificativas.

## 9. Reconciliation checks

| Check | How |
|---|---|
| Casillas 09, 06, 03 against **477** sub-accounts | Balance of the period by rate equals cuota declared |
| Casillas 11 and 13 equal to deductible counterparts | With full deduction, reverse charge output (11, 13) equals the matching input in 28-29/36-39 |
| Casilla 59 against modelo 349 | Sum of keys E and S for the period equals casilla 59 |
| Casilla 10 against modelo 349 | Keys A and I equal casilla 10 |
| Casilla 77 against DUAs | Each DUA in the period under the deferral option |
| **472**/**477** after settlement | Zero, except RECC pending sub-accounts and OSS sub-accounts |
| **4700** | Equals casilla 87 plus any refund requested and not yet received |
| SII | Libro registro data at the AEAT equals the ledger; Pre303 assistant figures agree |
