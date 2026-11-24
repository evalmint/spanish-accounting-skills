# Cotizaciones a la Seguridad Social 2026 (Régimen General)

Bases, tipos and worked calculations for employees in the Régimen General. Sources: Orden PJC/297/2026, de 30 de marzo (BOE 31-03-2026, in force 1-4-2026, effects from 1-1-2026), which develops RDL 3/2026 art. 3 and LGSS (RDLeg 8/2015). Seguridad Social is the same in all of Spain, including País Vasco, Navarra and Canarias.

## Contents

1. What changed in 2025-2026
2. Base de cotización
3. Bases mínimas y máximas 2026 by grupo
4. Tipos 2026
5. MEI
6. Cotización adicional de solidaridad
7. AT/EP: tarifa by CNAE-2025
8. Contratos de duración determinada under 30 days
9. Contratos formativos
10. Worked examples
11. Catch-up for the late Orden

## 1. What changed in 2025-2026

- **RDL 16/2025** (23-12-2025) carried the 2026 cotización rules but Congress voted it down; the derogation was published 28-01-2026 (BOE-A-2026-2024). **RDL 3/2026** (BOE 04-02-2026) re-enacted the measures and was convalidated on 26-02-2026. The Orden de cotización only arrived on 31 March 2026.
- **AT/EP tarifa** moved into LGSS DA 61ª and was re-coded to **CNAE-2025** (RD 10/2025) for liquidations from 1-1-2026. Companies that did not report their CNAE-2025 code get the highest AT/EP rate among all CNAE-2025 codes that correspond to their CNAE-2009 code (INE tables); a code reported during 2026 takes effect from the next liquidation period, never retroactively (LGSS DT 45ª, added by RDL 3/2026).
- **Ley 2/2026, de 29 de julio** (BOE-A-2026-16653, in force 1-8-2026) concerns *mutualidades alternativas* to RETA (the self-employed regime), not the Régimen General: it raises the mutualistas' minimum contribution to 86 % (2026) and 93 % (2027) of the RETA reference quota, 100 % in 2028 (LGSS DT 46ª), and adds transparency duties (LGSS DA 62ª-63ª). The passage (*pasarela*) from a mutualidad to RETA itself was not re-read here. Relevant for professionals, not for employee payroll; see `spanish-autonomo-tax`.
- **MEI** rose from 0,80 % to 0,90 %. **Solidaridad** rates rose from 0,92/1,00/1,17 % to 1,15/1,25/1,46 %.
- **Base máxima** 4 909,50 € (2025) → 5 101,20 € (2026).

## 2. Base de cotización

LGSS art. 147: total monthly remuneration in cash or kind that the worker is entitled to, or receives if higher, plus the monthly prorrata of pagas extra and other more-than-monthly items.

Excluded only (LGSS art. 147.2):

| Item | Limit |
|---|---|
| Locomoción in public transport with invoice | Actual amount |
| Kilometraje, manutención y estancia | Same amounts and conditions as RIRPF art. 9 (see `spanish-travel-expenses`) |
| Indemnizaciones por fallecimiento, traslado, suspensión | Up to the amount in law, sector norm or convenio |
| Indemnizaciones por despido | Statutory amount in the ET; not amounts fixed by agreement |
| Prestaciones de la Seguridad Social and company IT top-ups (*mejoras de IT*) | Full |
| Training required by the job | Full |
| Horas extraordinarias | Excluded from CC base, included in AT/EP base |

Everything else cotiza, including especie that is exempt from IRPF (seguro médico, cheque comida, guardería, transport card, shares). The employer must report every concept paid each month, included or not (LGSS art. 147.3), through the CRA file (see `filing-red-111-190.md`).

Then clamp the base between the grupo's base mínima and the base máxima (pro rata to days in the month for daily-paid groups, and to hours for part-time).

## 3. Bases mínimas y máximas 2026 (Orden PJC/297/2026 art. 3)

