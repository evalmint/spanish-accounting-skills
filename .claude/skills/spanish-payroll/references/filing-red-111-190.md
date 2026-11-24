# Filings: Seguridad Social (Sistema RED, SLD) and IRPF (modelos 111, 190)

What the employer files, where and when. An agent prepares drafts and calendars; it never confirms a TGSS liquidation, submits a modelo or orders a payment without the user's approval.

## Contents

1. Calendar at a glance
2. Before the first nómina
3. Sistema RED, SILTRA and the Sistema de Liquidación Directa
4. Deadlines and recargos for cotizaciones
5. Modelo 111
6. Modelo 190
7. Certificado de retenciones and payslip disclosure
8. Termination filings
9. Foral territories

## 1. Calendar at a glance

| Filing | Period | Deadline | Source |
|---|---|---|---|
| Alta in Seguridad Social | Each hire | Before work starts (up to 60 days earlier) | RD 84/1996 art. 32.3.1º |
| Contract to SEPE (Contrat@) | Each contract | 10 days after signing | ET art. 16.1 |
| Baja in Seguridad Social | Each termination | 3 calendar days after the end | RD 84/1996 art. 32.3.2º (unverified paragraph) |
| TGSS liquidation and payment | Month N | Last day of month N+1 | LGSS art. 29; RD 1415/2004 (RGR) art. 56.1 |
| CRA (conceptos retributivos abonados) | Month N | With the liquidation of month N (unverified exact deadline) | LGSS art. 147.3 |
| Modelo 111, quarterly | Quarter | 1-20 April, July, October, January | RIRPF art. 108.1 |
| Modelo 111, monthly (grandes empresas) | Month | 1-20 of the following month | RIRPF art. 108.1 |
| Modelo 190 | Calendar year | 1-31 January | RIRPF art. 108.2; Orden EHA/3127/2009 |
| Certificado de retenciones | Calendar year | Before the IRPF return period opens (early April) | RIRPF art. 108.3 |

Dates falling on a Saturday or holiday move to the next working day (AEAT instructions for modelo 111).

## 2. Before the first nómina

1. **Inscripción** of the company and a *código cuenta de cotización* (CCC) per province and activity, choosing the mutua for AT/EP (TGSS). Declare the CNAE-2025 code; it drives the AT/EP rate.
2. **Afiliación** of the worker (NAF) and **alta** before work starts, with contract type, grupo de cotización, working time and occupation code.
3. **Contrat@**: communicate the contract to SEPE.
4. **Modelo 145** signed by the employee (`irpf-retenciones.md`).
5. **Censo AEAT** (modelo 036): mark the obligation to withhold so modelo 111 appears in the census.
6. Identify the convenio and register working time (ET art. 34.9).

## 3. Sistema RED, SILTRA and the SLD

- **Sistema RED** is the TGSS electronic channel for employers and *graduados sociales*/advisers (authorised users). Online services cover afiliación, IT data and liquidations; **SILTRA** is the TGSS desktop application to send and receive files (afiliación, CRA, liquidation requests, and to download receipts).
- **Sistema de Liquidación Directa (SLD)**: the TGSS calculates each worker's cotización from the data it holds (altas, contract, grupo, IT, reductions) plus the bases the employer reports. Flow:
  1. Employer reports the period's bases and concepts or asks for a *borrador* (draft).
  2. TGSS returns the borrador per worker (RLC = Recibo de Liquidación de Cotizaciones; RNT = Relación Nominal de Trabajadores).
  3. Employer fixes errors and **confirms** the liquidation within the period.
  4. Payment by *cargo en cuenta* (direct debit, charged at month end) or electronic payment with the receipt reference.
- IT pago delegado is compensated automatically in the liquidation (`incapacidad-temporal.md`).
- Book from the RLC/RNT totals, not from the payroll software's estimate; differences (rounding, reductions, IT compensation) go through **476**.
- Direct-debit cut-off: the TGSS manuals have put it around the 22nd of the month (20th in February and December); confirmations after that date require electronic payment (unverified for 2026; check the current Sistema RED bulletin).

## 4. Deadlines and recargos for cotizaciones

