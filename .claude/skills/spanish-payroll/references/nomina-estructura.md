# Nómina structure, SMI, pagas extra and vacaciones

How a Spanish payslip (*recibo de salarios*) is built and which labour-law rules fix the amounts. Cotización is in `cotizaciones-2026.md`, IRPF in `irpf-retenciones.md`.

## Contents

1. Legal frame and the convenio colectivo
2. The recibo de salarios
3. Devengos: salariales and no salariales
4. SMI 2025, 2026, 2027
5. Pagas extraordinarias: prorrateadas or not
6. Horas extraordinarias
7. Vacaciones
8. Deducciones and order of calculation
9. Embargos de salario
10. Worked nómina

## 1. Legal frame and the convenio colectivo

- **Estatuto de los Trabajadores** (ET, RDLeg 2/2015): salary concept (art. 26), SMI (art. 27), equal pay and *registro retributivo* (art. 28), payment and payslip (art. 29), pagas extra (art. 31), working time and overtime (arts. 34-35), vacaciones (art. 38).
- The **convenio colectivo** (sector, province or company) sets salary tables per category, the number and amount of pagas extra, pluses (antigüedad, nocturnidad, transporte, toxicidad), IT top-ups and annual hours. Applying the wrong convenio is the most common payroll error. Convenios are published in the BOE or the provincial/regional bulletin; REGCON (Ministerio de Trabajo) holds the register.
- **Especie** may not exceed 30 % of the employee's total salary and may not reduce cash pay below the SMI (ET art. 26.1).
- Pay is due on the agreed date, at the latest monthly; late pay carries 10 % annual interest (ET art. 29.3).

## 2. The recibo de salarios

The payslip follows the official model (Orden ESS/2098/2014, which amended the 1994 model; the company may use another layout if a convenio or agreement allows and it contains the same data). Required blocks:

| Block | Content |
|---|---|
| Header | Company, CIF, CCC (código cuenta de cotización); employee, NIF, NAF (número de afiliación), category, grupo de cotización, seniority, period |
| I. Devengos | 1. Percepciones salariales; 2. Percepciones no salariales |
| II. Deducciones | Worker's cotización by concept, IRPF, anticipos, especie value, other |
| Líquido a percibir | Total devengado minus total a deducir |
| Bases | Base CC, base AT/EP and others, base IRPF and the tipo de retención applied (RIRPF art. 108.4 requires the % to be communicated) |

## 3. Devengos

**Percepciones salariales** (count for SMI, cotizan, tributan):

- *Salario base* per convenio table.
- *Complementos salariales*: personales (antigüedad, idiomas, títulos), de puesto (nocturnidad, turnicidad, peligrosidad), de calidad o cantidad (incentivos, primas, comisiones), de vencimiento periódico superior al mes (pagas extra, beneficios).
- *Horas extraordinarias*.
- *Salario en especie* (see `retribucion-en-especie.md`).

**Percepciones no salariales** (ET art. 26.2: not salary):

- Indemnizaciones o suplidos por gastos (dietas, locomoción, plus de distancia): excluded from cotización and IRPF only within RIRPF art. 9 limits and conditions (`spanish-travel-expenses`).
- Prestaciones e indemnizaciones de la Seguridad Social (IT in pago delegado).
- Indemnizaciones por traslado, suspensión, despido.

**Propinas** (tips) distributed by the employer: whether they belong in the cotización base is unsettled (unverified); follow `spanish-industry-hosteleria` and do not decide it in a generic payroll run.

Plus de transporte / distancia paid as a flat monthly amount for home-to-work commuting is **not** exempt: it cotiza and is subject to IRPF (only the art. 42.3.e transport ticket in especie is exempt).

## 4. SMI

| Year | Monthly (14 pagas) | Daily | Annual | Norm |
|---|---|---|---|---|
| 2025 | 1 184 € | 39,47 € (unverified) | 16 576 € | RD 87/2025 |
| 2026 | 1 221 € | 40,70 € | 17 094 € | RD 126/2026, art. 1; BOE 19-02-2026, effects 1-1-2026 |
| 2027 | 1 286 € | 42,87 € | 18 004 € | RD 1013/2026; BOE 19-11-2026, effects 1-1-2027 |

- Compliance is tested on **annual** total salary (*compensación y absorción*): a salary above 17 094 €/year in 2026 is compliant even if the monthly base is lower (RD 126/2026 art. 3). Part-time: pro rata to hours.
- Temporary or seasonal contracts up to 120 days: at least 57,82 €/jornada in 2026, including the prorrata of Sundays, holidays, pagas extra and vacaciones (RD 126/2026 art. 4.1).
- Empleados de hogar por horas: 9,55 €/hour in 2026 (art. 4.2).
- The 2026 SMI was approved in February with effect from 1 January, so January-February nóminas needed *atrasos*. The cotización on atrasos follows the deadline in `filing-red-111-190.md`.
- References to the SMI in private contracts and non-state norms are not updated automatically (transitional provision of each RD).

