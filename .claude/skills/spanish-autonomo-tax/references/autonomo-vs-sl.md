# Autónomo vs SL: when incorporating pays off

## Contents

- [The structural difference](#the-structural-difference)
- [Assumptions of the model](#assumptions-of-the-model)
- [Results, 2026](#results-2026)
- [Reading the results](#reading-the-results)
- [Non-tax factors](#non-tax-factors)
- [Moving from autónomo to SL](#moving-from-autónomo-to-sl)
- [Sources](#sources)

## The structural difference

| | Autónomo | SL with owner-director |
|---|---|---|
| Profit taxed by | IRPF general base, progressive (combined marginal ~19 % to ~47-54 % depending on region) | IS: micro 19 %/21 % in 2026, 17 %/20 % from 2027; ERD 23 % in 2026 falling to 20 % in 2029 (LIS art. 29, DT 44ª) |
| Owner's pay | n/a: all profit is the owner's income | Salary/director pay (deductible for IS, IRPF general base) + dividends (savings base 19-30 %) |
| Retained profit | Taxed anyway in IRPF | Taxed only at IS until distributed |
| RETA | On net income + own quotas, −7 % | On salary + dividends from the company (if ≥ 33 % or ≥ 25 % and director), −3 %; minimum base 1,424.40 euros/month in 2026 (LGSS art. 308.1.a regla 4ª) |
| Fixed costs | Low | Incorporation (notary, registry), annual accounts and their deposit, IS return, more complex bookkeeping (assumption: about 2,000 euros/year more, unverified market figure) |
| Liability | Unlimited (personal assets; Ley 14/2013 protects the main home only under conditions) | Limited to capital (minimum 1 euro since Ley 18/2022, with safeguards) |

## Assumptions of the model

Illustrative only; the agent must recompute with the user's region and data:

- Year 2026; profit P is profit before the owner's pay and RETA.
- IRPF combined general scale approximated as the state scale doubled: 19 / 24 / 30 / 37 / 45 / 49 % (brackets 12,450 / 20,200 / 35,200 / 60,000 / 300,000); mínimo personal 5,550; no family allowances or regional deductions. Savings scale 19 / 21 / 23 / 27 / 30 % (LIRPF arts. 63, 66, 76).
- Autónomo in EDS: RETA at the minimum base of the tramo for (P × 0.93)/12; 5 % allowance capped at 2,000.
- SL: microempresa 2026 (19 % on first 50,000, 21 % above); owner salary S as director (bylaws clause); RETA paid by the owner at the minimum base of the tramo for (S + dividends) × 0.97/12, never below 1,424.40; 2,000 "otros gastos" work-income deduction (LIRPF art. 19.2.f); extra SL running costs 2,000; either all after-tax profit distributed as dividends in the year, or all retained.
- Ignores: the art. 20 work-income reduction (small at these salaries), art. 32 reductions, start-up 15 % IS and 20 % IRPF start-up reduction, tarifa plana.

## Results, 2026

Total tax + RETA + extra SL costs, as share of P:

| Profit P | Autónomo | SL, salary 30,000, distribute all | SL, salary 45,000, distribute all | SL, salary 30,000, retain rest | SL, salary 45,000, retain rest |
|---|---|---|---|---|---|
| 40,000 | 31.0 % | 35.2 % | 36.6 % | 32.0 % | 37.6 % |
| 60,000 | 33.7 % | 36.8 % | 35.4 % | 27.7 % | 31.4 % |
| 80,000 | 36.2 % | 36.6 % | 35.6 % | 25.5 % | 28.3 % |
| 100,000 | 38.0 % | 37.4 % | 36.2 % | 24.6 % | 26.5 % |
| 150,000 | 40.3 % | 38.0 % | 37.1 % | 23.4 % | 24.7 % |

The "retain" columns defer the dividend tax: when the reserves are eventually distributed, add 19-30 % on them.

## Reading the results

1. **If the owner spends everything**, the SL breaks even only at about **80,000-100,000 euros** of profit, and gains 1-3 points above that. Below 60,000 the autónomo is cheaper, mainly because of the SL fixed costs and the societario's higher minimum RETA base.
2. **If profits can stay in the company** (investment, savings, later sale), the SL wins from about **50,000-60,000 euros**: the retained part pays 19-21 % instead of 37-45 % marginal IRPF.
3. The optimal salary is the one that pushes the owner's marginal IRPF rate up to roughly the combined IS + dividend cost (≈ 36-39 % in 2026 for a micro): around 35,000-50,000 euros of salary with the approximate scale.
4. The 2027-2029 IS cuts (micro 17/20 %, ERD 20 %) make the SL a bit more attractive each year.
5. Regions matter: in a low-tax region (Madrid) the autónomo's IRPF is lower and the break-even rises; in high-tax regions it falls.

## Non-tax factors

- Liability and risk of the business.
- Clients that prefer to contract with companies, public tenders.
- Exit: selling shares of an SL (capital gain, savings base) vs transferring an autónomo business (gains on each asset).
- Admin burden: accounts deposit (Registro Mercantil), IS returns, modelo 232 if related-party thresholds are met, bylaws.
- Access to the 15 % IS rate for new entities (LIS art. 29.1) is lost if the activity was carried on by the same person as an autónomo in the year before incorporation and they hold > 50 % (art. 29.1.b), so the autónomo-to-SL move does not get the 15 %.
- Interposition risk: an SL that just invoices the owner's personal professional services, with no means of its own, invites the AEAT to impute the income to the individual (LIS art. 18.6, LIRPF art. 27.1, LGT art. 16 simulation doctrine).
- Pension: RETA base chosen affects future benefits in both cases.

## Moving from autónomo to SL

| Step | Note |
|---|---|
| Incorporate the SL | See `spanish-start-company` |
| Transfer the business | Contribution of the branch of activity (*rama de actividad*) to the SL can use the neutrality regime (LIS arts. 76.3, 87: individual contributing a business that keeps accounts under the Código de Comercio) (unverified for EDS autónomos without commercial accounts); otherwise sale or contribution at market value with IRPF gains |
| IVA | Transfer of a whole business is not subject to IVA (LIVA art. 7.1º) |
| Deregister as autónomo for the activity | Modelo 036 baja; keep RETA as societario if controlling partner (no break) |
| Tarifa plana | Not available again if the person was in RETA in the last 2 years (LETA art. 38 ter) |
| Módulos | Ends: an SL cannot use módulos, and IVA simplificado ends for that activity |

## Sources

- LIS arts. 18, 29, DT 44ª; LIRPF arts. 19, 27, 63, 66, 76 (BOE consolidated, November 2026).
- LGSS arts. 305, 308; Orden PJC/297/2026 art. 18.
- LIVA art. 7.1º; LETA art. 38 ter.
