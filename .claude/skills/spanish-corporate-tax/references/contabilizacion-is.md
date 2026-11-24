# Booking the Impuesto sobre Sociedades (PGC 2007)

## Contents

- [Framework](#framework)
- [Accounts](#accounts)
- [During the year: instalments and withholdings](#during-the-year-instalments-and-withholdings)
- [Year-end: current tax](#year-end-current-tax)
- [Year-end: deferred tax](#year-end-deferred-tax)
- [Losses and BINs](#losses-and-bins)
- [Reserves (capitalización, nivelación)](#reserves-capitalización-nivelación)
- [Paying or collecting in July](#paying-or-collecting-in-july)
- [Worked example](#worked-example)
- [Sources](#sources)

## Framework

PGC 2007 norma de registro y valoración 13ª (impuestos sobre beneficios) and the ICAC Resolución de 9 de febrero de 2016 (desarrollo de las normas de registro, valoración y elaboración de cuentas anuales para la contabilización del Impuesto sobre beneficios). Tax expense = current tax ± deferred tax. PGC-Pymes (RD 1515/2007) uses the same accounts; microempresas applying the PGC-Pymes micro criteria (RD 1515/2007 art. 4) may book only the current tax (unverified: check the ICAC 2016 Resolución chapter on microempresas before using it).

## Accounts

| Account | Name | Use |
|---|---|---|
| **6300** | Impuesto corriente | Current tax expense of the year (cuota líquida) |
| **6301** | Impuesto diferido | Change in deferred tax assets/liabilities through PyG |
| **633** | Ajustes negativos en la imposición sobre beneficios | Corrections of prior-year tax expense (lower) |
| **638** | Ajustes positivos en la imposición sobre beneficios | Corrections of prior-year tax expense (higher) |
| **473** | Hacienda Pública, retenciones y pagos a cuenta | Withholdings suffered and modelo 202 instalments |
| **4752** | Hacienda Pública, acreedora por impuesto sobre sociedades | Cuota diferencial to pay |
| **4709** | Hacienda Pública, deudora por devolución de impuestos | Cuota diferencial to recover |
| **4740** | Activos por diferencias temporarias deducibles | Deferred tax asset from positive temporary adjustments |
| **4742** | Derechos por deducciones y bonificaciones pendientes de aplicar | Unused deductions recognised as assets |
| **4745** | Crédito por pérdidas a compensar del ejercicio | Deferred tax asset for BINs |
| **479** | Pasivos por diferencias temporarias imponibles | Deferred tax liability from negative temporary adjustments |
| **8300**, **8301** | Impuesto corriente / diferido (group 8) | Tax on items recognised directly in equity |

## During the year: instalments and withholdings

Modelo 202 paid on 20 April:

| Debit | Credit | Amount |
|---|---|---|
| **473** | **572** | Instalment |

Interest received with 19 % withholding (gross 1,000):

| Debit | Credit | Amount |
|---|---|---|
| **572** | | 810 |
| **473** | | 190 |
| | **769** | 1,000 |

## Year-end: current tax

Cuota líquida 15,000; withholdings and instalments in **473** 9,000:

| Debit | Credit | Amount |
|---|---|---|
| **6300** | | 15,000 |
| | **473** | 9,000 |
| | **4752** | 6,000 |

If **473** exceeds the cuota líquida, the difference goes to **4709**.

## Year-end: deferred tax

Measure at the rate expected when the difference reverses (NRV 13ª.4). With the 2025-2029 phase-in, an ERD must use 22 %, 21 % or 20 % for differences reversing in 2027, 2028, 2029 on, and remeasure existing balances when the expected rate changes (the effect goes to **6301**; ICAC Resolución de 9 de febrero de 2016).

| Event | Entry |
|---|---|
| Positive temporary adjustment (e.g. non-deductible impairment of a machine, 10,000 at 23 %) | Dr **4740** 2,300 / Cr **6301** 2,300 |
| Its reversal in a later year | Dr **6301** / Cr **4740** |
| Negative temporary adjustment (e.g. ERD double-rate depreciation, 8,000 extra at 23 %) | Dr **6301** 1,840 / Cr **479** 1,840 |
| Its reversal | Dr **479** / Cr **6301** |
| Permanent difference (fine, art. 21 dividend) | Only affects **6300** through the cuota; no deferred tax |

Recognise deferred tax assets only if it is probable that future taxable profits will absorb them (NRV 13ª.2.3; ICAC Resolución 2016): for start-ups with a loss history, usually do not recognise **4745**.

## Losses and BINs

Year with a negative base of 40,000, rate expected on use 23 %, recovery probable:

| Debit | Credit | Amount |
|---|---|---|
| **4745** | **6301** | 9,200 |

Withholdings and instalments of a loss year are refunded: Dr **4709** / Cr **473**.

When used: Dr **6301** / Cr **4745** for the BIN used × rate.

The BIN itself is tracked in the modelo 200 (page with "BINs pendientes"), not in the ledger; **4745** only exists if the asset meets the recognition test.

## Reserves (capitalización, nivelación)

- Capitalización: no deferred tax (permanent reduction). Book the restricted reserve when the junta allocates the result: Dr **129** / Cr **113** subaccount "Reserva de capitalización" (no PGC account is specific; a subaccount of **114** is also common).
- Nivelación: a temporary difference. The reduction (negative adjustment) creates a liability: Dr **6301** / Cr **479** at the rate of reversal; reverse when the amount is added back. Restricted reserve charged to the result as for capitalización.

## Paying or collecting in July

| Event | Entry |
|---|---|
| Pay modelo 200 | Dr **4752** / Cr **572** |
| Refund received | Dr **572** / Cr **4709** |
| Return shows more tax than booked (error in the provision) | Dr **638** / Cr **4752** (or **4709**) |
| Return shows less tax than booked | Dr **4752** / Cr **633** |

Material errors from prior years go to reserves under NRV 22ª, not to **633**/**638**.

## Worked example

ERD, calendar 2026, rate 23 %. Resultado contable antes de impuestos 100,000. Adjustments: fine +2,000 (permanent); non-deductible impairment of a machine +10,000 (temporary, reverses from 2027 at 22 %); ERD double depreciation −8,000 (temporary, reverses 2027-2030, assume 20 %). Reserva de capitalización −10,000. Instalments and withholdings 15,000.

| Step | Amount |
|---|---|
| Base previa: 100,000 + 2,000 + 10,000 − 8,000 | 104,000 |
| Capitalización | −10,000 |
| Base imponible | 94,000 |
| Cuota íntegra 23 % = cuota líquida | 21,620 |
| To pay: 21,620 − 15,000 | 6,620 |

Entries at 31 December 2026:

| Debit | Credit | Amount |
|---|---|---|
| **6300** | | 21,620 |
| | **473** | 15,000 |
| | **4752** | 6,620 |
| **4740** (10,000 × 22 %) | **6301** | 2,200 |
| **6301** (8,000 × 20 %) | **479** | 1,600 |

Tax expense in PyG: 21,620 − 2,200 + 1,600 = 21,020. Effective rate on accounting profit 21.0 %; the difference from 23 % comes from the capitalización saving (−2,300), the fine (+460) and the rate differential on deferred items.

## Sources

- PGC 2007 (RD 1514/2007), NRV 13ª and 22ª; quinta parte, definitions of accounts 473, 474, 4752, 479, 630, 633, 638.
- Resolución de 9 de febrero de 2016, del ICAC (BOE 16/02/2016).
- LIS arts. 25, 26, 105.