## 5. Pagas extraordinarias

- Two per year by law, one at Christmas, the other in the month set by convenio; the amount is set by convenio (ET art. 31). Many convenios add a third (*paga de beneficios*, *marzo*).
- The convenio may allow **prorrateo** over 12 monthly payments (ET art. 31).
- **Cotización** always uses the prorrata, whether paid monthly or not: percepciones of more-than-monthly accrual are spread over 12 months (LGSS art. 147.1). With 14 pagas of 2 200 €, the monthly prorrata is 2 × 2 200 / 12 = 366,67 €.
- **IRPF** is withheld when paid (RIRPF art. 78.1), so a non-prorrated paga extra has withholding in June and December but no cotización.
- **Accounting**: accrue each month even if paid in June and December (accrual principle, PGC framework). See `journal-entries.md`.
- The accrual period of each paga (calendar year, July-June, etc.) is set by convenio; it decides the prorrata due in the finiquito.

## 6. Horas extraordinarias

- Maximum 80 per year, excluding those compensated with rest within four months and those for *fuerza mayor* (ET art. 35.2).
- Paid at the convenio rate, never below the ordinary hour, or compensated with rest (ET art. 35.1).
- Cotización: not in the base for contingencias comunes, but in the AT/EP base, plus a specific rate: 14,00 % (12,00 + 2,00) for fuerza mayor, 28,30 % (23,60 + 4,70) for the rest (LGSS art. 147.2.e; Orden PJC/297/2026 art. 5).
- The *registro de jornada* is compulsory (ET art. 34.9); overtime cannot be paid or proved without it.

## 7. Vacaciones

- At least 30 calendar days a year, set by convenio or contract; never replaced by money while the contract lasts (ET art. 38.1).
- Paid at the normal salary including the average of regular variable pay (case law of the CJEU and Tribunal Supremo; the convenio sets the method).
- Unused days are paid only at termination, in the finiquito. Their cotización is a complementary liquidation for the days of vacation after the extinction date, without prorrateo, using the next month's tope if it spills over (LGSS art. 147.1).
- Days lost to IT may be taken after the IT ends, within 18 months from the end of the year in which they accrued (ET art. 38.3).
- Year-end: accrue unpaid vacation earned but not taken only when material and payable (`spanish-year-end-closing`).

## 8. Deducciones and order of calculation

1. Total devengado (salary + no salariales + especie at its valuation).
2. Base de cotización (see `cotizaciones-2026.md`).
3. Worker's cotización: CC 4,70 %, desempleo 1,55 % or 1,60 %, FP 0,10 %, MEI 0,15 %, solidaridad share if any, overtime rates.
4. IRPF: tipo × (dinerario devengado). Especie is not withheld but carries an *ingreso a cuenta* paid by the company; if the company passes it on to the employee (*repercute*), deduct it in the nómina.
5. Deduct the especie value already received (it was added to devengos only to compute bases).
6. Anticipos, embargos, union fees, other voluntary deductions.
7. Líquido a percibir.

## 9. Embargos de salario

Salary equal to the SMI is unseizable; above it, the court applies the scale of LEC art. 607.2: 30 % of the part up to a second SMI, 50 % up to a third, 60 % up to a fourth, 75 % up to a fifth, 90 % above. In the month a paga extra is paid, the prevailing practice treats it as a separate salary with its own unseizable SMI (unverified as a statutory rule; follow the court order). Use the SMI of the current year (17 094 €/14 = 1 221 € in 2026; 1 286 € from 2027). Family-charge reductions (art. 607.4) are applied by the court, not by the payroll clerk. The amount is withheld from the net and paid to the court's account (credit **465** or a payable to the court).

## 10. Worked nómina (2026, not prorrated)

Indefinido office employee, grupo 5, 14 pagas: salario base 2 000 € + complemento 200 € per month. Modelo 145 data give a tipo of 13,50 % (illustrative; compute with the AEAT algorithm).

| Line | € |
|---|---|
| Devengos: salario base + complemento | 2 200,00 |
| Prorrata pagas extra (for cotización only) | 366,67 |
| Base CC and AT/EP | 2 566,67 |
| CC 4,70 % | 120,63 |
| Desempleo 1,55 % | 39,78 |
| FP 0,10 % | 2,57 |
| MEI 0,15 % | 3,85 |
| IRPF 13,50 % × 2 200 | 297,00 |
| **Líquido** | **1 736,17** |

Employer cost on top: CC 605,73, desempleo 141,17, FOGASA 5,13, FP 15,40, MEI 19,25, AT/EP 1,50 % 38,50 = 825,18 €. Booking in `journal-entries.md`.