| Grupo | Categoría | Base mínima | Base máxima |
|---|---|---|---|
| 1 | Ingenieros y licenciados, alta dirección not in ET art. 1.3.c | 1 989,30 €/month | 5 101,20 €/month |
| 2 | Ingenieros técnicos, peritos y ayudantes titulados | 1 649,70 €/month | 5 101,20 €/month |
| 3 | Jefes administrativos y de taller | 1 435,20 €/month | 5 101,20 €/month |
| 4 | Ayudantes no titulados | 1 424,40 €/month | 5 101,20 €/month |
| 5 | Oficiales administrativos | 1 424,40 €/month | 5 101,20 €/month |
| 6 | Subalternos | 1 424,40 €/month | 5 101,20 €/month |
| 7 | Auxiliares administrativos | 1 424,40 €/month | 5 101,20 €/month |
| 8 | Oficiales de primera y segunda | 47,48 €/day | 170,04 €/day |
| 9 | Oficiales de tercera y especialistas | 47,48 €/day | 170,04 €/day |
| 10 | Peones | 47,48 €/day | 170,04 €/day |
| 11 | Trabajadores menores de 18 años | 47,48 €/day | 170,04 €/day |

- Tope mínimo for AT/EP: SMI + one sixth, not below 1 424,40 € (art. 2.2).
- Part-time: bases mínimas per hour are in the Orden; read them there for each grupo (not reproduced here).

## 4. Tipos 2026

| Concept | Empresa | Trabajador | Total | Article |
|---|---|---|---|---|
| Contingencias comunes | 23,60 % | 4,70 % | 28,30 % | art. 4.a |
| Horas extra, fuerza mayor | 12,00 % | 2,00 % | 14,00 % | art. 5 |
| Horas extra, other | 23,60 % | 4,70 % | 28,30 % | art. 5 |
| Desempleo, indefinido (incl. part-time, fijo discontinuo, formativos, relevo, sustitución, disability ≥ 33 %) | 5,50 % | 1,55 % | 7,05 % | art. 33.2.a.1º |
| Desempleo, duración determinada (full or part time) | 6,70 % | 1,60 % | 8,30 % | art. 33.2.a.2º |
| FOGASA | 0,20 % | | 0,20 % | art. 33.2.b |
| Formación profesional | 0,60 % | 0,10 % | 0,70 % | art. 33.2.c |
| MEI | 0,75 % | 0,15 % | 0,90 % | art. 16 |
| AT/EP | tarifa | | by CNAE / occupation | art. 4.b; LGSS DA 61ª |

Desempleo, FOGASA and FP use the AT/EP base (art. 33.1). When a temporary contract becomes indefinido, 7,05 % applies from the date of conversion.

## 5. MEI (Mecanismo de Equidad Intergeneracional)

LGSS art. 127 bis: a ring-fenced cotización for the Fondo de Reserva, on the CC base, never reduced by bonificaciones.

| Year | Total | Empresa | Trabajador |
|---|---|---|---|
| 2023 | 0,60 % | 0,50 % | 0,10 % |
| 2024 | 0,70 % | 0,58 % | 0,12 % |
| 2025 | 0,80 % | 0,67 % | 0,13 % |
| 2026 | 0,90 % | 0,75 % | 0,15 % |
| 2029 onward | 1,20 % | 1,00 % | 0,20 % |

2023-2024 splits and the 2027-2028 steps (expected 1,00 % and 1,10 %) are from the LGSS transitional schedule (unverified here; read the Orden each year).

## 6. Cotización adicional de solidaridad

Since 2025, the part of monthly remuneration (LGSS art. 147 concept) **above the base máxima** pays an extra cotización, split in the same proportion as contingencias comunes (LGSS art. 19 bis; Orden PJC/297/2026 art. 17).

