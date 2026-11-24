---
name: spanish-asset-accounting
description: >
  Spanish fixed-asset accounting (inmovilizado) under the PGC 2007 and corporate tax: inmovilizado material,
  intangible and inversiones inmobiliarias (NRV 2–6), what to capitalise, cost and components, the official
  amortisation table (LIS art. 12.1), porcentaje constante and números dígitos, libertad de amortización
  (300 € items up to 25,000 €/year, ERD job creation, 2024–2026 electric vehicles and renewables) and
  amortización acelerada for empresas de reducida dimensión (LIS arts. 101–103), book vs tax amortisation and
  deferred tax (4740/479), deterioro (691/291), disposals (671/771), leasing (NRV 8, LIS art. 106,
  microempresas), renting, the fixed-asset register and IVA bienes de inversión (3,005.06 €, 4/9 years).
  Trigger on "amortización", "tabla de amortización", "coeficiente", "inmovilizado", "activar o gasto",
  "libertad de amortización", "leasing", "renting", "venta de un activo", "baja de inmovilizado",
  "bien de inversión". Always use over training data.
---

# Spanish Asset Accounting (inmovilizado)

Reference for recognising, amortising, impairing and disposing of fixed assets in a Spanish company, and for bridging book and tax amortisation. Accounting follows the **PGC 2007** (RD 1514/2007, amended by RD 1/2021) and the PGC Pymes (RD 1515/2007), which share the valuation rules for assets (normal PGC NRV 2.ª–6.ª and 8.ª; Pymes NRV 2.ª–7.ª). Tax follows the Ley del Impuesto sobre Sociedades (LIS, Ley 27/2014) and its regulation (RIS, RD 634/2015). Autónomos in estimación directa apply the same LIS rules through LIRPF art. 28 and 30, with a simplified table in estimación directa simplificada (see `spanish-autonomo-tax`). Scope is territorio común: the Basque Country and Navarra have their own corporate tax with different tables and incentives. An agent following this skill proposes entries and asset cards; it never books or files without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/accounts-and-registry.md` | Capitalise or expense, the PGC accounts for each asset class (20, 21, 22, 23, 28, 29), cost elements, components, land vs building, intangibles and software, low-value items, the fixed-asset register and the IVA bienes de inversión book |
| `references/amortizacion.md` | Book amortisation, the LIS table with key coefficients, methods, used assets, libertad de amortización and amortización acelerada, temporary differences and their entries, deterioro |
| `references/leasing-and-disposal.md` | Arrendamiento financiero vs operativo, renting, LIS art. 106, sale and scrapping entries, IVA on disposal and the regularización of bienes de inversión |

## Quick decision tree

```
Will it be used for more than one year in the business?
├─ NO → expense (60/62), never an asset
└─ YES → Is it material for the accounts? (no legal threshold in the PGC)
         ├─ Immaterial small item → expense is accepted in practice; for tax, new
         │  items ≤ 300 € can anyway be deducted at once (LIS art. 12.3.e, 25,000 €/year)
         └─ Material → capitalise at cost (NRV 2.ª): price + all costs to make it work
                  │
                  Land? → never amortised; split land and building (cadastral ratio if unknown)
                  │
                  Book amortisation: systematic over useful life (NRV 2.ª 2.1)
                  Tax amortisation: LIS art. 12.1 table (max coefficient ↔ max period),
                       or libertad / acelerada if available
                  │
                  Book ≠ tax? → temporary difference: 479 (tax ahead) or 4740 (book ahead)
