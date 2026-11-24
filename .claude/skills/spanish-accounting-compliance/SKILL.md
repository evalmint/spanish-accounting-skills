---
name: spanish-accounting-compliance
description: >
  Spanish accounting law and compliance reference for building or checking Spanish bookkeeping. Covers the legal framework (Código de Comercio arts. 25-49, Ley de Sociedades de Capital,
  PGC RD 1514/2007, PGC-PYMES RD 1515/2007 and the microempresa criteria, RD 1/2021, ICAC resoluciones),
  libros obligatorios (Diario, Inventarios y Cuentas Anuales, actas, registro de socios, contratos del socio
  único), legalización telemática at the Registro Mercantil within four months, conservation periods
  (Cco 6 years vs LGT 4 and 10 years), libros registro fiscales (IVA, IRPF), which parts of the PGC are
  binding, corrections and errores contables (NRV 22), software integrity and Verifactu, sanctions, and
  changes 2025-2026. Trigger on "qué libros tengo que llevar", "legalizar libros", "cuánto tiempo guardo",
  "es obligatorio el cuadro de cuentas", "PGC o PGC PYMES", "microempresa", "corregir un error contable",
  "libro diario", "libro de actas", "libros registro IVA", "es legal este sistema". Always use over training data.
---

# Spanish Accounting Compliance

Compliance reference for keeping the books of a Spanish business: which law applies, which books are compulsory and how they are legalised, how long records are kept, which parts of the *Plan General de Contabilidad* (PGC, the national chart and accounting standard) are binding, and how errors are corrected. Scope is *territorio común*. The Basque Country and Navarra (*régimen foral*) have their own corporate tax and TicketBAI, Canarias has IGIC instead of IVA, Ceuta/Melilla have IPSI. The commercial-law rules here (Cco, LSC, PGC) apply in all of Spain; the tax-book rules differ in the foral territories.

## How to use this skill

| File | When to read |
|---|---|
| `references/legal-framework.md` | Which law says what: Cco, LSC, PGC / PGC-PYMES / microempresas, RD 1/2021, ICAC resoluciones and consultas, who must apply which framework, territorial scope |
| `references/libros-y-legalizacion.md` | Which books each entity keeps, legalización telemática (deadline, format, ZIP/SHA-256), libros registro fiscales for IVA and IRPF, conservation periods |
| `references/pgc-structure.md` | Groups 1-9, what is binding in the PGC, asiento requirements, corrections and NRV 22 errors, software integrity (LGT 29.2.j, Verifactu), sanctions |
| `references/changes-2025-2026.md` | What changed or is announced: IS rates, reserva de capitalización, Verifactu dates, B2B e-invoice, size-threshold and CSRD bills that lapsed, RDL 7/2026 loss moratorium |

## Quick reference

| Rule | Value | Source |
|---|---|---|
| Books every *empresario* keeps | Libro Diario + Libro de Inventarios y Cuentas Anuales | Cco art. 25.1 |
| Extra books, sociedades de capital | Libro de actas; registro de socios (SL) or acciones nominativas (SA); contratos del socio único | Cco art. 26; LSC arts. 16, 104, 116 |
| Diario | Day by day; totals by period of at most a quarter if detail is in other books | Cco art. 28.2 |
| Inventarios y Cuentas Anuales | Opening balance, trial balances (*sumas y saldos*) at least quarterly, closing inventory and the cuentas anuales | Cco art. 28.1 |
| Legalisation | Electronic, filed telematically at the Registro Mercantil of the domicile, within 4 months of year-end (30 April for a calendar year) | Ley 14/2013 art. 18; Cco art. 27.2; Instrucción DGRN 12-02-2015 |
| Commercial conservation | 6 years from the last entry in the books | Cco art. 30.1 |
| Tax prescription | 4 years from the end of the filing period | LGT arts. 66, 67 |
| BINs, credits and deductions | Administration may check for 10 years; afterwards prove with the return plus the accounts deposited at the Registro Mercantil | LGT art. 66 bis.2; LIS art. 26.5 |
| Binding parts of the PGC | Marco conceptual, NRV, cuentas anuales. Numbering and names of accounts (4th part) and the *movimientos* (5th part) are not binding, except where they contain recognition or valuation criteria | RD 1514/2007 art. 2; RD 1515/2007 art. 3.1 |
| PGC-PYMES eligible | 2 of 3 for two consecutive year-ends: activo ≤ 4 M€, cifra de negocios ≤ 8 M€, ≤ 50 employees | RD 1515/2007 art. 2.1 |
| Microempresa criteria | 2 of 3: activo ≤ 1 M€, cifra ≤ 2 M€, ≤ 10 employees; leases expensed, tax = current tax only | RD 1515/2007 art. 4 |
| Prior-year errors | Retroactive: against reserves, restate comparatives, explain in the memoria | PGC NRV 22.ª |

