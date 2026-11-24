# IRPF withholding on employment income (retenciones)

How to compute the *tipo de retención* for employees in territorio común. Sources: LIRPF (Ley 35/2006) arts. 99-101; RIRPF (RD 439/2007) arts. 74-88 and 108; AEAT *Algoritmo de cálculo del tipo de retención 2026* (version from 10 September 2026). País Vasco and Navarra apply their own foral tables and forms; Ceuta and Melilla (and La Palma for 2023-2026) get a 60 % reduction.

## Contents

1. Fixed rates
2. General procedure (RIRPF arts. 82-86)
3. 2026 parameters
4. Límites excluyentes (no withholding)
5. Minimum rates
6. Modelo 145 and employee communications
7. Regularización (RIRPF art. 87)
8. The SMI deductions: 2026 and 2027
9. Special cases

## 1. Fixed rates (RIRPF art. 80.1)

| Recipient | Rate |
|---|---|
| Administradores and consejeros (for the cargo) | 35 %; 19 % if the paying entity's INCN in the last closed year was under 100 000 € |
| Courses, conferences, seminars; literary/artistic/scientific works with assignment of rights | 15 % (7 % for works under conditions) |
| Atrasos attributable to prior years | 15 % |
| Everything else in an employment relationship | Procedure below |

## 2. General procedure

Steps of the AEAT algorithm (the payer may not apply a lower result; the employee may ask in writing for a higher one, RIRPF art. 88.5):

1. **Retribuciones totales** (*RETRIB*): fixed plus foreseeable variable cash pay for the year, including pagas extra and especie value (RIRPF art. 83.2). For a contract shorter than a year, use the remuneration of the contract period (not annualised); the 2 % floor then applies (art. 86.2).
2. **Gastos deducibles**: employee cotizaciones + 2 000 € general (art. 19.2.f LIRPF), + 2 000 € more for geographic mobility, + 3 500 € / 7 750 € for active workers with disability.
3. **Rendimiento neto** minus **reducción por rendimientos del trabajo** (LIRPF art. 20): 7 302 € if RNT ≤ 14 852 €; 7 302 − 1,75 × (RNT − 14 852) up to 17 673,52 €; 2 364,34 − 1,14 × (RNT − 17 673,52) up to 19 747,50 €; zero above.
4. Subtract pensiones compensatorias and descendant/spouse reductions where applicable → **base para calcular el tipo**.
5. **Cuota 1** = escala(base); **cuota 2** = escala(mínimo personal y familiar). Cuota = cuota 1 − cuota 2 (≥ 0).
6. **Límite del 43 %** when RETRIB ≤ 35 200 €: cuota ≤ 43 % × (RETRIB − límite excluyente of table 1) (art. 85.3).
7. Minus 2 % of RETRIB if the employee notified a pre-2013 home loan (art. 86.1, RETRIB < 33 007,20 €).
8. **Tipo** = cuota / RETRIB × 100, truncated to two decimals; apply the floors (§5).
9. Withhold tipo × each cash payment; apply tipo to especie for the ingreso a cuenta (RIRPF art. 102).

## 3. 2026 parameters (AEAT algorithm 2026)

**Escala de retención** (state + autonomic combined for withholding):

| Base up to | Cuota | Rest up to | Rate |
|---|---|---|---|
| 0 | 0 | 12 450 | 19 % |
| 12 450 | 2 365,50 | 7 750 | 24 % |
| 20 200 | 4 225,50 | 15 000 | 30 % |
| 35 200 | 8 725,50 | 24 800 | 37 % |
| 60 000 | 17 901,50 | 240 000 | 45 % |
| 300 000 | 125 901,50 | onward | 47 % |

**Mínimo personal y familiar** (LIRPF arts. 56-61): contribuyente 5 550 € (+1 150 € over 65, +1 400 € more over 75); descendientes 2 400 / 2 700 / 4 000 / 4 500 € (1st/2nd/3rd/4th+), +2 800 € under 3; ascendientes 1 150 € (+1 400 € over 75); taxpayer disability 3 000 € (33-65 %) / 9 000 € (65 % or more) plus 3 000 € asistencia. All amounts as used in the AEAT 2026 algorithm; descendants count when under 25 (or disabled) and living with the employee, split by halves when both parents claim.

The 2026 algorithm changed on 10 September 2026 only to extend the Ceuta/Melilla-style 60 % reduction to La Palma residents for 2026 (RDL 23/2026, LIRPF DA 57ª).

## 4. Límites excluyentes (RIRPF art. 81, as amended by RD 142/2024)

No withholding if RETRIB does not exceed:

