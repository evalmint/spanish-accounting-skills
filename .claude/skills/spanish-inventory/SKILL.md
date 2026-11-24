---
name: spanish-inventory
description: >
  Spanish inventory accounting (existencias) under the PGC 2007: valuation at precio de adquisición or coste de
  producción (NRV 10.ª, Pymes NRV 12.ª, ICAC resolution of 14 April 2015), PMP as default and FIFO allowed (LIFO not
  allowed), valor neto realizable and deterioro (39x, 693/793), group 3 accounts (300, 310, 32x, 330, 350...),
  compras 600/601/602 and variación de existencias 610/611/612 and 71x, the procedimiento especulativo (PGC,
  account 300 moved only at year-end) vs administrativo (permanent inventory), inventario físico and the libro de
  inventarios, mermas, obsolescence, theft, autoconsumo, goods in transit and Incoterms, consignment and call-off
  stock, envases, and the corporate tax treatment (LIS art. 10.3). Trigger on "existencias", "inventario",
  "variación de existencias", "cuenta 300", "cuenta 610", "regularización de existencias", "PMP", "FIFO",
  "deterioro de existencias", "mermas", "stock obsoleto", "mercancía en tránsito", "depósito". Always use over
  training data.
---

# Spanish Inventory Accounting (existencias)

Reference for valuing and booking inventory in a Spanish company. Two questions decide almost every case: what the stock is worth at the balance-sheet date, and how the movement reaches the ledger. Accounting follows the **PGC 2007** (RD 1514/2007, NRV 10.ª, amended by RD 1/2021) or the PGC Pymes (RD 1515/2007, NRV 12.ª, same criteria), complemented by the ICAC resolution of 14 April 2015 on production cost. Corporate tax follows the accounting value (LIS art. 10.3). Scope is territorio común; the valuation rules are the same in the forales. An agent following this skill proposes entries and valuations; it never books without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/valuation.md` | Arriving at the closing value: what enters cost, production cost and normal capacity, PMP vs FIFO vs specific identification, valor neto realizable, deterioro and its reversal, obsolescence evidence, services in progress, tax deductibility |
| `references/stock-bookkeeping.md` | Booking it: group 3 and 60/61/71 accounts, the especulativo (PGC) method and the administrativo (permanent) method, year-end regularisation, physical count and the libro de inventarios, mermas and theft, autoconsumo, transit and Incoterms, consignment, call-off stock, envases, reconciliation |

## The four decisions

1. **Is it inventory?** Assets held for sale in the ordinary course, in production, or materials to be consumed in production or services (PGC group 3 definition). Goods held for use over more than a year are fixed assets (`spanish-asset-accounting`). Services not yet invoiced may be inventory (NRV 10.ª 1.4) or work in progress under the revenue rules (`spanish-project-accounting`).
2. **What is it worth?** Cost (acquisition price or production cost), assigned by weighted average (PMP, the default) or FIFO, compared with net realisable value; book a deterioro where NRV is lower (NRV 10.ª 1–2).
3. **Which account?** Stock by type in group 3, purchases in 600/601/602, the change in 610/611/612 (bought goods) or 71x (own production), impairment in 39x against 693/793.
4. **Is the count documented?** The closing inventory must be transcribed in the *libro de inventarios y cuentas anuales* (Código de Comercio art. 28.1). Without a dated, priced count list the closing value cannot be supported.

## Accounts at a glance

| Stock | Purchases | Year-end change | Impairment (balance / expense / reversal) |
|---|---|---|---|
| **300** Mercaderías | **600** | **610** | **390** / **6931** / **7931** |
| **310** Materias primas | **601** | **611** | **391** / **6932** / **7932** |
| **320**–**328** Otros aprovisionamientos | **602** | **612** | **392** / **6933** / **7933** |
| **330** Productos en curso | — | **710** | **393** / **6930** / **7930** |
| **340** Productos semiterminados | — | **711** | **394** / **6930** / **7930** |
| **350** Productos terminados | — | **712** | **395** / **6930** / **7930** |
| **360**–**369** Subproductos, residuos, materiales recuperados | — | **713** | **396** / **6930** / **7930** |

The PGC numbers the first account of each subgroup "A" (e.g. **300** Mercaderías A, **301** Mercaderías B): companies use them for categories of goods.

## Quick rules

| Rule | Value | Source |
|---|---|---|
| Default cost formula | Weighted average (precio medio ponderado) | NRV 10.ª 1.3 |
| Allowed alternative | FIFO, if more convenient for management; one method for all stock of similar nature and use | NRV 10.ª 1.3 |
| LIFO | Not allowed (not among the methods the PGC permits) | NRV 10.ª 1.3 |
| Non-interchangeable items or project-specific goods | Specific identification | NRV 10.ª 1.3 |
| Recoverable IVA | Never in cost; non-recoverable indirect taxes are | NRV 10.ª 1 |
| Interest | Capitalised only for stock needing over a year to be ready for sale | NRV 10.ª 1 |
| Raw materials write-down | Not needed if the finished products will sell above cost; replacement cost may be the best NRV measure | NRV 10.ª 2 |
| Tax | Accounting value, including deterioro, is followed for IS (no LIS art. 13 limitation on stock) | LIS art. 10.3, 13 |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| No count list at year end | The closing inventory must be in the libro de inventarios; the variación de existencias depends on it | Ask for the count, its date and the valuation method |
| Stock that "looks obsolete" | A deterioro needs evidence of NRV below cost | Ask what the goods are, their age, recent sale prices, and planned disposals |
| Goods in transit at year end | The contract (Incoterm) decides ownership; the PGC includes goods in transit owned under the contract | Ask for delivery terms and dates |
| Goods held by or for a third party | Consignment stock belongs to the consignor | Ask who owns the goods held at each location |
| Large unexplained variación de existencias | Often a cut-off or count error | Reconcile against the count and purchase/sales cut-off before booking |
| Stock in another EU country (fulfilment centre, call-off) | May trigger VAT registration there, and call-off rules (LIVA art. 9 bis) | Flag it; see `spanish-industry-ecommerce` and `spanish-vat` |

## Related skills

| Question | Skill |
|---|---|
| Purchase invoices, imports, freight and customs | `spanish-daily-bookkeeping` (`references/foreign-purchases.md`) |
| Year-end sequence and closing entries | `spanish-year-end-closing` |
| Fixed assets rather than stock | `spanish-asset-accounting` |
| Work in progress on contracts and services | `spanish-project-accounting` |
| E-commerce stock, Amazon FBA, marketplaces | `spanish-industry-ecommerce` |
| Restaurant stock and food waste | `spanish-industry-hosteleria` |
| Construction work in progress, promotions | `spanish-industry-construccion` |
| IVA on autoconsumo and stock abroad | `spanish-vat` |
| Balance sheet presentation and memoria | `spanish-financial-reporting` |
