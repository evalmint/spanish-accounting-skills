# Existencias: Valuation

How to arrive at the closing value of inventory: cost, cost formula, net realisable value and impairment. Core rules: PGC 2007 NRV 10.ª (PGC Pymes NRV 12.ª has the same criteria), Resolución del ICAC de 14 de abril de 2015 on the criteria for determining production cost, LIS art. 10.3 for tax. Accounts are **PGC 2007**.

## Contents

- [1. Decision table](#1-decision-table)
- [2. Acquisition price](#2-acquisition-price)
- [3. Production cost](#3-production-cost)
- [4. Cost formulas: PMP, FIFO, specific identification](#4-cost-formulas-pmp-fifo-specific-identification)
- [5. Net realisable value and deterioro](#5-net-realisable-value-and-deterioro)
- [6. Obsolescence: the evidence](#6-obsolescence-the-evidence)
- [7. Inventory of services](#7-inventory-of-services)
- [8. Commodity traders](#8-commodity-traders)
- [9. Corporate tax](#9-corporate-tax)
- [10. Worked examples](#10-worked-examples)
- [11. Ask the user](#11-ask-the-user)
- [12. Sources](#12-sources)

## 1. Decision table

| Question | Answer | Source |
|---|---|---|
| Initial measurement | Cost: acquisition price (bought) or production cost (made) | NRV 10.ª 1 |
| Assigning cost to interchangeable items | Weighted average by default; FIFO allowed | NRV 10.ª 1.3 |
| After initial measurement | If NRV < cost, book an impairment as an expense; reverse it when the causes disappear | NRV 10.ª 2 |
| Raw materials | No write-down if the finished goods they go into will sell at or above cost | NRV 10.ª 2 |
| Goods under a firm sale contract | No write-down if the contract price covers cost plus costs to complete | NRV 10.ª 2 |
| Advances to suppliers of stock | At cost (**407**) | NRV 10.ª 1 |

## 2. Acquisition price

The amount invoiced by the seller after discounts, rebates and similar, plus all additional costs until the goods are located for sale: transport, customs duties, insurance and other costs directly attributable to the acquisition (NRV 10.ª 1.1).

| Item | In cost? | How it is booked in practice |
|---|---|---|
| Supplier price | Yes | **600**/**601**/**602** |
| Discounts on the invoice | Deducted | Book net |
| Prompt-payment discounts after the invoice | Deducted from cost conceptually | **606** (presented reducing purchases) |
| Volume rebates | Deducted | **609** |
| Returns | Deducted | **608** |
| Inbound freight, customs duties, transport insurance | Yes | Include in **600** (or a 600 subaccount); **624** only for freight not attributable to purchases |
| Recoverable IVA | No | **472** |
| Non-recoverable IVA (prorrata, recargo de equivalencia paid by a retailer) | Yes | Include in **600** |
| Storage after the goods are located for sale, selling costs | No | Expense |
| Interest included in the nominal of short-term payables without contractual rate | May be included if discounting is immaterial | NRV 10.ª 1.1 |
| Interest on financing | Only if the stock needs over a year to be ready for sale | NRV 10.ª 1 |
| Foreign-currency purchases | Converted at the spot rate on the transaction date; later exchange differences on the payable go to **668**/**768**, not to stock | NRV 11.ª |

Under the especulativo method, purchases sit in **600**–**609** during the year and the year-end stock value is determined from the count priced at cost. Make sure the priced count uses the same cost elements as the purchase accounts (e.g. freight included).

## 3. Production cost

Production cost = acquisition price of raw materials and consumables + directly attributable costs + a reasonable share of indirectly attributable costs, to the extent they relate to the production period and are based on the normal capacity of the production means (NRV 10.ª 1.2). The ICAC resolution of 14 April 2015 develops the criteria.

| In production cost | Not in production cost |
|---|---|
| Direct materials, direct labour | Abnormal waste of materials, labour or other costs |
| Variable indirect production costs (energy, consumables) on actual production | Administrative overheads not related to production |
| Fixed indirect production costs (factory depreciation, supervisors) allocated on normal capacity | Selling costs |
| | Storage costs, unless necessary in the production process |
| | Under-absorbed fixed costs from low production (expensed in the period) |

Normal capacity is the production expected over several periods under normal circumstances. With low production, do not increase the cost per unit: the unabsorbed fixed overhead is an expense.

Own production is not booked through purchases: the year-end value of **330**, **340**, **350** and **36x** is brought in through **71x** (`stock-bookkeeping.md`).

## 4. Cost formulas: PMP, FIFO, specific identification

| Formula | When | Note |
|---|---|---|
| Precio medio ponderado (PMP, weighted average) | General method (NRV 10.ª 1.3) | Periodic average (per year or month) or moving average after each purchase |
| FIFO | Allowed when the company considers it more convenient for management | Common in perishable or dated goods |
| Specific identification | Non-interchangeable goods, or goods produced and segregated for a specific project | Cars, real estate, made-to-order |
| LIFO | Not permitted | It is not among the methods in NRV 10.ª 1.3 (removed when the PGC 1990 was replaced) |
| Standard cost, retail method | Not mentioned in NRV 10.ª; usable only as an approximation if the result does not differ materially from cost (unverified as ICAC doctrine) | |

Use one method for all inventory of similar nature and use. Changing method is a change in accounting policy (NRV 22.ª): retrospective, with disclosure.

**Moving average example (mercaderías):**

| Date | Movement | Units | Unit cost | Value | Average after |
|---|---|---|---|---|---|
| 1 Jan | Opening | 100 | 10.00 | 1,000.00 | 10.00 |
| 10 Feb | Purchase | 200 | 11.50 | 2,300.00 | (1,000 + 2,300) / 300 = 11.00 |
| 15 Mar | Sale | −150 | 11.00 | −1,650.00 | 11.00 |
| 20 Apr | Purchase | 50 | 12.40 | 620.00 | (1,650 + 620) / 200 = 11.35 |

## 5. Net realisable value and deterioro

Net realisable value (valor neto realizable): estimated selling price in the ordinary course minus estimated costs to complete and to sell (PGC part 1, Marco Conceptual, 6.º; NRV 10.ª 2). For raw materials, replacement cost may be the best available measure.

| Step | Entry | Source |
|---|---|---|
| Year end: reverse last year's impairment | **39x** / **793x** (e.g. **390** / **7931**) | PGC part 5, subgroup 39 |
| Year end: book this year's estimate | **693x** / **39x** (e.g. **6931** / **390**) | Same |
| Presentation | **39x** reduces the stock line in the balance sheet | Same |

The PGC's movement for subgroup 39 replaces the full allowance each year (reverse the old, book the new) rather than adjusting the difference; the net P&L effect is the same.

Assess item by item, or by groups of similar items when they relate to the same product line and cannot be evaluated separately. Do not write down a whole category with a flat percentage without support.

## 6. Obsolescence: the evidence

The auditor and the AEAT will ask for evidence. Useful evidence:

| Evidence | Supports |
|---|---|
| Sales after the balance sheet date at prices below cost | NRV below cost |
| Ageing report: no movement in 12/24 months | Slow-moving, combined with price evidence |
| Expiry dates, product withdrawals, model changes | Obsolescence |
| Price lists, discount campaigns, offers from outlet buyers | Selling price estimate |
| Damage reports, quality control | Physical deterioration |
| Destruction certificate (waste manager) | Actual loss: derecognise, not impair |

Goods physically destroyed or discarded are not impaired: they leave the inventory (count) and the loss is in the variación de existencias, or in **678** for exceptional losses if the company reclassifies them (`stock-bookkeeping.md`).

## 7. Inventory of services

The same cost rules apply to services: inventory includes the production cost of services until the revenue is recognised under the revenue rules (NRV 10.ª 1.4). Most service businesses recognise revenue over time as they perform and hold no service inventory; where they do (a fixed-price project not yet meeting the revenue criteria), see `spanish-project-accounting`.

## 8. Commodity traders

Intermediaries trading listed commodities may value inventory at fair value less costs to sell, with changes in profit and loss, when this removes or significantly reduces an accounting mismatch (NRV 10.ª 3, added by RD 1/2021 for years from 1 January 2021). Rare in small companies.

## 9. Corporate tax

| Point | Rule | Source |
|---|---|---|
| Base | The accounting result under the Código de Comercio and the PGC, corrected only by LIS rules | LIS art. 10.3 |
| Cost formula | The accounting formula (PMP or FIFO) applies for tax | LIS art. 10.3 |
| Deterioro of stock | Deductible: LIS art. 13 restricts impairment of receivables, fixed assets and financial instruments, not of inventory. The usual tests of LIS art. 11 (accrual, booking) and proof apply | LIS art. 10.3, 11, 13 |
| Reversal | Taxable when it was deductible | LIS art. 11.6 |
| Autónomos | Same, through LIRPF art. 28 (estimación directa) | LIRPF |

There is no tax-specific inventory reserve or flat-rate write-down in territorio común.

## 10. Worked examples

**A. Deterioro of goods for resale.** Closing count at cost: 80,000 €. Line of discontinued products at cost 12,000 € sells after year end at 7,000 € with selling costs of 500 € → NRV 6,500 €. Prior-year allowance: 2,000 €.

| Cuenta | Debe | Haber |
|---|---|---|
| **390** Deterioro de valor de las mercaderías | 2,000.00 | |
| **7931** Reversión del deterioro de mercaderías | | 2,000.00 |
| **6931** Pérdidas por deterioro de mercaderías | 5,500.00 | |
| **390** Deterioro de valor de las mercaderías | | 5,500.00 |

Balance sheet: mercaderías 80,000 − 5,500 = 74,500.

**B. Production cost with low activity.** Normal capacity 10,000 units; fixed production overhead 50,000 € → 5 €/unit. Actual production 7,000 units: allocate 35,000 € to production; 15,000 € remains an expense of the year. Per-unit cost = materials + direct labour + variable overhead + 5 €.

## 11. Ask the user

- Which cost formula does the company use (PMP or FIFO), and since when?
- Does the priced count include inbound freight and duties?
- For own production: normal capacity, actual output, overhead pools.
- Which items are slow-moving or discontinued, and what are their post-year-end selling prices?
- Firm sale contracts covering stock at year end?
- Any goods destroyed, and is there a certificate?

## 12. Sources

RD 1514/2007 (PGC), part 1 Marco Conceptual and part 2 NRV 10.ª, 11.ª, 22.ª, part 5 subgroup 39, consolidated BOE text with RD 1/2021; RD 1515/2007 (PGC Pymes) NRV 12.ª; Resolución de 14 de abril de 2015, del ICAC, por la que se establecen criterios para la determinación del coste de producción; Ley 27/2014 (LIS) art. 10, 11, 13.
