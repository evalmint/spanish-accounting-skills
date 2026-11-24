# Ajustes extracontables (book-to-tax adjustments)

## Contents

- [Principle](#principle)
- [Permanent vs temporary](#permanent-vs-temporary)
- [Gastos no deducibles (art. 15)](#gastos-no-deducibles-art-15)
- [Amortizaciones (art. 12, ERD art. 103)](#amortizaciones-art-12-erd-art-103)
- [Deterioros (art. 13)](#deterioros-art-13)
- [Provisiones (art. 14)](#provisiones-art-14)
- [Gastos financieros (art. 16)](#gastos-financieros-art-16)
- [Imputación temporal (art. 11)](#imputación-temporal-art-11)
- [Checklist for a small SL](#checklist-for-a-small-sl)
- [Sources](#sources)

## Principle

The base imponible starts from the *resultado contable* computed under the Código de Comercio and the PGC, corrected only where the LIS says so (LIS art. 10.3). An expense is deductible if it is booked in PyG (or a reserve where the PGC requires), accrued, justified (invoice) and not excluded by art. 15 (art. 11.3, *inscripción contable*). Exception: free and accelerated depreciation is deductible without booking it (art. 11.3.1º).

## Permanent vs temporary

| Type | Effect | PGC consequence | Examples |
|---|---|---|---|
| Permanent (*diferencia permanente*) | Never reverses | Only current tax **6300** | Fines, IS itself, donations, entertainment above 1 % INCN, art. 21 exemption |
| Temporary (*diferencia temporaria*), positive now | Pay more tax now, less later | Deferred tax asset **4740** against **6301** | Impairment of fixed assets (art. 13.2.a), non-deductible provisions, excess accounting depreciation, art. 16 excess interest (carried forward) |
| Temporary, negative now | Pay less now, more later | Deferred tax liability **479** against **6301** | Free depreciation (art. 102, DA 17ª), ERD double-rate depreciation (art. 103), leasing excess (art. 106) |

Booking detail in `contabilizacion-is.md`.

## Gastos no deducibles (art. 15)

| Letter | Not deductible | Notes |
|---|---|---|
| a) | Remuneration of own funds: dividends, and interest on participating loans within a group | Interest on ordinary loans from partners is deductible at market value (art. 18) |
| b) | The IS itself (and the Pillar 2 *Impuesto Complementario*) | Add back the **630** charge; tax income from accounting it is not income |
| c) | Fines and penalties (criminal, administrative), *recargos del período ejecutivo*, the late-filing surcharge without prior request | Late-payment interest (*intereses de demora*) is deductible: TS 8 February 2021 (rec. 3588/2019) (unverified citation) |
| d) | Gambling losses | |
| e) | Donations and gifts (*liberalidades*) | Excluded from e): client/supplier gifts and entertainment up to **1 % of INCN**; usual staff gifts; promotional spending; spending correlated with income; pay to administrators for senior management or under a labour contract |
| f) | Spending on acts contrary to law (bribes) | |
| g) | Services with tax havens, unless the operation is proved real | |
| h) | Intra-group interest on debt used to buy group shares or contribute to group equity, without valid economic reasons | |
| i) | Severance above the higher of 1 M euros per recipient or the statutory amount | |
| k), l) | Impairment and fair-value losses on shareholdings that qualify for art. 21 (or non-resident ones failing the 10 % nominal tax test) | |
| m) | AJD paid by the borrower on mortgage loans where the lender is the taxpayer | |

Administrator pay: the TS (sentencia 2 enero 2018, rec. 4269/2014, "Mecanotubo") and DGT V1790-17 (unverified) treat pay for the post of *administrador* as deductible only if the bylaws state it is paid and how (LSC art. 217). Pay for senior management or a labour contract is excluded from "liberalidad" by art. 15.e itself. See `operaciones-vinculadas.md`.

## Amortizaciones (art. 12, ERD art. 103)

Deductible depreciation (art. 12.1) is the effective depreciation, accepted if it follows any of:

| Method | Rule |
|---|---|
| a) Official table (straight line) | Up to the maximum coefficient, not slower than the maximum period |
| b) Declining balance | Coefficient × 1.5 (life < 5 years), × 2 (5 to < 8), × 2.5 (≥ 8); minimum 11 %; not for buildings, furniture |
| c) Sum of digits | Not for buildings, furniture |
| d) Plan approved by the AEAT | RIS art. 5 |
| e) Justified by the taxpayer | |

Selected rows of the table in art. 12.1.a:

| Asset | Max. coefficient | Max. years |
|---|---|---|
| Commercial, administrative and residential buildings | 2 % | 100 |
| Industrial buildings | 3 % | 68 |
| Other installations | 10 % | 20 |
| Machinery | 12 % | 18 |
| External transport (vans, cars) | 16 % | 14 |
| Lorries (*autocamiones*) | 20 % | 10 |
| Furniture | 10 % | 20 |
| Tools | 25 % | 8 |
| Electronic equipment | 20 % | 10 |
| Data-processing equipment (computers) | 25 % | 8 |
| Software (*sistemas y programas informáticos*) | 33 % | 6 |
| Other items | 10 % | 20 |