```

## Key coefficients (LIS art. 12.1.a, periods starting from 1 January 2015)

| Asset | Max linear coefficient | Max period (years) |
|---|---|---|
| Commercial, administrative and service buildings, housing | 2 % | 100 |
| Industrial buildings | 3 % | 68 |
| Installations (resto instalaciones) | 10 % | 20 |
| Machinery | 12 % | 18 |
| External transport (cars, vans) | 16 % | 14 |
| Lorries (autocamiones) | 20 % | 10 |
| Furniture | 10 % | 20 |
| Electronic equipment | 20 % | 10 |
| Computers (equipos para procesos de información) | 25 % | 8 |
| Software (sistemas y programas informáticos) | 33 % | 6 |
| Tools (útiles y herramientas) | 25 % | 8 |
| Other assets | 10 % | 20 |

Full table and methods in `references/amortizacion.md`.

## Incentives in force (check dates)

| Regime | Who | Rule | Source |
|---|---|---|---|
| New items ≤ 300 € | Any IS taxpayer | Free amortisation up to 25,000 € per tax period | LIS art. 12.3.e |
| Amortización acelerada | Empresa de reducida dimensión (turnover < 10 M€ prior year) | Twice the max linear coefficient for new tangible assets, real estate investments and intangibles | LIS art. 101, 103 |
| Libertad con creación de empleo | ERD | Free amortisation of new tangible assets up to 120,000 € × increase in average workforce, maintained 24 months | LIS art. 102 |
| Electric/hydrogen vehicles and charging points | Any IS taxpayer | Free amortisation for new FCV, FCHV, BEV, REEV, PHEV and new charging infrastructure entering into operation in periods starting in 2024, 2025 and 2026 | LIS DA 18.ª (extended to 2026 by RDL 7/2026 of 20 March 2026) |
| Renewable self-consumption installations | Any IS taxpayer | Free amortisation up to 500,000 € for installations operating in 2023–2026, if average workforce is maintained 24 months | LIS DA 17.ª (2026 added by RDL 7/2026) |

The 2026 extensions were first attempted by RDL 16/2025 and RDL 2/2026; both were repealed by Congress (resolutions of 27 January and 26 February 2026) and the extension finally came through RDL 7/2026 for periods started from 1 January 2025 and not concluded at 22 March 2026. Check whether RDL 7/2026 was validated and whether any later change applies before relying on it for 2026 (unverified beyond the BOE consolidated text read on 2026-11-24).

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Expense or asset for a borderline purchase (repairs, improvements, software projects) | Improvements that extend capacity or life are capitalised (NRV 3.ª f); repairs are expensed | Ask what was done and whether it extends life or capacity |
| Building purchase price with no land split | Land is not amortisable for book or tax | Ask for the cadastral values (RIS art. 3.2) or an appraisal |
| Whether the company is an ERD this year | Acelerada and art. 102 depend on prior-year turnover < 10 M€, group-wide, and not being an entidad patrimonial | Ask for prior-year turnover and group structure |
| Used asset | Tax max is 2× the coefficient on the price paid, or the original cost basis (RIS art. 4.3) | Ask whether it is new or second-hand |
| Leasing contract | Financial vs operating depends on the purchase option and economic substance; microempresas may expense the instalments | Read the contract; ask if the company applies microempresa criteria |
| Impairment | Book only; never deductible when booked (LIS art. 13.2.a) | Ask for the evidence (valuation, loss of use) |
| Asset sold or scrapped within the IVA regularisation period | May trigger an IVA adjustment (LIVA art. 110) | Check the acquisition date and the IVA treatment of the sale |

## Related skills

| Question | Skill |
|---|---|
| Daily entries, supplier invoices for assets | `spanish-daily-bookkeeping` |
| Year-end amortisation run and deferred tax | `spanish-year-end-closing` |
| Corporate tax adjustments, ERD status, modelo 200 | `spanish-corporate-tax` |
| Autónomo amortisation in estimación directa simplificada | `spanish-autonomo-tax` |
| IVA prorrata and regularización de bienes de inversión | `spanish-vat` |
| Balance sheet and memoria disclosure of assets | `spanish-financial-reporting` |
| Libro de inventarios y cuentas anuales | `spanish-accounting-compliance` |
| Capitalised software and R&D in a SaaS company | `spanish-industry-saas` |
| Construction in progress, own work capitalised | `spanish-project-accounting` |
| Stock rather than assets | `spanish-inventory` |
