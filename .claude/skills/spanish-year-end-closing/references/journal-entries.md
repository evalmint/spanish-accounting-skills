# Closing journal entries (PGC)

## Contents

- [Conventions](#conventions)
- [Accruals and deferrals](#accruals-and-deferrals)
- [Amortisation](#amortisation)
- [Impairment and bad debts](#impairment-and-bad-debts)
- [Provisions](#provisions)
- [Inventory variation](#inventory-variation)
- [Foreign currency](#foreign-currency)
- [Capital subsidies](#capital-subsidies)
- [Corporate income tax](#corporate-income-tax)
- [Regularización](#regularización)
- [Groups 8 and 9](#groups-8-and-9)
- [Asiento de cierre and apertura](#asiento-de-cierre-and-apertura)

## Conventions

Dated 31-12-2026 unless stated; amounts in euros and illustrative. IVA is ignored where the entry has none. Accounts are PGC 2007 (RD 1514/2007 as amended by RD 1/2021); a company may use longer subaccounts under the same code. The agent proposes, the user posts.

## Accruals and deferrals

**Insurance paid 1-10-2026 for 12 months, 1,200 €** (9 months belong to 2027):
```
Debit  480   Gastos anticipados                       900
Credit 625   Primas de seguros                         900
```
On 1-01-2027 reverse it (debit **625**, credit **480**).

**Annual licence fee invoiced in advance, 6,000 €, service 1-07-2026 to 30-06-2027:**
```
Debit  705   Prestaciones de servicios              3,000
Credit 485   Ingresos anticipados                    3,000
```

**December electricity, invoice arrives in January, 800 € + IVA:**
```
Debit  628   Suministros                              800
Credit 4009  Proveedores, facturas pendientes de recibir o de formalizar   800
```
The IVA is booked when the invoice is received (no deductible IVA without an invoice, LIVA art. 97).

**Work done for a customer, not invoiced, 5,000 €:**
```
Debit  4309  Clientes, facturas pendientes de formalizar   5,000
Credit 705   Prestaciones de servicios                5,000
```

**Bank loan interest accrued 1-12 to 31-12, 350 €:**
```
Debit  6623  Intereses de deudas con entidades de crédito   350
Credit 527   Intereses a corto plazo de deudas con entidades de crédito   350
```

**Interest receivable on a loan granted, 120 €:**
```
Debit  547   Intereses a corto plazo de créditos      120
Credit 762   Ingresos de créditos                      120
```

## Amortisation

**Computer equipment 3,000 €, 25 % straight-line:**
```
Debit  681   Amortización del inmovilizado material   750
Credit 2817  Amortización acumulada de equipos para procesos de información   750
```
**Software 2,400 €, 3 years:**
```
Debit  680   Amortización del inmovilizado intangible  800
Credit 2806  Amortización acumulada de aplicaciones informáticas   800
```

## Impairment and bad debts

**Customer 2,420 € (IVA incl.) six months overdue; reclassify and impair:**
```
Debit  436   Clientes de dudoso cobro                2,420
Credit 430   Clientes                                 2,420

Debit  694   Pérdidas por deterioro de créditos por operaciones comerciales   2,420
Credit 490   Deterioro de valor de créditos por operaciones comerciales   2,420
```
The IVA part can be recovered through a *modificación de base imponible* under LIVA art. 80 if its conditions are met (`spanish-vat`); then reduce the impairment accordingly.

**Debt later declared uncollectable:**
```
Debit  650   Pérdidas de créditos comerciales incobrables   2,420
Credit 436   Clientes de dudoso cobro                 2,420

Debit  490   Deterioro de valor de créditos por operaciones comerciales   2,420
Credit 794   Reversión del deterioro de créditos por operaciones comerciales   2,420
```

**Inventory write-down to net realisable value, 1,500 €:**
```
Debit  6931  Pérdidas por deterioro de mercaderías   1,500
Credit 390   Deterioro de valor de las mercaderías    1,500
```
Next year, reverse the prior impairment (debit **390**, credit **7931**) and book the new one.

## Provisions

**Lawsuit, probable payment 10,000 € within a year:**
```
Debit  678   Gastos excepcionales                   10,000
Credit 5292  Provisión a corto plazo para otras responsabilidades   10,000
```
(Use the expense account by nature where one fits better.) Excess on settlement: debit **5292**, credit **7952**.

**Warranty provision on sales, 3,000 €:**
```
Debit  6959  Dotación a la provisión para otras operaciones comerciales   3,000
Credit 4999  Provisión para otras operaciones comerciales   3,000
```

## Inventory variation

**Mercaderías: opening 20,000 €, closing 26,000 €:**
```
Debit  610   Variación de existencias de mercaderías   20,000
Credit 300   Mercaderías                            20,000

Debit  300   Mercaderías                            26,000
Credit 610   Variación de existencias de mercaderías   26,000
```
Net: **610** credit 6,000, which reduces the cost of sales.

**Finished goods: opening 8,000 €, closing 5,000 €:**
```
Debit  712   Variación de existencias de productos terminados   8,000
Credit 350   Productos terminados                     8,000

Debit  350   Productos terminados                     5,000
Credit 712   Variación de existencias de productos terminados   5,000
```

## Foreign currency

**Supplier invoice 10,000 USD booked at 0.90 (9,000 €); closing rate 0.93 (9,300 €):**
```
Debit  668   Diferencias negativas de cambio           300
Credit 400   Proveedores                               300
```
A gain would go to **768**.

## Capital subsidies

**Subsidy of 10,000 € received for a machine, tax rate 23 %** (during the year):
```
Debit  572   Bancos                                 10,000
Credit 940   Ingresos de subvenciones oficiales de capital   10,000

Debit  8301  Impuesto diferido                       2,300
Credit 479   Pasivos por diferencias temporarias imponibles   2,300
```
**Year-end transfer in line with 10 % amortisation of the machine:**
```
Debit  840   Transferencia de subvenciones oficiales de capital   1,000
Credit 746   Subvenciones, donaciones y legados de capital transferidos al resultado del ejercicio   1,000

Debit  479   Pasivos por diferencias temporarias imponibles   230
Credit 8301  Impuesto diferido                         230
```
Groups 8 and 9 are then closed against **130** (below). Measure the tax effect at the rate expected when it reverses (NRV 13.ª), which changes yearly to 2029 for ERD (`tax-accrual.md`).

## Corporate income tax

Full computation: `tax-accrual.md`. Shape of the entries:
```
Debit  6300  Impuesto corriente                     24,610
Credit 473   Hacienda Pública, retenciones y pagos a cuenta   15,000
Credit 4752  Hacienda Pública, acreedora por impuesto sobre sociedades   9,610

Debit  4740  Activos por diferencias temporarias deducibles   1,100
Credit 6301  Impuesto diferido                       1,100

Debit  6301  Impuesto diferido                       2,200
Credit 479   Pasivos por diferencias temporarias imponibles   2,200
```
If payments on account exceed the tax, the difference is a receivable in **4709**.

## Regularización

Every income and expense account (groups 6 and 7, including **6300** and **6301**) is closed against **129**:
```
Debit  70x/75x/76x/79x ...   (each income account, its balance)
Credit 129   Resultado del ejercicio

Debit  129   Resultado del ejercicio
Credit 60x/62x/63x/64x/68x/69x ...   (each expense account, its balance)
```
Variation accounts (**610**, **712**) are closed on whichever side their balance falls. Credit balance on **129** = profit; debit balance = loss.

## Groups 8 and 9

Using the subsidy example:
```
Debit  940   Ingresos de subvenciones oficiales de capital   10,000
Credit 130   Subvenciones oficiales de capital        10,000

Debit  130   Subvenciones oficiales de capital         3,070
Credit 8301  Impuesto diferido (net 2,300 - 230)       2,070
Credit 840   Transferencia de subvenciones oficiales de capital   1,000
```
Net balance of **130**: 6,930 = 9,000 not yet transferred less 2,070 deferred tax.

## Asiento de cierre and apertura

**Cierre (31-12-2026):** debit every balance-sheet account with a credit balance and credit every account with a debit balance, so that all accounts of groups 1-5 (including **129**, **4752**, **479**, **28**x) end at zero.

**Apertura (1-01-2027):** the exact reverse. Then reverse the deferrals that belong to the new year (**480**, **485**), and clear **4009** and **4309** when the invoices arrive or are issued.
