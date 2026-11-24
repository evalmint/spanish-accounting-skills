# PGC accounts and journal entries for projects

## Contents

1. Which accounts carry project tags
2. Account summary
3. Over-time contract: entries
4. Point-in-time contract: entries
5. Expected losses
6. Contract costs and bids
7. IVA devengo vs revenue
8. Construction specifics
9. Year-end checklist per project

Account numbers follow the PGC 2007 (RD 1514/2007, amended by RD 1/2021). The numbering is not binding, but the valuation criteria are (RD 1514/2007 art. 2); most software uses these numbers. Sub-accounts with more digits are company-specific.

---

## 1. Which accounts carry project tags

Tag lines, not accounts. The project is a dimension next to the account (see `implementation-patterns.md`).

| Group | Tag? | Examples |
|---|---|---|
| 7 Ventas e ingresos | Always for project revenue | **705** *Prestaciones de servicios*, **700**-**704** sales, **740** grants to operations |
| 6 Compras y gastos | Direct costs always; indirect via allocation keys | **600**-**607** purchases and subcontracted work (**607** *Trabajos realizados por otras empresas*), **621**, **623**, **629**, **640**, **642** |
| 3 Existencias | Point-in-time contracts | **330** *Productos en curso*, **350** *Productos terminados* |
| 4 Acreedores y deudores | Project-related balances | **430**, **4309**, **438**, **4994** |
| 1 Financiación básica | Long-term contract liabilities and capital grants | **181**, **130** |
| 8 and 9 | Not for cost accounting | In the PGC 2007, groups 8 and 9 are expenses and income recognised in equity |

Cost accounting (*contabilidad analítica*) is outside the PGC chart. The PGC 2007 introduction says group 9, used for internal accounting in the 1990 plan, was freed for the new equity accounts, and companies that keep analytic accounts may use **group 0** (PGC 2007, Introducción). Most software does it with dimensions instead.

## 2. Account summary

| Account | Name | Use in projects |
|---|---|---|
| **705** | Prestaciones de servicios | Project revenue (services, construction) |
| **4309** | Clientes, facturas pendientes de formalizar | Contract asset: revenue recognised, not yet invoiced |
| **430** | Clientes | Invoiced receivable |
| **438** | Anticipos de clientes | Contract liability: billed or paid ahead of progress, short term |
| **181** | Anticipos recibidos por ventas o prestaciones de servicios a largo plazo | Same, long term |
| **485** | Ingresos anticipados | Deferred income on time-based services (subscriptions) |
| **330** / **331** | Productos en curso | Point-in-time projects in progress (costs as inventory) |
| **710** | Variación de existencias de productos en curso | Year-end change in **330** |
| **4994** | Provisión por contratos onerosos | Expected loss on a contract |
| **6954** | Dotación a la provisión por contratos onerosos | Expense side |
| **79544** | Exceso de provisión por contratos onerosos | Release |
| **480** | Gastos anticipados | Deferred incremental costs of obtaining a contract (one common choice) |
| **477** | Hacienda Pública, IVA repercutido | Output IVA, at devengo |
| **730** / **731** | Trabajos realizados para el inmovilizado intangible / material | Own-account projects that create company assets (not customer projects) |

## 3. Over-time contract: entries

Example from `revenue-recognition.md` §12 (200,000 euros, cost-to-cost). Costs are booked by nature as incurred (**640**, **642**, **607**, **629** against **465**, **476**, **400**, **410**), tagged to the project.

**Year 1.** Invoice on signing, 30 % = 60,000 + 21 % IVA:

| Account | Debit | Credit |
|---|---|---|
| **430** Clientes | 72,600 | |
| **705** Prestaciones de servicios | | 60,000 |
| **477** IVA repercutido | | 12,600 |

Year-end: progress 40 % → cumulative revenue 80,000; invoiced 60,000; recognise the difference as a contract asset, no IVA:

| Account | Debit | Credit |
|---|---|---|
| **4309** Clientes, facturas pendientes de formalizar | 20,000 | |
| **705** Prestaciones de servicios | | 20,000 |

Reverse on 1 January, or carry and adjust to the new cumulative figure; keep one approach.

