# Leasing, Renting and Disposal

Lease classification and entries for the lessee, the corporate tax regime for financial leases, renting, and the derecognition of assets with its IVA consequences. Accounts are **PGC 2007**. Spain's PGC has not adopted IFRS 16: operating leases stay off the lessee's balance sheet.

## Contents

- [1. Financial or operating lease](#1-financial-or-operating-lease)
- [2. Financial lease: lessee entries](#2-financial-lease-lessee-entries)
- [3. Corporate tax: LIS art. 106](#3-corporate-tax-lis-art-106)
- [4. Microempresas: instalments as expense](#4-microempresas-instalments-as-expense)
- [5. Renting and operating leases](#5-renting-and-operating-leases)
- [6. Disposal by sale](#6-disposal-by-sale)
- [7. Scrapping, loss, theft](#7-scrapping-loss-theft)
- [8. IVA on disposal and regularización](#8-iva-on-disposal-and-regularización)
- [9. Assets held for sale](#9-assets-held-for-sale)
- [10. Ask the user](#10-ask-the-user)

## 1. Financial or operating lease

A lease is financial when it transfers substantially all the risks and rewards of ownership (PGC NRV 8.ª 1.1; PGC Pymes NRV 7.ª). With a purchase option, transfer is presumed when there is no reasonable doubt the option will be exercised. Without an option, transfer is also presumed when, among others:

- ownership passes, or will clearly pass, at the end of the term;
- the term covers most of the asset's economic life;
- the present value of minimum payments is substantially all of the asset's fair value;
- the asset is so specialised that only the lessee can use it;
- the lessee bears the lessor's losses if it cancels;
- residual value fluctuations fall on the lessee.

| Contract | Usual classification |
|---|---|
| Bank or finance company *leasing* with a symbolic purchase option (one instalment) | Financial |
| *Renting* of a car or equipment, no option, maintenance included | Operating |
| Office or shop rent | Operating |
| Long rental where the lessee guarantees the residual value | Often financial: read the contract |

## 2. Financial lease: lessee entries

**Initial recognition:** asset by nature (21x or 20x) and a financial liability for the same amount: the lower of the fair value of the asset and the present value of minimum lease payments, including the option price when its exercise is not in doubt (NRV 8.ª 1.2). Direct initial costs of the lessee are added to the asset.

| Account | Use |
|---|---|
| 21x / 20x | The leased asset |
| **174** Acreedores por arrendamiento financiero a largo plazo | Principal due after 12 months |
| **524** Acreedores por arrendamiento financiero a corto plazo | Principal due within 12 months |
| **662** Intereses de deudas (**6623** if the lessor is a credit institution) | Finance charge, effective interest method |
| **472** | IVA on each instalment |
| **681** / **281x** | Amortisation of the asset over its useful life (shorter of term and life if ownership is not reasonably certain) |

IVA: until the option is exercised, the leasing is a service; IVA accrues on each instalment when it falls due (LIVA art. 75.Uno.7.º) and is charged on the whole instalment (principal recovery and finance charge). For cars, the 50 % presumption of LIVA art. 95.Tres applies to each instalment's IVA.

**Example: machine, fair value 50,000 €, 48 monthly instalments, option = one more instalment, implicit rate 5 %.**

| Event | Debe | Haber |
|---|---|---|
| Inception | **213** Maquinaria 50,000.00 | **524** (principal due in year 1), **174** (rest) |
| Each instalment (e.g. 1,151 € + 241.71 IVA) | **524** (principal part), **6623** (interest part), **472** 241.71 | **572** 1,392.71 |
| Year end: reclassify next year's principal | **174** | **524** |
| Monthly amortisation (life 10 years) | **681** 416.67 | **2813** 416.67 |

The amortisation schedule of the bank shows the split of each instalment between cost recovery and finance charge; use it.

## 3. Corporate tax: LIS art. 106

| Requirement | Rule | Source |
|---|---|---|
| Lessor | Credit institution or establecimiento financiero de crédito | LIS art. 106.1 |
| Minimum term | 2 years for movable goods; 10 years for real estate or industrial establishments | LIS art. 106.2 |
| Contract | Instalments split between cost recovery (excluding the option) and finance charge | LIS art. 106.3 |
| Cost-recovery part | Constant or increasing each year over the term | LIS art. 106.4 |
| Deductible | The finance charge, always; the cost-recovery part, except for land and other non-amortisable assets | LIS art. 106.5–6 |
| Limit on the cost-recovery deduction | 2 × the max linear table coefficient applied to the asset's cost; for ERDs 2 × coefficient × 1.5. The excess is deductible in later years within the same limit | LIS art. 106.6 |
| Booking | Not conditional on booking in profit and loss | LIS art. 106.7 |

So, for tax, the company deducts the cost-recovery instalments (within the limit) instead of the book amortisation. The difference between the two is a temporary difference: usually taxable (tax deduction ahead of book), booked as **6301** / **479** and reversed over the asset's remaining life after the term ends.

**Example:** car (16 % table) leased for 3 years, cost 36,000 €, recovery 12,000 €/year. Limit: 36,000 × 32 % = 11,520 €/year (ERD: × 1.5 → 17,280). Non-ERD deducts 11,520 in years 1–3 and the remaining 1,440 in year 4. Book amortisation over 8 years (4,500/year). Adjustment year 1: −(11,520 − 4,500) = −7,020; it reverses from year 4 onward. For a turismo, also check the company's IS deductibility of the vehicle (business use) and the 50 % IVA limit.

## 4. Microempresas: instalments as expense

A company applying the PGC Pymes that meets two of three limits at two consecutive year ends (total assets ≤ 1 M€, net turnover ≤ 2 M€, average staff ≤ 10) may apply the *criterios específicos para microempresas* as a block for at least three years (RD 1515/2007 art. 4.1–2). For financial leases of amortisable assets, it books the instalments accrued in the year as an expense (**621** for the cost-recovery part and **662** for the finance charge, as practice), and registers the asset at the option price when the option is exercised. It must disclose in the memoria the fair value of the asset at inception, its useful life, instalments paid, debt outstanding and the option price, with a yearly split of instalments between cost recovery and finance charge (RD 1515/2007 art. 4.3, 1.ª). For the microempresa thresholds, total assets include the outstanding lease commitments (art. 4.1).

For tax, LIS art. 106 still applies: deduct the cost-recovery part within the limit and the finance charge.

## 5. Renting and operating leases

| Item | Account | IVA | IS |
|---|---|---|---|
| Monthly renting fee (equipment) | **621** Arrendamientos y cánones | 21 % deductible | Deductible as accrued |
| Car renting | **621** | 50 % presumption (LIVA art. 95.Tres.2.ª) unless the business use is proven or it is a 100 % case | Deductible if used in the activity; private use by a socio or employee is salary in kind (`spanish-payroll`) |
| Initial fee or prepayment covering several months | **480** Gastos anticipados, released monthly to **621** | IVA when invoiced | Accrual |
| Rent of premises | **621** with 19 % retention (`spanish-daily-bookkeeping`) | 21 % | Deductible |
| Leasehold improvements | Asset (NRV 3.ª h): amortise over the lease term including likely renewals, or life if shorter | | Same period if it reflects effective depreciation |

## 6. Disposal by sale

Steps (NRV 2.ª 3):

1. Book amortisation up to the date of sale.
2. Derecognise cost and accumulated amortisation (and impairment).
3. Record the proceeds and the IVA charged.
4. The difference between net proceeds and carrying amount goes to **771** Beneficios procedentes del inmovilizado material or **671** Pérdidas procedentes del inmovilizado material (intangible **770**/**670**, real estate **772**/**672**).

**Example:** van bought for 20,000 €, accumulated amortisation 14,000 €, sold for 8,000 € + 1,680 € IVA on 30 June.

| Cuenta | Debe | Haber |
|---|---|---|
| **2818** Amortización acumulada de elementos de transporte | 14,000.00 | |
| **543** Créditos a corto plazo por enajenación de inmovilizado (or **572** if paid) | 9,680.00 | |
| **218** Elementos de transporte | | 20,000.00 |
| **477** Hacienda Pública, IVA repercutido | | 1,680.00 |
| **771** Beneficios procedentes del inmovilizado material | | 2,000.00 |

Deferred payment over 12 months: **253** Créditos a largo plazo por enajenación de inmovilizado. Customers for assets are never **430**.

Tax: the gain or loss is part of the accounting result and taxed with it. Release any deferred tax linked to the asset (temporary differences from libertad, acelerada or impairment reverse in full on disposal). If the company deducted free amortisation under LIS art. 102 or DA 17.ª/18.ª, check the workforce conditions are still met.

## 7. Scrapping, loss, theft

| Case | Entry |
|---|---|
| Asset fully amortised, scrapped | **281x** / 21x for the cost: no result |
| Asset not fully amortised, scrapped | **281x**, **671** (carrying amount) / 21x |
| Insurance compensation received | **572** / **778** Ingresos excepcionales (or reduce **671**; consistency matters) |
| Asset kept but no longer used | Test for impairment; do not derecognise until disposed of or no benefits are expected (NRV 2.ª 3) |

Keep evidence of scrapping (waste-management certificate, photos, police report for theft); the AEAT asks for it when a loss is deducted.

## 8. IVA on disposal and regularización

| Situation | Rule | Source |
|---|---|---|
| Sale of a movable asset by a business | Subject to IVA at the rate of the good (usually 21 %), invoiced to the buyer | LIVA art. 4, 90 |
| Asset whose purchase IVA was totally excluded from deduction under art. 95–96, or used only in exempt activities without deduction right | Its later delivery is exempt | LIVA art. 20.Uno.25.º and 24.º |
| Second and later delivery of buildings | Exempt (art. 20.Uno.22.º), with an option to waive the exemption when the buyer is a business with full deduction (art. 20.Dos), which triggers reverse charge (art. 84.Uno.2.º e) | LIVA art. 20, 84 |
| Sale within the regularisation period (4 years after purchase year; 9 for real estate) of an investment good | One-off regularisation for the remaining years: a taxable sale counts as 100 % deductible use; an exempt or non-subject sale counts as 0 % (with exceptions for exempt sales that give a deduction right) | LIVA art. 110 |
| Transfer of a whole business unit | Not subject (art. 7.1.º); the buyer steps into the regularisation position | LIVA art. 7.1.º, 110.Cuatro |
| Loss or destruction for reasons not attributable to the taxpayer, duly proven | No further regularisation | LIVA art. 107.Seis |

**Example (art. 110):** a company with a 60 % prorrata bought a machine in year 1 for 100,000 € + 21,000 € IVA, deducting 12,600. It sells the machine in year 3 with IVA. Remaining years in the period (year 3, 4, 5): treated as 100 % deductible. Extra deduction = 21,000 × (100 % − 60 %) × 3/5 = 5,040, capped at the IVA charged on the sale. Book **472** / **639** Ajustes positivos en la imposición indirecta (a negative regularisation goes **634** / **472**); see `spanish-vat`.

## 9. Assets held for sale

Under the full PGC, a non-current asset whose carrying amount will be recovered through sale, available for immediate sale and highly probable to be sold within a year, is reclassified to **580** Inmovilizado and stops being amortised; it is measured at the lower of carrying amount and fair value less costs to sell, with impairment in **599** (NRV 7.ª). The PGC Pymes does not use this category (RD 1515/2007 art. 3.2): Pymes keep the asset in its 21x account until sold.

## 10. Ask the user

- Copy of the leasing contract: lessor, term, option price, schedule of instalments.
- Does the company apply the microempresa criteria?
- Date of sale or scrapping, proceeds, buyer (business or individual, Spain or abroad).
- Was the asset bought within the IVA regularisation period, and did the company have a prorrata?
- Was free or accelerated amortisation used on the asset?
