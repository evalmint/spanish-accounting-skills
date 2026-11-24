# Hacienda, Seguridad Social and the Owner

Part A covers paying and settling taxes and social security: the entries behind modelos 303, 111, 115, 123, 202, 200 and 130, Seguridad Social charges, domiciliaciones, aplazamientos, recargos and interest. Part B covers money between the business and its owner: the autónomo's **550**, the socio's current account **551**, loans from socios, contributions and dividends. Accounts are **PGC 2007**. Territorio común: the Basque Country and Navarra collect their own corporate tax and IVA for many businesses, with other forms and calendars.

## Contents

- [A1. The tax accounts](#a1-the-tax-accounts)
- [A2. Calendar of the usual modelos](#a2-calendar-of-the-usual-modelos)
- [A3. Settling and paying modelo 303](#a3-settling-and-paying-modelo-303)
- [A4. Retentions: modelos 111, 115, 123](#a4-retentions-modelos-111-115-123)
- [A5. Corporate tax: modelos 202 and 200](#a5-corporate-tax-modelos-202-and-200)
- [A6. Autónomo: modelo 130 and personal taxes](#a6-autónomo-modelo-130-and-personal-taxes)
- [A7. Seguridad Social](#a7-seguridad-social)
- [A8. Domiciliaciones](#a8-domiciliaciones)
- [A9. Aplazamientos and fraccionamientos](#a9-aplazamientos-and-fraccionamientos)
- [A10. Late filing: recargos, interest, sanctions](#a10-late-filing-recargos-interest-sanctions)
- [B1. Router by entity type](#b1-router-by-entity-type)
- [B2. Autónomo: 550 Titular de la explotación](#b2-autónomo-550-titular-de-la-explotación)
- [B3. SL/SA: 551 Cuenta corriente con socios y administradores](#b3-slsa-551-cuenta-corriente-con-socios-y-administradores)
- [B4. Loans from socios to the company](#b4-loans-from-socios-to-the-company)
- [B5. Contributions without return](#b5-contributions-without-return)
- [B6. Dividends](#b6-dividends)
- [B7. Private expenses paid by the company](#b7-private-expenses-paid-by-the-company)
- [B8. Ask the user](#b8-ask-the-user)

## A1. The tax accounts

| Account | Use |
|---|---|
| **472** Hacienda Pública, IVA soportado | Deductible input IVA |
| **477** Hacienda Pública, IVA repercutido | Output IVA |
| **4700** Hacienda Pública, deudora por IVA | Excess of input over output IVA in a period: to compensate or to refund |
| **4750** Hacienda Pública, acreedora por IVA | IVA to pay for a period |
| **4709** Hacienda Pública, deudora por devolución de impuestos | Refunds requested (IS, IRPF, IVA when a refund is requested) |
| **4751** Hacienda Pública, acreedora por retenciones practicadas | Retentions withheld from employees, professionals, landlords, socios |
| **4752** Hacienda Pública, acreedora por impuesto sobre sociedades | Corporate tax payable for the year |
| **473** Hacienda Pública, retenciones y pagos a cuenta | Retentions suffered and pagos fraccionados made |
| **476** Organismos de la Seguridad Social, acreedores | Social security owed |
| **471** Organismos de la Seguridad Social, deudores | Social security receivable (e.g. sick pay advanced under pago delegado) |
| **6300** Impuesto corriente | Corporate tax expense for the year |
| **631** Otros tributos | Local taxes and non-recoverable taxes |
| **669** Otros gastos financieros | Late-payment interest (intereses de demora) |
| **678** Gastos excepcionales | Recargos and sanctions |

## A2. Calendar of the usual modelos

| Modelo | What | Period and deadline | Source |
|---|---|---|---|
| 303 | IVA self-assessment | Quarterly: 1–20 April, July, October; 4Q 1–30 January. Monthly filers (SII, REDEME, large companies): 1–30 of the following month, January's by end of February | RIVA art. 71; AEAT 303 instructions |
| 390 | IVA annual summary | 1–30 January (not required for most SII filers) | RIVA art. 71 |
| 111 | Retentions on work and professional income | Quarterly: first 20 days of April, July, October and January; monthly for large companies | RIRPF art. 108.1 |
| 115 | Retentions on rent | Same as 111 | RIRPF art. 108.1 |
| 123 | Retentions on capital income (dividends, interest) | Same as 111 | RIRPF art. 108.1 |
| 190, 180, 193 | Annual summaries of 111, 115, 123 | 1–31 January | RIRPF art. 108.2 |
| 202 | Corporate tax instalments | First 20 days of April, October and December | LIS art. 40.1 |
| 200 | Corporate tax return | 25 days after the six months following year end (1–25 July for a calendar year) | LIS art. 124.1 |
| 130 | Autónomo IRPF instalment (estimación directa) | 1–20 April, July, October; 4Q 1–30 January | RIRPF art. 111.1 |
| 349 | Intra-EU operations | Monthly, first 20 days of the next month (July's by 20 September); quarterly if neither the quarter nor any of the previous four exceeded 50,000 € of intra-EU supplies of goods and services; last period of the year by 30 January | RIVA art. 81 |

When a deadline falls on a non-working day it moves to the next working day. Check the AEAT *calendario del contribuyente* for the year.

## A3. Settling and paying modelo 303

At the end of each IVA period, close **472** and **477** against the result:

| Result | Debe | Haber |
|---|---|---|
| To pay | **477** (its balance) | **472** (its balance), **4750** (difference) |
| To compensate in later periods, or to refund | **477**, **4700** (difference) | **472** |

Payment: **4750** / **572**. Refund received: **572** / **4700**. A credit to compensate stays in **4700** and is applied in later 303s; it can be compensated within four years from the return in which it arose (LIVA art. 99.Cinco), or refunded in the last period of the year (4Q or December) or monthly under REDEME.

Before closing, reconcile the 472 and 477 balances with the *libros registro* of invoices issued and received (RIVA art. 62) and, for SII filers, with the AEAT's Pre303 data. A difference means an invoice is missing on one side.

## A4. Retentions: modelos 111, 115, 123

Each modelo pays the balance of its own **4751** subaccount for the period: **4751** / **572**. The amount in the modelo must equal the retentions in the period's invoices and payrolls; a negative modelo is filed when retentions were zero because of the amount but rents subject to retention were paid (RIRPF art. 108.1, last paragraph).

Retentions cannot be deferred (LGT art. 65.2.b): an aplazamiento request for them is inadmissible. Pay them on time even when cash is short.

## A5. Corporate tax: modelos 202 and 200

| Event | Debe | Haber |
|---|---|---|
| Pago fraccionado (202) | **473** | **572** |
| Retentions suffered on bank interest, rent received, etc. | **572**, **473** | **769** / **752** |
| Year end: tax expense | **6300** | **473** (payments on account), **4752** (to pay) or **4709** Debe (to refund) |
| Paying the 200 | **4752** | **572** |
| Refund received | **572** | **4709** |

Deferred tax (**4740**, **479**, **6301**) and the full year-end calculation are in `spanish-year-end-closing` and `spanish-corporate-tax`. Microempresas using the PGC Pymes simplified criteria book only the current tax (RD 1515/2007 art. 4.3, 2.ª).

## A6. Autónomo: modelo 130 and personal taxes

The autónomo's IRPF (modelo 130 instalments, the annual return) is a personal tax of the titular, not a business expense. If the business keeps PGC books, book it to **550** (drawings). Same for the titular's own IBI on the private home, private car taxes, and so on.

The autónomo's own Seguridad Social cuota (RETA) is a deductible expense of the activity for IRPF; it is commonly booked to **642** (A7).

## A7. Seguridad Social

| Event | Debe | Haber |
|---|---|---|
| Monthly payroll: employee share withheld | **640** (part of gross) | **476** |
| Employer share | **642** | **476** |
| TGSS charge for the month | **476** | **572** |
| Autónomo's own RETA cuota | **642** (practice; some use **649**) | **572** |
| Recargo for late payment | **678** | **572** |

Payment period: cuotas of the Régimen General are paid within the month following the month they accrue; the RETA cuota is charged in the same month it refers to (RD 1415/2004, Reglamento General de Recaudación de la Seguridad Social, art. 56) (unverified).

Late payment surcharges (LGSS art. 30): if the contribution documents were filed on time, 10 % when paid within the first calendar month after the deadline and 20 % after that; if they were not filed on time, 20 % before the end of the deadline in the debt claim and 35 % after it.

**A company paying its socio-administrator's RETA cuota:** treatment for the company and the socio depends on whether it is remuneration agreed under the bylaws and how it is paid. Do not book it silently as **642**: flag it and see `spanish-payroll`.

## A8. Domiciliaciones

Direct debit of the 303, 111, 115 and similar: the return is filed with an order to debit the account on the last day of the payment period. The domiciliation window closes earlier than the filing window: for quarterly returns 1–15 April, July and October and 1–25 January for 4Q (AEAT calendario del contribuyente; extended when the filing deadline moves). Since 2024 the debit account may be at a non-collaborating SEPA bank (AEAT 303 instructions).

Book the payment on the debit date: debit the liability (**4750**, **4751**, **473** for 202), credit **572**. The justificante is the filed return plus the bank charge. If the debit fails, the debt enters the executive period with surcharges (LGT art. 28): ask the user immediately.

## A9. Aplazamientos and fraccionamientos

**AEAT (LGT art. 65; RGR RD 939/2005 art. 44–54):**

| Rule | Value | Source |
|---|---|---|
| No guarantee needed up to | 50,000 € of total pending debt, from 15 April 2023 (previously 30,000 €) | LGT art. 82.2.a; Orden HFP/311/2023 |
| Automated grant, maximum | 12 monthly instalments for companies, 24 for individuals (including autónomos) | AEAT Instrucción 2/2023, sexta 3.2 |
| Not deferrable (inadmissible) | Retentions and ingresos a cuenta; taxes legally passed on (IVA repercutido) unless it is shown the IVA was not collected; corporate tax pagos fraccionados | LGT art. 65.2.b, f, g |
| Interest | Interés de demora: 4.0625 % in 2024, 2025 and 2026 (set by the 2023 budget law, Ley 31/2022, which remains extended) (from AEAT and secondary sources; check the budget law if a new one is passed). Interés legal (3.25 % for 2026) if fully guaranteed by bank guarantee or surety insurance | LGT art. 26.6 and 65.4 |

Accounting: the deferred debt stays in its tax account or a dedicated subaccount (e.g. 4750001 IVA aplazado). The PGC lets balances with public administrations due after more than one year remain in group 4 and be reclassified for presentation (PGC part 5, group 4 introduction). Present the part due after twelve months as non-current. Accrue interest monthly to **669** against the same subaccount.

**Seguridad Social (LGSS art. 23):** TGSS can defer contributions, but never the workers' share or the accident and occupational disease (AT/EP) contributions; these must be paid for the deferral to take effect.

## A10. Late filing: recargos, interest, sanctions

| Situation | Consequence | Source |
|---|---|---|
| Filed late without prior AEAT requirement | Recargo 1 % plus 1 % per full month of delay, no sanction, no interest; after 12 months, 15 % plus interest from month 13 | LGT art. 27.2 (as amended by Ley 11/2021) |
| Filed on time but not paid (and no aplazamiento) | Executive period: recargo ejecutivo 5 %, reducido 10 %, or de apremio 20 % (ordinario) plus interest | LGT art. 28 |
| Found by the AEAT | Sanctions under LGT art. 191 et seq., plus interest | LGT |

Corporate tax: recargos for late filing without requirement, executive-period surcharges, and sanctions are not deductible (LIS art. 15.c). Late-payment interest is a financial expense; the Supreme Court held it deductible (STS 150/2021, 8 February 2021) (see `spanish-corporate-tax`). Book recargos and sanctions to **678**, interest to **669**.

## B1. Router by entity type

| Entity | Owner's account | Owner takes money | Owner puts money in |
|---|---|---|---|
| Autónomo (empresario individual) | **550** Titular de la explotación | **550** debit; no tax effect, the profit is taxed in IRPF anyway | **550** credit |
| SL or SA | **551** Cuenta corriente con socios y administradores | Loan to socio (needs junta approval in an SL), salary, or dividend; never a cost | Loan to the company (B4), contribution (B5) or capital increase |
| Comunidad de bienes, sociedad civil (atribución de rentas) | **550**-type accounts per member, or **551** (company choice) | Distribution of the attributed profit | Contribution |

## B2. Autónomo: 550 Titular de la explotación

The PGC defines **550** as the current account with the sole trader: credited with funds he contributes, debited with funds and goods he takes for himself; at year end its balance is transferred to **102** Capital (PGC part 5, account 550).

| Event | Debe | Haber |
|---|---|---|
| Titular transfers money to the business account | **572** | **550** |
| Titular withdraws money | **550** | **572** |
| Business pays a private expense of the titular | **550** | **572** |
| Titular pays a business expense with a private card (invoice in the business's name) | **629** etc., **472** | **550** |
| Titular takes goods from stock for private use | **550** | **700** (at cost, as autoconsumo base) and **477** (LIVA art. 9.1.º.a and 79.Tres) |
| Year end | **102** or **550** for the net balance | the other |

IRPF on the profit is computed on the business result regardless of drawings. The autónomo's IRPF and personal taxes go to **550** (A6).

## B3. SL/SA: 551 Cuenta corriente con socios y administradores

**551** holds current-account balances with socios and administrators that are not trade or formal loan balances (PGC part 5, accounts 551/552). A debit balance is an asset (the socio owes the company); a credit balance is a liability.

| Event | Debe | Haber |
|---|---|---|
| Company pays something private for the socio | **551** | **572** |
| Socio pays a company expense personally (invoice in the company's name) | **6xx**, **472** | **551** |
| Socio repays | **572** | **551** |

Rules that matter:

- **Junta approval for credit to socios in an SL**: advancing funds, granting loans or guarantees to socios or administrators requires a specific junta resolution for each case (LSC art. 162.1). Financing the purchase of the company's own shares is prohibited (LSC art. 143.2 for SL, art. 150 for SA).
- **Market interest**: a socio with 25 % or more, and administrators, are related parties (LIS art. 18.2.a). Loans between them and the company must carry market interest (LIS art. 18.1). An interest-free loan to a socio can be adjusted by the AEAT, and the socio's benefit may be treated as a distribution or salary in kind. Accrue interest: **551** / **762** Ingresos de créditos.
- **A debit balance that is never repaid** looks like a hidden distribution or salary. Ask what it is before year end and regularise it (repayment, payroll with retention, or a junta resolution on a dividend).
- Balances with group companies go to **552** (5523, 5524, 5525), not 551.

## B4. Loans from socios to the company

A formal loan (written agreement, term, interest) from a socio:

| Lender | Account |
|---|---|
| Socio who is a related party under NECA 15.ª (control, significant influence, administrators) | Long term: **1635** Otras deudas a largo plazo con otras partes vinculadas; short term: **5135** |
| Socio who is not a related party | **171** Deudas a largo plazo / **521** Deudas a corto plazo |
| Informal, at call, no term | **551** (credit balance) |

| Event | Debe | Haber |
|---|---|---|
| Loan received | **572** | **1635** / **5135** (or **171**/**521**) |
| Interest accrued and paid to an individual socio | **6622** Intereses de deudas, otras partes vinculadas (or **6624**) | **4751** (19 % retention, RIRPF art. 90; modelo 123), **572** |
| Reclassify the part due within 12 months at year end | **1635** | **5135** |

Interest must be at market value if the socio is related (LIS art. 18). An interest-free loan from a socio to the company is common; its tax consequences for the socio and the company are a related-party valuation question: flag it for `spanish-corporate-tax`. Loans are exempt from ITP (RDLeg 1/1993 art. 45.I.B.15) but the autonomous community may still require the tax form (modelo 600) to be filed (unverified for each community).

## B5. Contributions without return

Money a socio puts in without any repayment obligation and without new shares is **118** Aportaciones de socios o propietarios (equity). It is used, for example, to cover losses. It is not income for the company. A capital increase goes through **100** Capital social after the public deed and registry inscription, with the formalities of the LSC; see `spanish-start-company`.

## B6. Dividends

| Step | Debe | Haber | Source |
|---|---|---|---|
| Junta approves the annual accounts and the application of the result | **129** | **112** Reserva legal (10 % of profit until it reaches 20 % of capital), **113** Reservas voluntarias, **526** Dividendo activo a pagar | LSC art. 273–274 |
| Payment to individual socios | **526** | **4751** (19 % retention, modelo 123), **572** | RIRPF art. 90 |
| Payment to a corporate socio | **526** | **4751** (19 %, unless the participation exemption conditions allow no retention), **572** | RIRPF / LIS art. 128 (see `spanish-corporate-tax`) |
| Interim dividend (a cuenta) | **557** Dividendo activo a cuenta | **526** | LSC art. 277: liquidity statement by the administrators; amount limited to profit since year end minus losses, mandatory reserves and estimated tax |
| At the next junta, the interim dividend is netted against the result | **129** | **557** | |

Dividends may only be paid from profit or freely available reserves if net equity does not fall below capital (LSC art. 273.2). The administrators must document it; an agent should never book a dividend without the junta resolution.

## B7. Private expenses paid by the company

In an SL, a private expense paid by the company is never a company cost:

| What it really is | Entry | Tax effect |
|---|---|---|
| Socio will repay | **551** / **572** | None if repaid; market interest if left long |
| Salary in kind for a socio who works in the company | **640** (in-kind remuneration) / **572**, with ingreso a cuenta | Payroll and IRPF of the employee (`spanish-payroll`) |
| Distribution of profit | Through a junta resolution, **526** | 19 % retention; not deductible for the company (LIS art. 15.a) |

IVA on a private expense is never deductible (LIVA art. 95). If it was already deducted, reverse it.

## B8. Ask the user

- Which tax period and modelo does this AEAT charge belong to? Is there a filed return to match?
- Was the 303 result to pay, to compensate or to refund?
- For an aplazamiento: which debts, the approval resolution and the instalment schedule.
- For money to or from a socio: is it a loan (agreement, interest, term), a salary, a dividend, a contribution, or a private expense to be repaid?
- Has the junta approved the dividend, and for what amount per socio?
- For the autónomo: is this payment for the business or personal (IRPF, home, family)?
