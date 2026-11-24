# Bookkeeping entries for travel (PGC 2007)

Accounts and worked entries. Amounts follow `tax-rules.md`; IVA follows `vat-on-travel.md`. IRPF in the examples at 15 % for simplicity; use the employee's tipo. An agent proposes entries; it never posts them without the user's approval.

## Contents

1. Accounts
2. A: Expense report reimbursed outside the nómina
3. B: Dietas within limits paid with the nómina
4. C: Dietas above limits
5. D: Kilometraje
6. E: Travel advance (anticipo a justificar)
7. F: Company card
8. G: Hotel abroad and foreign currency
9. H: Client meal on a trip
10. I: Travel-agency invoice
11. J: Autónomo's own trip
12. Reporting

## 1. Accounts

| Account | Use |
|---|---|
| **629** Otros servicios | Staff travel: hotels, tickets, taxis, exempt dietas and kilometraje (PGC description of 629 includes *gastos de viaje del personal*). Use a company-specific subaccount for travel if needed |
| **640** Sueldos y salarios | Taxable excess of dietas, flat allowances to administradores |
| **642** Seguridad Social a cargo de la empresa | Employer cotización on the taxable excess |
| **627** Publicidad, propaganda y relaciones públicas | Atenciones a clientes (client meals, gifts) |
| **621** Arrendamientos y cánones | Hire car (alternatively **629** for short trip rentals; keep one policy) |
| **628** Suministros | Fuel, if not booked with travel on **629** |
| **472** Hacienda Pública, IVA soportado | Deductible Spanish IVA |
| **4709** Hacienda Pública, deudora por devolución de impuestos | Foreign VAT claimed via modelo 360 |
| **4751** Hacienda Pública, acreedora por retenciones practicadas | IRPF on the taxable excess |
| **476** Organismos de la Seguridad Social, acreedores | Cotización on the excess |
| **465** Remuneraciones pendientes de pago | Amounts owed to the employee (with or outside the nómina) |
| **544** Créditos a corto plazo al personal | Travel advances to justify |
| **5201** Deudas a corto plazo por crédito dispuesto | Credit card balance, if settled monthly by the bank |
| **555** Partidas pendientes de aplicación | Card charges awaiting receipts |
| **551** Cuenta corriente con socios y administradores | Expenses of administradores pending settlement |
| **668** / **768** | Exchange differences |
| **572** | Bank |

## 2. A: Expense report reimbursed outside the nómina

Employee paid a Madrid hotel (220 € incl. 20 € IVA, full invoice to the company) and a train ticket (55 € incl. 5 € IVA, in the company's name).

| Account | Debit | Credit |
|---|---|---|
| **629** | 250,00 | |
| **472** | 25,00 | |
| **465** | | 275,00 |

Payment: **465** / **572** 275,00. Hotel and ticket costs reimbursed at cost with invoices are not employee income and are not reported in modelo 190.

## 3. B: Dietas within limits paid with the nómina

Three days in Barcelona with two overnight stays: 2 × 53,34 + 26,67 = 133,35 € paid as manutención.

| Account | Debit | Credit |
|---|---|---|
| **629** | 133,35 | |
| **465** | | 133,35 |

No IRPF, no cotización, no IVA. Report in modelo 190 as exempt dietas (clave L) and include in the CRA file for the TGSS (LGSS art. 147.3).

## 4. C: Dietas above limits

Same trip, company pays 60 €/day: 180 €. Exempt 133,35 €; excess 46,65 € is salary.

| Account | Debit | Credit |
|---|---|---|
| **629** (exempt part) | 133,35 | |
| **640** (excess) | 46,65 | |
| **642** (employer cotización on 46,65 at the company's rate, e.g. 32,15 %) | 15,00 | |
| **4751** (IRPF 15 % on 46,65) | | 7,00 |
| **476** (employer 15,00 + employee 6,50 % = 3,03) | | 18,03 |
| **465** | | 169,97 |

Cotización is computed by TGSS in the month's liquidation; use its figures.

## 5. D: Kilometraje

Own car, 420 km, tolls 18,40 € with receipt, paid at 0,26 €/km = 109,20 €.

| Account | Debit | Credit |
|---|---|---|
| **629** | 127,60 | |
| **465** | | 127,60 |

If the company pays 0,30 €/km, the excess 0,04 × 420 = 16,80 € goes to **640** with IRPF and cotización.

## 6. E: Travel advance

| Event | Debit | Credit |
|---|---|---|
| Advance of 500 € | **544** 500,00 | **572** |
| Expense report 430 € (costs and exempt dietas) | **629** / **472** 430,00 | **544** 430,00 |
| Employee returns 70 € | **572** 70,00 | **544** 70,00 |

An unjustified advance not returned becomes salary: move it to **640** through the nómina.

## 7. F: Company card

Debit card: book each charge against **572** when the receipt is matched. Credit card settled monthly:

| Event | Debit | Credit |
|---|---|---|
| Card statement, receipts matched | **629** / **472** / **627** | **5201** |
| Charges without receipt yet | **555** | **5201** |
| Monthly settlement | **5201** | **572** |
| Private charge by the employee | **544** (to recover) or **640** through the nómina | **555** |

Clear **555** each month; an old balance usually hides private or undocumented spending.

## 8. G: Hotel abroad and foreign currency

Hotel in Germany, 350 EUR incl. 22,90 EUR German VAT (7 %), paid with the company card. Modelo 360 claim intended.

| Account | Debit | Credit |
|---|---|---|
| **629** | 327,10 | |
| **4709** | 22,90 | |
| **5201** | | 350,00 |

If the claim is refused or not filed, move **4709** to **629**. In a non-euro currency, translate at the exchange rate of the transaction date (PGC NRV 11ª) and book the card settlement difference to **668** / **768**.

## 9. H: Client meal on a trip

Dinner with a client, 110 € incl. 10 € IVA, invoice with company NIF.

| Account | Debit | Credit |
|---|---|---|
| **627** | 110,00 | |
| **5201** / **572** | | 110,00 |

IVA is not deductible (LIVA art. 96.Uno.5º); book gross. Track **627** atenciones against the 1 % of turnover IS limit (LIS art. 15.e). The employee's manutención allowance for that day should be reduced if the meal replaced it (policy).

## 10. I: Travel-agency invoice

Under REAV (no IVA shown): debit **629** with the total. Under the general regime (art. 147, IVA shown per component): split **629** and **472**.

## 11. J: Autónomo's own trip

Autónomo (estimación directa) pays lunch 24,20 € (2,20 € IVA, simplified invoice with NIF) by card, day trip to another municipality; hotel 120 € + 12 € IVA.

| Account | Debit | Credit |
|---|---|---|
| **629** | 142,00 | |
| **472** | 14,20 | |
| **572** | | 156,20 |

Manutención deductible for IRPF up to 26,67 €/day without overnight stay (here 22,00 € net: fully deductible). IVA on the meal is deductible because the cost is IRPF-deductible (LIVA art. 96.Uno.6º). Paid in cash: not deductible for IRPF, and then its IVA is not deductible either. Record in the libro registro de gastos (`spanish-autonomo-tax`).

## 12. Reporting

- Modelo 190: exempt dietas and kilometraje paid to employees (clave L, subclave per the instructions); taxable excess under clave A with the salary.
- Modelo 111: IRPF on the excess in the period paid.
- TGSS: all concepts, including exempt dietas, in the CRA file; the excess in the cotización base.
- Modelo 303: deductible Spanish IVA on **472**; foreign VAT never.
