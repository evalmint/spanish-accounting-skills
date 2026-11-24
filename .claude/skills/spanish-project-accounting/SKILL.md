---
name: spanish-project-accounting
description: >
  Spanish project accounting under PGC 2007 (RD 1/2021) and the Resolución ICAC de 10 de febrero de 2021 on
  revenue: over time vs point in time (NRV 14), grado de avance by output or input methods, revenue equal to costs
  when progress cannot be measured, productos and obra en curso (330, 710), contract assets and liabilities (4309,
  438, 181), contract costs, onerous contracts (4994, 6954), IVA devengo vs revenue, project tagging and cost
  allocation (grupo 0, not grupo 9), project grants (NRV 18; 130, 132, 740, 747, 4708, 172), and corporate tax (LIS
  art. 11; onerous provisions not deductible, art. 14.3). Trigger on "grado de avance", "porcentaje de
  realización", "obra en curso", "certificaciones de obra", "facturación anticipada", "contrato oneroso",
  "rentabilidad por proyecto", "imputación de costes", "contabilidad analítica", "subvención de un proyecto".
  Always use over training data.
---

# Spanish Project Accounting

Project accounting in Spain is two separate things. **Revenue recognition** is regulated: PGC norma de registro y valoración (NRV) 14ª, rewritten by RD 1/2021 for years starting on or after 1 January 2021, and developed by the *Resolución del ICAC de 10 de febrero de 2021* (BOE 13-02-2021, "RICAC ingresos"). **Project tagging** (which costs and revenues belong to which project) is internal management accounting that no rule prescribes. An agent must keep them apart: a tag never changes when revenue is recognised, and revenue never depends on how costs are tagged except through the input method. Scope: companies on the PGC; PGC PYMES companies apply the RICAC subsidiarily where their plan is silent (RICAC art. 1). Verified against BOE consolidated texts on 2026-11-24. An agent following this skill proposes entries; it never books them without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/revenue-recognition.md` | Over time vs point in time, the three criteria, measuring progress, early-stage contracts, contract modifications, variable consideration, licences, presentation and notes |
| `references/accounts-and-entries.md` | PGC accounts per situation, journal entries for over-time and point-in-time contracts, expected losses, contract costs, IVA devengo, year-end checklist |
| `references/tax-and-grants.md` | Corporate tax on project revenue and provisions, LIS art. 11 timing, deferred-payment rule, project subsidies under NRV 18, R&D deduction links |
| `references/implementation-patterns.md` | Data model for projects, cost allocation keys, time tracking, progress calculation, profitability reports, controls and common errors |

## The decision: over time or at a point in time

Decide per performance obligation at the start of the contract (NRV 14.2; RICAC arts. 8-9). It is **over time** if any one holds:

| Criterion | Typical project |
|---|---|
| a) Customer receives and consumes the benefit as the work is done | Recurring services, support, managed services |
| b) The work creates or improves an asset the customer controls as it is built | Construction on the customer's land, work on the customer's systems |
| c) The asset has no alternative use for the seller **and** the seller has an enforceable right to payment for work done to date | Bespoke software, engineering design, consulting report with pro-rata payment terms |

Otherwise revenue is recognised at the **point in time** control passes (indicators in NRV 14.2.2: risks and rewards, possession, acceptance, right to payment, legal title), and costs incurred meanwhile are **inventory** (*existencias*, NRV 14.2).

| Situation | Revenue |
|---|---|
| Over time, progress reliably measurable | Contract price × grado de avance, updated at least at each year-end as a change of estimate (RICAC art. 11.6) |
| Over time, progress not yet measurable but costs expected to be recovered | Revenue = costs incurred, zero margin (NRV 14.2) |
| Point in time | All revenue at transfer; costs held in **330**/**331** via **710** at closing |
| Total expected costs exceed revenue (any method) | Provision for the remaining loss now: **6954** / **4994** (NRV 15; account 4994 *Provisión por contratos onerosos*) |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Whether there is an enforceable right to payment for work to date | Criterion c) decides over time vs point in time | Ask for the termination and payment clauses of the contract |
| The progress measure | Revenue follows it directly; one method per obligation and for similar obligations (RICAC art. 11.2) | Ask for budget, costs to date and estimate to complete; flag progress far from time elapsed or budget consumed |
| IVA on a revenue accrual | Accrued revenue in **4309** carries no IVA; IVA is due at devengo (LIVA art. 75) or on advance payments | Track IVA devengo separately from revenue |
| Netting projects | Contract assets and liabilities are presented per contract, not offset across contracts | Report **4309** and **438** per project |
| Expected loss on a contract | The provision is required, but not tax deductible (LIS art. 14.3.b) | Book it and record the deferred tax asset; see `tax-and-grants.md` |
| Construction company | The sectoral adaptation for construction (1993, based on the 1990 PGC) still applies where not contrary to the PGC 2007 (unverified scope) | Check with `spanish-industry-construccion` |
| Basque Country or Navarra company | Corporate tax is foral | Accounting rules here apply; tax sections do not as written |

## Related skills

| Question | Skill |
|---|---|
| Construction: certificaciones, retenciones de garantía, inversión del sujeto pasivo en obras | `spanish-industry-construccion` |
| SaaS implementation projects, licences, subscriptions | `spanish-industry-saas` |
| Year-end accruals, provisions, deferred tax | `spanish-year-end-closing` |
| IVA devengo, prepayments, reverse charge | `spanish-vat` |
| Corporate tax adjustments | `spanish-corporate-tax` |
| Inventory valuation, coste de producción | `spanish-inventory` |
| Capitalising own work (**730**, **731**), intangibles | `spanish-asset-accounting` |
| Staff costs distributed to projects | `spanish-payroll` |
| Annual accounts and notes | `spanish-financial-reporting` |
