# Closing process (cierre contable)

## Contents

- [Legal basis](#legal-basis)
- [Phase 1: reconciliations](#phase-1-reconciliations)
- [Phase 2: periodificaciones](#phase-2-periodificaciones)
- [Phase 3: amortisation](#phase-3-amortisation)
- [Phase 4: impairment (deterioro)](#phase-4-impairment-deterioro)
- [Phase 5: provisions](#phase-5-provisions)
- [Phase 6: inventories](#phase-6-inventories)
- [Phase 7: foreign currency](#phase-7-foreign-currency)
- [Phase 8: subsidies and IVA prorrata](#phase-8-subsidies-and-iva-prorrata)
- [Phase 9: corporate income tax](#phase-9-corporate-income-tax)
- [Phase 10: regularización, cierre, apertura](#phase-10-regularización-cierre-apertura)
- [Phase 11: after closing](#phase-11-after-closing)
- [Autónomos](#autónomos)

Entries for each step: `journal-entries.md`. All entries are dated at year-end (e.g. 31-12-2026) unless stated.

## Legal basis

| Rule | Source |
|---|---|
| Accrual: income and expenses in the year they relate to, regardless of payment | Cco art. 38.d; PGC Marco conceptual, principio de devengo |
| Prudence: only realised profits; all risks known up to formulation; amortisation and impairment whether profit or loss | Cco art. 38.c |
| Closing inventory and cuentas anuales transcribed in the Libro de Inventarios y Cuentas Anuales | Cco art. 28.1 |
| Post-closing events that show conditions at year-end are adjusted; others only disclosed | PGC NRV 23.ª |
| Formulation within 3 months | LSC art. 253.1 |

## Phase 1: reconciliations

| Area | Check | Accounts |
|---|---|---|
| Banks | Balance per bank statement at year-end; book bank charges, interest and pending items | **572**, **626**, **662**/**769** |
| Customers | Ageing; confirm open invoices; identify doubtful debts | **430**, **431**, **436** |
| Suppliers | Statements; invoices received after year-end for goods or services of the year | **400**, **410**, **4009** |
| Staff | Payroll of December, pagas extraordinarias accrued, advances | **640**, **465**, **460** |
| Social security | December contributions payable in January | **642**, **476** |
| Tax | IVA of the last period moved to **4750**/**4700**; IRPF withholdings **4751**; payments on account of IS in **473** | **472**, **477**, **4700**, **4750**, **4751**, **473** |
| Partner and related accounts | Balances with partners and administrators | **551**, **552** |
| Suspense | **555** Partidas pendientes de aplicación must be cleared | **555** |
| Fixed-asset register | Additions, disposals, assets in use; agree to **21**x | **21**x, **28**x |

## Phase 2: periodificaciones

| Case | Treatment | Accounts |
|---|---|---|
| Expense paid in advance (insurance, rent, licences) covering next year | Defer the part for next year | **480** Gastos anticipados |
| Income received in advance (subscriptions, rent collected) | Defer the part for next year | **485** Ingresos anticipados |
| Expense of the year without an invoice yet (utilities, audit, advisers) | Accrue | **4009** Proveedores, facturas pendientes de recibir o de formalizar (or **410** for creditors) |
| Income earned, not invoiced | Accrue (revenue per NRV 14.ª and ICAC Res. 10-02-2021) | **4309** Clientes, facturas pendientes de formalizar |
| Interest payable accrued | Accrue | **662**/**6623** vs **527** or **528** |
| Interest receivable accrued | Accrue | **547** vs **762** |
| Pagas extraordinarias accrued but unpaid | Accrue | **640** vs **465** |

Interest on debt measured at amortised cost is recognised with the effective interest rate (NRV 9.ª); for simple bank loans the accrual equals the contractual interest.

## Phase 3: amortisation

- Each asset with a limited useful life is amortised systematically and rationally (Cco art. 39.1; NRV 2.ª-5.ª). Intangibles have a definite life; 10 years if not reliably estimable; goodwill 10 years (Cco art. 39.4).
- Book **680** (intangible) / **681** (material) / **682** (investment property) against **280** / **281** / **282**.
- Tax deductibility follows LIS art. 12 (tables, limits). Differences (e.g. *libertad de amortización*, accelerated amortisation for ERD under LIS art. 103) create temporary differences: `tax-accrual.md`. Detail: `spanish-asset-accounting`.

## Phase 4: impairment (deterioro)

| Asset | Test | Accounts |
|---|---|---|
| Fixed assets | Recoverable amount below book value (NRV 2.ª.2, 6.ª) | **690**/**691** vs **290**/**291**; reversal **790**/**791** |
| Inventories | Net realisable value below cost (NRV 10.ª.2) | **693** vs **39**x; reversal **793** |
| Trade receivables | Objective evidence of non-collection (NRV 9.ª) | **694** vs **490** (or reclassify to **436**); reversal **794**; definitive loss **650** |
| Financial investments | NRV 9.ª | **696**-**699** vs **29**x/**59**x |

Tax: impairment of receivables is deductible only when, at year-end, 6 months have passed since the due date, the debtor is in insolvency proceedings, has been charged with *alzamiento de bienes*, or the debt is claimed in court (LIS art. 13.1); not for public entities or related parties except in insolvency. ERD may deduct a global impairment of up to 1 % of the receivables at year-end (LIS art. 104.1). The difference is temporary: **4740**.

## Phase 5: provisions

A provision is recognised for a present obligation (legal, contractual or constructive) from a past event, probable outflow, reliably estimated (NRV 15.ª). Contingencies are disclosed only.

| Type | Long term / short term | Expense |
|---|---|---|
| Taxes (e.g. a likely tax assessment) | **141** / **5291** | **633** for IS of prior years, **631** for other taxes, interest **669**, sanctions **678** |
| Other liabilities (litigation, guarantees given) | **142** / **5292** | Account of group 6 by nature (e.g. **623**, **629**, **678**) |
| Dismantling | **143** | Capitalised in the asset (NRV 2.ª) |
| Restructuring | **146** | By nature |
| Trade (warranties, onerous contracts) | **499** (**4994**, **4999**) | **695** (**6954**, **6959**) |

Long-term provisions are discounted; the unwinding goes to **660**. Excess is released to **795**x. Tax: several provisions are not deductible when booked (LIS art. 14: e.g. implicit obligations, restructuring without a legal obligation, onerous contracts, returns) and become deductible when applied; book the temporary difference.

## Phase 6: inventories

Periodic method (the PGC default): purchases go to group 60 during the year; at year-end the opening stock is removed and the closing stock entered through the variation accounts.

| Stock | Out (opening) | In (closing) |
|---|---|---|
| Mercaderías | Debit **610**, credit **300** | Debit **300**, credit **610** |
| Materias primas | Debit **611**, credit **31**x | Debit **31**x, credit **611** |
| Productos en curso | Debit **710**, credit **330** | Debit **330**, credit **710** |
| Productos terminados | Debit **712**, credit **350** | Debit **350**, credit **712** |

Value at cost (FIFO or weighted average; LIFO not allowed, NRV 10.ª.1), then impairment to net realisable value. Software with a perpetual inventory still presents the variation lines in the PyG model. Detail: `spanish-inventory`.

## Phase 7: foreign currency

At year-end, monetary items in foreign currency (cash, receivables, payables, loans) are translated at the closing rate; differences go to PyG (NRV 11.ª.2.2): losses **668**, gains **768**. Non-monetary items at historical cost keep the historical rate.

## Phase 8: subsidies and IVA prorrata

- Capital subsidies (non-repayable) are booked in equity (**130**, net of tax effect **479**) and transferred to PyG in proportion to the amortisation of the funded asset (NRV 18.ª): **840**/**746**. The tax effect is booked through **8301** and **479**.
- IVA prorrata: final percentage regularisation in the last period (LIVA arts. 105-106): **634**/**639** (**6341**/**6342**, **6391**/**6392**). See `spanish-vat`.

## Phase 9: corporate income tax

Compute the current tax and the deferred tax, book **6300** and **6301**, and net the payments on account in **473**. Full method and example: `tax-accrual.md`.

## Phase 10: regularización, cierre, apertura

1. **Regularización.** Close every group 6 and 7 account against **129** Resultado del ejercicio. The balance of **129** is the profit (credit) or loss (debit) after tax.
2. **Groups 8 and 9.** Close income and expense recognised in equity against the group 13 accounts they belong to (e.g. **940** and **8301** against **130**; **840** against **130**).
3. **Closing inventory.** Transcribe the detailed balance and the cuentas anuales in the Libro de Inventarios y Cuentas Anuales (Cco art. 28.1).
4. **Asiento de cierre.** Every balance-sheet account (groups 1-5, including **129**) is debited or credited to zero. The Cco does not prescribe this entry by name, but the Diario conventionally ends with it.
5. **Asiento de apertura.** On the first day of the new year, the exact reverse. **129** stays open until the junta applies the result.

Many software packages skip the physical closing and opening entries and carry balances forward; the Diario export for legalisation should still show regularización and, where the company follows the convention, cierre and apertura.

## Phase 11: after closing

| Step | When | Source |
|---|---|---|
| Formulate the cuentas anuales and proposed application of profit | Within 3 months | LSC art. 253 |
| Legalise the books | Within 4 months | Ley 14/2013 art. 18 |
| Junta approves accounts and application of profit | Within 6 months | LSC art. 164 |
| Book the application of profit | On the junta date | `aplicacion-resultado.md` |
| Deposit | Within 1 month of approval | LSC art. 279 |
| IS return | 25 days after the 6 months following year-end | LIS art. 124.1 |

## Autónomos

| Situation | Year-end work |
|---|---|
| Cco accounting (estimación directa normal, mercantile activity; RIRPF art. 68.2) | Same phases 1-8 and 10-11 (no IS, no deposit, no junta). The result in **129** is transferred to the owner's capital (**102**) or to **550** Titular de la explotación |
| Libros registro (simplificada, professionals, non-mercantile activity) | No accounting closing. Update the libro de bienes de inversión with the year's amortisation (official tables; simplified table in simplificada, RIRPF art. 30.1.ª); in simplificada, provisions and hard-to-justify expenses are 5 % of the net result, max 2,000 € (RIRPF art. 30.2.ª); reconcile income and expenses with the quarterly modelo 130 and IVA returns |
| Estimación objetiva (módulos) | Keep invoices; amortisation only if signs and modules allow it |

The annual IRPF return (modelo 100) closes the year for the autónomo: `spanish-autonomo-tax`.
