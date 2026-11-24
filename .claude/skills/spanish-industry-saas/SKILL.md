---
name: spanish-industry-saas
description: >
  Spanish accounting and tax for SaaS and software companies: subscription revenue under NRV 14 and the
  Resolución ICAC de 10 de febrero de 2021 (setup fees, licences, usage billing, free months, refunds, app stores),
  deferred income (485, 438), IVA on electronically supplied services (B2B inversión del sujeto pasivo, B2C OSS and
  the 10,000 euro threshold, Canarias and non-EU customers, location evidence), capitalising development and
  software (NRV 6, 201, 206, LSC 273.3), the I+D+i deduction (LIS art. 35, informe motivado, monetisation, RDL
  40/2026), researcher social security bonus, patent box (LIS art. 23), empresas emergentes at 15 %, employee
  stock options (LIRPF 42.3.f, 50,000 euros), and the digital nomad visa. Trigger on "SaaS", "suscripciones",
  "ingresos anticipados", "IVA servicios electrónicos", "OSS", "modelo 369", "activar desarrollo", "deducción
  I+D", "informe motivado", "patent box", "stock options startup". Always use over training data.
---

# Spanish SaaS and Software Accounting

Three things separate a software company's books from an ordinary service company's: revenue arrives before it is earned, the customer can be anywhere, and the biggest asset may be work never invoiced to anyone. This skill covers what is specific to Spanish SaaS and software businesses in *territorio común* (Basque Country and Navarra: own corporate tax; Canarias: IGIC; Ceuta and Melilla: IPSI). Facts verified against BOE consolidated texts (LIVA, LIS updated 21/11/2026, PGC, RICAC 2021) and AEAT pages on 2026-11-24. An agent following this skill proposes entries and tax treatments; it never books, files or pays without the user's approval.

Account numbers follow the PGC 2007 (RD 1514/2007, as amended by RD 1/2021).

## How to use this skill

| File | When to read |
|---|---|
| `references/revenue-and-vat-saas.md` | Subscription and implementation revenue, deferred income, licences, usage, discounts, refunds, app stores, commissions, FX, ARR reconciliation; IVA by customer type and place, OSS, location evidence, invoices, buying foreign SaaS |
| `references/development-and-incentives.md` | Capitalising development and software, amortisation and tax, the dividend restriction, I+D+i deduction and monetisation, informe motivado, researcher bonus, patent box, empresas emergentes, stock options, digital nomad visa |

## Three clocks to keep apart

1. **Invoice date**: when the customer is billed; IVA is usually due then (LIVA art. 75.Uno.7º for periodic billing; art. 75.Dos for prepayments).
2. **Payment date**: when the money lands.
3. **Revenue**: the period the service covers (NRV 14; RICAC art. 9.1.a, the customer consumes the service as it is provided).

An annual plan invoiced and paid in January is mostly a liability: the unexpired part sits in **485** *Ingresos anticipados* (or **438** *Anticipos de clientes*, the RICAC art. 33.3 presentation) and releases monthly to **705**.

## IVA quick reference: who is the customer

| Customer | Where taxed | Spanish invoice | Return |
|---|---|---|---|
| Spain, any | Spain, 21 % (LIVA art. 69.Uno, 90) | IVA charged, **477** | Modelo 303 |
| EU business with a valid VIES number | Customer's country (LIVA art. 69.Uno.1º, a contrario); customer self-assesses | No IVA, "Inversión del sujeto pasivo" (RD 1619/2012 art. 6.1.m) | Modelo 303 (non-subject operations box) and modelo 349 |
| EU consumer, seller's EU-wide B2C TBE and distance sales ≤ 10,000 euros this and last year | Spain, 21 % (art. 70.Uno.8º, 73) | IVA charged | Modelo 303 |
| EU consumer above the threshold, or option exercised | Customer's country at its rate (art. 70.Uno.4º) | Destination IVA | Modelo 369 OSS, quarterly, by the end of the following month (art. 163 duovicies) |
| Business or consumer outside the EU, or in Canarias, Ceuta, Melilla | Not subject to Spanish IVA (AEAT) | No IVA, state non-subject | Modelo 303 non-subject box; Canarias consumers: IGIC may be due, see reference |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Self-serve signup from another EU country | Business or consumer changes the treatment; the VIES check is the proof | Ask how the checkout validates VAT numbers and what evidence it stores |
| Customer in Canarias | IVA does not apply; B2B is reverse-charged in IGIC, B2C electronic services may oblige the seller to register for IGIC | Ask the customer type and send B2C cases to an adviser (IGIC registration unverified here) |
| Revenue through an app store or marketplace | The platform may be the seller to the end user (RICAC art. 26; Reg. 282/2011 art. 9a) | Ask for payout reports and platform terms before choosing gross or net |
| Development spend | Capitalisation needs project-level evidence of technical success and profitability, and blocks dividends (LSC art. 273.3) | Ask for project records and whether the company wants to capitalise |
| An option or phantom share plan | Payroll, corporate tax timing (LIS art. 14.3.e, 14.6) and startup exemption all differ | Ask for the plan terms, grant dates and settlement type |
| I+D+i deduction | Needs project-level cost tracking and ideally an informe motivado; RDL 40/2026 changed rates and monetisation on 21-11-2026 | Read `development-and-incentives.md`; flag that the RDL is pending convalidation |
| Multi-year prepaid deal | Long-term part is a non-current liability | Ask for the contract period and what is included |

## Related skills

| Question | Skill |
|---|---|
| IVA rules, OSS, reverse charge in depth | `spanish-vat` |
| Buying foreign SaaS and cloud (the mirror case) | `spanish-daily-bookkeeping` (`references/foreign-purchases.md`) |
| Implementation projects, grado de avance | `spanish-project-accounting` |
| Intangible assets and amortisation | `spanish-asset-accounting` |
| Corporate tax, deductions, rates | `spanish-corporate-tax` |
| Payroll, stock options in kind, researcher bonus | `spanish-payroll` |
| Starting the company, Ley de startups, ENISA | `spanish-start-company` |
| Accruals and year-end | `spanish-year-end-closing` |
| Invoices, Verifactu | `spanish-invoice-compliance`, `spanish-e-invoicing` |
| Selling physical goods online too | `spanish-industry-ecommerce` |
