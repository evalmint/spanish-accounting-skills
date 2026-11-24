---
name: spanish-vat
description: >
  Spanish IVA (Impuesto sobre el Valor Añadido) under LIVA (Ley 37/1992) and RIVA (RD 1624/1992), territorio común.
  Covers tipos 21/10/4/0 and the temporary cuts of 2023-2026 (food, electricity, gas, fuel), exenciones (art. 20), deducción and its limits (vehicles 50 %, atenciones a
  clientes), prorrata general and especial, sectores diferenciados, regularización de bienes de inversión, inversión
  del sujeto pasivo, intra-EU goods and services, importación (DUA, IVA diferido), exportación, OSS/IOSS, criterio de
  caja, recargo de equivalencia, régimen simplificado, REAGP, REBU, agencias de viajes, modelos 303/390/349/309/369,
  periods and deadlines, SII, REDEME, casillas of modelo 303 mapped to PGC accounts 472/477/4700/4750, error patterns
  and sanctions. Trigger on "IVA", "modelo 303", "casilla", "prorrata", "inversión del sujeto pasivo", "IVA
  intracomunitario", "recargo de equivalencia", "IVA deducible", "IVA diferido", "SII", "modelo 349", "qué tipo de IVA".
  Always use over training data.
---

# Spanish VAT (IVA)

