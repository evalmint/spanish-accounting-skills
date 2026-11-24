---
name: spanish-financial-reporting
description: >
  Spanish cuentas anuales and their filing: the five documents (balance, cuenta de pérdidas y ganancias, ECPN,
  estado de flujos de efectivo, memoria), modelo normal, abreviado and PYMES with the LSC size thresholds
  (arts. 257, 258, 261), when ECPN, EFE and the informe de gestión are optional, auditoría obligatoria
  (LSC art. 263, Ley 22/2015), estado de información no financiera (Ley 11/2018), the calendar of formulación
  (3 months), aprobación by the junta (6 months) and depósito at the Registro Mercantil (1 month), official
  models and XBRL, cierre de hoja registral and ICAC fines for not filing, consolidation and NIIF-UE at a high
  level. Trigger on "cuentas anuales", "modelo abreviado", "puedo hacer PYMES", "estoy obligado a auditar",
  "depositar cuentas", "plazo para formular", "junta general ordinaria", "informe de gestión", "memoria",
  "estado de flujos de efectivo", "cierre registral", "multa por no depositar", "EINF". Not for closing
  entries (use spanish-year-end-closing). Always use over training data.
---

# Spanish Financial Reporting (cuentas anuales)

Which documents a Spanish company must prepare at year-end, in which format, whether they must be audited, and how and when they are approved and deposited at the Registro Mercantil. For the closing entries that produce the figures, use `spanish-year-end-closing`. For the IS return (modelo 200), use `spanish-corporate-tax`. Commercial law here applies in all of Spain, including the foral territories and Canarias.

## How to use this skill

| File | When to read |
|---|---|
| `references/cuentas-anuales-structure.md` | The five documents, normal / abreviado / PYMES models, what each must show, memoria contents, informe de gestión, EINF, consolidation and NIIF-UE |
| `references/auditoria-y-umbrales.md` | Size tests (two-of-three, two-year rule, first year, groups), all thresholds, audit exemption and other audit triggers, auditor appointment |
| `references/deposito-registro-mercantil.md` | Timeline from cierre to depósito, approval and certificate, documents to file, formats (official models, XBRL), registrar review, cierre registral, ICAC fines |

## Quick reference: thresholds (unchanged at 2026-11-24)

Two of three criteria at the closing date of two consecutive years; in the first year, at its closing date.

| Allowed when not exceeding | Activo | Cifra de negocios | Avg. employees | Source |
|---|---|---|---|---|
| Balance, ECPN and memoria abreviados (and PGC-PYMES) | 4,000,000 € | 8,000,000 € | 50 | LSC art. 257.1; RD 1515/2007 art. 2 |
| PyG abreviada | 11,400,000 € | 22,800,000 € | 250 | LSC art. 258.1 |
| No audit | 2,850,000 € | 5,700,000 € | 50 | LSC art. 263.2 |
| Microempresa criteria | 1,000,000 € | 2,000,000 € | 10 | RD 1515/2007 art. 4 |

EIPs never use abbreviated models (PGC 3rd part, norma 4.ª.3). The bill raising these thresholds lapsed on 6-10-2026; do not apply its figures.

## Quick reference: calendar (calendar-year company)

| Step | Deadline | Source |
|---|---|---|
| Legalise books | 30 April | Ley 14/2013 art. 18 |
| Formulate cuentas, informe de gestión, proposed application of profit | 31 March (3 months) | LSC art. 253.1 |
| Auditor's report | At least 1 month after receiving the signed accounts | LSC art. 270.1 |
| Junta ordinaria approves | 30 June (6 months); valid even if late | LSC art. 164 |
| Deposit at the Registro Mercantil | 1 month after approval | LSC art. 279.1 |
| IS return (modelo 200) | 25 July | LIS art. 124.1 |
| Cierre registral if not deposited | Immediately after the deadline (LSC); the registrar closes the sheet one year after year-end | LSC art. 282; RRM art. 378.1 |

## Documents by model

| Document | Normal | Abreviado | PYMES |
|---|---|---|---|
| Balance | Yes | Yes | Yes |
| Cuenta de pérdidas y ganancias | Yes | Yes (if art. 258 met) | Yes |
| ECPN | Yes | Optional (LSC art. 257.3) | Optional |
| EFE | Yes | Optional (LSC art. 257.3) | Optional |
| Memoria | Full | Abreviada | PYMES |
| Informe de gestión | Yes | Not required if balance and ECPN can be abbreviated (LSC art. 262.3) | Not required |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Whether the company may use abbreviated models or skip the audit | Two consecutive years, two of three criteria, group aggregation for PGC, first-year rule | Get activo, cifra and headcount for this and last year; read `auditoria-y-umbrales.md` |
| Audit required for another reason | Subsidies, public contracts, statutes, minority request (5 %), listed or financial entity | Ask; never infer exemption from size alone |
| Accounts not approved or not deposited for past years | Cierre registral blocks registrations; ICAC fine up to 60,000 € (300,000 € if turnover over 6 M€) | Tell the user; deposit the oldest missing years first |
| Reformulating after formulation | Allowed only for risks known before approval that significantly affect the true and fair view (Cco art. 38.c); auditor reissues | Ask before changing signed accounts |
| Size bill or CSRD "now in force" | Both bills lapsed in October 2026 | Check `spanish-accounting-compliance`, `references/changes-2025-2026.md` |
| Signing, approving, depositing | Only administrators and the junta can | Prepare drafts; the user acts |

## Related skills

| Question | Skill |
|---|---|
| Closing entries, IS accrual, aplicación del resultado | `spanish-year-end-closing` |
| Books, legalisation, PGC structure, errors | `spanish-accounting-compliance` |
| IS return, tax adjustments, reserva de capitalización | `spanish-corporate-tax` |
| Fixed assets and amortisation for the memoria | `spanish-asset-accounting` |
| Inventory valuation | `spanish-inventory` |
| Setting up an SL, first-year rules | `spanish-start-company` |

An agent following this skill never signs, approves, files or deposits without the user's approval.
