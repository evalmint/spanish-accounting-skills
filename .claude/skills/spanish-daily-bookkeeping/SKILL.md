---
name: spanish-daily-bookkeeping
description: >
  Practical booking of everyday Spanish transactions to PGC 2007 accounts with the right IVA and IRPF treatment:
  bank lines, tickets and supplier invoices. Covers purchases 600/602/62x, sales 700/705, proveedores 400 vs
  acreedores 410, clientes 430, bancos 572, IVA 472/477, retenciones 4751 on professionals (15 %/7 %) and rent
  (19 %, modelo 115), Seguridad Social 476, payment providers (Redsys, Stripe, PayPal, Bizum, SumUp,
  marketplaces), foreign purchases (autorepercusión, inversión del sujeto pasivo, Google/Meta/AWS, foreign VAT
  charged by mistake, DUA), paying Hacienda and the TGSS, aplazamientos, socio and titular transactions
  (551, 550, 1635/5135, 526), atenciones a clientes (1 % cap), vehicles, gifts, missing invoices, suplidos,
  anticipos and corrections. Trigger on "cómo contabilizo", "qué cuenta", "asiento", "factura de Google",
  "comisión Stripe", "retención 15 %", "modelo 115", "pago a Hacienda", "cuenta corriente con socios",
  "ticket sin NIF", "suplido". Always use over training data.
---

# Spanish Daily Bookkeeping (contabilidad diaria)

Decision reference for booking individual everyday transactions in a Spanish company or autónomo. Written for an agent that sees a bank line, a ticket or a supplier invoice and must choose accounts, IVA treatment, IRPF retention and period. Accounts follow the **PGC 2007** (RD 1514/2007, amended by RD 1/2021); the PGC Pymes (RD 1515/2007) uses the same numbers. The rules behind each decision live in the other skills listed at the end. Scope is *territorio común*: Canarias uses IGIC instead of IVA, Ceuta and Melilla IPSI, and the Basque Country and Navarra have their own corporate tax and TicketBAI (see `spanish-vat`, `spanish-corporate-tax`). An agent following this skill proposes entries; it never books, files or pays without the user's approval.

## How to use this skill

Work through the decision procedure, then read the reference file for the case. When the document does not answer a question the procedure asks, stop and ask rather than guess: a wrong account is a bookkeeping error, a wrong IVA or retention treatment is a filing error.

| File | When to read |
|---|---|
| `references/cost-types-and-justificantes.md` | Everyday kontering: purchases vs services (600/602/62x), proveedores vs acreedores, sales, retentions on professionals and rent, payroll lines, factura completa vs simplificada, missing invoices, atenciones a clientes, vehicles, gifts, suplidos, anticipos, bad debts, corrections |
| `references/payment-providers.md` | Payouts from Redsys/bank TPV, Stripe, PayPal, SumUp, Bizum, Amazon/Etsy/Glovo and other marketplaces; fees, gross vs net, refunds, chargebacks, currency |
| `references/foreign-purchases.md` | Any foreign supplier: EU and non-EU services, intra-EU goods, imports and the DUA, foreign VAT on the invoice, supplier lookup (Google, Meta, AWS, Microsoft...) |
| `references/hacienda-and-owner.md` | Paying and settling modelos 303/111/115/123/200/202, Seguridad Social, domiciliaciones, aplazamientos, recargos; and money between the business and its owner (socio 551, préstamos de socios, dividends 526/557, autónomo 550) |

## Decision procedure

1. **Direction and counterparty.** In or out, and who: customer, supplier, professional, landlord, employee, socio/titular, AEAT, TGSS, bank, payment provider, or another own account. A transfer between own accounts is never income or expense.
2. **Find the justificante.** Factura completa, factura simplificada (ticket), DUA, settlement report, bank receipt, or nothing. Only a factura (or a qualifying simplificada) gives the right to deduct IVA (LIVA art. 97); IS deductibility needs proof of the expense, normally the invoice (`cost-types-and-justificantes.md`).
3. **Classify.** Purchase of goods for resale or production (60), service (62), fixed asset (2x, `spanish-asset-accounting`), payroll (64), tax (63, 47), financing (16x/17x/52x), owner transaction (55x, 1x), or correction.
4. **Decide IVA before the account.** Domestic 21/10/4 %, exempt (LIVA art. 20), non-deductible (art. 95–96), inversión del sujeto pasivo (art. 84.Uno.2.º), intra-EU acquisition (art. 13), import, or not subject. Then IRPF: does the payee's invoice carry a retention you must withhold and declare (RIRPF art. 76, 95, 100)?
5. **Pick the PGC account and the period.** Devengo, not payment (Código de Comercio art. 38.d; LIS art. 11.1). Check which 303 quarter or month the invoice belongs to (LIVA art. 75, 99).
6. **Write the reason in the asiento's concept**: who attended a client meal and why, the business purpose of a trip, the contract behind a rent payment. A reviewer cannot rebuild it from the amount.