**If billed ahead of progress** (say invoiced 100,000 and progress gives 80,000):

| Account | Debit | Credit |
|---|---|---|
| **705** Prestaciones de servicios | 20,000 | |
| **438** Anticipos de clientes | | 20,000 |

IVA on the 100,000 was due at invoicing or collection anyway (see §7).

**Advance received before any work** (down payment 30,000 + IVA, collected):

| Account | Debit | Credit |
|---|---|---|
| **572** Bancos | 36,300 | |
| **438** Anticipos de clientes | | 30,000 |
| **477** IVA repercutido | | 6,300 |

IVA is due on collection of the advance (LIVA art. 75.Dos). Apply **438** to **705** as work is performed.

## 4. Point-in-time contract: entries

Costs by nature during the year (tagged). At year-end, capitalise the cost of unfinished projects as inventory (production cost per ICAC Resolución 14-04-2015):

| Account | Debit | Credit |
|---|---|---|
| **330** Productos en curso | 45,000 | |
| **710** Variación de existencias de productos en curso | | 45,000 |

Next year-end, reverse the opening balance and book the new one (the net movement is the variation). On delivery and acceptance, invoice to **705** (or **700**-**701** for goods) with IVA. Test **330** for net realisable value; a write-down goes to **693** *Pérdidas por deterioro de existencias* against **393** (check the exact sub-accounts in the chart).

## 5. Expected losses

Year 2 of the example: total cost 210,000 > revenue 200,000. Cumulative result after recognising revenue is −7,143; the remaining expected loss is −2,857:

| Account | Debit | Credit |
|---|---|---|
| **6954** Dotación a la provisión por contratos onerosos | 2,857 | |
| **4994** Provisión por contratos onerosos | | 2,857 |

Apply the provision as the remaining costs are incurred (debit **4994**, credit **79544** for any excess at the end). Tax: not deductible when booked (LIS art. 14.3.b); record a deferred tax asset (**4740**) if recoverable. See `tax-and-grants.md`.

For a point-in-time contract, first write down **330** to net realisable value, then provide for any further unavoidable loss.

## 6. Contract costs and bids

- Sales commission payable only on signature, recoverable: defer (debit **480** or a specific asset sub-account, credit the commission payable) and release over the contract's transfer pattern (RICAC art. 21).
- Set-up costs that create a resource used to fulfil the contract: inventory or intangible (RICAC art. 22).
- Bid costs before the contract is probable: expense as incurred.

## 7. IVA devengo vs revenue

Revenue recognition and IVA are independent clocks.

| Event | IVA devengo | Source |
|---|---|---|
| Service performed | When performed | LIVA art. 75.Uno.2º |
| *Ejecución de obra* with materials supplied | When the work is put at the owner's disposal | art. 75.Uno.2º, third paragraph |
| Works for a public administration | On formal reception | art. 75.Uno.2º bis |
| Continuous services with periodic billing | When each instalment becomes payable | art. 75.Uno.7º |
| Advance payment | On collection, for the amount received | art. 75.Dos |

The year-end entry to **4309** carries no IVA; issue the invoice and charge IVA when devengo occurs. Domestic construction subcontracts can fall under *inversión del sujeto pasivo* (LIVA art. 84.Uno.2º.f): see `spanish-industry-construccion` and `spanish-vat`.

## 8. Construction specifics

The 1993 sectoral adaptation for construction companies adds detailed sub-accounts (production executed pending certification, retentions) that many construction ledgers still use; they map onto **4309** and **430** sub-accounts in PGC 2007 terms (unverified, check `spanish-industry-construccion`). *Retenciones de garantía* withheld by the customer stay in receivables until released.

## 9. Year-end checklist per project

1. Estimate to complete refreshed and approved by the project manager.
2. Progress computed with the same method as last year.
3. Cumulative revenue minus billed = **4309** (if positive) or **438** (if negative), per project, no netting across projects.
4. Total estimated costs vs revenue: provision if a loss (**4994**).
5. Point-in-time projects: **330** at production cost, NRV test.
6. IVA: every invoice or advance collected reported in modelo 303 of its period.
7. Closed projects: **4309**, **438**, **330** and **4994** balances at zero.
