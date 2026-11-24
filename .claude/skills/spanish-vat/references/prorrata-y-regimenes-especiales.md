# Prorrata, capital goods and special IVA schemes

Deduction when a business makes both taxable and exempt supplies, the regularisation of IVA on capital goods, and the special schemes of LIVA title IX. General deduction rules (arts. 92-99, limits of arts. 95-96) are in `vat-reference.md`.

Sources: LIVA (BOE consolidated 07/10/2026) arts. 9.1º.c, 101-114, 120-163 sexiesdecies, DT 13ª; RIVA (28/02/2026) arts. 28, 30, 33-61 septies; AEAT pages on régimen simplificado (updated 12/11/2026) and Orden HAC/1161/2026. Checked 2026-11-24.

## Contents

1. [Which deduction regime applies](#1-which-deduction-regime-applies)
2. [Prorrata general](#2-prorrata-general)
3. [Prorrata especial](#3-prorrata-especial)
4. [Sectores diferenciados](#4-sectores-diferenciados)
5. [Regularización de bienes de inversión](#5-regularización-de-bienes-de-inversión)
6. [Booking prorrata and regularisations](#6-booking-prorrata-and-regularisations)
7. [Criterio de caja (RECC)](#7-criterio-de-caja-recc)
8. [Recargo de equivalencia](#8-recargo-de-equivalencia)
9. [Régimen simplificado](#9-régimen-simplificado)
10. [REAGP (agriculture, livestock, fishing)](#10-reagp-agriculture-livestock-fishing)
11. [REBU (used goods, art, antiques)](#11-rebu-used-goods-art-antiques)
12. [Agencias de viajes](#12-agencias-de-viajes)
13. [Grupo de entidades and investment gold](#13-grupo-de-entidades-and-investment-gold)

## 1. Which deduction regime applies

```
Does the business make exempt supplies without deduction right (art. 20)?
├── No ─────────────────────────────────── full deduction (subject to arts. 95-96)
└── Yes
    ├── Are the exempt activities a different CNAE group AND would their
    │   deduction % differ from the main activity by more than 50 points?
    │   └── Yes → sectores diferenciados: separate deduction per sector (art. 101)
    └── Within each sector with mixed supplies → regla de prorrata (art. 102)
        ├── Opted for prorrata especial, or general would give ≥ 10 % more
        │   deduction than especial in the year → prorrata especial (art. 103.Dos)
        └── Otherwise → prorrata general (art. 104)
```

Exempt supplies that do not reduce deduction: exports and intra-EU supplies (art. 94), and the items art. 104.Tres excludes from the calculation.

## 2. Prorrata general

**Percentage (art. 104.Dos):**

```
            supplies with deduction right (year)
prorrata = ──────────────────────────────────────── × 100, rounded UP to the next whole number
            total supplies (year)
```

Excluded from both numerator and denominator (art. 104.Tres): operations of permanent establishments outside Spain; the IVA itself; sales of capital goods used in the business; real-estate or financial operations that are not the habitual activity (letting is always habitual); operations not subject under art. 7; self-supplies of art. 9.1º.d. Subsidies not linked to the price do not enter either term (current wording of art. 104.Dos).

**Procedure (art. 105):**

| Step | Rule |
|---|---|
| During the year | Apply the previous year's definitive percentage as provisional |
| New activity | Use the provisional percentage proposed to AEAT under art. 111.Dos, or a reasonable estimate |
| Significant change | Ask AEAT for a different provisional percentage (art. 105.Dos) |
| Last return of the year (4T or December) | Compute the definitive percentage on the year's figures and regularise all deductions of the year in casilla 44 |
| Interruption of activity | Use the global percentage of the last three years with operations (art. 105.Cinco) |

Non-deductible IVA under arts. 95-96 is excluded before applying the prorrata (art. 104.Uno).

**Worked example.** Year 1: taxable sales 600,000, exempt residential rent 150,000. Prorrata = 600,000 / 750,000 = 80 %. Year 2 provisional = 80 %. Year 2 input IVA on common costs: 40,000; quarterly deduction 32,000. Year 2 definitive: taxable 500,000, exempt 200,000 → 71.43 % rounded up to 72 %. Deduction due 28,800; casilla 44 of the 4T return: -3,200; entry: debit **6341** 3,200, credit **472** 3,200 (or a cost account).

## 3. Prorrata especial

| Rule | Detail |
|---|---|
| Method (art. 106) | IVA on inputs used only for taxable supplies: 100 % deductible. Used only for exempt supplies: 0 %. Common inputs: general prorrata percentage |
| Option | In the last return of the year (casilla in the 303 of 4T or December); at start of activity, in the first return of the period the activity starts; minimum three years; revocation in the last return of a year after that (RIVA art. 28.1.1º) |
| Compulsory | When, in a calendar year, general prorrata gives 10 % or more deduction than especial (art. 103.Dos.2º). Compute both at year end |
| Records | Track each input to taxable, exempt or common use |

The compulsory test is easy to miss in companies that buy a building for exempt letting and have otherwise taxable income: prorrata general would deduct part of the building's IVA, prorrata especial none, so especial is compulsory.

## 4. Sectores diferenciados

A sector is diferenciado (art. 9.1º.c) when:

| Type | Test |
|---|---|
| a') Different activity and deduction regime | Different CNAE groups (3 digits) and the deduction percentage of the non-main activity differs from the main one by more than 50 points. The main activity is the one with the highest volume last year. Accessory activities (≤ 15 % of the main activity's volume last year and contributing to it) follow the main one |
| b') Special schemes | Activities in simplificado, REAGP, investment gold or recargo de equivalencia are always separate sectors |
| c') Financial leasing (Ley 10/2014 DA 3ª) | Separate sector |
| d') Assignment of credits or loans (except factoring) | Separate sector |

Each sector has its own deduction regime (art. 101); common inputs use a prorrata calculated on the operations of the sectors involved. AEAT may authorise a common regime for a') sectors (application in November, RIVA art. 28.1.2º), lost in a year where it gives 20 % more deduction.

## 5. Regularización de bienes de inversión

**Capital good (art. 108):** tangible movable or immovable goods normally used for more than one year as work instruments. Not capital goods: spare parts, repairs, packaging, work clothes, and any good with acquisition value under €3,005.06 (the law's 500,000 pesetas).

| Rule | Detail | Source |
|---|---|---|
| Regularisation period | Year of purchase (or entry into use) plus the next four years; land and buildings plus the next nine | Art. 107.Uno, Tres |
| Trigger | Definitive prorrata of a later year differs by more than 10 percentage points from the year of purchase | Art. 107.Uno |
| Calculation | (deduction that would apply with this year's percentage − deduction made in the purchase year) ÷ 5 (÷ 10 for property) | Art. 109 |
| Where | Last return of the year, casilla 43 | Art. 107.Siete |
| Sale during the period | One-off regularisation for the remaining years: taxable sale counts as 100 % deduction for the rest of the period (capped at the IVA charged on the sale); exempt sale counts as 0 % | Art. 110 |
| Change of use to arts. 95-96 excluded use | Treated as an exempt sale (art. 110.Uno.2º) | |
| Loss or destruction not attributable to the taxpayer | No further regularisation | Art. 107.Seis |
| Business transfer not subject (art. 7.1º) | Acquirer inherits the regularisation | Art. 107.Cinco |
| Vehicles (art. 95.Tres.3ª) | Same procedure, with the degree of business use instead of the prorrata | |

**Worked example.** Building bought in year 1 for 1,000,000 + IVA 210,000; prorrata year 1 = 90 % → deducted 189,000. Year 3 definitive prorrata = 70 % (difference 20 points). Deduction with 70 % = 147,000; difference −42,000 ÷ 10 = −4,200 to return in casilla 43 of year 3. Entry: debit **6342** 4,200, credit **472** 4,200.

Track capital goods with their IVA, prorrata and remaining years in the asset register (see `spanish-asset-accounting`).

## 6. Booking prorrata and regularisations

| Situation | Entry |
|---|---|
| Purchase of current expense under provisional prorrata 80 %, IVA 1,000 | Debit **62x** with base + 200, debit **472** 800, credit **410** |
| Purchase of capital good, provisional prorrata 80 %, IVA 21,000 | Debit **21x** with base + 4,200, debit **472** 16,800, credit **523** or **173** |
| Year-end definitive prorrata higher than provisional, on current inputs | Debit **472**, credit **6391** |
| Year-end definitive prorrata lower, on current inputs | Debit **6341**, credit **472** |
| Same on capital goods | **6392** / **6342** (PGC permits treating the adjustment as part of the asset only when it relates to the year of purchase; later regularisations go to results) |

The PGC accounts are **634** *Ajustes negativos en la imposición indirecta* (**6341** current assets, **6342** investments) and **639** *Ajustes positivos* (**6391**, **6392**).

## 7. Criterio de caja (RECC)

| Point | Rule | Source |
|---|---|---|
| Who | Businesses with volume ≤ €2,000,000 in the previous year (annualised for a start in the previous year); excluded if cash collections from a single customer exceed €100,000 in the year | Art. 163 decies; RIVA art. 61 septies-nonies |
| Option | At alta (modelo 036) or in December for the next year; three years minimum after renunciation | RIVA art. 61 septies; art. 163 undecies |
| Scope | All operations except special schemes (simplificado, REAGP, RE, gold, OSS, groups), exports and intra-EU supplies, AIB, reverse charge, imports, self-supplies | Art. 163 duodecies |
| Output VAT | Due at collection, or 31 December of the year after the operation at the latest | Art. 163 terdecies.Uno |
| Input VAT | Deductible when paid, or 31 December of the year after | Art. 163 terdecies.Tres |
| Customers of a RECC supplier | Also deduct only when they pay, even if they are not in the scheme | Art. 163 terdecies.Tres; art. 163 quinquiesdecies |
| Invoice | Must say "régimen especial del criterio de caja" | RD 1619/2012 art. 6.1.p |
| Records | Collection and payment dates and means in the libros registro | RIVA art. 61 decies |
| 303 | Informative casillas 62-63 (supplies) and 74-75 (purchases) | AEAT Instrucciones 2026 |

Booking: issue the invoice with IVA in a pending sub-account (for example 477.9 *IVA repercutido pendiente de devengo*, a company sub-account of **477**) and move it to the ordinary **477** sub-account when collected. Same logic on **472** for purchases.

## 8. Recargo de equivalencia

| Point | Rule | Source |
|---|---|---|
| Who | Retailers (*comerciantes minoristas*) who are individuals or entities in attribution of income (all members individuals), selling goods without transformation, with more than 80 % of sales of those goods to consumers in the previous year (the 80 % test does not apply to those classified as retailers in IAE under conditions) | LIVA arts. 148-149; RIVA art. 59 |
| Excluded products | Vehicles, boats, aircraft and their parts; jewellery; luxury furs; art and antiques; used goods; petroleum products subject to excise; machinery for industrial use; gold; and others in RIVA art. 59.2 | RIVA art. 59.2 |
| Mechanism | Suppliers charge IVA plus the recargo (5.2 / 1.4 / 0.5 / 1.75 %). The retailer charges customers normal IVA, files no 303 for this activity and deducts nothing | Arts. 154, 161 |
| Retailer's own obligations | Modelo 309 for intra-EU acquisitions, reverse charge purchases and imports (where it pays IVA and the recargo itself); must tell suppliers it is in RE | Art. 154.Uno; RIVA art. 61 |
| Supplier side | Charge recargo when the buyer is in RE; report it in casillas 16-24, 156-158, 168-170 of the 303 | AEAT Instrucciones 2026 |
| Sanction | Retailer buying without recargo on the invoice: 50 % of the recargo, minimum €30 per purchase | Art. 171.Uno.1º |
| Invoices to consumers | RE retailers are not obliged to issue invoices for retail sales unless the customer asks (RD 1619/2012 art. 3) | |

Booking at the retailer: IVA and recargo paid are part of the purchase cost (debit **600** with the total). At the supplier: credit **477** (company sub-accounts for IVA and recargo).

## 9. Régimen simplificado

| Point | Rule | Source |
|---|---|---|
| Who | Individuals and entities in attribution of income with activities listed in the annual Orden de módulos, under the IRPF objective estimation method | Arts. 122-123 |
| Exclusion thresholds (previous year) | Volume of income over €250,000 for all activities except agriculture (€250,000 for agricultural activities); purchases (excluding fixed assets) over €250,000. The statutory figure is €150,000; AEAT applies €250,000 for 2016-2026 although the 2025-2026 extensions were repealed by Congress (see note) | Art. 122.Dos; DT 13ª; AEAT page updated 12/11/2026 |
| Other exclusions | IRPF direct estimation in any activity; activities outside Spain; certain related-party shares | Art. 122.Dos |
| Mechanics | Quarterly 303 with *ingresos a cuenta* (a percentage of the annual quota computed from modules); annual quota in 4T; deduction of input IVA on current operations limited by the modules, plus fixed-asset IVA (casillas 48-58) | Art. 123; Orden HAC/1425/2025 (2026), Orden HAC/1161/2026 (2027, same modules) |
| Renunciation | December of the previous year (for 2027: 6 November-31 December 2026, Orden HAC/1161/2026), or tacitly by filing the first 303 of the year under the general regime; minimum three years | RIVA art. 33 |
| Simplificado with AIB, reverse charge, fixed asset sales | Declared in casillas 51-53 of the same 303 | AEAT Instrucciones 2026 |

Note on the limits: RDL 9/2024, RDL 16/2025 and RDL 2/2026 each extended the €250,000 limit and were each repealed (BOE 23/01/2025, 28/01/2026, 28/02/2026). The BOE consolidated DT 13ª names only 2016-2024. AEAT and the DGT have stated publicly that the €250,000 limit is maintained for 2025 and 2026. Flag this to the user if a business is between €150,000 and €250,000. For 2027 there is no extension yet (unverified as of 2026-11-24).

## 10. REAGP (agriculture, livestock, fishing)

| Point | Rule | Source |
|---|---|---|
| Who | Farmers, livestock farmers and fishers selling natural products from their own holdings; voluntary renunciation possible | Arts. 124-126 |
| Exclusions | Volume over €250,000 for the scheme's activities (statutory €150,000, same DT 13ª issue), purchases over the limit, IRPF direct estimation, sociedades mercantiles, cooperatives and SAT (art. 124.Dos.1º-2º) | Art. 124.Dos; DT 13ª |
| Mechanism | No 303, no deduction. The buyer (a business) pays the farmer a compensation: 12 % for agricultural and forestry products, 10.5 % for livestock and fishing products | Art. 130 |
| Buyer | Issues a *recibo* (self-billed receipt), deducts the compensation in casilla 42 of the 303 | Arts. 130, 134; RD 1619/2012 art. 16 |
| Farmer | May request refund of compensations on exports and intra-EU supplies (modelo 341) | |

## 11. REBU (used goods, art, antiques)

| Point | Rule | Source |
|---|---|---|
| Who | Resellers (*revendedores*) of used goods, art, antiques and collectors' items bought from private persons, REBU resellers or exempt sellers | Arts. 135-136 |
| Base | Margin (sale price including IVA minus purchase price including IVA), minus the IVA in the margin; option for global margin per period for certain goods | Art. 137 |
| Invoice | Must state "régimen especial de los bienes usados" (or art/antiques); no separate IVA, and the buyer cannot deduct | RD 1619/2012 art. 6.1.o |
| Option | Can apply the general regime per operation (art. 138) | |
| Not REBU | Second-hand goods bought from a business that charged full IVA | |

Typical users: second-hand car dealers, vintage clothing, antiques. For online resale platforms see `spanish-industry-ecommerce`.

## 12. Agencias de viajes

| Point | Rule | Source |
|---|---|---|
| Scope | Agencies and tour operators acting in their own name with customers, using goods and services from third parties | Art. 141 |
| Base | Gross margin: price charged (excluding IVA) minus costs of third-party services for the trip (IVA included) | Art. 145 |
| Exemption | Services for trips outside the EU are exempt | Art. 143 |
| Invoice | IVA is not shown separately and is included in the price; mention "régimen especial de las agencias de viajes" | Art. 142; RD 1619/2012 art. 6.1.n |
| Option | General regime per operation for B2B customers | Art. 147 |

## 13. Grupo de entidades and investment gold

**Grupo de entidades (arts. 163 quinquies-nonies).** A parent holding more than 50 % of capital or votes of Spanish subsidiaries (throughout the year) may form an IVA group. Option in December for the next year, minimum three years. Each entity files individual modelo 322 monthly and the parent files the aggregate modelo 353. Optional advanced level: intra-group supplies taxed on cost, as a separate differentiated sector. All entities file monthly and use SII.

**Investment gold (arts. 140-140 sexies).** Supplies of investment gold are exempt; waiver possible between businesses, then reverse charge (art. 140 quinque). Supplies of unwrought gold ≥ 325 thousandths are reverse charged under art. 84.Uno.2º.b.
