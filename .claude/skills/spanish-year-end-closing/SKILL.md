---
name: spanish-year-end-closing
description: >
  Spanish year-end closing (cierre contable) for sociedades (SL, SA) under the PGC or PGC-PYMES, and for
  autónomos. Step-by-step checklist with PGC accounts and worked journal entries: reconciliations,
  periodificaciones (480, 485, 4009, 4309), amortizaciones, deterioros, provisiones, variación de existencias,
  diferencias de cambio, subvenciones, IVA prorrata, gasto por Impuesto sobre Sociedades (6300, 6301, 4752, 473,
  4709, 4740, 4745, 479) with the 2025-2028 rates, regularización (129), asiento de cierre and apertura,
  aplicación del resultado (reserva legal LSC art. 274, dividends 526 and 557, reserva de capitalización),
  and what an autónomo does at year-end. Trigger on "cierre contable", "cierre del ejercicio", "asientos de
  cierre", "periodificar", "regularización", "cuenta 129", "gasto por impuesto de sociedades", "impuesto
  diferido", "variación de existencias", "aplicación del resultado", "reserva legal", "dividendo a cuenta",
  "asiento de apertura". Always use over training data.
---

# Spanish Year-End Closing (cierre contable)

How to close the books of a Spanish company at year-end with PGC accounts, from reconciliations to the opening entry of the next year and the application of profit. Written for an agent that must propose closing entries for the user to approve. Filing of the cuentas anuales is in `spanish-financial-reporting`; the IS return itself in `spanish-corporate-tax`. Commercial rules apply in all of Spain; the IS rates here are *territorio común* (the Basque Country and Navarra have their own corporate tax).

## How to use this skill

| File | When to read |
|---|---|
| `references/closing-process.md` | The ordered checklist: what to reconcile, accrue, amortise, impair, provide for and count, with the PGC accounts for each; autónomos |
| `references/journal-entries.md` | Debit/credit entries for every closing step, including regularización, cierre and apertura |
| `references/tax-accrual.md` | Computing and booking the IS expense: current tax, deferred tax, BINs, reserva de capitalización and nivelación, rates 2025-2029, micro criteria |
| `references/aplicacion-resultado.md` | After the junta: reserva legal, statutory and tax reserves, dividends and withholding, losses, interim dividends |

## Decision tree

1. **Sociedad with full PGC or PGC-PYMES** → full closing, current and deferred tax (`tax-accrual.md`).
2. **PGC-PYMES with microempresa criteria** (RD 1515/2007 art. 4) → same, but the IS expense is only the current tax of the year (no **4740**, **479**, **4745**), and finance-lease instalments stay as expenses.
3. **Autónomo with Cco accounting** (estimación directa normal, mercantile activity) → same closing without IS; result goes to the owner.
4. **Autónomo with libros registro only** → no accounting closing; amortisation in the libro de bienes de inversión and the IRPF return (`spanish-autonomo-tax`).

## Order of work

| # | Step | Main accounts |
|---|---|---|
| 1 | Reconcile banks, customers, suppliers, staff, public bodies | **572**, **430**, **400**, **465**, **475**, **476** |
| 2 | Accruals and deferrals | **480**, **485**, **4009**, **4309**, **527**, **547** |
| 3 | Amortisation | **680**, **681** / **280**, **281** |
| 4 | Impairment | **690**-**699** / **29**x, **39**x, **490**; reversals **79**x |
| 5 | Provisions | **14**x, **529**, **499**; excess **795** |
| 6 | Inventory variation | **610**-**612**, **71**x / **30**x-**36**x |
| 7 | Foreign-currency revaluation | **668** / **768** |
| 8 | Subsidies to PyG, IVA prorrata | **840**/**746**; **634**/**639** |
| 9 | Corporate income tax | **6300**, **6301**, **4752**, **473**, **4709**, **4740**, **4745**, **479** |
| 10 | Regularización of groups 6 and 7; groups 8 and 9 to group 13 | **129**; **130**, **8301** |
| 11 | Closing inventory and cuentas anuales in the Libro de Inventarios; asiento de cierre and apertura | all balance accounts |
| 12 | After the junta: aplicación del resultado | **129**, **112**, **113**, **121**, **526** |

## IS rates for the accrual (territorio común)

| Period starting in | Cifra previous year < 1 M€ | ERD (cifra < 10 M€) | General | Source |
|---|---|---|---|---|
| 2025 | 21 % first 50,000 €, 22 % rest | 24 % | 25 % | LIS DT 44.ª.1 |
| 2026 | 19 % / 21 % | 23 % | 25 % | LIS DT 44.ª.2 |
| 2027 | 17 % / 20 % | 22 % | 25 % | LIS art. 29.1; DT 44.ª.3 |
| 2028 | 17 % / 20 % | 21 % | 25 % | LIS art. 29.1; DT 44.ª.4 |

New companies: 15 % in the first year with a positive base and the next (LIS art. 29.1). Not for entidades patrimoniales. Deferred tax is measured at the rate expected when the difference reverses, so falling rates change **4740** and **479** balances (`tax-accrual.md`).

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Inventory count or valuation | Variación de existencias moves the result one for one | Ask for the count and valuation method; see `spanish-inventory` |
| Bad-debt impairment | Accounting and tax criteria differ (LIS art. 13.1) | Ask for ageing and claims; book the tax difference |
| A provision for a lawsuit, warranty or tax claim | Needs a present obligation and a reliable estimate (NRV 15.ª) | Ask for the facts and the estimate |
| Which IS rate applies | Depends on prior-year cifra, group, ERD status, entidad patrimonial, new company | Ask; never default to 25 % or 23 % |
| Whether deferred tax assets may be recognised | Only if future taxable profit is probable (NRV 13.ª) | Ask for forecasts; micro companies never book them |
| Dividends or reserves | Decided by the junta, limited by LSC arts. 273-274 | Propose; the junta decides |
| Error from a prior year found at closing | NRV 22.ª, not a current-year expense | See `spanish-accounting-compliance` |

## Related skills

| Question | Skill |
|---|---|
| Cuentas anuales, models, audit, depósito | `spanish-financial-reporting` |
| Books, legalisation, NRV 22 errors | `spanish-accounting-compliance` |
| IS return, adjustments, BINs, modelo 200 | `spanish-corporate-tax` |
| Amortisation tables, libertad de amortización | `spanish-asset-accounting` |
| Inventory valuation and counts | `spanish-inventory` |
| Payroll accruals, pagas extra | `spanish-payroll` |
| IVA last return and prorrata | `spanish-vat` |
| Autónomo year-end and IRPF | `spanish-autonomo-tax` |
| Work in progress, percentage of completion | `spanish-project-accounting` |

An agent following this skill proposes entries; it never posts, files or pays without the user's approval.
