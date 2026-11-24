# Corporate tax planning for SMEs

## Contents

- [Year-end sequence](#year-end-sequence)
- [Salary vs dividend for the owner-manager](#salary-vs-dividend-for-the-owner-manager)
- [Using the phased rate cut](#using-the-phased-rate-cut)
- [I+D+i](#idi)
- [Instalment strategy](#instalment-strategy)
- [What the AEAT checks](#what-the-aeat-checks)
- [Sources](#sources)

## Year-end sequence

Run in this order before the books close (calendar year: November-December), then again when the accounts are drawn up (before 31 March):

1. **Confirm the rate bucket** for the period: previous period's INCN of the company and of the group (art. 101.3); entidad patrimonial test (art. 5.2). See `tipos-y-base-imponible.md`.
2. **Timing of income and expenses**: legitimate accrual decisions (invoices for work done, provisions that meet PGC). No tax-only deferral is allowed outside arts. 11-14.
3. **Depreciation choices**: ERD double-rate (art. 103), free depreciation for ≤ 300-euro items up to 25,000 (art. 12.3.e), renewables up to 500,000 for assets running by 31 December 2026 (DA 17ª, ends with 2026), job-creation free depreciation (art. 102). These are deductible without booking (art. 11.3.1º) and create a **479** liability.
4. **Bad debts**: identify receivables over 6 months past due at 31 December (art. 13.1.a); ERD global 1 % (art. 104).
5. **Reserva de capitalización**: the reduction depends on the increase in own funds during the year; avoid distributing dividends out of reserves that cut the increase, and plan headcount growth for the 23/26.5/30 % bonus (art. 25).
6. **Reserva de nivelación** (ERD): consider if a loss is likely within 5 years, and note the open question on eligibility at the transitional rates (`reservas-y-bins.md`).
7. **BINs**: under 1 M euros of base, all can be used; above, 70 %. Use them before they become hard to prove (10 years, art. 26.5).
8. **Owner pay and related-party items**: bylaws clause, market value, modelo 232 thresholds (`operaciones-vinculadas.md`).
9. **Instalments**: decide method for next year by February (modelo 036).

## Salary vs dividend for the owner-manager

Mechanics:

| Route | Company | Owner |
|---|---|---|
| Salary/director pay | Deductible: saves IS at 19-25 % | General IRPF base: progressive, state + regional scale; withholding modelo 111; RETA quota deductible in IRPF |
| Dividend | Not deductible: paid out of profit after IS | Savings base: 19 % to 6,000; 21 % to 50,000; 23 % to 200,000; 27 % to 300,000; 30 % above (state + regional; LIRPF arts. 66 and 76, Ley 7/2024 for 30 % from 2025); company withholds 19 % (modelo 123) |
| Retain in company | Taxed at IS rate; reserva de capitalización can cut it by 20 % of the increase | Nothing until distributed or the shares are sold |

IRPF general scale, state part (LIRPF art. 63, unchanged since 2021):

| Base liquidable up to | State rate on the bracket |
|---|---|
| 12,450 | 9.5 % |
| 20,200 | 12 % |
| 35,200 | 15 % |
| 60,000 | 18.5 % |
| 300,000 | 22.5 % |
| above | 24.5 % |

Each region sets its own half; the regional scale is roughly symmetrical in many regions, giving combined marginal rates of about 19 / 24 / 30 / 37 / 45 / 47 % (state × 2, an approximation: Madrid is lower, Cataluña, Valencia and Asturias higher at the top). Always ask the owner's region of residence.

Rule of thumb (ERD 2026, IS 23 %, dividend taxed at 19-23 %):

- Total tax on a euro paid as dividend: 23 % + 77 % × 21 % ≈ 39 % (at 21 %); ≈ 41 % at 23 %.
- Salary is cheaper while the owner's combined marginal IRPF rate is below about 37-39 %, i.e. up to roughly 35,000-60,000 euros of general base depending on the region, then dividends or retention win.
- Micro in 2026 (19 % on first 50,000): dividend route costs 19 % + 81 % × 21 % ≈ 36 % on the first 50,000 of profit: salary wins only below that marginal IRPF level.

Constraints: director pay must be in the bylaws; RETA contributions follow the owner's income including the director pay and, for controlling partners, the dividends attributed through the company (LGSS art. 308.1.c, regla 1ª); the minimum RETA base for societarios is 1,424.40 euros/month in 2026 (see `spanish-autonomo-tax`, `references/reta-cuotas-2026.md`). Sole-trader vs SL comparison → `spanish-autonomo-tax`, `references/autonomo-vs-sl.md`.

## Using the phased rate cut

ERD rates fall 24 % (2025) → 23 % → 22 % → 21 % → 20 % (2029); micro rates bottom out in 2027 (17/20 %). Consequences:

- Accelerating deductions (free depreciation, ERD double rate) is worth slightly more now than later; deferring income is worth slightly more too, within accrual rules.
- Deferred tax balances must be remeasured each year at the rate expected on reversal (NRV 13ª): a **4740** asset loses value as the rate falls.
- Reserva de nivelación added back in year 5 is taxed at the lower future rate: a small permanent gain.
- The INCN thresholds (1 M, 10 M) are cliffs. A company at 1.05 M euros of INCN pays the ERD rate on all its base the next year; check whether splitting activities across companies is caught by art. 101.3 aggregation (it is, if under common control) and by the anti-abuse rule (LGT art. 15).

## I+D+i

| Step | Detail |
|---|---|
| Classify | I+D (new knowledge, art. 35.1.a; includes advanced software via new theorems, algorithms, operating systems, languages, interfaces) vs innovación tecnológica (art. 35.2.a); routine software maintenance excluded |
| Document | Projects with separate cost records (art. 35.1.b: "individualizados por proyectos") |
| Secure | *Informe motivado* (Ministerio de Ciencia; binding on the AEAT, art. 35.4.a) or *acuerdo previo de valoración* (art. 35.4.c) |
| Compute | 25 %/42 %/+17 % (I+D); 8 % investments; 12 %/15 % (IT, 15 % from RDL 40/2026) |
| Apply | Within the 25 %/50 % cuota limit (art. 39.1), or monetise with 20 % discount (art. 39.2, caps 3 M + 2 M from RDL 40/2026) |
| Social Security | 40 % bonus on employer contributions for researchers in I+D+i exclusively (RD 475/2014, amended by RDL 40/2026 art. 31; unverified detail) |

Software companies: `spanish-industry-saas`.

## Instalment strategy

| Situation | Best method |
|---|---|
| Stable or growing profits | Art. 40.2 (18 % of last cuota): pays less than real during growth |
| Falling profits, or one-off gain last year | Opt for art. 40.3 in February |
| First years of a new company | Art. 40.2 gives zero (no prior cuota); no option needed |
| INCN > 6 M (12 months before) | Art. 40.3 compulsory; ≥ 10 M adds the 23 % minimum |

## What the AEAT checks

- Expenses of partners booked as company costs (cars, travel, meals, family members' pay) without business link.
- Director pay without bylaws basis; pay to relatives above market.
- Interposed companies billing professional services to reduce IRPF (art. 18.6 safe harbour, LIRPF art. 27.1).
- Growing **551** balances (loans to partners): disguised dividends.
- BINs from old years without deposited accounts.
- Reserva de capitalización without the restricted reserve, or with distributions within 3 years.
- I+D+i deductions without informe motivado.
- Tax-planning abuse under LGT arts. 15-16 (conflict in application, simulation).

## Sources

- LIS arts. 11-13, 25, 35, 39, 40, 101-105, DA 17ª; DT 44ª (BOE consolidated, last update 21/11/2026).
- LIRPF arts. 27, 63, 66 (BOE consolidated, last update 18/11/2026); Ley 7/2024.
- RDL 40/2026 (BOE-A-2026-24437).
