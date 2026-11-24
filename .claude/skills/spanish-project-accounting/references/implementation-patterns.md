# Implementation patterns for project accounting software

## Contents

1. Principles
2. Data model
3. Project lifecycle
4. Cost capture and allocation
5. Progress and revenue engine
6. Profitability reporting
7. Controls and common errors

How to build project accounting on top of a Spanish general ledger. The legal rules are in `revenue-recognition.md` and `accounts-and-entries.md`; this file is design guidance, not law.

---

## 1. Principles

- **Project is a dimension, not an account.** Keep the PGC chart clean (**705**, **640**, **607**) and tag each journal line with a project ID. Do not create one revenue account per project.
- **Analytic accounting is optional and off-chart.** No law requires cost accounting for an ordinary company; the PGC 2007 suggests group 0 if a company wants analytic accounts in the ledger (PGC Introducción), not group 9, which holds income recognised in equity.
- **Revenue recognition is a period-end process**, driven by progress data, that writes a small number of adjusting entries (**4309**, **438**, **4994**, **330**/**710**). Source documents (invoices, payslips) are never altered by it.
- **The agent proposes, the user approves.** Generated period-end entries are drafts until a person confirms them.

## 2. Data model

| Entity | Key fields |
|---|---|
| Project | id, customer, contract reference, start/end, status, type (fixed price, time and materials, cost plus, internal), recognition pattern (over time / point in time), progress method, currency |
| Performance obligation | project id, description, allocated price, pattern, method |
| Budget | obligation id, version, total revenue, total cost by category, approved by, date |
| Estimate to complete | obligation id, period, remaining cost, remaining hours, author |
| Journal line tag | line id, project id, obligation id (optional), cost category |
| Timesheet | person, project, obligation, date, hours, cost rate (loaded) |
| Billing schedule | project, milestone, amount, due condition |
| Contract modification | project, date, scope change, price change, treatment (separate / prospective / catch-up) |
| Grant | project, award amount, conditions, repayable flag, milestones |

Keep budget and estimate history: auditors ask how progress moved.

## 3. Project lifecycle

| Status | Allowed | Checks on leaving |
|---|---|---|
| Draft | Budget, bid costs (expensed) | Contract signed and meets RICAC art. 3 |
| Active | Costs, time, invoices, period-end recognition | |
| Completed | Final invoice, warranty provision | Revenue = contract price; **4309**, **438**, **330** at zero |
| Closed | Nothing | Zero balances checked; **4994** applied or released |

## 4. Cost capture and allocation

- **Direct costs:** supplier invoices, subcontractors (**607**), materials, travel, tagged on entry.
- **Labour:** hours × loaded cost rate (salary **640** + employer social security **642** + allocated paid leave), posted as a management allocation, not a second ledger entry. In the ledger, salaries stay where payroll booked them; the project report uses timesheets.
- **Indirect costs:** allocate with documented keys (hours, direct cost, headcount, m²). For inventory and the input method, only production costs count: direct costs plus a reasonable share of indirect production costs based on normal capacity; no general administration, selling or financial costs except as the ICAC 2015 cost resolution allows.
- Keep allocation keys stable within a year; changes are documented.

## 5. Progress and revenue engine

For each over-time obligation at period end:

```
progress        = method(obligation)              # cost-to-cost, hours, milestones, output survey
if not measurable and costs recoverable:
    cumulative_revenue = cumulative_costs         # NRV 14.2, zero margin
else:
    cumulative_revenue = allocated_price * progress
period_revenue  = cumulative_revenue - revenue_recognised_to_date
billed          = sum(invoices to date, net of IVA)
contract_asset  = max(cumulative_revenue - billed, 0)    # 4309
contract_liab   = max(billed - cumulative_revenue, 0)    # 438 / 181
expected_total  = cumulative_costs + estimate_to_complete
loss            = max(expected_total - allocated_price, 0)
provision       = loss - (cumulative_costs - cumulative_revenue)   # remaining loss, 4994
```

Rules:
- Cost-to-cost excludes uninstalled third-party materials and abnormal waste (RICAC art. 11.5).
- Compute per obligation, present per contract; never net across contracts.
- For point-in-time obligations, compute the year-end **330** balance at production cost and test net realisable value.
- Flag for review: progress more than 20 points away from time elapsed or budget consumed; estimate to complete unchanged for three periods; negative estimate to complete; costs after "Completed".

## 6. Profitability reporting

| Report | Content |
|---|---|
| Project P&L | Revenue recognised, direct costs, labour, allocated overhead, margin, margin % |
| WIP schedule | Per project: contract value, progress, cumulative revenue, billed, **4309**/**438**, provision |
| Budget vs actual | Cost by category vs approved budget and current estimate |
| Backlog | Remaining performance obligations (contract value less revenue recognised) |
| Utilisation | Billable hours / available hours per person |

Reconcile monthly: sum of project revenue = **705** (and other revenue accounts) in the ledger; sum of project contract assets = **4309**.

## 7. Controls and common errors

| Error | Consequence | Control |
|---|---|---|
| Revenue booked straight from the billing schedule on a fixed-price over-time project | Revenue follows invoices, not progress | Period-end engine required for fixed-price over-time obligations |
| IVA charged on the **4309** accrual | IVA reported too early | Accrual entries carry no tax code |
| Netting **4309** of one project with **438** of another | Misstated balance sheet | Per-project balances |
| Loss contract with no provision | Overstated profit | Expected-total check every period |
| Changing progress method mid-contract | Arbitrary revenue | Method locked per obligation |
| Untagged costs | Wrong progress (input method) and margins | Required tag on cost accounts for project companies |
| Grant booked entirely to income on award | Wrong period | Grant module with NRV 18 classification |
| Closed project with residual balances | Audit finding | Zero-balance check on closing |
