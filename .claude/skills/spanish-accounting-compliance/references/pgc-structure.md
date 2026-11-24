# PGC structure, entries, corrections and software integrity

## Contents

- [The five parts and what binds](#the-five-parts-and-what-binds)
- [The cuadro de cuentas: groups 1-9](#the-cuadro-de-cuentas-groups-1-9)
- [Account numbering in practice](#account-numbering-in-practice)
- [Asientos: what an entry needs](#asientos-what-an-entry-needs)
- [Corrections](#corrections)
- [Errors, changes in policy and estimates (NRV 22)](#errors-changes-in-policy-and-estimates-nrv-22)
- [Software integrity and Verifactu](#software-integrity-and-verifactu)
- [Sanctions](#sanctions)

## The five parts and what binds

| Part | Content | Binding? |
|---|---|---|
| 1 Marco conceptual | Imagen fiel, requisitos de la información, principios (empresa en funcionamiento, devengo, uniformidad, prudencia, no compensación, importancia relativa), elements, recognition, valuation bases | Yes |
| 2 Normas de registro y valoración (NRV 1.ª-23.ª) | Recognition and measurement | Yes |
| 3 Cuentas anuales | Normas de elaboración, normal and abbreviated models, memoria | Yes (models are fixed formats) |
| 4 Cuadro de cuentas | Numbered chart, groups 1-9 | Numbering and names not binding, except where they carry recognition or valuation criteria |
| 5 Definiciones y relaciones contables | What each account records, its debit and credit movements | *Movimientos* not binding, same exception |

Source: RD 1514/2007 art. 2 (PGC) and RD 1515/2007 art. 3.1 (PGC-PYMES, same wording). In practice almost every Spanish company and all accounting software use the PGC numbering, because the official models of the cuentas anuales map their headings to it and the Registro Mercantil XBRL deposit expects the model headings. A company may use its own codes if it can still produce the official models.

## The cuadro de cuentas: groups 1-9

| Group | Name | Content | Statement |
|---|---|---|---|
| 1 | Financiación básica | Capital **100**, reserves **112**/**113**, results **120**/**121**/**129**, subsidies **130**, provisions **14**x, long-term debt **17**x, deferred tax liability is in group 4 (**479**) | Balance (patrimonio neto, pasivo no corriente) |
| 2 | Activo no corriente | Intangible **20**x, material **21**x, investment property **22**x, financial **24**x-**25**x, amortisation **28**x, impairment **29**x | Balance |
| 3 | Existencias | **300** mercaderías, raw materials, products, impairment **39**x | Balance |
| 4 | Acreedores y deudores por operaciones comerciales | Suppliers **400**, creditors **410**, customers **430**, staff **46**x, public bodies **47**x, accruals **480**/**485**, impairment **490** | Balance |
| 5 | Cuentas financieras | Short-term debt **52**x, partner accounts **551**, cash and banks **570**/**572** | Balance |
| 6 | Compras y gastos | Purchases **60**x, services **62**x, taxes **63**x, staff **64**x, financial **66**x, amortisation **68**x, impairment **69**x | PyG |
| 7 | Ventas e ingresos | Sales **70**x, other income **75**x, financial **76**x, reversals **79**x | PyG |
| 8 | Gastos imputados al patrimonio neto | e.g. tax effect **8301**, transfer of subsidies **840** | ECPN |
| 9 | Ingresos imputados al patrimonio neto | e.g. subsidies received **940** | ECPN |

Groups 1-5 are balance-sheet accounts, 6-7 PyG, 8-9 income and expense recognised directly in equity (closed against group 13 accounts at year-end). PGC-PYMES keeps the same group structure with fewer accounts.

## Account numbering in practice

- The PGC defines 2-digit subgroups, 3-digit accounts and 4-digit subaccounts. Companies add digits for detail (e.g. one customer per subaccount under **430**). Software usually fixes a length (8-10 digits) and pads with zeros.
- Accounts with tax or model consequences must keep their meaning: LGT art. 200.1.b sanctions using accounts with a meaning other than their nature where it hinders a tax check.
- PGC account names for IVA: **472** (soportado) and **477** (repercutido) have no 4-digit subaccounts in the PGC; **4700** and **4750** are the IVA receivable and payable after the return.

## Asientos: what an entry needs

The Cco does not list fields, but its rules imply them:

| Requirement | Source |
|---|---|
| Chronological order, day by day | Cco arts. 25.1, 28.2 |
| No blank spaces, interpolations, crossings-out or erasures | Cco art. 29.1 |
| No abbreviations or symbols whose meaning is not clear | Cco art. 29.1 |
| Amounts in euros | Cco art. 34.5 (art. 29.2 still says pesetas) |
| Every entry supported by a document (invoice, contract, bank statement, acta) | Cco art. 30.1 (conservation of *justificantes*); LGT art. 106.4 for tax deductions |
| Recorded within 4 months for tax purposes | LGT art. 200.1.e (delay over 4 months is an infraction) |

Software should give each entry a date, a sequential number within the year, a description, at least two lines balancing to zero, a document reference, the user and the timestamp of recording.

## Corrections

| Case | How | Why |
|---|---|---|
| Error in the current open year | Reverse (*contraasiento*) and re-book, or book a difference entry, dated when the error is found; keep the original visible | Cco art. 29.1: errors are corrected as soon as noticed, never by erasure |
| Entry already in legalised books | New correcting entry in the current year; if the legalised file itself is wrong, a rectification filing with an administrators' certificate | Instrucción DGRN 12-02-2015, Decimotercera |
| Error in a prior year's cuentas anuales | NRV 22 (below) | |
| Error that changes a filed IVA return | Correct the return (complementaria / rectificación), separately from the accounting entry | See `spanish-vat` |

Deleting a posted entry is never acceptable. In software terms: once an entry is posted (and certainly once a period is closed or the books are legalised), only new entries change the balances.

## Errors, changes in policy and estimates (NRV 22)

| Type | Definition | Treatment |
|---|---|---|
| Error | Omissions or inaccuracies in prior-year cuentas anuales from not using, or misusing, reliable information that was available when they were formulated | Retroactive: cumulative effect at the start of the year against a reserve account (normally **113**), unless it affects another equity item; restate the comparative figures; disclose in the memoria |
| Change in accounting policy | Only allowed under the consistency principle | Same as error, from the earliest year with information |
| Change in estimate | New information, more experience or new facts (useful life, bad-debt estimate, provision amount) | Prospective: through PyG of the current year (or equity where applicable) and future years; disclose if significant |

A material post-closing discovery before the cuentas are approved may require reformulation (Cco art. 38.c; PGC NRV 23.ª).

**Tax side (LIS art. 11.3).** An expense booked in a later year than it accrued, or income booked in an earlier year, is taxed in the year it was booked, provided this does not result in lower tax. Expenses booked against reserves through NRV 22 are deductible (art. 11.3.a allows PyG or reserves). If the error changes a year whose IS return was filed, consider a *complementaria* or a rectification request for that year rather than relying on the current one.

Example: an unrecorded 2025 supplier invoice of 1,000 € (base) found in 2026 after the 2025 accounts were approved, IVA deductible now:

```
Debit  113   Reservas voluntarias                  1,000
Debit  472   Hacienda Pública, IVA soportado         210
Credit 400   Proveedores                          1,210
```

(The IVA is deducted in the period in which it is booked, within 4 years, LIVA art. 99.3; check with `spanish-vat`.) Restate the 2025 comparatives in the 2026 cuentas anuales and explain in the memoria.

## Software integrity and Verifactu

| Rule | Content | Source |
|---|---|---|
| General integrity duty | Accounting, invoicing and management software must guarantee integrity, conservation, accessibility, legibility, traceability and inalterability of records; no interpolations, omissions or alterations without a trace in the system | LGT art. 29.2.j |
| Sanctions on software | Producing or selling non-compliant software: 150,000 € per year and per product type; owning (*tenencia*) uncertified or altered software where certification is required: 50,000 € per year | LGT art. 201 bis |
| Verifactu (Reglamento de sistemas informáticos de facturación) | Applies to systems that issue invoices; IS taxpayers, IRPF taxpayers with economic activities, IRNR with PE, entities in attribution of income | RD 1007/2023 art. 3.1 |
| Exclusion | Taxpayers keeping IVA books through SII | RD 1007/2023 art. 3.3 |
| Dates (in force text) | Systems adapted before 1-01-2027 (IS taxpayers) and 1-07-2027 (rest) | RD 1007/2023 DF 4.ª, as amended by RDL 15/2025 (BOE 03-12-2025) |

A pure accounting program that does not issue invoices is not an invoicing system under RD 1007/2023, but it still falls under the general LGT art. 29.2.j duty. Verifactu does not apply in the foral territories (TicketBAI / Batuz). Detail: `spanish-e-invoicing`.

## Sanctions

| Breach | Sanction | Source |
|---|---|---|
| Inaccurate or omitted entries, accounts used with a wrong meaning | 1 % of the amounts affected, min 150 €, max 6,000 € | LGT art. 200.3 |
| Not keeping or not conserving the accounting, books, software or codes | 1 % of turnover of the year, min 600 € | LGT art. 200.3 |
| Two sets of books for the same activity and year | 600 € per year | LGT art. 200.3 |
| Books more than 4 months behind | 300 € | LGT art. 200.3 |
| Late SII submission | 0.5 % of each invoice, min 300 € per quarter, max 6,000 € | LGT art. 200.3 |
| Criminal *delito contable*: no accounts at all in estimación directa; double books; unrecorded or fictitious entries (the last two only if returns were omitted or reflect the false books and the amounts exceed 240,000 € per year) | Prison 5-7 months | Código Penal art. 310 |
| Not depositing the cuentas anuales | Cierre registral and ICAC fine | LSC arts. 282-283; see `spanish-financial-reporting` |