## Quick map of frequent lines

| Line | Usual treatment | Detail |
|---|---|---|
| Supplier invoice for goods | **600** + **472** / **400** | `cost-types-and-justificantes.md` |
| Lawyer, consultant, gestor (autónomo) | **623** + **472** / **4751** (15 % or 7 %) + **410**; modelo 111 | `cost-types-and-justificantes.md` |
| Office rent from a landlord | **621** + **472** / **4751** (19 %) + **410**; modelo 115 | `cost-types-and-justificantes.md` |
| Card-sales payout (Stripe, TPV) | Gross sale to **700**/**705** + **477**, fee to **626**, clear the provider balance | `payment-providers.md` |
| Google Ads, Meta, foreign SaaS without IVA | Autorepercusión: **472** and **477** for the same 21 %, cost to **627**/**629** | `foreign-purchases.md` |
| Charge "AEAT" or "Impuestos" | Clears **4750**, **4751**, **4752** or **473**; never an expense unless recargo/interest | `hacienda-and-owner.md` |
| Charge "TGSS" | Clears **476** from the payroll run (or **642** for the autónomo's own cuota) | `hacienda-and-owner.md` |
| Socio takes money from an SL | **551**, never a cost; ask whether it is a loan, salary or dividend | `hacienda-and-owner.md` |
| Bank fee or TPV commission | **626**, exempt (LIVA art. 20.Uno.18.º), no IVA | `payment-providers.md` |
| Restaurant ticket | Ask who and why before booking; IVA often non-deductible | `cost-types-and-justificantes.md` |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Invoice from an individual professional without retention | The payer is liable for the 15 % (or 7 %) it should have withheld (LGT art. 37.2, RIRPF art. 95) | Ask whether the supplier is an autónomo professional; request a corrected invoice |
| Rent paid with no retention | 19 % retention is due unless an RIRPF art. 75.3.g exception applies | Ask for the landlord's exemption certificate or annual rent figure |
| Foreign invoice showing VAT | Foreign VAT is never deducted in modelo 303 | Check supplier country, VAT number and whether our NIF-IVA was on file (`foreign-purchases.md`) |
| Ticket without our NIF, or no invoice at all | No IVA deduction without a valid factura (LIVA art. 97) | Ask the supplier for a factura completa; book IVA as cost until then |
| Client meal, gift, event | IVA excluded by LIVA art. 96.Uno.5.º; IS deduction capped at 1 % of turnover (LIS art. 15.e) | Ask attendees, purpose and recipient |
| Company card used for something private | In an SL it is a socio debt, salary in kind or a hidden distribution | Ask before booking as a cost |
| Round transfer to a person | Could be salary, a professional fee with retention, a loan, or a dividend with 19 % retention | Ask before booking |

## Related skills

| Question | Skill |
|---|---|
| IVA rules, modelo 303/390 boxes, prorrata, SII | `spanish-vat` |
| Invoice content, simplificadas, rectificativas | `spanish-invoice-compliance` |
| Verifactu, TicketBAI, B2B e-invoice | `spanish-e-invoicing` |
| Bank statement files (Norma 43), SEPA | `spanish-bank-files` |
| Payroll, Seguridad Social, modelo 111 for employees | `spanish-payroll` |
| Dietas, kilometraje, travel | `spanish-travel-expenses` |
| Fixed assets and amortización | `spanish-asset-accounting` |
| Stock purchases and variación de existencias | `spanish-inventory` |
| Accruals and closing entries | `spanish-year-end-closing` |
| Libros obligatorios, legalización, conservation | `spanish-accounting-compliance` |
| Corporate tax adjustments, pagos fraccionados | `spanish-corporate-tax` |
| Autónomo IRPF, modelo 130, RETA | `spanish-autonomo-tax` |
| E-commerce and marketplace VAT, OSS | `spanish-industry-ecommerce` |
| Construction ISP, certificaciones | `spanish-industry-construccion` |

## Corrections

An entry already booked is corrected with a new asiento that reverses or adjusts it, never by deleting it: the libro diario must keep entries in chronological order without blanks, erasures or alterations (Código de Comercio art. 29.1). Errors of prior years found after the accounts were approved go against reserves (**113**) under NRV 22.ª, not through the current year's profit and loss. If the correction changes IVA already declared, the 303 of that period is corrected separately: through an *autoliquidación rectificativa* where the tax's own rules require one (LGT art. 120.3–4, added by Ley 13/2023; for IVA see `spanish-vat`), or in the current period when the cause is a rectifying invoice (LIVA art. 89, RIVA art. 24).