| Tramo (monthly remuneration) | 2026 total | Empresa | Trabajador | 2025 total |
|---|---|---|---|---|
| 5 101,21 to 5 611,32 € (up to +10 %) | 1,15 % | 0,96 % | 0,19 % | 0,92 % |
| 5 611,33 to 7 651,80 € (+10 % to +50 %) | 1,25 % | 1,04 % | 0,21 % | 1,00 % |
| Above 7 651,80 € | 1,46 % | 1,22 % | 0,24 % | 1,17 % |

The rates rise each year until they reach 5,5 / 6 / 7 % (LGSS art. 19 bis, target values; reached in 2045 per the transitional schedule, unverified). Remuneration includes the prorrata of pagas extra.

## 7. AT/EP: tarifa de primas

- LGSS DA 61ª (added by RDL 3/2026): *Cuadro I* gives a rate per CNAE-2025 activity (IT + IMS); *Cuadro II* gives rates by occupation that override Cuadro I when they differ. Paid entirely by the employer.
- Cuadro II 2026: a) office-only staff 1,50 % (0,80 + 0,70); b) sales representatives 2,00 %; d) building trades 6,70 %; f) truck drivers over 3,5 t 6,70 %; g) cleaning 3,60 %; h) security staff 3,60 %.
- Examples from Cuadro I: 41 construcción de edificios 6,70 %; 47 comercio al por menor (most) 1,65 %; 56 servicios de comidas y bebidas 1,50 %; 62 programación y consultoría informática 1,50 %; 86 actividades sanitarias (except 869) 1,50 %.
- "Office staff" means people not exposed to the risks of the company's activity, working only in office premises (DA 61ª.2, rule 3).
- During IT and other suspensions with cotización, the rate of the activity/occupation still applies.
- TGSS assigns the rate from the CNAE the company declared. Check the CNAE-2025 code in the TGSS record before running January.

## 8. Contratos de duración determinada under 30 days

At the end of a temporary contract shorter than 30 days, the employer pays a fixed **33,62 €** (2026) extra cotización (Orden PJC/297/2026 art. 28; LGSS art. 151). Excluded: contratos de sustitución, formación en alternancia, some agrarian, domestic and mining contracts, among others (art. 28.2).

## 9. Contratos formativos

*Contrato de formación en alternancia*: fixed monthly cuotas when the base does not exceed the base mínima (art. 46): CC 69,23 € (57,72 empresa + 11,51 trabajador), AT/EP 7,95 €, FOGASA 4,38 €, FP 2,44 € (2,16 + 0,28). Above that, the general rules. *Contrato formativo para la obtención de práctica profesional* cotiza under the general rules.

## 10. Worked examples

**A. Standard office employee** (2 200 €/month × 14, indefinido, grupo 5): base 2 566,67 € (2 200 + 366,67 prorrata).

| Concept | Empresa | Trabajador |
|---|---|---|
| CC | 605,73 | 120,63 |
| Desempleo | 141,17 | 39,78 |
| FOGASA | 5,13 | |
| FP | 15,40 | 2,57 |
| MEI | 19,25 | 3,85 |
| AT/EP 1,50 % | 38,50 | |
| **Total** | **825,18** | **166,83** |

**B. High earner** (7 000 €/month including prorrata): base capped at 5 101,20 €. Solidaridad on the 1 898,80 € above: 510,12 € in tramo 1 and 1 388,68 € in tramo 2. Empresa 510,12 × 0,96 % + 1 388,68 × 1,04 % = 19,34 €; trabajador 510,12 × 0,19 % + 1 388,68 × 0,21 % = 3,89 €.

**C. Temporary contract, 20 days**: desempleo 6,70 % + 1,60 %, plus 33,62 € when it ends.

Rounding: TGSS computes per worker and concept in the SLD; use its figures for booking, not your own.

## 11. Catch-up for the late Orden

Differences from applying the 2026 Orden retroactively to January-March 2026 (disposición transitoria primera): in liquidación directa, pay by the last day of the month after the TGSS notice; in autoliquidación, without recargo by the last day of the second month after the Orden's publication. Atrasos de convenio follow RGR art. 56.1.c and Orden art. 29 (complementary liquidation with the bases and rates of each month affected).
