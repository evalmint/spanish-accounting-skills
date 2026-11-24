# Booking Inventory in Practice

How goods get into the books, out of them, and onto the balance sheet at year end. Accounts and their movements are from the **PGC 2007** part 4 and part 5 (BOE consolidated text). Import VAT and intra-EU acquisitions are not repeated here: see `spanish-daily-bookkeeping`, `references/foreign-purchases.md`.

## Contents

- [1. Two methods: especulativo and administrativo](#1-two-methods-especulativo-and-administrativo)
- [2. Especulativo (the PGC's method): worked entries](#2-especulativo-the-pgcs-method-worked-entries)
- [3. Administrativo (permanent inventory): worked entries](#3-administrativo-permanent-inventory-worked-entries)
- [4. Own production: 71x](#4-own-production-71x)
- [5. Physical count and the libro de inventarios](#5-physical-count-and-the-libro-de-inventarios)
- [6. Mermas, theft, destruction](#6-mermas-theft-destruction)
- [7. Autoconsumo and gifts from stock](#7-autoconsumo-and-gifts-from-stock)
- [8. Goods in transit and cut-off](#8-goods-in-transit-and-cut-off)
- [9. Consignment, deposit and call-off stock](#9-consignment-deposit-and-call-off-stock)
- [10. Returnable packaging](#10-returnable-packaging)
- [11. Reconciliation checklist](#11-reconciliation-checklist)
- [12. Ask the user](#12-ask-the-user)

## 1. Two methods: especulativo and administrativo

| | **Especulativo** (periodic) | **Administrativo** (permanent inventory) |
|---|---|---|
| During the year | Purchases to **600**–**602**; stock accounts (**300**, **310**, **32x**) untouched | Purchases to the stock account; each sale also books the cost of goods sold out of stock |
| Year end | Opening stock out (**610** / **300**), closing stock in (**300** / **610**) from the count | Stock account already shows the book quantity; adjust to the count, the difference is a shrinkage loss |
| Cost of goods sold | Derived: purchases ± variación de existencias | Booked transaction by transaction |
| P&L presentation | *Aprovisionamientos*: purchases and variación (600 ± 610) | Must still present *consumo de mercaderías* and the variation in the official P&L model |
| PGC | This is the movement described in part 5: accounts 300/309 "solamente funcionarán con motivo del cierre del ejercicio" | Part 5 is not binding (RD 1514/2007 art. 2), so a perpetual system is allowed if the annual accounts follow the official models |

**Recommendation for a small company:** especulativo. It is what the PGC describes, what most Spanish software does by default, and the legal duty to count at year end is the same either way. Use administrativo (with a warehouse system) when management needs a reliable monthly gross margin. Neither method removes the year-end count.

## 2. Especulativo (the PGC's method): worked entries

**Purchase** of goods for resale, 10,000 € + 21 % IVA:

| Cuenta | Debe | Haber |
|---|---|---|
| **600** Compras de mercaderías | 10,000.00 | |
| **472** Hacienda Pública, IVA soportado | 2,100.00 | |
| **400** Proveedores | | 12,100.00 |

**Sale**, 16,000 € + 21 % IVA:

| Cuenta | Debe | Haber |
|---|---|---|
| **430** Clientes | 19,360.00 | |
| **700** Ventas de mercaderías | | 16,000.00 |
| **477** Hacienda Pública, IVA repercutido | | 3,360.00 |

**Year end**, opening stock 15,000 €, counted closing stock 18,000 €:

| Cuenta | Debe | Haber |
|---|---|---|
| **610** Variación de existencias de mercaderías | 15,000.00 | |
| **300** Mercaderías | | 15,000.00 |
| **300** Mercaderías | 18,000.00 | |
| **610** Variación de existencias de mercaderías | | 18,000.00 |

Net effect: **610** has a credit balance of 3,000, reducing the cost of goods for the year; it closes to **129** with the other P&L accounts. Sign rule: an increase in stock credits **610** (less cost); a decrease debits it.

The same pattern applies to raw materials (**310**/**611**) and other supplies (**32x**/**612**). Accounts 300–309 can separate categories (Mercaderías A, B...).

Monthly accounts under especulativo: either count monthly, or estimate closing stock with the gross margin method and reverse it the next month; label estimates clearly.

## 3. Administrativo (permanent inventory): worked entries

**Purchase:** **300** 10,000 + **472** 2,100 / **400** 12,100 (many companies keep the purchase in **600** and transfer to **300** in the same entry, to keep purchase statistics: **600** / **400**, then **300** / **610**).

**Cost of each sale** (e.g. 9,600 € at PMP): **610** / **300** 9,600, or with a dedicated cost-of-sales subaccount mapped to *aprovisionamientos* in the P&L.

**Year end:** compare the book stock with the count. Shrinkage of 400 €: **610** / **300** 400 (normal shrinkage), or **678** / **300** for exceptional losses (§6).

Whatever the internal flow, the published P&L must show *Aprovisionamientos* (consumption = purchases ± variation) per the official model. Check that the mapping produces it.

## 4. Own production: 71x

Accounts 71x record the variation of own-produced stock. Movement (PGC part 5, subgroup 71): debited with opening stock and credited with closing stock, against **330**, **340**, **350** and **36x**; the balance closes to **129**.

| Cuenta | Debe | Haber |
|---|---|---|
| **712** Variación de existencias de productos terminados (opening) | 40,000.00 | |
| **350** Productos terminados | | 40,000.00 |
| **350** Productos terminados (closing, at production cost) | 52,000.00 | |
| **712** Variación de existencias de productos terminados | | 52,000.00 |

71x accounts are in group 7 and appear in the P&L as *Variación de existencias de productos terminados y en curso de fabricación*, separate from aprovisionamientos.

## 5. Physical count and the libro de inventarios

| Duty | Content | Source |
|---|---|---|
| Libro de inventarios y cuentas anuales | Opens with the detailed opening balance; trial balances at least quarterly; the closing inventory of each year and the annual accounts are transcribed | Código de Comercio art. 28.1 |
| Legalisation | The books are legalised electronically at the Registro Mercantil within four months of year end | Ley 14/2013 art. 18; see `spanish-accounting-compliance` |
| Conservation | Six years from the last entry | Código de Comercio art. 30 |

The law does not prescribe a counting procedure. Practice that holds up in an audit or tax inspection:

- Count at or close to the balance-sheet date; roll forward or back documented movements if not on the date.
- Count list per location with item code, description, unit, quantity, unit cost, total, condition (damaged, obsolete), counter and checker signatures and date.
- Freeze movements during the count, or record them precisely (cut-off documents: last delivery note in and out).
- Include goods owned but held elsewhere (in transit, at consignees, at a 3PL warehouse); exclude third-party goods held by the company.
- Reconcile count to book stock (administrativo) or to purchases and sales (especulativo), investigate differences above a threshold.

## 6. Mermas, theft, destruction

| Case | Accounting | IVA | IS |
|---|---|---|---|
| Normal shrinkage (evaporation, breakage within normal ranges) | Included in the variación de existencias: lower closing count | No adjustment | Deductible as part of cost of goods |
| Abnormal production waste | Not part of production cost (NRV 10.ª 1.2 and ICAC resolution 14 April 2015); expense of the period | No adjustment | Deductible |
| Theft, fire, flood (exceptional) | In especulativo the lower count already reflects it; optionally reclassify to **678** Gastos excepcionales against **610** to show it apart. Insurance compensation: **778** | Theft or destruction duly proven is not an autoconsumo, so the deducted IVA is not reversed (unverified as consolidated DGT doctrine: check before relying on it) | Deductible if proven (police report, insurance claim, destruction certificate) |
| Deliberate destruction of unsaleable goods | Leaves stock; keep a waste manager's certificate | No autoconsumo if destroyed (same caveat) | Deductible with evidence |
| Expired goods donated to an NGO | Leaves stock; cost to **678** or **659** | Delivery free of charge may be an autoconsumo (LIVA art. 9.1.º.b); food donations to NGOs have had specific base rules (see `spanish-vat`) | Not deductible as a liberality (LIS art. 15.e), possible Ley 49/2002 deduction |

## 7. Autoconsumo and gifts from stock

| Case | Entry | IVA |
|---|---|---|
| Autónomo takes goods for private use | **550** / **600** (reduce purchases at cost) or **700**, per company practice | Autoconsumo subject to IVA (LIVA art. 9.1.º.a); base = acquisition cost or similar goods' cost at that time (LIVA art. 79.Tres): **477** |
| Company gives goods to clients as gifts | **627** / **600** at cost (or leave in purchases and let the count reflect it) | Autoconsumo (art. 9.1.º.b) unless free samples or advertising objects within art. 7.2.º and 7.4.º limits (200 € per recipient and year) |
| Goods used as fixed assets or for the business itself (e.g. a computer from stock used in the office) | **217** / **731** (own work capitalised) or reduce **600** | Possible autoconsumo only if used in a non-deductible activity |
| Goods given to employees | Salary in kind (`spanish-payroll`) | Autoconsumo |

## 8. Goods in transit and cut-off

PGC part 5, subgroup 30: goods in transit owned by the company under the contract are included in closing stock; the same applies to all group 3 subgroups. Ownership follows the contract terms; Incoterms indicate where risk passes and are the usual evidence:

| Incoterm (2020) | Typical ownership/risk transfer | Buyer includes in stock at year end if shipped but not arrived? |
|---|---|---|
| EXW, FCA, FAS, FOB | At or near the seller's premises or port of shipment | Yes |
| CFR, CIF, CPT, CIP | Risk passes at shipment, although seller pays freight | Usually yes (risk passed) |
| DAP, DPU, DDP | At destination | No |

Ownership in Spanish law can also depend on the contract (reservation of title, *reserva de dominio*); when the contract says otherwise, it prevails. Purchase cut-off: goods received before year end without invoice go to **600** / **4009** Proveedores, facturas pendientes de recibir o de formalizar, and are counted. Sales cut-off: goods shipped and transferred before year end are sales (and out of stock) even if invoiced later (**4309**).

## 9. Consignment, deposit and call-off stock

| Arrangement | Whose stock | Booking |
|---|---|---|
| Company sends goods to a consignee (distributor sells for the company) | The company's until the consignee sells | Keep in **300**; record sale when the consignee sells; consignee's commission to **623** |
| Company holds a supplier's goods on consignment | The supplier's | Not in the count; purchase only when taken or sold |
| Goods at a third-party warehouse (3PL, Amazon FBA) | The company's | Include in the count with the provider's stock report |
| Call-off stock: goods sent to a known customer in another EU state who takes them later | Seller's until taken | Keep in stock; the intra-EU supply happens when the customer takes the goods, if the conditions of LIVA art. 9 bis are met (customer identified, registers kept, taken within 12 months, reported in modelo 349) |

Stock in another EU state outside call-off conditions can create a VAT registration duty there: see `spanish-industry-ecommerce`.

## 10. Returnable packaging

| Account | Use |
|---|---|
| **326** Embalajes, **327** Envases | Own packaging held as stock |
| **406** Envases y embalajes a devolver a proveedores | Deposits charged by suppliers for returnable packaging (reduces the supplier debt when returned) |
| **437** Envases y embalajes a devolver por clientes | Deposits charged to customers for returnable packaging |
| **219** Otro inmovilizado material | Returnable packaging used over more than a year (pallets, kegs) |

## 11. Reconciliation checklist

1. The closing stock booked equals the priced count list, signed and dated.
2. The count uses the declared cost formula (PMP or FIFO) and includes freight and duties.
3. Goods in transit, at third parties and on consignment are treated by ownership.
4. Purchases and sales cut-off: delivery notes around the year end match **4009**/**4309**.
5. Deterioro: allowance reversed and re-estimated with evidence.
6. Gross margin compared with the prior year and with budget; explain large swings.
7. The opening stock in the new year equals last year's closing stock (**300** balance after closing).
8. The closing inventory is transcribed in the libro de inventarios y cuentas anuales.

## 12. Ask the user

- Especulativo or administrativo? Which software and how is the stock module mapped to the PGC?
- Date of the count and who performed it; count lists available?
- Goods in transit at year end and their Incoterms.
- Goods held at third parties or for third parties.
- Theft, damage or destruction during the year, with evidence.
- Goods taken by the owner, given to customers or employees.
