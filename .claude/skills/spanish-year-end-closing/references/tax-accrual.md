# Corporate income tax at year-end (gasto por Impuesto sobre Sociedades)

## Contents

- [Framework](#framework)
- [Rates](#rates)
- [From accounting result to tax payable](#from-accounting-result-to-tax-payable)
- [Current and deferred tax in the accounts](#current-and-deferred-tax-in-the-accounts)
- [Worked example (ERD, 2026)](#worked-example-erd-2026)
- [Losses and tax credits](#losses-and-tax-credits)
- [Rate changes and remeasurement](#rate-changes-and-remeasurement)
- [Microempresa criteria](#microempresa-criteria)
- [Payments on account during the year](#payments-on-account-during-the-year)

## Framework

| Rule | Source |
|---|---|
| Accounting for income tax | PGC NRV 13.ª; ICAC Resolución 9-02-2016 |
| Tax base starts from the accounting result, adjusted by the LIS | LIS art. 10.3 |
| Expense = current tax + deferred tax | NRV 13.ª.1-2 |
| Deferred tax assets only if future taxable profit is probable | NRV 13.ª.2.3 |
| Measured at the rates expected to apply when they reverse, enacted or about to be enacted | NRV 13.ª.3 |
| Not discounted | NRV 13.ª.3 |
| Microempresa option: only current tax | RD 1515/2007 art. 4.3, 2.ª |

Scope: territorio común. The Basque Country and Navarra apply their own corporate tax laws and rates.

## Rates

| Taxpayer | 2025 | 2026 | 2027 | 2028 | 2029+ | Source |
|---|---|---|---|---|---|---|
| Cifra de negocios of the previous period < 1 M€: base 0-50,000 € | 21 % | 19 % | 17 % | 17 % | 17 % | LIS art. 29.1.a; DT 44.ª |
| Same, rest of the base | 22 % | 21 % | 20 % | 20 % | 20 % | LIS art. 29.1.b; DT 44.ª |
| ERD (cifra < 10 M€, LIS art. 101) | 24 % | 23 % | 22 % | 21 % | 20 % | LIS art. 29.1; DT 44.ª |
| New company, first year with positive base and the next | 15 % | 15 % | 15 % | 15 % | 15 % | LIS art. 29.1 |
| General | 25 % | 25 % | 25 % | 25 % | 25 % | LIS art. 29.1 |

Years are those in which the tax period *starts*. Short periods prorate the 50,000 € band by days/365. Group companies measure cifra de negocios at group level (LIS art. 101.3). Entidades patrimoniales pay 25 %. Cooperatives, non-profits and investment vehicles have their own rates (LIS art. 29.2-4).

## From accounting result to tax payable

```
  Resultado contable antes de impuestos
± Diferencias permanentes (e.g. fines and penalties, LIS art. 15.c; gifts, 15.e; IS expense itself, 15.b)
± Diferencias temporarias (e.g. non-deductible impairment, provisions, libertad de amortización)
= Base imponible previa
− Reserva de capitalización (LIS art. 25)
− Compensación de BINs (LIS art. 26)
− Reserva de nivelación (ERD, LIS art. 105)
= Base imponible
× Tipo de gravamen
= Cuota íntegra
− Deducciones y bonificaciones
= Cuota líquida            → current tax (6300)
− Retenciones e ingresos a cuenta, pagos fraccionados (473)
= Cuota diferencial        → 4752 if positive, 4709 if negative
```

| Reduction | Rule (periods from 1-01-2025) | Source |
|---|---|---|
| Reserva de capitalización | 20 % of the increase in fondos propios (23 / 26.5 / 30 % with headcount growth); limit 20 % of the base before it, 25 % if cifra < 1 M€; excess carried 2 years; reserve non-distributable 3 years | LIS art. 25 |
| BINs | Up to 70 % of the base before the reserve and compensation, always at least 1 M€; no limit in the first 3 years with a positive base of a new company | LIS art. 26.1, 26.3 |
| Reserva de nivelación | ERD applying the rate of the first paragraph of art. 29.1 (whether the ERD-only rate qualifies after Ley 7/2024 rewrote art. 29.1 is unverified): up to 10 % of the positive base, max 1 M€; added back within 5 years against BINs or at the end; reserve from the year's profit | LIS art. 105 |

The *nivelación* reduction is a temporary difference: book a deferred tax liability (**479**) for it. The *capitalización* reduction is permanent.

## Current and deferred tax in the accounts

| Item | Entry |
|---|---|
| Current tax | Debit **6300**; credit **473** (payments on account) and **4752** (rest) or debit **4709** if refundable |
| Deductible temporary difference arising (tax base > accounting result) | Debit **4740**, credit **6301** |
| Taxable temporary difference arising (tax base < accounting result) | Debit **6301**, credit **479** |
| Reversal | Opposite entries |
| Tax loss of the year, recovery probable | Debit **4745**, credit **6301** |
| Deductions pending | Debit **4742**, credit **6301** |
| Adjustments to prior-year tax | **633** (negative) / **638** (positive) |
| Tax effect of items in equity (subsidies, fair value) | **8301** / **479** or **4740** (groups 8-9) |

## Worked example (ERD, 2026)

SL, calendar year, cifra 2025 = 3 M€ (ERD, not < 1 M€), so 23 % for 2026. Expected rate at reversal: 22 % (2027).

| Item | € |
|---|---|
| Resultado contable antes de impuestos | 120,000 |
| Traffic fine (permanent, LIS art. 15.c) | + 2,000 |
| Customer impairment not yet deductible (temporary) | + 5,000 |
| Libertad de amortización on a new asset (temporary, reverses later) | − 10,000 |
| Base imponible previa | 117,000 |
| Reserva de capitalización: 20 % × 50,000 increase in fondos propios; limit 20 % × 117,000 = 23,400 | − 10,000 |
| Base imponible | 107,000 |
| Cuota íntegra 23 % = cuota líquida | 24,610 |
| Payments on account and withholdings (**473**) | 15,000 |
| Payable (**4752**) | 9,610 |

```
Debit  6300  Impuesto corriente                     24,610
Credit 473   Hacienda Pública, retenciones y pagos a cuenta   15,000
Credit 4752  Hacienda Pública, acreedora por impuesto sobre sociedades   9,610

Debit  4740  Activos por diferencias temporarias deducibles (5,000 × 22 %)   1,100
Credit 6301  Impuesto diferido                       1,100

Debit  6301  Impuesto diferido                       2,200
Credit 479   Pasivos por diferencias temporarias imponibles (10,000 × 22 %)   2,200
```

Tax expense: 24,610 + 2,200 − 1,100 = 25,710. Check: (120,000 + 2,000 − 10,000) × 23 % = 25,760, less 50 because the temporary differences are measured at 22 % instead of 23 % ((10,000 − 5,000) × 1 %). The reserva de capitalización (10,000) is booked when the profit is applied (`aplicacion-resultado.md`). If the libertad de amortización reverses over several years at 22 %, 21 % and 20 %, use the rate for each reversal year.

## Losses and tax credits

- A tax loss creates a BIN usable without time limit, within the art. 26 limits. Book **4745** only if future taxable profits are probable (NRV 13.ª.2.3); otherwise disclose only.
- The AEAT can check BINs for 10 years; after that the company proves them with the return and the accounts deposited at the Registro Mercantil (LIS art. 26.5; LGT art. 66 bis).
- When a BIN is used: debit **6301**, credit **4745**.

## Rate changes and remeasurement

The ERD and small-company rates fall each year until 2029 (LIS DT 44.ª). At each year-end:

1. Re-estimate when each **4740**, **4745** and **479** balance will reverse.
2. Measure it at the rate of the reversal year.
3. Book the change through **6301** (or **633**/**638** per the company's policy and ICAC Res. 9-02-2016; unverified which the ICAC prefers), or through equity if the original item was booked in equity.

A company that grows past 1 M€ or 10 M€ cifra changes its rate the following period; ERD status continues for 3 periods after crossing 10 M€ if it was ERD in that and the two previous periods (LIS art. 101.4).

## Microempresa criteria

Under RD 1515/2007 art. 4.3, 2.ª the expense is the tax of the year's return: debit **6300** for the cuota líquida, credit **473** and **4752** (or debit **4709**). No **4740**, **4745** or **479**. The memoria (note 9, situación fiscal) lists the differences between result and tax base, pending BINs and incentives.

## Payments on account during the year

| Item | Rule | Entry |
|---|---|---|
| Pagos fraccionados (modelo 202), 1-20 April, October, December | LIS art. 40 | Debit **473**, credit **572** |
| Withholdings suffered (bank interest, rents, dividends received) | LIS art. 128 | Debit **473** when the income is booked |
| Annual return (modelo 200) | Within 25 days after the 6 months following year-end | Debit **4752**, credit **572** (or collect **4709**) |
