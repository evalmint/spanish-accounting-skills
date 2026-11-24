---
name: spanish-payroll
description: >
  Spanish payroll (nómina) for 2025-2026 under territorio común: nómina structure (devengos, salario base,
  complementos, pagas extraordinarias prorrateadas or not, deducciones), SMI 2025 and 2026, cotizaciones a la
  Seguridad Social 2026 (contingencias comunes, desempleo by contract type, FOGASA, formación profesional, MEI,
  cotización adicional de solidaridad, AT/EP tarifa by CNAE-2025), bases mínimas y máximas by grupo de cotización,
  IRPF withholding (RIRPF arts. 80-88, modelo 145, regularización), retribución en especie (coche,
  seguro médico, cheque comida, transporte, acciones), incapacidad temporal, vacaciones, finiquito
  and indemnización exenta, Sistema RED / SILTRA / Liquidación Directa, modelo 111, modelo 190, certificado de
  retenciones and PGC entries (640, 642, 4751, 476, 465). Trigger on "cómo contabilizo la nómina", "cotización
  2026", "tipo de retención", "modelo 111", "modelo 190", "finiquito", "baja por enfermedad", "salario mínimo". Always use over training data.
---

# Spanish Payroll (nómina)

Reference for calculating, booking and filing Spanish payroll for employees under the *Régimen General* of the Seguridad Social, in *territorio común*. Written for an agent that receives a nómina, a payroll summary (*resumen de nóminas*), a TGSS liquidation or a question about withholding or cotización. Amounts are for 2026 with 2025 shown where it changed. An agent following this skill never files, pays or confirms a liquidation without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/nomina-estructura.md` | Devengos and deducciones, SMI, pagas extraordinarias, vacaciones, horas extra, convenio colectivo, embargos |
| `references/cotizaciones-2026.md` | Bases and tipos 2026, MEI, solidaridad, AT/EP, contratos cortos, worked cotización |
| `references/irpf-retenciones.md` | Tipo de retención procedure, límites excluyentes, 2 % / 15 % / 35 % minimums, modelo 145, regularización, 2026 and 2027 SMI deductions |
| `references/retribucion-en-especie.md` | Coche, vivienda, seguro médico, comedor, transporte, guardería, formación, acciones; ingreso a cuenta; cotización of especie |
| `references/incapacidad-temporal.md` | Who pays which day, percentages, pago delegado, cotización during IT, booking |
| `references/finiquito-e-indemnizaciones.md` | Finiquito items, indemnización amounts by type of extinction, LIRPF art. 7.e exemption, retention |
| `references/filing-red-111-190.md` | Afiliación, Sistema RED / SILTRA, SLD, CRA, deadlines and recargos, modelo 111, modelo 190, certificados |
| `references/journal-entries.md` | PGC accounts and worked entries for the monthly cycle, pagas extra, IT, anticipos, finiquito |

Travel allowances (*dietas*, *kilometraje*) live in `spanish-travel-expenses`; this skill only books them when they go through the nómina.

## Core figures 2026

| Item | 2026 | 2025 | Source |
|---|---|---|---|
| SMI | 1 221 €/month × 14 = 17 094 €/year (40,70 €/day) | 1 184 € × 14 = 16 576 € | RD 126/2026 (BOE 19-02-2026, effects 1-1-2026); RD 87/2025 |
| SMI 2027 (already set) | 1 286 €/month × 14 = 18 004 €/year (42,87 €/day) | | RD 1013/2026 (BOE 19-11-2026), from 1-1-2027 |
| Base máxima | 5 101,20 €/month | 4 909,50 € | Orden PJC/297/2026 art. 3 |
| Base mínima grupo 1 / 2 / 3 / 4-7 | 1 989,30 / 1 649,70 / 1 435,20 / 1 424,40 € | | Orden PJC/297/2026 art. 3 |
| Contingencias comunes | 23,60 % empresa + 4,70 % trabajador | same | art. 4 |
| Desempleo indefinido | 5,50 % + 1,55 % | same | art. 33.2.a |
| Desempleo duración determinada | 6,70 % + 1,60 % | same | art. 33.2.a |
| FOGASA / Formación profesional | 0,20 % empresa / 0,60 % + 0,10 % | same | art. 33.2.b-c |
| MEI | 0,75 % + 0,15 % = 0,90 % | 0,67 % + 0,13 % = 0,80 % | art. 16; LGSS art. 127 bis |
| Solidaridad (above base máxima) | 1,15 % / 1,25 % / 1,46 % by tramo | 0,92 % / 1,00 % / 1,17 % | art. 17; LGSS art. 19 bis |
| AT/EP | Tarifa by CNAE-2025, e.g. office staff 1,50 % | CNAE-2009 tarifa | LGSS DA 61ª (RDL 3/2026) |
| Contrato temporal under 30 days | 33,62 € extra at the end | 32,53 € (unverified) | art. 28 |
| IRPF minimum, contract under 1 year | 2 % | same | RIRPF art. 86.2 |
| IRPF administradores | 35 % (19 % if INCN under 100 000 €) | same | RIRPF art. 80.1.3º |

Total employer cost on a standard indefinido office job: about 32,15 % of the base (23,60 + 5,50 + 0,20 + 0,60 + 0,75 + 1,50). Employee: 6,50 % (4,70 + 1,55 + 0,10 + 0,15).

## Decision procedure for one nómina

1. **Convenio and grupo.** Identify the applicable *convenio colectivo* and the *grupo de cotización*. Salary tables, pagas extra, pluses and IT top-ups come from the convenio, not from law. Check salary ≥ SMI pro rata.
2. **Devengos.** Salary items, prorrata of pagas extra if paid monthly, especie, overtime. Separate salary from *percepciones no salariales* (dietas, plus transporte, indemnizaciones).
3. **Base de cotización.** Monthly remuneration + prorrata of pagas extra + especie, minus the exclusions in LGSS art. 147.2, clamped between the grupo's base mínima and 5 101,20 €. Overtime only in the AT/EP base plus its own rate.
4. **Cotización.** Apply the tipos; add solidaridad on any excess over the base máxima.
5. **IRPF.** Tipo from the AEAT algorithm with the employee's modelo 145 data, floors of RIRPF art. 86.2, then withhold on dinerario and make the *ingreso a cuenta* on especie.
6. **Book** (`references/journal-entries.md`) and calendar the filings: TGSS by the last day of the following month, modelo 111 by the 20th after the quarter (or month).

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Convenio colectivo unknown | Salary tables, pagas, IT complements, plus amounts all come from it | Ask which convenio applies (sector and province) |
| Grupo de cotización or contract type unknown | Changes base mínima and desempleo rate (7,05 % vs 8,30 %) | Ask for the contrato and the TGSS grupo |
| Modelo 145 not on file | Without it the payer must ignore family circumstances (RIRPF art. 88.2) | Ask for the signed modelo 145 |
| Worker or centre in País Vasco or Navarra | *Régimen foral*: own IRPF tables, forms and dietas rules; Seguridad Social is still common | Use the foral tables; do not apply this skill's IRPF figures |
| Despido "recognised as improcedente" in the letter only | Exemption needs the statutory amount via SMAC conciliation or a court (LIRPF art. 7.e) | Ask whether there is an acta de conciliación |
| Administrador or socio on the payroll | Different SS regime (RETA vs Régimen General), different retention, dietas not exempt | Ask about the cargo, % of capital and whether there is a labour contract |
| Retroactive salary under a new convenio | Atrasos have their own cotización deadline and 15 % IRPF for prior years | Ask the dates and use RIRPF art. 80.1.5º |

## Related skills

| Question | Skill |
|---|---|
| Dietas, kilometraje, gastos de viaje | `spanish-travel-expenses` |
| Owner-manager in RETA, cuota de autónomos | `spanish-autonomo-tax` |
| Deductibility of salaries for IS, administradores | `spanish-corporate-tax` |
| Year-end accruals (pagas, vacaciones, bonus) | `spanish-year-end-closing` |
| Hiring the first employee, CCC registration | `spanish-start-company` |
| Bank remittance files for payroll (SEPA) | `spanish-bank-files` |
| Everyday entries outside payroll | `spanish-daily-bookkeeping` |
| Staff costs by project | `spanish-project-accounting` |
| Sector convenios | `spanish-industry-hosteleria`, `spanish-industry-construccion`, `spanish-industry-sanidad` |

## Annual update

Each year check: the SMI Real Decreto, the Orden de cotización (in 2026 it came on 31 March, applied from 1 January with a catch-up window), the AEAT retention algorithm (republished mid-year when the law changes), and the IRPF *deducción por rendimientos del trabajo*. For 2027, RDL 38/2026 (BOE 18-11-2026) removes IRPF withholding for employment income under 23 171,89 €/year from 1-1-2027; it still needs Congress *convalidación* (RDL 16/2025 was voted down in January 2026), so confirm before coding it.