Other rules:

- Intangibles with a reliable life: over their life; without one, and goodwill: max 1/20 a year (art. 12.2). Accounting under PGC amortises goodwill over 10 years (RD 602/2016), so accounting > tax: positive temporary difference.
- Free depreciation (art. 12.3): new tangible items ≤ 300 euros each, up to 25,000 euros a year; I+D assets (not buildings); I+D expenses capitalised; SAL/SLL assets in their first 5 years.
- ERD (art. 103): new tangible assets, real estate investments and intangibles put into use while ERD: **2 × the table's maximum coefficient**. Free depreciation with job creation: 120,000 euros × average headcount increase (art. 102).
- DA 17ª: free depreciation up to 500,000 euros for renewable self-consumption installations entering into operation in 2023-2026, keeping headcount for 24 months.
- Land is never depreciated; split building and land values (RIS art. 3; cadastral ratio is the usual evidence).

## Deterioros (art. 13)

| Item | Deductible? |
|---|---|
| Trade receivables: individual impairment if at devengo 6 months have passed since maturity, or debtor in *concurso*, or prosecuted for *alzamiento de bienes*, or claimed in court/arbitration | Yes (art. 13.1) |
| Receivables from public bodies (unless in litigation), from related parties (unless *concurso* in liquidation phase), and general provisions for bad debts | No (art. 13.1). ERD exception: global provision up to 1 % of debtors at year-end (art. 104) |
| Tangible fixed assets, real estate investments, intangibles including goodwill | No (art. 13.2.a): temporary difference, deductible when the asset is sold, scrapped or depreciated |
| Shares | No if art. 21 applies; others only on sale or liquidation (arts. 13.2.b, 15.k) |
| Debt securities | No (art. 13.2.c) |
| Inventories (PGC 39x) | Yes, follows accounting (not listed in art. 13.2) |

## Provisiones (art. 14)

Not deductible:

- implicit or tacit obligations (art. 14.3.a), internal pension funds and long-term staff remuneration except contributions to pension plans (art. 14.1-2);
- restructuring, unless they relate to legal or contractual obligations (art. 14.3.b);
- the risk of returns on sales (art. 14.3.d);
- share-based staff pay (art. 14.3.e).

Deductible with limits: guarantees for repairs and reviews, up to the ratio of real costs in the current and two prior years over sales with live guarantees (art. 14.9); environmental, under a plan accepted by the AEAT (art. 14.6). Provisions not used for their purpose and reversed without income go back into the base (art. 11.7).

## Gastos financieros (art. 16)

- Net financial expenses deductible up to **30 % of beneficio operativo** (≈ EBITDA, adjusted per art. 16.1); in any case **1 M euros** a year is deductible.
- Excess carries forward indefinitely; unused headroom carries forward 5 years (art. 16.2).
- Leveraged acquisition of shares: extra 30 % limit on the acquirer's own EBITDA, waived if debt ≤ 70 % of price and amortised (art. 16.5).
- For a typical SME with net interest under 1 M euros, art. 16 never bites; still compute it if loans from partners are large.

## Imputación temporal (art. 11)

Accrual follows accounting. Notable tax rules: instalment sales (*operaciones a plazos*) may be taxed as collected (art. 11.4); expenses booked in a later year are deductible there if that does not lower tax (art. 11.3); reversals of non-deductible impairment are not income (art. 11.6); deferred tax assets converted under art. 11.12 have their own 70 % limit.

## Checklist for a small SL

Run through the trial balance at year-end:

1. **630** charge: add back.
2. **678**/**669** and **629** lines with fines, traffic tickets, recargos: add back.
3. Gifts and entertainment (**627**, **629**): over 1 % INCN, add back; private spending of partners: add back and check art. 18.
4. Administrator pay (**640**/**623**): bylaws clause? If not, flag.
5. **681**/**680**: above table maximum? Add back (temporary). ERD or free depreciation unused? Consider a negative adjustment.
6. **694**/**490**: general bad-debt provision above the 1 % ERD limit, or under 6 months: add back (temporary).
7. **691**, **690**, impairment of fixed assets: add back (temporary).
8. **14x** provisions: classify as in art. 14.
9. Financial income from qualifying shareholdings: art. 21 (95 % exempt).
10. Goodwill: accounting 10 %, tax 5 %: add back the difference.

## Sources

- LIS arts. 10-16, 102-104, 106, DA 17ª (BOE consolidated, 21/11/2026).
- RIS (RD 634/2015) arts. 1-6.
- AEAT, Manual práctico de Sociedades 2025, capítulos 3-4.
