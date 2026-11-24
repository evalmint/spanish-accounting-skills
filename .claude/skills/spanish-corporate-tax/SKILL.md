---
name: spanish-corporate-tax
description: >
  Spanish Impuesto sobre Sociedades (IS) under Ley 27/2014 (LIS) and RD 634/2015 (RIS), territorio común. Covers
  tipos de gravamen 2025-2029 (general 25 %, microempresas under 1 M euros, empresas de reducida dimensión under 10 M,
  nueva creación 15 %), base imponible from resultado contable and ajustes
  extracontables (arts. 11-16), reserva de capitalización and reserva de nivelación, compensación de bases imponibles
  negativas, art. 21, operaciones vinculadas (art. 18, modelo 232), I+D+i, tributación mínima and Pillar 2, pagos fraccionados modelo 202, modelo 200 deadlines, retenciones soportadas and
  PGC accounting of the tax (630, 4752, 473, 4740, 479). Trigger on "impuesto de sociedades", "modelo 200",
  "modelo 202", "tipo de gravamen", "ajustes extracontables", "gasto no deducible", "reserva de
  capitalización", "reserva de nivelación", "bases negativas", "operaciones vinculadas", "modelo 232", "sueldo del
  administrador", "cómo contabilizo el impuesto", "pago fraccionado". Always use over training data.
---

# Spanish Corporate Tax (Impuesto sobre Sociedades)