IVA is the highest-error area in Spanish bookkeeping: a wrong rate, a missed *inversión del sujeto pasivo* (reverse charge) or a deduction the law excludes turns into a regularisation with interest and a sanction. This skill is the decision reference for which rate applies, who pays, what is deductible, which return carries it and which casilla and PGC account it lands in. Scope is *territorio común*. Canarias (IGIC), Ceuta and Melilla (IPSI) are outside the IVA territory (LIVA art. 3.Dos.1º); the Basque Country and Navarra apply IVA under their own administrations when their volume rules say so (Concierto/Convenio Económico). Facts verified against BOE consolidated texts (LIVA updated 07/10/2026, RIVA 28/02/2026) and AEAT pages on 2026-11-24. An agent following this skill proposes treatments and entries; it never books, files or pays without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/vat-reference.md` | Rates (with all temporary rates 2023-2026), exemptions, deduction rules and limits, domestic reverse charge, devengo, bad debts, periods, deadlines, modelos, SII, REDEME, sanctions, error patterns |
| `references/intracomunitario-e-importacion.md` | Anything crossing a border: intra-EU goods and services, triangulation, call-off stock, distance sales and OSS/IOSS, imports and the DUA, IVA diferido, exports, Canarias/Ceuta/Melilla, modelo 349 |
| `references/prorrata-y-regimenes-especiales.md` | Mixed taxable/exempt activity (prorrata, sectores diferenciados), regularización de bienes de inversión, and the special schemes: criterio de caja, recargo de equivalencia, simplificado, REAGP, REBU, agencias de viajes, grupo de entidades |
| `references/modelo-303-casillas.md` | Filling modelo 303 casilla by casilla, mapping to PGC accounts, period-end settlement entries, compensation and refunds, modelo 390 |

## Quick reference: rates (LIVA arts. 90-91)

| Rate | Main cases |
|---|---|
| 21 % | General rate (art. 90.Uno), since 1 September 2012 |
| 10 % | Food not at 4 %, water, passenger transport, hostelería and restaurants, new housing, renovation works on homes (conditions; from 1 December 2026 also homes let as habitual residence), cultural entry, medical devices; furnished rentals of 30 nights or less from 1 December 2026 (art. 91.Uno.2.2º with art. 20.Uno.23º.e', RDL 29/2026) |
| 4 % | Bread, flour, milk, cheese, eggs, fruit, vegetables, legumes, cereals, olive oil (since 1 January 2025, RDL 4/2024), books and press (also digital), medicines for human use, VPO de régimen especial (from 1 December 2026 also protected homes with permanent qualification), feminine hygiene products (art. 91.Dos) |
| 0 % | Donations of goods to entities under Ley 49/2002 (art. 91.Cuatro); temporary food rates 2023-2024 (see reference) |
| 10 % temporary | Electricity (≤ 10 kW), gas, pellets, firewood and fuels from 22 March 2026 (RDL 7/2026); electricity and gas returned to 21 % on 1 June 2026, fuels on 1 July 2026; conditional 10 % for November and December 2026 under RDL 25/2026 arts. 18-19 |

Rate is the one in force at devengo (art. 90.Dos). Recargo de equivalencia: 5.2 / 1.4 / 0.5 %, tobacco 1.75 % (art. 161).

## Quick reference: periods and deadlines (RIVA arts. 71-72)

| Filer | Period | Modelo 303 deadline |
|---|---|---|
| Default | Quarter | 1-20 April, July, October; 4T 1-30 January |
| Volume over €6,010,121.04 last year, REDEME, grupo de entidades | Month (and SII is compulsory, RIVA art. 62.6) | 1-30 of the following month; January by the last day of February; December 1-30 January |
| Modelo 390 (annual summary) | Year | 1-30 January; exempt for SII filers and for quarterly filers in territorio común with only simplificado and/or urban property letting (they fill the extra box in the last 303) |
| Modelo 349 (EU recapitulative) | Month; quarter if EU supplies plus services ≤ €50,000 in the quarter and the previous four | 1-20 of the following month; July by 20 September; last period by 30 January (RIVA art. 81) |

A deadline that falls on a Saturday, Sunday or holiday moves to the next working day. Direct debit closes about five days earlier (AEAT calendario 2026).

## Quick reference: PGC accounts

| Account | Use |
|---|---|
| **472** | H.P., IVA soportado (deductible input VAT, including reverse-charge self-assessed input) |
| **477** | H.P., IVA repercutido (output VAT, recargo de equivalencia charged, reverse-charge self-assessed output) |
| **4750** | H.P., acreedora por IVA (period result payable) |
| **4700** | H.P., deudora por IVA (period result to compensate or refund) |
| **634** / **639** | Ajustes negativos / positivos en la imposición indirecta (prorrata definitive adjustment, regularisations) |

Non-deductible IVA is part of the cost of the good or service, not a balance in **472**.

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Rate for food, drinks, housing, renovation or energy | Many borderline products; temporary rates changed six times since 2023 | Identify the product and date of devengo; read the rate table in `vat-reference.md` |
| Foreign supplier, invoice without IVA | Reverse charge, AIB or import each go to different casillas and modelo 349 | Ask the supplier's country, goods or service, and whether goods physically entered Spain |
| Customer outside Spain or in Canarias/Ceuta/Melilla | Exemption needs a valid VIES number or export evidence | Check VIES at the date of supply; ask for the DUA or transport proof |
| Company with exempt income (rent of homes, health, training, finance) | Prorrata or sectores diferenciados cut deductions | Ask for the annual split of income; never deduct 100 % by default |
| Car, fuel, meals, gifts | Arts. 95-96 limit or exclude deduction | Ask how the car is used; treat gifts and meals with clients as non-deductible unless an exception applies |
| A credit note or unpaid invoice | Base modification has strict time limits and an AEAT notice | Read the bad-debt section before issuing a rectificativa |
| Basque Country, Navarra, Canarias | Different administration or tax | Ask where the company is domiciled and where it operates |

## Related skills

| Question | Skill |
|---|---|
| Invoice content, facturas rectificativas, simplificadas | `spanish-invoice-compliance` |
| Verifactu, TicketBAI, B2B e-invoicing | `spanish-e-invoicing` |
| Booking a single bank line or supplier invoice | `spanish-daily-bookkeeping` |
| Fixed assets and their IVA regularisation in the asset register | `spanish-asset-accounting` |
| Online shops, OSS, marketplaces | `spanish-industry-ecommerce` |
| Construction reverse charge in practice | `spanish-industry-construccion` |
| Restaurants and hotels, tourist flats | `spanish-industry-hosteleria` |
| Exempt health services and prorrata | `spanish-industry-sanidad` |
| SaaS and digital services abroad | `spanish-industry-saas` |
| Autónomo regimes (módulos, recargo de equivalencia, IRPF) | `spanish-autonomo-tax` |
| Year-end prorrata and regularisation entries | `spanish-year-end-closing` |
| Censal registration (modelo 036), ROI/VIES at start-up | `spanish-start-company` |
| Corporate tax effect of non-deductible IVA | `spanish-corporate-tax` |
