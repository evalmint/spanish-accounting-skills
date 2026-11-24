# Healthcare: mixed activity, prorrata and running a clinic

What changes once a clinic has taxable income next to exempt healthcare, and the tax, legal-form, social security and data rules a clinic's books depend on. Checked against boe.es consolidated texts on 24 November 2026. Prorrata mechanics in depth are in `spanish-vat`.

## Contents

- [1. When the clinic is mixed](#1-when-the-clinic-is-mixed)
- [2. Prorrata general](#2-prorrata-general)
- [3. Prorrata especial](#3-prorrata-especial)
- [4. Sectores diferenciados](#4-sectores-diferenciados)
- [5. Investment goods and premises](#5-investment-goods-and-premises)
- [6. A fully exempt clinic](#6-a-fully-exempt-clinic)
- [7. Legal form, retentions and mutualidades](#7-legal-form-retentions-and-mutualidades)
- [8. Patient data in the accounting records](#8-patient-data-in-the-accounting-records)
- [9. Software: Verifactu and e-invoicing](#9-software-verifactu-and-e-invoicing)
- [10. Registro sanitario and other permits](#10-registro-sanitario-and-other-permits)
- [11. Monthly checklist](#11-monthly-checklist)

## 1. When the clinic is mixed

A clinic is mixed when, in the same business activity, it makes supplies that give the right to deduct (aesthetic treatments, product sales, room lettings, expert reports) and exempt supplies that do not (healthcare). The *regla de prorrata* then applies (LIVA art. 102). Typical mixed cases: a dental clinic that also whitens teeth and sells oral-care products; a medical clinic with an aesthetic medicine unit; a physiotherapy centre that runs fitness classes; an optician (exempt tests, taxed glasses).

First decide whether the taxable side is a separate *sector diferenciado* (§4). If not, apply prorrata to the single sector.

## 2. Prorrata general

| Rule | Detail | Basis |
|---|---|---|
| What is deductible | Only the percentage of **all** input IVA, including IVA on costs used only for taxable supplies; there is no direct attribution under the general rule | art. 104.Uno |
| Percentage | Taxable supplies giving the right to deduct / total supplies (taxable + exempt), for the calendar year | art. 104.Dos |
| Rounding | Rounded **up** to the next whole number | art. 104.Dos, last paragraph |
| Excluded from both sides | Sales of investment goods, occasional property and financial operations, and some others | art. 104.Tres |
| During the year | Provisional percentage = last year's definitive one (or a reasonable estimate in the first year) | art. 105 |
| Last return of the year | Recalculate with the definitive percentage and regularise the year's deductions | art. 105.Tres |

Example: taxable turnover 30,000 €, exempt healthcare 170,000 € → 30,000 / 200,000 = 15 %. Of 10,000 € input IVA, 1,500 € is deductible; 8,500 € is a cost (added to the expense or asset).

Accounting: the non-deductible part is booked as part of the cost of each item (PGC NRV 12.ª), or at regularisation to **634** (negative adjustment) or **639** (positive) when the definitive percentage differs.

## 3. Prorrata especial

- Input IVA on goods and services used **exclusively** for taxable supplies is deducted in full; on those used exclusively for exempt supplies, not at all; on common costs, by the general percentage (art. 106).
- Optional: elect it in the last return of the calendar year, with effect for that year, or at the start of the activity; the election lasts at least three years (RIVA art. 28.1.1.º).
- **Compulsory** when the deduction under the general rule exceeds that under the special rule by 10 % or more in a year (LIVA art. 103.Dos.2.º). A clinic whose taxable activity has heavy specific costs (an aesthetic laser used only for cosmetic treatments) may fall into this case without noticing. Run both calculations each year.
- Requires the books to identify costs by use; ask whether the clinic tracks this before recommending it.

## 4. Sectores diferenciados

Activities form separate sectors, each with its own deduction regime, when both conditions hold (LIVA art. 9.1.º c a'):

1. They are **different economic activities**: assigned different groups (three-digit level) of the CNAE. Medical and dental practice and beauty treatments sit in different groups (codes to be checked against the CNAE in force, now CNAE-2025; unverified mapping).
2. Their **deduction percentages differ by more than 50 points**: healthcare near 0 % and aesthetics at 100 % qualify.

An accessory activity whose turnover did not exceed 15 % of the main activity's in the previous year, and which contributes to it, is not treated as distinct and follows the main activity. If the aesthetic or product side is above 15 % and in a different CNAE group, it is a separate sector: input IVA on its exclusive costs is fully deductible, the healthcare sector deducts nothing, and common costs are apportioned using the general prorrata of the whole business (art. 101 and 104; see `spanish-vat`).

Moving goods from one sector to another is a self-supply (*autoconsumo*, art. 9.1.º c), with IVA consequences; ask before reallocating equipment.

## 5. Investment goods and premises

- Investment goods (items expected to last more than a year, other than those costing up to 3,005.06 € under LIVA art. 108) have their deduction regularised over the year of use and the following **four** years (nine for property) whenever the definitive percentage differs by **more than 10 points** from the year of purchase (art. 107).
- Expensive equipment (lasers, CBCT scanners, ultrasound) should be logged with its purchase-year percentage for this purpose.
- **Rent of premises**: a landlord letting business premises charges IVA at 21 % regardless of the tenant's activity; the exempt clinic simply cannot deduct it (or deducts the prorrata share). The landlord must also have the 19 % IRPF retention applied (modelo 115) unless an exception applies (see `spanish-daily-bookkeeping`).
- Fit-out works on leased premises are assets (**211** or other **21x** accounts per their nature; see `spanish-asset-accounting`).

## 6. A fully exempt clinic

- A business that only makes supplies exempt under LIVA art. 20 is not required to file periodic IVA returns or the annual summary (RIVA art. 71.1, third paragraph).
- It must still self-assess IVA on purchases where it is the taxpayer (services from foreign suppliers such as software subscriptions, intra-EU purchases of equipment), which in practice requires filing modelo 303 for those periods and, for intra-EU operations, modelo 349 (unverified: the interaction with RIVA art. 71.1 should be confirmed with `spanish-vat`). That IVA is not deductible and becomes a cost.
- It must still issue invoices for exempt healthcare (RD 1619/2012 art. 3.1.a) and file the annual third-party return (modelo 347) where amounts exceed 3,005.06 € per counterparty.
- All input IVA is part of cost: book supplier invoices gross, without **472**.

## 7. Legal form, retentions and mutualidades

| Form | Tax | Points to check |
|---|---|---|
| Individual professional (*profesional colegiado*) | IRPF, rendimientos de actividades económicas, usually estimación directa; quarterly modelo 130 unless 70 %+ of income bears retention | Invoices to clinics and insurers carry 15 % retention (7 % in the start year and two following years, if no professional activity in the prior year, with written notice to the payer) (RIRPF art. 95.1) |
| Clinic company (SL) | IS; see `spanish-corporate-tax` | No IRPF retention on its invoices; payments to self-employed doctors carry retention (**4751**, modelo 111 and 190) |
| Sociedad profesional (Ley 2/2007) | IS | Required where the company's object is the common exercise of a profession requiring a degree and college membership; registered in the Registro Mercantil and the college's register (Ley 2/2007 art. 1, 8). A company that merely provides facilities to independent doctors is not one |
| Socio-doctor working in his or her own SL | Income for professional services to the company is activity income for the socio when he or she is in RETA or a mutualidad alternativa (LIRPF art. 27.1, third paragraph); the socio invoices the company, exempt if healthcare, with 15 % retention. Related-party valuation applies (LIS art. 18) | See `spanish-autonomo-tax` and `spanish-corporate-tax` |

**Mutualidades alternativas al RETA.** College-registered professionals (doctors, for example with Mutual Médica, and others) may insure with a professional mutual instead of joining RETA (LGSS DA 18.ª and 19.ª).
- IRPF: contributions to the mutual acting as an alternative to RETA are a deductible expense up to the RETA maximum contribution for common contingencies of that year (LIRPF art. 30.2.1.ª); the excess may reduce the tax base as social welfare contributions (LIRPF art. 51).
- **Pasarela al RETA (new in 2026)**: Ley 2/2026, de 29 de julio (BOE 31-7-2026, BOE-A-2026-16653), amends LGSS DA 18.ª and 19.ª to let mutualistas transfer their accumulated rights to the Seguridad Social and move into RETA. The application window opens with the implementing regulation, which had not been confirmed as published on 24-11-2026 (unverified). The law's minimum-contribution changes for mutualidades (reported as a phased percentage of the RETA reference contribution) are also unverified here; check `spanish-autonomo-tax`.
- Accounting for an SL: the company does not pay the socio's mutual contributions unless agreed; if it does, they are remuneration to the socio.

## 8. Patient data in the accounting records

- Health data are a special category under GDPR art. 9; the LOPDGDD (LO 3/2018) and its DA 17.ª govern their processing in Spain.
- Accounting and tax records need the patient's identity on full invoices (RD 1619/2012 art. 6.1.d) but not the diagnosis. Keep invoice concepts generic and keep clinical detail in the clinical record, not in the ledger, bank references or invoice descriptions.
- The gestoría, accounting software and Verifactu provider are data processors: a written processing agreement is required (GDPR art. 28).
- Retention periods differ: accounting books and supporting documents six years from the last entry (Código de Comercio art. 30); tax records at least the four-year limitation period (LGT art. 66 and 70); clinical records at least five years from discharge of each episode (Ley 41/2002 art. 17.1). Do not keep clinical documents in the accounting file to "save time".
- Evidence for the therapeutic purpose of an exempt aesthetic treatment (`iva-exento-sanidad.md` §3) lives in the clinical record; in an AEAT check, provide it in a way that discloses only what is needed (ask the clinic's data protection officer).

## 9. Software: Verifactu and e-invoicing

- Clinics and professionals that invoice with software fall under RD 1007/2023 (Verifactu) whether their supplies are exempt or not: companies from 1-1-2027, individual professionals from 1-7-2027 (RD 1007/2023 DF 4.ª, as amended by RDL 15/2025). Clinics in the Basque Country use TicketBAI instead.
- Mandatory B2B e-invoicing (Ley 18/2022, RD 238/2026) will cover invoices to insurers, other clinics and companies: 12 months after the Orden HAC/1028/2026 (in force 6-10-2026) for businesses with turnover above 8 million €, 24 months for the rest. Invoices to patients (B2C) are outside it. Check the exact dates in `spanish-e-invoicing`.

## 10. Registro sanitario and other permits

- Every health centre, service or establishment needs authorisation from the regional health authority and is entered in the *Registro General de centros, servicios y establecimientos sanitarios* (RD 1277/2003). Aesthetic medicine is a specific health unit (U.48 in RD 1277/2003 annex). The authorisation number must appear in advertising.
- Purely aesthetic beauty salons are not health centres and cannot offer medical treatments; a salon booking "botox" without a health authorisation is a legal risk, not only a tax one.
- Ask for the authorisation and the registered units: they also help support the exemption for services within those units.

## 11. Monthly checklist

1. Split income into exempt healthcare, taxed services and product sales by rate.
2. Apply the provisional prorrata (or sector rules) to input IVA; book the non-deductible part to cost.
3. For each doctor's invoice: exempt, retention 15 % or 7 % if an individual, none if a company.
4. Check new equipment for the investment-goods log.
5. Keep aesthetic treatment indications documented in the clinical record.
6. December: compute the definitive prorrata, compare general and special, regularise in the last return, and update the investment-goods regularisations.