- Cotizaciones for month N must be paid within month N+1 (RGR art. 56.1).
- The liquidation must be requested and confirmed within the same period; filing it in time reduces the surcharge (LGSS art. 30):

| Situation | Paid in month after the deadline | Paid later |
|---|---|---|
| Liquidation filed in time, not paid | 10 % | 20 % |
| Liquidation not filed in time | 20 % (before the end of the term in the reclamación de deuda) | 35 % |

- Atrasos (retroactive salary under a convenio): complementary liquidation with the bases and rates of each month, by the deadline in RGR art. 56.1.c (Orden PJC/297/2026 art. 29).
- Unpaid cotizaciones block certificates of being up to date (*certificado de estar al corriente*), needed for public contracts and subsidies, and cancel bonificaciones for the unpaid periods (LGSS art. 20.3).

## 5. Modelo 111

*Retenciones e ingresos a cuenta del trabajo, actividades económicas, premios y determinadas ganancias e imputaciones de renta* (Orden EHA/586/2011). One return per period for all employment income, professional invoices with withholding, prizes, etc.

- **Who files monthly**: companies whose volumen de operaciones in the previous year exceeded 6 010 121,04 € (*gran empresa*, RIVA art. 71.3.1º) and public bodies with budgets over 6 million €. Everyone else quarterly (RIRPF art. 108.1).
- **Content**: number of recipients and amounts in cash and in kind, withholdings and ingresos a cuenta, by type (employment, activities, prizes...).
- **Negative return**: required when income subject to withholding was paid but no withholding resulted because of the amount; not required when no such income was paid (RIRPF art. 108.1).
- **2026 domiciliación and filing dates** (AEAT 2026 calendar):

| Period | Direct debit by | File by |
|---|---|---|
| 4T 2025 / 12M 2025 | 15 January 2026 | 20 January 2026 |
| 1T 2026 | 15 April | 20 April |
| 2T 2026 | 15 July | 20 July |
| 3T 2026 | 15 October | 20 October |
| Monthly 5M | 17 June | 22 June |
| Monthly 7M | 17 August | 20 August |
| Monthly 8M | 16 September | 21 September |
| Monthly 11M | 16 December | 21 December |

Other monthly periods: 1-20 of the following month, direct debit until about the 15th. 4T 2026 and 12M 2026 fall in January 2027; check the 2027 calendar.

- **Booking**: on payment, debit **4751**, credit **572**. Reconcile **4751** to zero after each payment; a balance means a missed withholding or a booking error.

## 6. Modelo 190

Annual summary of withholdings and ingresos a cuenta, with one line per recipient: NIF, name, province, *clave* and *subclave* of income, cash and in-kind amounts, withholdings, ingresos a cuenta, exempt dietas, personal data used for the tipo (birth year, family situation, children, disability), employee cotizaciones deducted, contract type (RIRPF art. 108.2).

- Electronic only; 1-31 January of the following year.
- Claves used most: A (employees), E (administradores and consejeros), G (professionals), L (exempt income, including exempt dietas and exempt indemnizaciones; subclaves per the instructions).
- The sum of the four 111 returns must equal the 190 totals for the same income keys. Reconcile before filing; AEAT cross-checks.
- Data feed the employees' draft returns; errors trigger AEAT requirements to the employer.

## 7. Certificado de retenciones and payslip disclosure

- The payer issues each employee a certificate of income, withholdings and the data in the 190, before the IRPF return period opens (RIRPF art. 108.3).
- Each payment must state the withholding % applied (RIRPF art. 108.4); the payslip carries it.

## 8. Termination filings

Baja in the TGSS, certificado de empresa to SEPE through Certific@2, complementary liquidation for unused vacation, and the finiquito in the 111 of the period (`finiquito-e-indemnizaciones.md`).

## 9. Foral territories

País Vasco (Álava, Bizkaia, Gipuzkoa) and Navarra collect IRPF withholdings under their own regulations, tables and forms (e.g. modelo 110/111 equivalents and 190 for the Diputación or Hacienda Foral). Which administration is competent for employment withholdings depends on where the work is done (Concierto Económico art. 7; Convenio con Navarra art. 9; unverified articles). Seguridad Social filings are the same everywhere.
