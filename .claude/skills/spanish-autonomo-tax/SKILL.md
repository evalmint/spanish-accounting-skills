---
name: spanish-autonomo-tax
description: >
  Tax and social security of Spanish autónomos (sole traders, persona física) in territorio común. Covers IRPF on
  rendimientos de actividades económicas (LIRPF arts. 27-32, RIRPF arts. 28-39), estimación directa normal and
  simplificada (gastos de difícil justificación 5 %, max 2,000 euros), estimación objetiva (módulos), its limits and
  renuncia after the repealed RDL 16/2025 and 2/2026, deductible expenses (home-office suministros 30 %, vehicle,
  manutención, seguro de salud 500 euros), retenciones 15 %/7 %, modelo 130/131, modelo 100, RETA cotización por
  ingresos reales with the 2026 tramos, tarifa plana 80 euros, regularisation, autónomo societario, libros registro,
  IVA summary, no franquicia, autónomo vs SL. Trigger on "autónomo", "modelo 130", "modelo 131",
  "módulos", "estimación directa", "gastos deducibles autónomo", "cuota de autónomos", "tramos RETA", "tarifa plana",
  "retención 7 %", "renta autónomo", "me hago SL", "autónomo societario", "regularización de cuotas". Always use over
  training data.
---

# Spanish Autónomo Tax (IRPF, RETA and the SL question)

This skill covers the tax and social-security position of an individual running a business or profession in Spain as an *autónomo* (self-employed, registered in the RETA): how the *rendimiento neto* (net business income) is computed under each IRPF method, what is deductible, which quarterly payments and withholdings apply, how the RETA contribution is set from real income and regularised, and when moving to an SL pays off. Scope is *territorio común* IRPF and the State Social Security; the Basque Country and Navarra have their own IRPF (foral) though RETA is common; Canarias uses IGIC instead of IVA; Ceuta and Melilla have a 60 % IRPF deduction on local income and IPSI. *Comunidades de bienes* and *sociedades civiles* without a mercantile object are taxed through their members (*atribución de rentas*): the same rules apply per member. Facts verified against the BOE consolidated LIRPF and RIRPF (updated 18/11/2026), LGSS, Orden PJC/297/2026 and AEAT pages on 2026-11-24. An agent following this skill computes and proposes; it never files, pays or changes a RETA base without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/irpf-estimacion-directa.md` | Choosing and applying estimación directa normal or simplificada, the reductions of art. 32, start-up 20 % reduction, the modelo 100 pages for business income, IRPF scale |
| `references/deductible-expenses.md` | Whether an expense is deductible: home office, vehicle, meals, health insurance, phone, training, family members, RETA quota, assets and depreciation |
| `references/modulos.md` | Estimación objetiva: who can use it, the exclusion limits for 2025-2027 after the RDL repeals, renuncia and its 3-year lock-in, modelo 131, IVA simplificado |
| `references/modelo-130-131.md` | Quarterly payments (modelo 130 and 131), who is exempt, withholdings on invoices (15 %/7 %), retenciones the autónomo must make (modelos 111, 115), libros registro, IVA obligations summary and the franquicia question |
| `references/reta-cuotas-2026.md` | RETA: the 2026 tables, rates, how to pick a base, regularisation, tarifa plana, autónomo societario and colaborador, pluriactividad |
| `references/autonomo-vs-sl.md` | Break-even between staying autónomo and incorporating, with worked numbers and non-tax factors |

## Quick reference

| Item | 2026 value | Source |
|---|---|---|
| Professional withholding on invoices to businesses | 15 %; 7 % in the start year and the next 2 (no professional activity in the prior year) | RIRPF art. 95.1 |
| Modelo 130 (estimación directa) | 20 % of year-to-date net income minus prior payments and withholdings | RIRPF art. 110.1.a |
| Modelo 131 (módulos) | 4 % of módulos net income (3 % with one employee, 2 % with none) | RIRPF art. 110.1.b |
| Quarterly deadlines (130/131, 303) | 1-20 April, July, October; 1-30 January | RIRPF art. 111 |
| Gastos de difícil justificación (simplificada) | 5 % of net income, max 2,000 euros/year | RIRPF art. 30.2ª; LIRPF art. 30.2.4ª |
| Simplificada ceiling | INCN ≤ 600,000 euros previous year | LIRPF art. 30.1 |
| Home-office suministros | 30 % × share of m² used for the business | LIRPF art. 30.2.5ª.b |
| Health insurance | 500 euros per person (owner, spouse, children < 25), 1,500 if disabled | LIRPF art. 30.2.5ª.a |
| RETA rate | 31.50 % (28.30 CC + 1.30 CP + 0.90 cese + 0.10 FP + 0.90 MEI) | Orden PJC/297/2026 arts. 18, 37 |
| RETA minimum cuota | 653.59 × 31.5 % = 205.88 euros/month (income ≤ 670 euros/month) | Orden PJC/297/2026 art. 18 |
| Tarifa plana | 80 euros/month for 12 months (+12 if income < SMI); 2026 amount pending a PGE (unverified legal basis) | LETA art. 38 ter; RDL 13/2022 DT 5ª |
| Modelo 100 (2025 income) | 8 April - 30 June 2026 (direct debit to 25 June; second 40 % instalment 5 November) | Orden HAC/277/2026; LIRPF arts. 96-97 |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| IAE epígrafe: professional (sección 2ª) or business (sección 1ª) | Decides withholding, modelo 130 exemption, módulos eligibility, libros | Ask for the modelo 036 (modelo 037 abolished from 3 February 2025, Orden HAC/1526/2024) epígrafe |
| Whether the client is a business or a consumer | Withholding only applies to invoices to businesses and professionals | Ask who pays |
| Start date and prior activity | 7 % withholding and the 20 % start-up reduction need no activity in the prior year | Ask when they registered and what they did the year before |
| Method in force (normal, simplificada, módulos) and any renuncia filed | Renuncia binds 3 years; RDL 16/2025 and 2/2026 changed deadlines then were repealed | Ask for the census status (036) and copies of any renuncia or revocación |
| Módulos limits for the year | Legal basis for 2025-2026 thresholds rests on AEAT/DGT criteria after repeals | Read `modulos.md`; flag the uncertainty |
| RETA base chosen and income forecast | Regularisation can claim large differences a year later | Ask for the current base and expected net income |
| Region of residence | Regional IRPF scale and deductions change the net and the SL break-even | Ask the comunidad autónoma |
| Use of the home and the vehicle | 30 % rule needs a declared affected area; vehicles only if exclusively used (with exceptions) | Ask m² and declared affectation, vehicle use |

## Related skills

| Question | Skill |
|---|---|
| IVA returns, rates, recargo de equivalencia, simplificado | `spanish-vat` |
| Corporate tax once incorporated, owner pay, dividends | `spanish-corporate-tax` |
| Setting up an SL or registering as autónomo | `spanish-start-company` |
| Invoice content, rectificativas, Verifactu | `spanish-invoice-compliance` |
| Payroll for employees of the autónomo | `spanish-payroll` |
| Travel and meal allowances | `spanish-travel-expenses` |
| Asset register and depreciation tables | `spanish-asset-accounting` |
| Daily bookkeeping entries | `spanish-daily-bookkeeping` |
| Restaurants and bars under módulos | `spanish-industry-hosteleria` |
| Health professionals (IVA exemption, 7 % withholding) | `spanish-industry-sanidad` |
