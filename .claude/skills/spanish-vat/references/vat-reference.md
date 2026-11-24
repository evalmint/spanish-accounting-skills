# IVA reference: rates, exemptions, deduction, filing

Core IVA rules for *territorio común*. Cross-border rules are in `intracomunitario-e-importacion.md`, prorrata and special schemes in `prorrata-y-regimenes-especiales.md`, the 303 form in `modelo-303-casillas.md`.

Sources: LIVA (Ley 37/1992, BOE consolidated text updated 07/10/2026), RIVA (RD 1624/1992, consolidated 28/02/2026), LGT (Ley 58/2003), RD 1619/2012 (Reglamento de facturación), AEAT *Manual práctico IVA 2026* and modelo 303 *Instrucciones 2026*. Checked 2026-11-24.

## Contents

1. [What changed in 2024-2026](#1-what-changed-in-2024-2026)
2. [Territory](#2-territory)
3. [Rates](#3-rates)
4. [Exemptions (art. 20)](#4-exemptions-art-20)
5. [Devengo (when VAT is due)](#5-devengo-when-vat-is-due)
6. [Domestic inversión del sujeto pasivo](#6-domestic-inversión-del-sujeto-pasivo-art-84uno2)
7. [Deduction: requirements, timing, limits](#7-deduction-requirements-timing-limits)
8. [Base modification: credit notes and bad debts](#8-base-modification-credit-notes-and-bad-debts)
9. [Periods, returns and deadlines](#9-periods-returns-and-deadlines)
10. [SII and REDEME](#10-sii-and-redeme)
11. [Sanctions and late filing](#11-sanctions-and-late-filing)
12. [Error patterns](#12-error-patterns)

## 1. What changed in 2024-2026

| Change | Dates | Source |
|---|---|---|
| Temporary food rates ended; basic foods back to 4 %, seed oils and pasta back to 10 % | From 1 January 2025 | RDL 4/2024 art. 1 (rates ran to 31 December 2024) |
| Olive oil moved permanently to 4 % | From 1 January 2025 | LIVA art. 91.Dos.1.1º.g (RDL 4/2024 art. 2) |
| Electricity (≤ 10 kW, and bono social severe vulnerability), gas, biomass pellets/briquettes, firewood and fuels (hydrocarbon tariff epígrafes listed in the RDL) at 10 % | 22 March 2026 to 30 June 2026; dropped in June for any product whose April CPI rose 15 % or less | RDL 7/2026 art. 42 (convalidated 26 March 2026; amended by RDL 10/2026) |
| Electricity and gas back to 21 % (April CPI condition not met); fuels kept 10 % to 30 June, 21 % from 1 July 2026 | 1 June / 1 July 2026 | RDL 7/2026 art. 42; Supercontable summary of INE data (secondary source) |
| Conditional 10 % for electricity and gas in July-October 2026 | Depends on CPI | RDL 18/2026 (unverified whether the condition was met in any month) |
| Conditional 10 % for electricity (≤ 10 kW, bono social) and gas, pellets, firewood in November and December 2026, if the INE CPI subclass for September (for November) or October (for December) exceeds the same month of 2025 by more than 15 % | November and December 2026 | RDL 25/2026 arts. 18-19 (convalidated, BOE 16 October 2026). Whether the condition was met: (unverified), check the INE CPI and AEAT notice for the month |
| Furnished apartment or home rentals of 30 nights or less to the same tenant are no longer exempt (taxed at 10 %), unless in the landlord's own habitual residence | From 1 December 2026 | LIVA art. 20.Uno.23º.e') and art. 91.Uno.2.2º, as amended by RDL 29/2026 art. 7 (convalidated, BOE 12 November 2026). RDL 26/2026 with the same content was repealed by Congress on 2 October 2026 |
| 10 % rate for renovation and repair works on homes extended to homes let as habitual residence (whoever the landlord is); the wording requires payment by card, bank transfer, nominative cheque or bank deposit | From 1 December 2026 | LIVA art. 91.Uno.2.10º, RDL 29/2026 art. 7.Tres and preamble |
| 4 % rate extended to protected homes with permanent or indefinite qualification (*viviendas protegidas sujetas a calificación permanente o indefinida*) sold by their developers | From 1 December 2026 | LIVA art. 91.Dos.1.6º, RDL 29/2026 art. 7.Cuatro and preamble |
| Régimen simplificado and REAGP limit of €250,000: extension for 2025 and 2026 enacted three times and repealed three times (RDL 9/2024, 16/2025, 2/2026); BOE consolidated DT 13ª still only names 2016-2024 | 2025-2026 | AEAT applies €250,000 for "2016 a 2026" (AEAT page updated 12/11/2026); treat 2027 as open |
| B2B e-invoicing regulation approved | RD 238/2026 in force 20 April 2026; the periods run from the entry into force of Orden HAC/1028/2026 on 6 October 2026: 12 months for volume over €8 million (about 6 October 2027), 24 months for the rest (about 6 October 2028) | See `spanish-e-invoicing` |
| Domestic small-business exemption (Directive (EU) 2020/285, applicable in the EU from 1 January 2025) | Not transposed: LIVA contains no such franquicia as of the 07/10/2026 consolidation | LIVA consolidated text |

## 2. Territory

| Place | IVA? | Consequence |
|---|---|---|
| Peninsula and Balearic Islands | Yes, *territorio de aplicación del impuesto* | Normal rules |
| Canarias | No (outside the harmonised VAT area): IGIC applies | Supplies of goods from the peninsula to Canarias are exports (art. 21); goods from Canarias are imports. Services follow arts. 69-70 place-of-supply rules, treating Canarias as a third territory |
| Ceuta and Melilla | No (outside the customs union): IPSI applies | Same as Canarias for goods |
| Basque Country, Navarra | Yes, IVA, but managed by the foral administrations | Who files where depends on domicile and volume (over €10 million: split by volume per territory). Casilla 65 of modelo 303 carries the territorio común percentage |

Source: LIVA art. 3.Dos.1º; Ley 12/2002 (Concierto) and Ley 28/1990 (Convenio).

## 3. Rates

### 3.1 Permanent rates (LIVA arts. 90-91)

| Rate | Goods and services |
|---|---|
| 21 % | Everything not listed below (art. 90.Uno). Includes alcohol, sugary soft drinks and juices (excluded from the food rate by art. 91.Uno.1.1º.b), professional services, most repairs, clothing, electronics, vehicles, software, used goods sold outside REBU |
| 10 % | Food and products for human or animal nutrition not at 4 %; animals and plants for food production; seeds, fertilisers, pesticides; water for food or irrigation; veterinary medicines; pharmaceutical products of CN chapter 30 not at 4 %; medical devices of Anexo apartado octavo for personal use of people with disabilities; homes (new) with up to two garage spaces; flowers and ornamental plants; passenger transport; hostelería, camping, spas, restaurants and food for immediate consumption; furnished rentals of art. 20.Uno.23º.e' (from 1 December 2026 includes stays of 30 nights or less); public cleaning, waste services; entry to libraries, museums, cinemas, theatres, concerts and live cultural shows; amateur sports events; trade fairs; renovation works on homes when the customer is a private person using the home privately or a community of owners (from 1 December 2026 also homes let as habitual residence, whoever the landlord, with payment by card, transfer, nominative cheque or bank deposit), the home was finished at least two years earlier and materials are 40 % or less of the base; lease with purchase option of homes; timeshare; services of performers to film producers; construction of homes under a direct contract with the developer (art. 91.Uno.3); imports of art and certain supplies of art (art. 91.Uno.4-5) |
| 4 % | Bread, bread flour, milk (natural, pasteurised, UHT, powdered, fermented etc.), cheese, eggs, natural fruit, vegetables, legumes, tubers and cereals, olive oils; books, newspapers and magazines, including digital, unless mainly advertising or video/music; medicines for human use; vehicles and wheelchairs for people with reduced mobility (with prior recognition for adapted vehicles); prostheses and implants for people with disabilities; VPO de régimen especial or promoción pública sold by the developer (from 1 December 2026 also protected homes with permanent or indefinite qualification); homes bought by entities in the IS residential-letting regime with the art. 49 LIS bonificación; tampons, pads, condoms and other non-medical contraceptives; teleassistance, home help and residential care services under Ley 39/2006 when publicly funded or concerted (art. 91.Dos) |
| 0 % | Donations of goods to non-profit entities of Ley 49/2002 used for their general-interest purposes (art. 91.Cuatro) |

Works that produce a good taxed at a reduced rate take that rate (art. 91.Tres).

### 3.2 Temporary rates 2023-2026 (outside LIVA, in RDLs)

| Product | 2023-H1 2024 | 1 Jul-30 Sep 2024 | 1 Oct-31 Dec 2024 | From 1 Jan 2025 |
|---|---|---|---|---|
| Bread, flour, milk, cheese, eggs, fruit, vegetables, legumes, tubers, cereals | 0 % (RE 0 %) | 0 % (RE 0 %) | 2 % (RE 0.26 %) | 4 % |
| Olive oil | 5 % (RE 0.62 %) | 0 % | 2 % | 4 % |
| Seed oils, pasta | 5 % (RE 0.62 %) | 5 % (RE 0.62 %) | 7.5 % (RE 1 %) | 10 % |

Sources: RDL 20/2022 art. 72 as extended by RDL 8/2023 art. 20 (1 January 2023 to 30 June 2024); RDL 4/2024 art. 1.

| Energy | Period | Rate | Source |
|---|---|---|---|
| Electricity ≤ 10 kW (when the previous month's wholesale price exceeded €45/MWh) and bono social severe vulnerability | 1 January-31 December 2024 | 10 % | RDL 8/2023 art. 21.1 |
| Natural gas | 1 January-31 March 2024 | 10 % | RDL 8/2023 art. 21.2 |
| Pellets, briquettes, firewood | 1 January-30 June 2024 | 10 % | RDL 8/2023 art. 21.3 |
| Electricity, gas, pellets, firewood, fuels | 2025 to 21 March 2026 | 21 % | General rate |
| Electricity ≤ 10 kW and bono social, gas, pellets, firewood | 22 March-31 May 2026 | 10 % | RDL 7/2026 art. 42 |
| Fuels (gasoline, diesel and other listed hydrocarbons) | 22 March-30 June 2026 | 10 % | RDL 7/2026 art. 42.c |
| Electricity, gas | July-October 2026 | 10 % only if CPI condition met | RDL 18/2026 (unverified) |
| Electricity ≤ 10 kW and bono social; gas, pellets, firewood | November and December 2026 | 10 % if CPI condition met, else 21 % | RDL 25/2026 arts. 18-19 |

When the reduced rate depends on a CPI condition, confirm on the AEAT news page for the month before invoicing or booking. Recargo de equivalencia follows the rate band (1.4 % with a 10 % IVA rate).

### 3.3 Recargo de equivalencia rates (art. 161)

| IVA rate | Recargo |
|---|---|
| 21 % | 5.2 % |
| 10 % | 1.4 % |
| 4 % | 0.5 % |
| Tobacco (Impuesto sobre las Labores del Tabaco) | 1.75 % |

## 4. Exemptions (art. 20)

Exempt operations carry no IVA and give no right to deduct, unless the law says otherwise (art. 94: exports and intra-EU supplies are exempt with deduction). The main ones:

| Art. 20.Uno | Exemption | Typical trap |
|---|---|---|
| 2º, 3º, 5º | Hospital and medical care, doctors and health professionals, dentists | Aesthetic treatments without a therapeutic purpose are taxed at 21 % |
| 8º | Social assistance by public or social entities | Requires *carácter social* (art. 20.Tres) |
| 9º, 10º | Education of children and youth, officially recognised education; private lessons by individuals on curriculum subjects | Corporate training by a company is usually taxed |
| 16º | Insurance | Brokers' commissions exempt, claims handling outsourced is not always |
| 18º | Financial operations: loans, payment services, transfers, current accounts | Card-processing fees are normally exempt; advisory and custody fees can be taxed |
| 20º | Land that is not building land | Waivable (art. 20.Dos) |
| 22º | Second and later deliveries of buildings | Waivable when the buyer is a business with full or partial deduction right; then reverse charge (art. 84.Uno.2º.e) |
| 23º | Rental of land and of buildings used as homes | Not exempt: commercial premises, garages rented separately, furnished rentals with hotel services or of 30 nights or less (from 1 December 2026), rental to a company even if the employee lives there (DGT doctrine) |
| 24º, 25º | Delivery of goods used only in exempt activities, or whose purchase had no deduction right | Sale of a car bought without deduction is exempt |
| 26º | Author's rights services by artists, writers, translators etc. | |

The art. 20.Dos waiver for 20º and 22º requires the buyer to be a business with a full or partial deduction right, and it is communicated in the deed or separately.

## 5. Devengo (when VAT is due)

| Operation | Devengo (art. 75) |
|---|---|
| Delivery of goods | When goods are put at the buyer's disposal |
| Services | When performed; continuous services at each payment due date |
| Advance payment (anticipo) | When paid, for the amount paid (art. 75.Dos) |
| Intra-EU supply exempt (art. 25) | 15th of the month after dispatch, or invoice date if earlier (art. 75.Uno.8º) |
| Reverse charge services | When performed |
| Criterio de caja | When collected; at the latest 31 December of the following year (art. 163 terdecies) |

The invoice date does not decide the period; devengo does.

## 6. Domestic inversión del sujeto pasivo (art. 84.Uno.2º)

The Spanish business buyer self-assesses the IVA (credit **477**, debit **472** if deductible) and the seller invoices without IVA, with the mention "inversión del sujeto pasivo".

| Letter | Operation | Conditions |
|---|---|---|
| a) | Supplies of goods and services by a supplier not established in Spain to a Spanish business | Not for exempt supplies, distance sales, or rentals of property; the buyer must be a business or professional |
| b) | Unwrought or semi-wrought gold of 325 thousandths or more | Also investment gold under art. 140 quinque when waived |
| c) | Scrap, waste and recovered materials (ferrous and non-ferrous metals, plastic, paper, cardboard, glass, textiles), their processing, and semi-finished non-ferrous metal products (ingots, bars etc.) except nickel | Anexo of LIVA lists the materials |
| d) | Greenhouse gas emission allowances | |
| e) | Property supplies: in insolvency proceedings, exempt supplies where the exemption was waived, and foreclosures (also dation in payment) | Buyer must be a business |
| f) | Construction or renovation works and staff provision under a direct contract between developer (*promotor*) and contractor for urbanisation, construction or rehabilitation of buildings; also to the main contractor and subcontractors | Buyer must communicate in writing that it acts as a business and that the works are urbanisation/construction/rehabilitation (RIVA art. 24 quater.3-4); see `spanish-industry-construccion` |
| g) | Silver, platinum, palladium; mobile phones, game consoles, laptops and tablets | Phones, consoles, laptops, tablets only when the buyer is a reseller, or another business and the invoice exceeds €10,000 excluding IVA |

Sanction for not self-assessing: 10 % of the unreported cuota (arts. 170.Dos.4º and 171.Uno.4º), even though the net effect is zero.

## 7. Deduction: requirements, timing, limits

### 7.1 Requirements

| Requirement | Rule |
|---|---|
| Document | Valid full invoice (*factura completa*) in the buyer's name, the DUA for imports, or the self-assessment for reverse charge (art. 97). A simplified invoice deducts only if the business buyer asked for its NIF and address and the separate cuota to be shown (RD 1619/2012 art. 7.2) |
| Use | Goods and services used directly and exclusively in the business (art. 95.Uno). Mixed-use goods: see vehicles below |
| Timing | Deduction arises at devengo of the cuota (art. 98). Deduct in that period or any later one within four years (art. 99.Tres) |
| Excess | An excess of deductible over payable can be compensated within four years from the return in which it arose, or refunded in the last period of the year (art. 99.Cinco and 115) or monthly if in REDEME |
| Registration | The invoice must be recorded in the libro registro de facturas recibidas (or SII) |

### 7.2 Limits (arts. 95-96)

| Item | Rule | Source |
|---|---|---|
| Passenger cars, motorcycles, mopeds (including mixed vehicles and 4x4) | Presumed 50 % business use; deduct 50 % unless the taxpayer proves a different real use. 100 % presumption for vans used to carry goods, taxis, driving schools, manufacturers' test cars, sales representatives' cars, security services | Art. 95.Tres.2ª |
| Fuel, repairs, parts, parking, tolls of those vehicles | Same percentage as the vehicle | Art. 95.Cuatro |
| Proof | Any evidence; the 303 or the accounting entry is not proof (art. 95.Tres.4ª). AEAT expects logbooks, routes, client visits | |
| Jewellery, precious stones, gold or platinum objects | No deduction | Art. 96.Uno.1º |
| Food, drinks, tobacco | No deduction, unless bought for resale or for a business that supplies them | Art. 96.Uno.3º and Dos |
| Entertainment and leisure services | No deduction | Art. 96.Uno.4º |
| *Atenciones a clientes, asalariados o terceros* (gifts, client meals) | No deduction, except free samples and promotional items of small value (art. 7.2º and 4º: up to €200 per recipient per year) | Art. 96.Uno.5º |
| Travel, hotels, restaurants | Deductible only if the expense is deductible for IRPF or IS (business trip of staff, properly documented) | Art. 96.Uno.6º |
| Goods not in the accounts or not part of business assets | No deduction | Art. 95.Dos.3º-4º |

Non-deductible IVA increases the cost of the asset or expense (PGC NRV 2ª and 12ª). It is not an IVA balance.

### 7.3 Deductions before starting activity

Input VAT on purchases before the first sale is deductible if the intention to start is shown by objective evidence (art. 111). Register with modelo 036 first. Refund can be requested in the last period of the year, or monthly by joining REDEME.

## 8. Base modification: credit notes and bad debts

| Case | Rule | Source |
|---|---|---|
| Returns, discounts after the sale, cancelled sale | Issue a factura rectificativa; reduce base in the period of the rectification (or of devengo for errors); within four years of devengo | Art. 80.Dos, art. 89; RD 1619/2012 art. 15 |
| Customer in insolvency (*concurso*) | Modification within the deadline set by art. 80.Tres (two months after the deadline for creditors' claims under the Ley Concursal) | Art. 80.Tres |
| Unpaid debt (*crédito incobrable*) | Conditions: one year from devengo without collection (six months or one year if the creditor's volume was ≤ €6,010,121.04); recorded in the books; buyer is a business or the base exceeds €50; claim by court or notarial demand. Issue the rectificativa within six months after that period | Art. 80.Cuatro |
| Notice to AEAT | Communicate electronically within one month of issuing the rectificativa | RIVA art. 24.2 |
| Buyer side | The buyer reduces its deducted cuota in the period it receives the rectificativa (casillas 40-41 of the 303) | Art. 80.Cinco |

Never reduce the base for a bad debt by simply booking a provision.

## 9. Periods, returns and deadlines

| Modelo | Purpose | Who | Period and deadline | Source |
|---|---|---|---|---|
| 303 | Periodic self-assessment | Every business or professional, also with no operations, except those with only exempt art. 20 operations | Quarter: 1-20 April, July, October; 4T 1-30 January. Month: 1-30 of next month; January return by last day of February | RIVA art. 71.3-4; AEAT Manual IVA 2026 |
| 390 | Annual summary | All 303 filers except SII filers and quarterly filers with only simplificado and/or urban letting in territorio común | 1-30 January | RIVA art. 71.7; Orden of the 390 |
| 349 | Recapitulative of intra-EU operations | Anyone with intra-EU supplies, acquisitions, services, triangulation, call-off stock | Monthly 1-20 of next month (July by 20 September); quarterly if ≤ €50,000 per quarter in the quarter and the previous four; last period by 30 January | RIVA arts. 78-81 |
| 309 | Non-periodic IVA return | Non-filers who must pay IVA occasionally: e.g. a private person buying a new car in another EU country, RE retailers on intra-EU acquisitions or reverse charge purchases, REAGP farmers | Per operation (RE: quarterly) | RIVA art. 71.8 and others |
| 369 | OSS/IOSS return | Registered in the Union, non-Union or import scheme | Quarterly for Union/non-Union, by end of the month after the quarter; monthly for IOSS, by end of next month | LIVA arts. 163 duovicies, 163 septvicies |
| 035 | Registration in OSS/IOSS | Same | Before the first operation | Orden HAC/610/2021 (unverified number) |
| 036 | Censal registration (alta, ROI for intra-EU, REDEME, SII option, special schemes) | Everyone | Before starting; options in November or at alta | RD 1065/2007. Modelo 037 abolished from February 2025 (unverified) |
| 308 | Refund for occasional sellers of new means of transport to the EU, RE retailers exporting etc. | Special cases | Per operation | |
| 322 / 353 | Grupo de entidades, individual and aggregate | Groups | Monthly | |

Monthly filers are exactly those in RIVA art. 71.3: volume over €6,010,121.04 in the previous year (art. 121 LIVA volume), acquirers of a business whose combined volume crosses that amount, REDEME members, IVA groups and hydrocarbon fiscal warehouses. All monthly filers must use SII (RIVA art. 62.6), which is why their deadline is 30 days.

The 4T or December 303 is where the definitive prorrata (casilla 44), capital goods regularisation (casilla 43) and the prorrata especial option go.

The corrective return is an *autoliquidación rectificativa* filed on the same modelo 303 (casillas 70, 108, 109, 111), not a complementary return or a rectification request (RIVA art. 74 bis, added by RD 117/2024; AEAT Instrucciones 2026).

## 10. SII and REDEME

**SII (Suministro Inmediato de Información)**, RIVA arts. 62.6 and 69 bis:

| Point | Rule |
|---|---|
| Who must | Every monthly filer: volume over €6,010,121.04, REDEME, IVA groups. Others may opt (RIVA art. 68 bis), option in November for the next year, minimum one year |
| Issued invoices | Within four calendar days of issue (eight days if issued by the customer or a third party), and before the 16th of the month after devengo |
| Received invoices | Within four calendar days of booking, and before the 16th of the month after the period in which they are deducted |
| Imports | Four days from booking the DUA, before the 16th of the following month |
| Rectificativas | Four days from issue or booking |
| Weekends | Saturdays, Sundays and national holidays do not count in the four days (RIVA art. 69 bis.1, last paragraph) |
| Effect | Exempt from modelo 390 (and 347 and 340) |
| Sanction for late reporting | 0.5 % of the invoice amount, minimum €300 and maximum €6,000 per quarter (LGT art. 200.3) |

**REDEME (registro de devolución mensual)**, RIVA art. 30: lets any business recover excess IVA monthly instead of waiting for the last period. Join in November for the next year (or in the period of the return, or before starting activity); minimum one year; requires monthly 303, SII and electronic notifications. Exclusion bars re-entry for three years.

## 11. Sanctions and late filing

| Situation | Consequence | Source |
|---|---|---|
| Late 303 filed voluntarily, no AEAT request | Recargo 1 % plus 1 % per full month of delay; after 12 months 15 % plus late interest; recargo reduced by 25 % if paid on time | LGT art. 27 |
| Not paying the tax due (AEAT finds it) | Sanction 50 % (leve) to 150 % (muy grave) of the amount; reduced 30 % for conformidad and a further 40 % for prompt payment (LGT art. 188.1.b and 188.3) | LGT arts. 191, 188 |
| Overclaimed refund or compensation | Art. 193 (obtaining undue refunds) or art. 195 (improper compensation balance: 15 %) | LGT |
| Not reporting reverse charge | 10 % of the cuota | LIVA art. 171.Uno.4º |
| Not reporting deferred import VAT in the 303 | 10 % of the cuota | LIVA art. 171.Uno.7º |
| Retailer buying without recargo de equivalencia on the invoice | 50 % of the recargo, minimum €30 per purchase | LIVA art. 171.Uno.1º |
| Late informative return (349) without economic loss | €20 per data set, minimum €300, maximum €20,000; halved if filed late without an AEAT request | LGT art. 198.1-2 |
| Inaccurate books | 1 % of the amounts, €150 to €6,000 | LGT art. 200.3 |
| SII late | 0.5 % of invoice amount, €300 to €6,000 per quarter | LGT art. 200.3 |

## 12. Error patterns

1. **Foreign service booked with no IVA at all.** Google Ads, Meta, AWS, Shopify, Amazon fees from EU entities are B2B services: casillas 10-11 (intra-EU acquisitions of services) with **477**/**472** and modelo 349 key I. Non-EU suppliers: casillas 12-13.
2. **Foreign VAT on the invoice booked as deductible.** Foreign VAT is never deductible in the 303. Ask the supplier for a corrected invoice; recover through the EU refund procedure (modelo 360) only where it was legitimately charged.
3. **Domestic reverse charge one-sided.** Booking only **472** or only the net cost. Both sides must appear (casillas 12-13 and 28-29).
4. **Car at 100 %.** Passenger cars deduct 50 % by default; the AEAT routinely rejects 100 % without evidence.
5. **Client meals and gifts deducted.** Excluded by art. 96.Uno.5º regardless of IS treatment.
6. **Exempt income ignored.** Renting a flat, training, medical services or interest income in the same company triggers prorrata; deducting 100 % is the most common audit adjustment.
7. **Invoice date used instead of devengo.** Advances, continuous services and intra-EU supplies have their own devengo.
8. **Intra-EU supply without a valid VIES number.** The exemption fails; Spanish IVA is due. Check VIES on the date of supply and keep the screenshot.
9. **Canarias treated as intra-EU.** Goods to Canarias are exports (casilla 60), not intra-EU supplies (casilla 59), and do not go in modelo 349.
10. **Unclosed IVA accounts.** **472** and **477** must be cleared every period into **4750** or **4700**; a residual balance means an entry is missing.
11. **Old temporary rates kept.** Food rates of 0 %, 2 %, 5 % and 7.5 % ended on 31 December 2024. Energy at 10 % in 2026 applies only in the months and to the products listed.
12. **Bad debt reduced without the procedure.** No court or notarial claim, no notice to AEAT within a month: the reduction is rejected.
