# Corporate tax and grants for projects

## Contents

1. Corporate tax follows the accounts
2. Where tax and accounts diverge
3. Project grants under NRV 18
4. Grant entries
5. R&D and innovation projects
6. Ask the user

Verified 2026-11-24 against the consolidated LIS (Ley 27/2014, last updated 21/11/2026) and PGC 2007. Scope: *territorio común*; the Basque Country and Navarra have their own corporate tax laws.

---

## 1. Corporate tax follows the accounts

- The tax base starts from the accounting result (LIS art. 10.3).
- Income and expenses are allocated to the period of their accrual under accounting rules (LIS art. 11.1). Revenue recognised by grado de avance under NRV 14 is therefore taxed as recognised, with no separate tax method.
- A different criterion used to give a true and fair view needs AEAT approval (art. 11.2).
- Expenses booked in a later year than their accrual, or income booked earlier, are taxed when booked provided that does not lower tax (art. 11.3.1º).
- Changes of accounting policy credited or charged to reserves enter the base in the year made, without double counting (art. 11.3.2º).

## 2. Where tax and accounts diverge

| Item | Accounts | Tax | Source |
|---|---|---|---|
| Onerous contract provision (**4994**) | Expense when the loss is probable | Not deductible; deductible when the provision is applied | LIS art. 14.3.b, 14.5 |
| Deferred-payment sales (*operaciones a plazos*): last instalment due more than a year after accrual | Revenue at transfer | May be taxed as instalments fall due, unless the company opts for accrual | LIS art. 11.4 |
| Inventory write-down of **330** | Expense | Deductible (no specific limitation) | LIS art. 10.3 |
| Contract-cost amortisation | Expense over the contract | Follows accounting | LIS art. 11.1 |
| Impairment of project receivables | Expense | Deductible after 6 months overdue and other conditions | LIS art. 13.1 |

The non-deductible provision creates a temporary difference: deferred tax asset (**4740**) against **6301**, if recovery is probable.

## 3. Project grants under NRV 18

| Grant type | Recognition | Accounts |
|---|---|---|
| Non-repayable, to finance an asset (capital grant) | Equity, net of tax effect, then to profit as the asset is amortised | **940** then **130** *Subvenciones oficiales de capital*; deferred tax **479**; transfer **840** to **746** |
| Non-repayable, to finance specific expenses (project costs, salaries) | Equity first, then to profit as the financed expenses are incurred; if granted for expenses already incurred, direct to profit | **942** then **132** *Otras subvenciones, donaciones y legados*; transfer **842** to **747** |
| To guarantee profitability or cover operating deficits, or for current expenses in the same year | Profit and loss | **740** *Subvenciones, donaciones y legados a la explotación* |
| Repayable (conditions not yet met with reasonable assurance) | Liability | **172** (long term) / **522** (short term) *Deudas transformables en subvenciones* |
| Granted, not yet collected | Receivable from the public body | **4708** *Hacienda Pública, deudora por subvenciones concedidas* |

A grant is "non-repayable" when there is an individual agreement, all conditions are met, and there are no reasonable doubts it will be received (NRV 18.1.1). For multi-year projects with milestones, the grant is usually repayable until the milestone conditions are met.

Tax: the grant is taxed as it reaches profit and loss (LIS art. 11.1). The equity amount is shown net of the deferred tax liability (**479**).

## 4. Grant entries

Grant of 100,000 euros for an R&D project's personnel costs, conditions met, collected later:

| Step | Debit | Credit |
|---|---|---|
| Award | **4708** 100,000 | **942** 100,000 |
| Tax effect at the applicable rate (say 25 %) | **8301** 25,000 | **479** 25,000 |
| Close groups 9/8 to equity | **942** 100,000 | **132** 75,000; **8301** 25,000 |
| As the financed costs are incurred (say 40 % this year) | **842** 40,000 | **747** 40,000 |
| Reverse the tax effect on the transferred part | **479** 10,000 | **8301** 10,000 |
| Close groups 8/9 to equity | **132** 30,000; **8301** 10,000 | **842** 40,000 |
| Collection | **572** 100,000 | **4708** 100,000 |

Use the company's actual IS rate (25 % general; 2026 micro-company and reduced-size rates in `spanish-corporate-tax`). When the grant and the financed expenses fall in the same year, many companies book directly to **740**; agree the policy with the auditor.

## 5. R&D and innovation projects

- Track R&D projects separately: the art. 35 LIS deduction requires expenses "specifically individualised by project" (art. 35.1.b), and grants received for the activity reduce the deduction base.
- R&D deduction: 25 % of expenses (42 % on the excess over the average of the two previous years), plus 17 % of qualified researchers' personnel costs; technological innovation 12 %, raised to **15 %** in the first two periods with such expenses, when they grow at least 20 %, or when they are not below the prior two-year average, by RDL 40/2026 of 20 November 2026 (BOE 21-11-2026, in force the same day; pending convalidation; which tax periods it covers is not stated in the text) (LIS art. 35). Detail in `spanish-industry-saas` (`references/development-and-incentives.md`).
- Capitalised development (**201**) under NRV 6 vs expense; tax free amortisation of capitalised R&D (LIS art. 12.3.c). See `spanish-asset-accounting`.

## 6. Ask the user

- Which projects are fixed price, which time-and-materials, and which have a termination clause that pays work done?
- What is the estimate to complete for each open project, and who approves it?
- Any project expected to lose money?
- Any grant: the resolution, conditions, milestones and whether any part may have to be repaid?
- Is the company on the PGC or the PGC PYMES, and is it audited?