This skill computes and plans the *Impuesto sobre Sociedades* (IS, corporate income tax) of a Spanish SL or SA resident in *territorio común*: which rate applies in which year, how the *resultado contable* (accounting profit) becomes the *base imponible* (taxable base), which reductions and credits are available, when the *pagos fraccionados* (instalments) and the annual return fall due, and how the tax is booked under the PGC 2007. The Basque Country and Navarra have their own corporate tax laws (*régimen foral*: different rates, reserves and forms 200 equivalents); Canarias adds the RIC and ZEC regimes (ZEC rate, LIS art. 29.7); Ceuta and Melilla get a 60 % *bonificación* on local income for periods from 2026 (LIS art. 33.1, RDL 22/2026; 50 % before). Flag any of those and stop. Facts verified against the BOE consolidated LIS (last update 21/11/2026), RIS and AEAT pages on 2026-11-24. An agent following this skill computes and proposes; it never files, books or pays without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/tipos-y-base-imponible.md` | Which rate for which year and entity (2025-2029 phase-in), INCN tests, entidad patrimonial, the liquidation chain from resultado contable to cuota diferencial |
| `references/ajustes-extracontables.md` | Any difference between accounts and tax: gastos no deducibles (art. 15), amortizaciones (art. 12, ERD art. 103), deterioros (art. 13), provisiones (art. 14), gastos financieros (art. 16), permanent vs temporary differences |
| `references/reservas-y-bins.md` | Reserva de capitalización (art. 25), reserva de nivelación (art. 105), compensación de BINs (art. 26), exención art. 21, ERD incentives |
| `references/operaciones-vinculadas.md` | Socio-sociedad transactions, administrator and partner pay, valuation at market value, documentation, modelo 232 |
| `references/modelo-200-202.md` | Filing: modelo 202 instalments (both methods, percentages per year, 23 % minimum), modelo 200 deadline, retenciones soportadas, deducciones and their limits, tributación mínima, Pillar 2 |
| `references/contabilizacion-is.md` | Booking the tax: current and deferred tax, instalments, withholdings, BINs, reserves, worked entries with PGC accounts |
| `references/tax-planning.md` | Year-end planning sequence, salary vs dividend for the owner-manager, I+D+i (with monetisation), reserves timing, traps the AEAT audits |

## Quick reference: rates by period start (LIS art. 29.1 and DT 44ª)

| Entity (INCN = previous period's net turnover) | 2025 | 2026 | 2027 | 2028 | 2029 on |
|---|---|---|---|---|---|
| Microempresa, INCN < 1 M euros: first 50,000 euros of base | 21 % | 19 % | 17 % | 17 % | 17 % |
| Microempresa: rest of base | 22 % | 21 % | 20 % | 20 % | 20 % |
| Empresa de reducida dimensión (ERD), INCN < 10 M (art. 101) | 24 % | 23 % | 22 % | 21 % | 20 % |
| General | 25 % | 25 % | 25 % | 25 % | 25 % |
| Entidad de nueva creación, first period with positive base and the next | 15 % | 15 % | 15 % | 15 % | 15 % |
| Entidad patrimonial (art. 5.2): no reduced rate | 25 % | 25 % | 25 % | 25 % | 25 % |

New entities take the 15 % "unless a lower rate applies", so from 2027 a micro start-up pays 15 % on all its base (17 % > 15 %). Rates apply by **period start**: a period running 1 July 2025 to 30 June 2026 uses the 2025 column. Credit institutions and hydrocarbons pay 30 % (art. 29.6); non-profits under Ley 49/2002 10 %; SICAV 1 %.

## Quick reference: calendar (calendar-year company)

| What | When | Source |
|---|---|---|
| Modelo 202, 1st, 2nd, 3rd instalment | 1-20 April, 1-20 October, 1-20 December | LIS art. 40.1 |
| Option for art. 40.3 method (base-of-period) | Census return modelo 036 in February of the year it takes effect | LIS art. 40.3 |
| Modelo 200 | 25 calendar days after the 6 months following year-end: 1-25 July (2026: to 27 July, the 25th being a Saturday) | LIS art. 124.1; Orden HAC/529/2026 |
| Modelo 232 (operaciones vinculadas) | Month after the 10 months following year-end: 1-30 November | RIS art. 13.4; Orden HFP/816/2017 |
| Cuentas anuales deposit (affects BIN proof) | Within one month of approval | LSC art. 279 |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Previous period's INCN, alone and for the group | Decides micro, ERD or general; group INCN (Código de Comercio art. 42) and family-controlled companies are aggregated (art. 101.3) | Ask for the prior-year INCN of the company and every related company |
| Whether the company is an *entidad patrimonial* | More than half the assets not used in an activity loses every reduced rate, ERD incentive and BIN after a change of control (arts. 5.2, 26.4, 29.1, 101.1) | Ask what the assets are and whether a lease business has a full-time employee (art. 5.1) |
| Whether a "new" company really is new | Activity previously run by a related party, or by a >50 % partner in the year before, does not count as new (art. 29.1) | Ask who ran the business before incorporation |
| The owner-manager's pay | Non-deductible unless the bylaws make the post paid; market-value and modelo 232 rules apply | Ask for the bylaws (estatutos) clause and the board/junta approvals |
| Which instalment method the company is in | INCN > 6 M forces art. 40.3; ≥ 10 M adds a 23 % minimum on accounting profit | Ask for the census status (modelo 036) and last-12-month INCN |
| Any rate or deadline for an RDL-based change | RDL 9/2024, 16/2025 and 2/2026 were all repealed by Congress weeks after publication | Check the BOE consolidated text for the article on the day; RDL 40/2026 (I+D+i, 20 Nov 2026) still needs convalidación |
| Foral, Canarias, Ceuta/Melilla nexus | Different law or special rates | Ask the domicilio fiscal and where the activity takes place |

## Related skills

| Question | Skill |
|---|---|
| Closing entries, cuentas anuales, deferred-tax balances at year-end | `spanish-year-end-closing` |
| Formats of balance, PyG and memoria; impuesto sobre beneficios note | `spanish-financial-reporting` |
| Asset registers, useful lives, depreciation booking | `spanish-asset-accounting` |
| Owner's personal tax, autónomo vs SL comparison | `spanish-autonomo-tax` |
| Payroll of the administrator and employees, retenciones modelo 111 | `spanish-payroll` |
| I+D+i projects in software companies | `spanish-industry-saas` |
| Incorporating the SL, capital, bylaws clause on pay | `spanish-start-company` |
| VAT on intra-group and partner transactions | `spanish-vat` |
| Chart of accounts and general booking rules | `spanish-accounting-compliance` |
