# Payroll journal entries (PGC 2007)

Accounts and worked entries for the payroll cycle. Figures follow the worked nómina in `nomina-estructura.md` (2 200 € gross, 14 pagas, tipo 13,50 %). An agent proposes entries; it never posts them without the user's approval.

## Contents

1. Accounts
2. Monthly nómina
3. Paying net, TGSS and modelo 111
4. Pagas extraordinarias: monthly accrual
5. Anticipos and loans to staff
6. IT in pago delegado
7. Especie and ingreso a cuenta
8. Atrasos de convenio
9. Year-end checks

## 1. Accounts

| Account | Name | Use |
|---|---|---|
| **640** | Sueldos y salarios | Gross salary, pluses, overtime, pagas extra, especie agreed as salary, taxable excess of dietas |
| **641** | Indemnizaciones | Severance, transfer compensation |
| **642** | Seguridad Social a cargo de la empresa | Employer cotización: CC, desempleo, FOGASA, FP, MEI, solidaridad, AT/EP |
| **643** | Retribuciones a largo plazo mediante sistemas de aportación definida | Employer pension plan contributions |
| **649** | Otros gastos sociales | Canteen, health insurance, nursery, training, staff events |
| **460** | Anticipos de remuneraciones | Salary advances, deducted in a later nómina |
| **544** | Créditos a corto plazo al personal | Loans to employees |
| **465** | Remuneraciones pendientes de pago | Net pay due; accrued pagas extra |
| **466** | Remuneraciones mediante sistemas de aportación definida pendientes de pago | Pension contributions due |
| **471** | Organismos de la Seguridad Social, deudores | IT paid in pago delegado, bonificaciones to recover |
| **476** | Organismos de la Seguridad Social, acreedores | Employer + employee cotización due to TGSS |
| **4751** | Hacienda Pública, acreedora por retenciones practicadas | IRPF withheld and ingresos a cuenta, paid with modelo 111 |
| **572** | Bancos e instituciones de crédito c/c vista, euros | Payments |

Dietas and travel expenses reimbursed with the nómina go to **629** per `spanish-travel-expenses`; only the taxable excess goes to **640**.

## 2. Monthly nómina (month without paga extra, pagas accrued monthly)

| Account | Debit | Credit |
|---|---|---|
| **640** Sueldos y salarios (2 200 + accrual of pagas 366,67) | 2 566,67 | |
| **642** Seguridad Social a cargo de la empresa | 825,18 | |
| **4751** IRPF withheld (13,50 % × 2 200) | | 297,00 |
| **476** Employer 825,18 + employee 166,83 | | 992,01 |
| **465** Net pay (2 200 − 166,83 − 297,00) | | 1 736,17 |
| **465** Pagas extra accrued | | 366,67 |

If the company does not accrue pagas monthly, drop the 366,67 lines and book the full paga to **640** in June and December. Monthly accrual is the better reflection of the accrual principle and is needed for interim statements.

## 3. Paying net, TGSS and modelo 111

| Event | Debit | Credit | When |
|---|---|---|---|
| Transfer of net pay (SEPA remittance, `spanish-bank-files`) | **465** 1 736,17 | **572** | Pay date |
| TGSS liquidation paid | **476** 992,01 | **572** | Last day of next month |
| Modelo 111 paid (quarter's total) | **4751** | **572** | 1-20 after quarter |

## 4. Pagas extraordinarias

Monthly accrual (above) builds **465** to 2 200 × 6/6 by June. In June, the paga is paid:

| Account | Debit | Credit |
|---|---|---|
| **465** Accrued paga | 2 200,00 | |
| **4751** IRPF on the paga (13,50 %) | | 297,00 |
| **465** Net paga | | 1 903,00 |

No cotización entry in June: cotización on the paga was charged monthly through the prorrata. If the convenio prorates pagas in 12 payments, there is no accrual: 2 566,67 € is paid each month and withheld each month.

## 5. Anticipos and loans to staff

| Event | Debit | Credit |
|---|---|---|
| Salary advance paid | **460** | **572** |
| Deducted in the next nómina | **465** (reduces net) | **460** |
| Loan to employee | **544** | **572** |
| Instalment deducted | **465** | **544** |

An interest-free or below-legal-rate loan creates especie (`retribucion-en-especie.md`).

## 6. IT in pago delegado

| Event | Debit | Credit |
|---|---|---|
| Days 4-15 at the employer's charge and convenio top-up | **640** | **465** / **4751** / **476** |
| Benefit from day 16 paid on behalf of INSS/mutua | **471** | **465** / **4751** / **476** |
| Compensation in the TGSS liquidation | **476** | **471** |

## 7. Especie and ingreso a cuenta

| Event | Debit | Credit |
|---|---|---|
| Health insurance premium paid by the company | **649** | **572** |
| Ingreso a cuenta on the taxable excess, borne by the company | **640** | **4751** |
| Same, passed on to the employee | **465** | **4751** |

## 8. Atrasos de convenio

New convenio signed in October 2026 with a raise from January:

| Event | Debit | Credit |
|---|---|---|
| Atrasos for 2026 months | **640** / **642** | **465**, **4751** (normal tipo), **476** |
| Atrasos for prior years | **640** (if not accrued, a prior-period error per PGC NRV 22 when material) / **642** | **465**, **4751** at 15 %, **476** |

Accrue at the 31 December close any raise that is certain and measurable (`spanish-year-end-closing`).

## 9. Year-end checks

- **476** equals the December TGSS liquidation (paid in January).
- **4751** equals the 4T (or December) modelo 111.
- **465** equals unpaid net pay plus accrued, unpaid pagas extra (e.g. half of a paga accrued July-December paid in the following June, depending on the convenio's accrual period).
- **471** contains only IT not yet compensated.
- **460** and **544** reconcile to employee balances.
- Modelo 190 totals equal the year's 111 returns and the gross on **640** less non-reported items (exempt dietas are reported; check by key).