| Situación familiar | 0 children | 1 child | 2 or more |
|---|---|---|---|
| 1. Single, widowed, divorced or separated with children living with them | n/a | 17 644 € | 18 694 € |
| 2. Spouse with income ≤ 1 500 €/year | 17 197 € | 18 130 € | 19 262 € |
| 3. Other cases (incl. single without children) | 15 876 € | 16 342 € | 16 867 € |

These limits were set to the 2024 SMI and were **not** updated for 2025 or 2026. A single employee on the 2026 SMI (17 094 €) is above 15 876 € and suffers withholding during 2026; the RDL 5/2026 deduction (§8) gives it back in the annual return.

## 5. Minimum rates (RIRPF art. 86.2)

| Case | Floor | Ceuta/Melilla |
|---|---|---|
| Contract or relationship shorter than one year (includes artists' special relationship since 2023) | 2 % | 0,8 % |
| Other *relaciones laborales especiales de carácter dependiente* (except prisoners and disabled workers in centros especiales de empleo) | 15 % | 6 % |

The 2 % floor applies even when the result is zero, but not when RETRIB is under the límite excluyente (then no withholding at all). After a regularisation, the tipo may not exceed 47 % (art. 87.5).

## 6. Modelo 145 and employee communications (RIRPF art. 88)

- The employee communicates personal and family data on **modelo 145** (AEAT resolution) before 1 January or before starting work; the payer keeps it signed. Not repeated each year unless data change.
- Contents: NIF and birth year, situación familiar (1, 2 or 3) and spouse NIF in situation 2, disability degree, geographic mobility, descendants under 25 (birth/adoption year, disability, whether computed by halves), ascendants over 65 living with the employee, pensiones compensatorias and anualidades por alimentos by court order, pre-2013 home loan.
- Without modelo 145 the payer computes without family circumstances (art. 88.2), which is never too low; do not invent data.
- Changes lowering the tipo take effect if communicated at least 5 days before the nómina is prepared; changes raising it must be communicated within 10 days (art. 88.4).

## 7. Regularización (RIRPF art. 87)

Recompute when, among others: a temporary contract is extended or renewed in the year; salary changes (raise, promotion, new convenio, bonus not foreseen); geographic mobility; birth or adoption; disability; court-ordered pensions; spouse's income exceeds 1 500 €; change of residence to/from foral territory or Ceuta/Melilla; the RETRIB crosses 33 007,20 € with the home-loan reduction.

Method: new annual cuota per art. 85 with updated data, minus withholding already made, divided by remaining remuneration to year-end = new tipo (two decimals; floors still apply; no refund if negative). Payer may choose to regularise from 1 April, 1 July, 1 October for changes in the previous quarter (art. 87.4). Regularisations caused only by a fall in base or new alimentos cannot raise the tipo (art. 87.5).

## 8. The SMI deductions: 2026 and 2027

| Year | Rule | Effect on payroll |
|---|---|---|
| 2025 | DA 61ª LIRPF deducción por rendimientos del trabajo (unverified amounts for 2025) | Annual return only |
| 2026 | RDL 5/2026 art. 28 (BOE 19-02-2026), effects 1-1-2026: 590,89 € if employment income ≤ 17 094 €; 590,89 − 0,2 × (income − 17 094) up to 20 048,45 €; other income ≤ 6 500 € | **No change to withholding in 2026**; recovered in the 2026 annual return (spring 2027) |
| 2027 | RDL 38/2026 art. 5 (BOE 18-11-2026), effects 1-1-2027: 1 033,58 € if ≤ 18 004 €; 1 033,58 − 0,2 × (income − 18 004) up to 23 171,89 € | RDL 38/2026 art. 6 adds a new art. 85.3 RIRPF from 1-1-2027: withholding is reduced by the same amount, never below zero, for employment income under 23 171,89 € a year |

RDL 38/2026 must be convalidated by Congress within 30 days of publication. Check the convalidación and the AEAT 2027 algorithm before releasing January 2027 payroll.

## 9. Special cases

- **Two payers or a second job**: each payer computes independently; the employee may ask for a higher rate.
- **Temporary employees renewed**: regularise (art. 87.2.1º).
- **Beckham regime** (impatriados, LIRPF art. 93): withholding at 24 % up to 600 000 € and 47 % above, as non-residents (RIRPF art. 114; unverified figures); needs the AEAT certificate.
- **Non-residents**: IRNR, flat 24 % (19 % EU/EEA) on Spanish-source salary; seasonal workers 2 % (TRLIRNR art. 25; unverified).
- **Indemnización por despido**: exempt part not withheld; the excess is withheld at the employee's tipo with the 30 % reduction of LIRPF art. 18.2 if the seniority exceeds two years (see `finiquito-e-indemnizaciones.md`).
- **Especie**: ingreso a cuenta = tipo × valuation (RIRPF art. 102). If the company bears it, the ingreso a cuenta itself is more especie and is added to the value in the modelo 190 (LIRPF art. 43.2).