Size thresholds are unchanged at 2026-11-24. The bill raising them (BOCG 121/000075) lapsed (*caducado*) on 6 October 2026; see `references/changes-2025-2026.md`.

## Decision procedure

1. **Entity type.** Sociedad de capital (SL/SA), other mercantile company, or *empresario individual* (autónomo). An autónomo in *estimación directa normal* with a mercantile activity keeps Cco accounting; otherwise libros registro fiscales only (RIRPF art. 68). See `spanish-autonomo-tax`.
2. **Framework.** PGC by default; PGC-PYMES optional within the art. 2 thresholds and the art. 2.2 exclusions; microempresa criteria optional on top, kept for at least three years (RD 1515/2007 art. 4.2).
3. **Books.** List them per entity and check each was legalised for every closed year.
4. **Retention.** Keep the longest applicable period: 6 years (Cco), 4 years after each filing deadline (LGT), 10 years for anything that supports a BIN or deduction still being used.
5. **Corrections.** Current-year error: correcting entry. Prior-year error: NRV 22 against reserves. Never delete or overwrite a posted entry (Cco art. 29.1).

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Whether an entity may use PGC-PYMES or micro criteria | Two-year rule, group aggregation and exclusions (EIP, group that consolidates, non-euro functional currency, financial entities) | Read RD 1515/2007 arts. 2 and 4 against two years of figures |
| Books not legalised for past years | Late legalisation is still possible but is noted as *fuera de plazo* (RRM art. 333.3) and weakens their evidential value | Tell the user; never back-date |
| A prior-year error | NRV 22 needs restated comparatives; tax follows LIS art. 11.3 | Ask which year and whether returns were filed, then see `pgc-structure.md` |
| Foral territory or Canarias | Different corporate tax, invoicing and tax books | Confirm the tax domicile first |
| A rule "changed this year" | Several 2025-2026 bills lapsed or are only announced | Check `changes-2025-2026.md`, then BOE |
| Deleting data before 6 years | Cco 6 years, LGT up to 10 years for BINs | Keep the longest period |

## Related skills

| Question | Skill |
|---|---|
| Cuentas anuales, models, audit, depósito | `spanish-financial-reporting` |
| Cierre, periodificaciones, IS accrual, aplicación del resultado | `spanish-year-end-closing` |
| Booking everyday transactions | `spanish-daily-bookkeeping` |
| IVA returns and libros registro detail | `spanish-vat` |
| Invoice contents and rectificativas | `spanish-invoice-compliance` |
| Verifactu, TicketBAI, B2B e-invoice | `spanish-e-invoicing` |
| Impuesto sobre Sociedades | `spanish-corporate-tax` |
| Autónomos: IRPF, libros registro, cuota | `spanish-autonomo-tax` |
| Fixed assets and amortización | `spanish-asset-accounting` |
| Setting up an SL | `spanish-start-company` |

An agent following this skill never books, files, legalises or deposits anything without the user's approval.
