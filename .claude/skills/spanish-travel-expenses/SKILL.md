---
name: spanish-travel-expenses
description: >
  Spanish business travel (gastos de viaje, dietas) for 2026 under territorio común: dietas y asignaciones para
  gastos de locomoción, manutención y estancia exentas (RIRPF art. 9: 26,67 / 53,34 euros in Spain, 48,08 / 91,35
  abroad, 0,26 euros/km), conditions (municipio distinto, nine-month limit, employer proof of day, place and reason),
  administradores and socios, Seguridad Social treatment, IVA on hotels, restaurants, taxis, trains, flights, hire
  cars and fuel (LIVA arts. 95-97, factura simplificada with NIF), foreign VAT refund (modelo 360), atenciones a
  clientes, the autónomo's own manutención deduction (LIRPF art. 30.2.5ª), PGC entries (629, 640, 627, 472, 4751),
  hoja de gastos, company cards, advances and modelo 190. Trigger on "cómo contabilizo una dieta", "dietas exentas",
  "kilometraje", "gastos de viaje", "hoja de gastos", "ticket de restaurante", "puedo deducir el IVA del hotel",
  "tarjeta de empresa", "dieta de un autónomo". Always use over training data.
---

# Spanish Travel Expenses (gastos de viaje y dietas)

