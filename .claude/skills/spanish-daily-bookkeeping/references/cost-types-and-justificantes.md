# Everyday Entries, Cost Types and Justificantes

How to book the ordinary run of purchases, sales, professional fees, rent and payroll lines, and which document each needs. Accounts are **PGC 2007** (RD 1514/2007 as amended by RD 1/2021), checked against the BOE consolidated text. Territorio común; for IGIC (Canarias) and IPSI (Ceuta/Melilla) the account logic is the same but the tax accounts and rates differ.

Notation: entries are shown as `Debe / Haber`. Amounts are illustrative.

## Contents

- [1. Purchases: 60 or 62?](#1-purchases-60-or-62)
- [2. Proveedores 400 vs acreedores 410](#2-proveedores-400-vs-acreedores-410)
- [3. Sales and customers](#3-sales-and-customers)
- [4. IRPF retentions you must withhold](#4-irpf-retentions-you-must-withhold)
- [5. Payroll lines in the daily flow](#5-payroll-lines-in-the-daily-flow)
- [6. Justificantes: factura completa, simplificada, nothing](#6-justificantes-factura-completa-simplificada-nothing)
- [7. Atenciones a clientes, gastos de representación, gifts](#7-atenciones-a-clientes-gastos-de-representación-gifts)
- [8. Vehicles](#8-vehicles)
- [9. Suplidos](#9-suplidos)
- [10. Anticipos](#10-anticipos)
- [11. Discounts, returns, rappels](#11-discounts-returns-rappels)
- [12. Bad debts](#12-bad-debts)
- [13. Cash](#13-cash)
- [14. Quick lookup](#14-quick-lookup)
- [15. Ask the user](#15-ask-the-user)

## 1. Purchases: 60 or 62?

Subgroup 60 *Compras* is for goods that enter the production or sales cycle; subgroup 62 *Servicios exteriores* is for services and supplies consumed by the business.

| What was bought | Account | Note |
|---|---|---|
| Goods for resale | **600** Compras de mercaderías | Stock adjusted at year-end through **610** (`spanish-inventory`) |
| Raw materials | **601** Compras de materias primas | Variation through **611** |
| Packaging, fuel stocks, spare parts, office supplies held as stock | **602** Compras de otros aprovisionamientos | Variation through **612**; small office material is usually booked here or in **629** without stock count |
| Subcontracted work that is part of production | **607** Trabajos realizados por otras empresas | E.g. a printer finishing your product |
| Rent of premises, equipment, software licences (cánones) | **621** Arrendamientos y cánones | Renting and operating leases too |
| Repairs and maintenance | **622** Reparaciones y conservación | Improvements that extend life are assets (NRV 3.ª) |
| Lawyers, gestoría, auditors, consultants, notaries | **623** Servicios de profesionales independientes | Check retention (§4) |
| Transport paid to third parties | **624** Transportes | Freight on purchases goes into **600** (NRV 10.ª 1.1) |
| Insurance premiums (not social) | **625** Primas de seguros | Exempt from IVA (LIVA art. 20.Uno.16.º); IPS tax is part of the cost |
| Bank fees, TPV commissions | **626** Servicios bancarios y similares | Exempt (art. 20.Uno.18.º) |
| Advertising, sponsorship, public relations, atenciones a clientes | **627** Publicidad, propaganda y relaciones públicas | Atenciones: see §7 |
| Electricity, water, gas, fuel not stocked | **628** Suministros | |
| Phone, internet, travel, office material, cleaning, SaaS subscriptions, courier, everything else | **629** Otros servicios | Most common default |
| Local taxes (IBI, IAE, IVTM), non-deductible indirect taxes | **631** Otros tributos | |
| Fixed assets | Group 2 | Threshold and activation in `spanish-asset-accounting` |

The PGC is binding on the criteria, not on the account numbers or texts of parts 4 and 5 (RD 1514/2007 art. 2; RD 1515/2007 art. 3.1 for Pymes). Companies may open their own subaccounts; most software uses 7–10 digit codes (e.g. 6290001 Telefonía). Stay consistent.

**Purchase of goods, domestic, 21 %:**

| Cuenta | Debe | Haber |
|---|---|---|
| **600** Compras de mercaderías | 1,000.00 | |
| **472** Hacienda Pública, IVA soportado | 210.00 | |
| **400** Proveedores | | 1,210.00 |

Payment: **400** / **572**.

## 2. Proveedores 400 vs acreedores 410

| Account | Use |
|---|---|
| **400** Proveedores | Suppliers of goods and services recorded in group 60 (PGC part 5, subgroup 40) |
| **410** Acreedores por prestaciones de servicios | Suppliers of services that are not proveedores in the strict sense: rent, professionals, utilities, 62 accounts |
| **4009** / **4109** | Facturas pendientes de recibir o de formalizar: goods or services received at period end without invoice |
| **4004** / **4104** | Same in foreign currency |
| **173** / **523** | Proveedores de inmovilizado (long/short term): suppliers of fixed assets, never 400 |
| **407** | Anticipos a proveedores (§10) |

Many small businesses put everything in 400 or 410; the balance sheet presentation is the same line for both (Acreedores comerciales). The one hard rule is that fixed-asset suppliers go to **523**/**173**, because they present as other debts, not trade creditors.

## 3. Sales and customers

| Event | Account |
|---|---|
| Sale of goods | **700** Ventas de mercaderías |
| Services | **705** Prestaciones de servicios |
| Customer receivable | **430** Clientes (**4300** euros, **4304** foreign currency) |
| Sale delivered but not yet invoiced at period end | **4309** Clientes, facturas pendientes de formalizar |
| Other income (recharging costs, small services outside the main activity) | **759** Ingresos por servicios diversos |
| Rental income | **752** Ingresos por arrendamientos |
| Commissions earned | **754** Ingresos por comisiones |
| Output IVA | **477** Hacienda Pública, IVA repercutido |

**Sale of services, 21 %:**

| Cuenta | Debe | Haber |
|---|---|---|
| **430** Clientes | 1,210.00 | |
| **705** Prestaciones de servicios | | 1,000.00 |
| **477** Hacienda Pública, IVA repercutido | | 210.00 |

**Autónomo professional whose client withholds 15 %:** the retention is a payment on account of the professional's IRPF.

| Cuenta | Debe | Haber |
|---|---|---|
| **430** Clientes | 1,060.00 | |
| **473** Hacienda Pública, retenciones y pagos a cuenta | 150.00 | |
| **705** Prestaciones de servicios | | 1,000.00 |
| **477** Hacienda Pública, IVA repercutido | | 210.00 |

The PGC defines **472** and **477** at three digits only; subaccounts such as 4720021 (IVA 21 %) are company choices and are not PGC accounts.

## 4. IRPF retentions you must withhold

Companies, entities and autónomos acting in their activity must withhold on the payments below (RIRPF art. 76.1). The retention is a liability on **4751** Hacienda Pública, acreedora por retenciones practicadas, declared quarterly in modelo 111 (work and professional income) or 115 (rent) in the first 20 days of April, July, October and January; monthly for companies above 6,010,121.04 € turnover or in the large-company list (RIRPF art. 108.1, referring to RIVA art. 71.3). Annual summaries: modelo 190 and 180, 1–31 January (RIRPF art. 108.2).

| Payee | Rate | Base | Source |
|---|---|---|---|
| Professional (IAE sections 2 and 3: lawyer, architect, consultant, designer, translator...) | 15 % | Fee excluding IVA | RIRPF art. 95.1 |
| Professional in the year of starting and the two following, if no professional activity in the prior year and they tell you in writing | 7 % | Same | RIRPF art. 95.1 (keep the signed communication) |
| Rent of urban premises (office, shop, warehouse) | 19 % | All amounts paid to the landlord excluding IVA | RIRPF art. 100 |
| Rent exceptions: rent under 900 €/year to the same landlord, or landlord certified under IAE group 861 with the cadastral test, or housing for employees | 0 % | | RIRPF art. 75.3.g |
| Administrators' fees (consejeros) | 35 %, or 19 % if the company's turnover in the last closed year was under 100,000 € | | RIRPF art. 80.1.3.º |
| Dividends and interest paid to individuals | 19 % | | RIRPF art. 90; modelo 123 |
| Businesses (empresarios) in general, e.g. a carpenter or a shop | None, except some activities in estimación objetiva (1 %) | | RIRPF art. 95.6 |

**Professional invoice, 15 % retention:**

| Cuenta | Debe | Haber |
|---|---|---|
| **623** Servicios de profesionales independientes | 1,000.00 | |
| **472** Hacienda Pública, IVA soportado | 210.00 | |
| **4751** Hacienda Pública, acreedora por retenciones practicadas | | 150.00 |
| **410** Acreedores por prestaciones de servicios | | 1,060.00 |

**Monthly office rent, 19 % retention:**

| Cuenta | Debe | Haber |
|---|---|---|
| **621** Arrendamientos y cánones | 1,000.00 | |
| **472** Hacienda Pública, IVA soportado | 210.00 | |
| **4751** Hacienda Pública, acreedora por retenciones practicadas | | 190.00 |
| **410** Acreedores por prestaciones de servicios | | 1,020.00 |

Keep separate subaccounts of **4751** for modelo 111 (work, professionals), 115 (rent) and 123 (capital income): each modelo is reconciled against its own balance. A professional who is a company (SL) does not suffer retention; an autónomo does. If the invoice comes from an autónomo professional and shows no retention, the payer is still liable for it as retenedor (LGT art. 23 and 37.2; LIRPF art. 99): ask for a corrected invoice (see `spanish-invoice-compliance`).

Housing rent paid by an autónomo or company to an individual landlord also bears 19 % unless an art. 75.3.g exception applies. Rent of premises is subject to 21 % IVA; rent of housing is exempt (LIVA art. 20.Uno.23.º).

## 5. Payroll lines in the daily flow

Payroll is computed in `spanish-payroll`; the daily entries are:

| Event | Debe | Haber |
|---|---|---|
| Monthly payroll accrual | **640** Sueldos y salarios (gross) | **4751** (IRPF withheld), **476** (employee's Seguridad Social share), **465** Remuneraciones pendientes de pago (net) |
| Employer's Seguridad Social | **642** Seguridad Social a cargo de la empresa | **476** Organismos de la Seguridad Social, acreedores |
| Paying net salaries | **465** | **572** |
| TGSS charge (cuotas of the month) | **476** | **572** |
| Payroll advance | **460** Anticipos de remuneraciones | **572** |
| Meal vouchers, health insurance, training paid as social expenses | **649** Otros gastos sociales | **572** / **410** |

Note: the employee's IRPF is declared in modelo 111 together with professional retentions.

## 6. Justificantes: factura completa, simplificada, nothing

| Document | IS / IRPF deduction | IVA deduction | Source |
|---|---|---|---|
| Factura completa with your NIF and the IVA shown separately | Yes, if the expense is real, accrued and related to the activity | Yes, subject to art. 95–96 | LIVA art. 97.Uno.1.º; RD 1619/2012 art. 6 |
| Factura simplificada (≤ 400 € incl. IVA, or ≤ 3,000 € in retail, hospitality, transport and other listed sectors) without your data | Yes, as proof of the expense, if the link to the activity is shown | **No**: art. 97 requires the recipient's NIF and address and the cuota stated separately | RD 1619/2012 art. 4 |
| Factura simplificada *cualificada*: the issuer adds your NIF, address and the cuota separately at your request | Yes | Yes | RD 1619/2012 art. 7.2 |
| Card slip, bank charge, delivery note | Weak proof only | No | |
| Nothing | Only with other evidence (contract, email, bank payment); the AEAT may reject it | No | LGT art. 105–106 |

**Missing invoice, three separate consequences:**

1. IVA: not deductible until the factura arrives; book the full amount as cost, or book the expense against **4009**/**4109** at period end and deduct IVA in the period you receive the invoice (LIVA art. 99.Tres; deduction allowed within four years from accrual).
2. Corporate tax or IRPF: the expense is deductible if proven by any means admitted in law; the invoice is the preferred proof (LGT art. 106.4 for IVA and expenses: "los gastos deducibles... deberán justificarse, de forma prioritaria, mediante la factura").
3. Bookkeeping: the accounts must be orderly and supporting documents kept six years (Código de Comercio art. 25 and 30); prepare an internal note explaining the payment, attach the bank receipt and any correspondence.

**Ask for a factura completa** whenever the ticket is over a trivial amount and IVA is deductible. In restaurants and taxis, ask the issuer to put the company's NIF on the ticket (art. 7.2).

## 7. Atenciones a clientes, gastos de representación, gifts

**Corporate tax (LIS art. 15.e):** donativos y liberalidades are not deductible. Excluded from that ban, and therefore deductible: expenses for *atenciones a clientes o proveedores*, customary staff expenses (Christmas dinner, gifts), promotional expenses, and expenses correlated with income. Atenciones a clientes o proveedores are deductible only up to **1 % of the importe neto de la cifra de negocios** of the tax period; the excess is a positive adjustment in modelo 200 (permanent difference).

**IVA (LIVA art. 96.Uno.5.º and 6.º):** IVA on goods and services destined to *atenciones a clientes, asalariados o terceros* is never deductible, whatever the IS treatment. Exceptions: free samples and advertising objects of low value (art. 7.2.º and 4.º). IVA on travel, hotels and restaurants is deductible only if the expense is deductible for IS/IRPF (art. 96.Uno.6.º) and the other requirements are met.

| Case | Account | IVA | IS |
|---|---|---|---|
| Lunch with a client | **627** (or a 629 subaccount "atenciones") | Not deductible (atención a cliente): IVA added to cost | Deductible within the 1 % cap |
| Employee's lunch on a business trip | **629** | Deductible with factura (simplificada cualificada) | Deductible; employee's dietas rules in `spanish-travel-expenses` |
| Christmas hamper for clients | **627** | Not deductible | Within 1 % cap |
| Christmas hamper or dinner for staff | **649** | Not deductible (atención a asalariados) | Deductible (usos y costumbres); may be salary in kind for the employee (`spanish-payroll`) |
| Branded pens, calendars (advertising objects) | **627** | Deductible; free delivery not subject if total to one recipient ≤ 200 €/year (art. 7.4.º) | Deductible (promotion) |
| Free samples | **627** | Deductible; delivery not subject (art. 7.2.º) | Deductible |
| Gift of goods from own stock to a client | Cost stays in **600**; IVA of the purchase was deducted | Delivery is an autoconsumo subject to IVA (art. 9.1.º.b) unless art. 7 applies or IVA was not deducted | Within 1 % cap |
| Donation to an NGO | **678** Gastos excepcionales (or 659) | | Not deductible as an expense; possible deduction in the cuota under Ley 49/2002 art. 20 if the entity qualifies (see `spanish-corporate-tax`) |

Document in the concept: who attended, which company they represent, the business purpose. An IS deduction for client entertainment without that evidence is routinely rejected.

## 8. Vehicles

| Tax | Rule | Source |
|---|---|---|
| IVA on a car (turismo), its fuel, parking, tolls, repairs | Presumed 50 % business use; 100 % for mixed goods vehicles, taxis, driving schools, sales reps' cars, security and manufacturers' test cars. A different percentage must be proven by any means; the 303 or the books are not proof | LIVA art. 95.Tres.2.ª and Cuatro |
| Corporate tax | No fixed percentage: deductible if related to the activity and booked. If a socio or employee uses it privately, the private use is salary in kind for them (`spanish-payroll`) | LIS art. 10.3, 15 |
| IRPF of an autónomo | A turismo is an affected asset only if used exclusively for the activity; incidental private use outside working hours does not count as accessory for cars | RIRPF art. 22.2 and 22.4 |

**Fuel for a company car, 50 % IVA:**

| Cuenta | Debe | Haber |
|---|---|---|
| **628** Suministros (or 629 subaccount) | 105.00 | |
| **472** Hacienda Pública, IVA soportado | 10.50 | |
| **572** Bancos | | 115.50 |

(Ticket of 100 + 21 IVA; half of the IVA goes into the cost.)

Vehicle purchase and renting: `spanish-asset-accounting` (`references/leasing-and-disposal.md`).

## 9. Suplidos

A *suplido* is an amount paid in the customer's name and on its behalf under an express mandate (typically a gestoría paying registry fees or taxes for a client). It is not part of the IVA base, the payer cannot deduct any IVA in it, and the amount must be justified (LIVA art. 78.Tres.3.º).

| Step | Debe | Haber |
|---|---|---|
| Pay the fee for the client | **440** Deudores (subaccount per client) or **555** Partidas pendientes de aplicación | **572** |
| Invoice the client: fees + IVA, suplido listed apart without IVA | **430** | **705**, **477**, **440** |
| Receiving a supplier's invoice that includes a suplido (e.g. a notary passing on registry fees) | Book the suplido to the expense it is (e.g. **631** or **623**) without IVA | **410** |

If the document for the suplido is issued in your name (not the client's), it is not a suplido but a recharged cost: book as your expense and invoice it with IVA.

## 10. Anticipos

IVA accrues when an advance is collected or paid for a taxable supply (LIVA art. 75.Dos), so the advance needs an invoice.

| Event | Debe | Haber |
|---|---|---|
| Pay an advance to a supplier of goods | **407** Anticipos a proveedores, **472** | **572** |
| Final invoice from that supplier | **600**, **472** (on the remainder) | **407** (cancel), **400** |
| Collect an advance from a customer | **572** | **438** Anticipos de clientes, **477** |
| Final invoice to that customer | **438** (cancel), **430** | **700**/**705**, **477** (on the remainder) |
| Advance for a fixed asset | **239** Anticipos para inmovilizaciones materiales (or **209** intangible) | **572** |

## 11. Discounts, returns, rappels

| Event | Purchases side | Sales side |
|---|---|---|
| Discount on the invoice itself | Book net in **600** | Book net in **700** |
| Prompt payment discount after the invoice | **606** Descuentos sobre compras por pronto pago | **706** Descuentos sobre ventas por pronto pago |
| Returns | **608** Devoluciones de compras | **708** Devoluciones de ventas |
| Volume rebates | **609** Rappels por compras | **709** Rappels sobre ventas |

Each needs a factura rectificativa when it changes the IVA base (LIVA art. 80.Dos; RD 1619/2012 art. 15).

## 12. Bad debts

| Step | Debe | Haber |
|---|---|---|
| Debt becomes doubtful (reclassification) | **436** Clientes de dudoso cobro | **430** |
| Impairment at period end | **694** Pérdidas por deterioro de créditos por operaciones comerciales | **490** Deterioro de valor de créditos por operaciones comerciales |
| Definitive loss | **650** Pérdidas de créditos comerciales incobrables | **436** |

Corporate tax deducts the impairment when, at accrual, six months have passed since maturity, or the debtor is in insolvency proceedings, or the debt is claimed in court (LIS art. 13.1). Empresas de reducida dimensión may also deduct a global 1 % of debtors (LIS art. 104). Recovering the IVA of an unpaid invoice requires a rectificativa within the LIVA art. 80.Cuatro deadlines and the AEAT communication: see `spanish-vat`.

## 13. Cash

Cash is **570** Caja, euros (**571** foreign currency). Payments in cash are prohibited from 1,000 € when either party acts as a business or professional (10,000 € for a non-resident private payer), counting split payments together (Ley 7/2012 art. 7.Uno.1, limit lowered from 2,500 € by Ley 11/2021). Keep proof of non-cash payment for five years. A negative cash balance is impossible and signals missing entries.

## 14. Quick lookup

| Item | Account | IVA |
|---|---|---|
| Office rent | **621** | 21 %, deductible; retention 19 % |
| Gestoría monthly fee | **623** | 21 %; retention 15 % if autónomo |
| Notary | **623** | 21 %; retention 15 % (professional) |
| Registro Mercantil fees | **623** or **631** | Not subject (public fee) |
| Electricity | **628** | 21 % (rate may vary by temporary measures: check `spanish-vat`) |
| Mobile phone | **629** | Deductible in the business-use proportion |
| SaaS from a Spanish supplier | **629** | 21 % |
| Insurance | **625** | Exempt |
| Bank fee, TPV commission | **626** | Exempt |
| Bank loan interest | **662** Intereses de deudas | Exempt |
| Late payment interest to AEAT | **669** Otros gastos financieros | Not subject; IS-deductible per TS case law (`spanish-corporate-tax`) |
| AEAT recargo or sanction | **678** Gastos excepcionales | Not deductible for IS (LIS art. 15.c) |
| IAE, IBI | **631** | Not subject |
| Training courses | **629** or **649** if for staff | Usually 21 %; some exempt (art. 20.Uno.9.º) |
| Professional association fees | **629** | Usually exempt (LIVA art. 20.Uno.12.º) |
| Books, press | **629** | 4 % |

## 15. Ask the user

- Who is the supplier (individual or company) and do they apply retention?
- Is this a cost of the business, or private? In an SL, who used it?
- For meals, gifts and events: attendees, company, purpose.
- For a car: what kind of vehicle, who drives it, private use?
- No invoice: can the supplier issue one? Is there any other evidence?
- Is the amount a suplido paid for a client, or a cost to recharge?