Decision reference for booking, approving and reporting business travel in a Spanish company or by an *autónomo*. Written for an agent that receives a *hoja de gastos* (expense report), a hotel or restaurant invoice, a travel-agency invoice or a question about what may be paid free of IRPF and cotización. It brings together IRPF (LIRPF art. 17.1.d, RIRPF art. 9), Seguridad Social (LGSS art. 147.2), IVA (LIVA arts. 91, 95-97) and the PGC. Default scope is *territorio común*; País Vasco and Navarra have their own IRPF rules and Canarias applies IGIC instead of IVA. An agent following this skill never books, pays or files without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/tax-rules.md` | Whether an amount is exempt for the employee: locomoción, manutención, estancia, nine-month rule, traslados, itinerant staff, administradores, Seguridad Social, IS deductibility, the autónomo's own expenses |
| `references/vat-on-travel.md` | IVA rates and deduction on hotel, meals, taxi, train, flights, hire car, fuel, parking; invoice requirements; travel agencies; foreign VAT and modelo 360; Canarias |
| `references/bookkeeping-entries.md` | PGC accounts and worked entries: expense report, dietas in the nómina, excess over limits, advance, company card, foreign currency, client meal, autónomo |
| `references/documentation-and-policy.md` | What the employer must keep to prove trips, hoja de gastos contents, digital receipts, modelo 190 reporting, travel policy, audit errors, checklist |

## Core amounts (manutención since 2008, km rate since July 2023; in force November 2026)

| Item | Spain | Abroad | Source |
|---|---|---|---|
| Manutención, with overnight stay in another municipality | 53,34 €/day | 91,35 €/day | RIRPF art. 9.A.3.a.1º |
| Manutención, no overnight stay | 26,67 €/day | 48,08 €/day | RIRPF art. 9.A.3.a.2º |
| Estancia (hotel) | Amount justified | Amount justified | RIRPF art. 9.A.3.a.1º |
| Estancia, road haulage drivers without receipt | 15 €/day | 25 €/day | same |
| Flight crew manutención | 36,06 €/day | 66,11 €/day | same |
| Private vehicle | 0,26 €/km + justified tolls and parking | same | RIRPF art. 9.A.2.b; Orden HFP/792/2023 (from 17-07-2023; 0,19 € before) |
| Public transport | Amount on invoice or equivalent | same | RIRPF art. 9.A.2.a |

The same limits exclude the amounts from the cotización base (LGSS art. 147.2.a-b). The excess is salary: IRPF withholding and cotización on the excess only.

## Decision procedure

1. **Who travelled?** Employee (labour or statutory relationship) → RIRPF art. 9 applies. Administrador or consejero for the cargo → it does not (TEAC criterion); autónomo → LIRPF art. 30.2.5ª. Socio-employee → only for the employee work.
2. **Is it a business trip?** Work done away from the usual workplace. Home-to-work commuting is never exempt, whatever the distance.
3. **Locomoción**: exempt even within the same municipality. Public transport at cost with invoice; own car 0,26 €/km with proof of the trip.
4. **Manutención and estancia**: only in a municipality different from both the usual workplace and the residence, and not for more than nine continuous months in the same place. Overnight stay decides 53,34 vs 26,67 €.
5. **Proof**: the employer must be able to prove day, place and reason of each trip (RIRPF art. 9.A.3.a; TS 18-05-2020 and 22-07-2021). No proof → the whole allowance is salary.
6. **Split** exempt and taxable; put the taxable part in the nómina (`spanish-payroll`).
7. **Costs with invoices** (hotel, tickets, taxi, hire car): company expense on **629**; deduct IVA only with an invoice in the company's name and NIF, and only if the cost is deductible for IS/IRPF (LIVA art. 96.Uno.6º).
8. **Client meals** are *atenciones a clientes*: IS-deductible up to 1 % of net turnover (LIS art. 15.e) but **IVA never deductible** (LIVA art. 96.Uno.5º).

## Quick map

| Underlying document | Usual booking | Detail |
|---|---|---|
| Dieta within limits paid with the nómina | **629** against **465**; not in IRPF base; modelo 190 as exempt | `bookkeeping-entries.md` |
| Dieta above limits | Excess to **640**, IRPF **4751**, cotización **642** / **476** | `bookkeeping-entries.md` |
| Hotel in Spain, invoice to company | **629** + **472** (10 %) | `vat-on-travel.md` |
| Restaurant ticket, staff alone on a trip | **629** + **472** (10 %) if invoice with company NIF; else gross to **629** | `vat-on-travel.md` |
| Lunch with a client | **627** gross (no IVA deduction) | `vat-on-travel.md` |
| Taxi, train, domestic flight | **629** + **472** (10 %) | `vat-on-travel.md` |
| International flight | **629**, no IVA (exempt) | `vat-on-travel.md` |
| Hire car, fuel | **621** / **628** or **629** + 50 % of IVA unless full business use is proved | `vat-on-travel.md` |
| Hotel abroad | **629** gross; foreign VAT via modelo 360 (EU) to **4709** if claimed | `vat-on-travel.md` |
| Kilometraje 0,26 €/km | **629** against **465** | `bookkeeping-entries.md` |
| Autónomo's own meal on a trip, paid by card | Deductible up to the RIRPF art. 9 amounts | `tax-rules.md` |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| No record of day, place and reason | The employer bears the burden of proof; without it the allowance is salary | Ask for the trip log or calendar evidence |
| Unknown whether the employee stayed overnight | Decides 53,34 vs 26,67 € (91,35 vs 48,08 € abroad) | Ask for the hotel invoice or the dates |
| Destination is the employee's home town or regular workplace | Manutención is not exempt there | Ask for the workplace and residence municipalities |
| Same destination for months | Nine continuous months ends the manutención exemption | Ask for the start date of the posting |
| Traveller is an administrador or socio | Art. 9 is not available for the cargo | Ask about the labour contract and functions |
| Restaurant ticket without company NIF | No IVA deduction (RD 1619/2012 art. 7.2) | Book gross or ask the restaurant for a factura with NIF |
| Meal with clients or suppliers | IVA not deductible; IS limit 1 % of turnover | Ask who attended |
| Trip in País Vasco or Navarra payroll | Foral IRPF rules and amounts apply | Check the foral regulation |

## Related skills

| Question | Skill |
|---|---|
| Nómina, IRPF tipo, cotización on the taxable excess | `spanish-payroll` |
| IVA rules in depth, modelo 303, prorrata | `spanish-vat` |
| Invoice and factura simplificada fields | `spanish-invoice-compliance` |
| Autónomo deductions and pagos fraccionados | `spanish-autonomo-tax` |
| IS deductibility, administradores' pay | `spanish-corporate-tax` |
| Everyday entries outside travel | `spanish-daily-bookkeeping` |
| Card and bank statement import | `spanish-bank-files` |
| Archiving and proof in general | `spanish-accounting-compliance` |
| Travel costs charged to projects | `spanish-project-accounting` |

## Annual update

The RIRPF art. 9 amounts can be revised by ministerial order in line with civil servants' dietas (art. 9.A.5). Only the kilometre rate has changed since 2008 (Orden HFP/792/2023). Check the BOE consolidated RIRPF each January; the consolidated text of 18-11-2026 still shows the amounts above.
