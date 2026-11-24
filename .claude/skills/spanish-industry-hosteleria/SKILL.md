---
name: spanish-industry-hosteleria
description: >
  Spanish accounting for hostelería: restaurants, bars, cafés and hotels. Covers IVA 10 % on servicios de
  restauración and hostelería including alcohol served on the premises, take-away and delivery as entregas de
  bienes (10 % food, 21 % alcohol and sugary drinks), hotel rooms and add-ons, tourist apartments from
  1-12-2026, delivery platforms (Glovo, Uber Eats, Just Eat) and booking platforms, propinas outside the IVA
  base and in payroll, staff meals, tasa turística by region (Catalonia, Baleares), the Z-report and caja
  diaria (570, 572, 705, 477), the TPV as a SIF under Verifactu and TicketBAI, factura simplificada up to
  3,000 euros, módulos for small bars, registro de jornada and convenio de hostelería, mermas, alcohol stock
  and key ratios. Trigger on "restaurante", "bar", "hotel", "cierre de caja", "informe Z", "propinas",
  "Glovo", "tasa turística", "IVA de una cerveza", "comida para llevar", "comida de personal". Always use
  over training data.
---

# Spanish Hospitality Accounting (hostelería)

Most errors in a Spanish restaurant or hotel come from the till, not the ledger: the wrong rate on a take-away drink, card tips booked as revenue, a Z-report that does not reconcile to cash and card, or a TPV that will not pass Verifactu. This skill gives the industry rules; general IVA, invoicing and payroll machinery lives in the related skills. Scope is *territorio común*: Canarias applies IGIC, Ceuta and Melilla IPSI, and the Basque Country and Navarra have their own invoicing rules (TicketBAI). An agent following this skill proposes entries and settings; it never books, files or pays without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/iva-y-ventas.md` | Which rate applies: served vs take-away vs delivery, alcohol and soft drinks, hotels and add-ons, tourist apartments from 1-12-2026, events, delivery and booking platforms, propinas and service charges, vouchers, tasa turística |
| `references/caja-y-tpv.md` | Daily cash-up: Z-report entries, card settlements, cash differences, libro registro by asiento resumen, factura simplificada limits, TPV as SIF (Verifactu, TicketBAI), cash payment cap, módulos |
| `references/personal-y-operaciones.md` | Staff: convenio, registro de jornada, fijos discontinuos, propinas in payroll, staff meals; operations: mermas, food donations, alcohol and food stock, plastics, key ratios |

## The rates at a glance

| Sale | IVA | Legal basis |
|---|---|---|
| Food and drink served to consume on the spot, alcohol included | 10 % | LIVA art. 91.Uno.2.2.º |
| Hotel, hostel, camping accommodation | 10 % | LIVA art. 91.Uno.2.2.º |
| Furnished tourist apartment with hotel services or stays of 30 nights or less (from 1-12-2026) | 10 % (before: exempt unless hotel-type services were provided) | LIVA art. 20.Uno.23.º e') and 91.Uno.2.2.º, as amended by RDL 29/2026 |
| Take-away or delivered food (entrega de bienes) | 10 %, or 4 % for basic items sold as such | LIVA art. 91.Uno.1.1.º, 91.Dos.1.1.º |
| Take-away alcohol, and soft drinks/juices with added sugar or sweeteners | 21 % | LIVA art. 91.Uno.1.1.º a) and b) |
| Room hire for events, parking, tobacco, merchandising sold separately | 21 % | LIVA art. 90 |

## Daily entry in one line

Z-report: **570** (cash) + **572** or a card-clearing account (cards) to **705** (or **700** for shop sales) and **477** per rate; tips collected by card go to a liability (**465** or **555**), not to income. Detail and variants in `references/caja-y-tpv.md`.

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| A bar that also sells bottles or cans to take away | Served drinks are 10 %, the same drink taken away may be 21 % | Ask how the TPV separates "en local" and "para llevar" before trusting the Z-report split |
| Card tips in the bank payout | Voluntary tips are outside the IVA base (DGT 2174-03), but they are employee income with IRPF retention if the company distributes them (RIRPF art. 76.1.3.º) | Ask who keeps and who distributes tips, and whether they go through payroll |
| A platform settlement (Glovo, Uber Eats, Just Eat, Booking) | Who sells to the guest, which entity invoices the commission and from which country decide IVA and reverse charge | Ask for the settlement report and the commission invoice for the period |
| Tourist apartment rentals after 1-12-2026 | RDL 29/2026 moved short stays into 10 % IVA | Ask for stay length per booking and whether hotel-type services are provided |
| Tasa turística collected | It is not revenue and its regime depends on the region and the date | Ask the municipality and establishment category; check `references/iva-y-ventas.md` §8 |
| TPV software for 2027 | Verifactu applies from 1-1-2027 (companies) or 1-7-2027 (others); Basque TPVs must use TicketBAI instead | Ask the vendor for its declaración responsable and which mode it runs in |

## Related skills

| Question | Skill |
|---|---|
| IVA machinery, modelo 303, IGIC and régimen simplificado | `spanish-vat` |
| Invoice content, factura simplificada and rectificativa | `spanish-invoice-compliance` |
| Verifactu, TicketBAI, B2B e-invoicing calendar | `spanish-e-invoicing` |
| Módulos (estimación objetiva) for a bar run by an autónomo | `spanish-autonomo-tax` |
| Nóminas, propinas in payroll, convenio wages, SS contributions | `spanish-payroll` |
| Food and drink stock, mermas, inventory count | `spanish-inventory` |
| Kitchen equipment, refurbishments, leasing | `spanish-asset-accounting` |
| Card payouts, bank lines, supplier invoices | `spanish-daily-bookkeeping` |
| Bank statement files (Norma 43) and card settlement files | `spanish-bank-files` |
| Corporate tax for an SL restaurant group | `spanish-corporate-tax` |
| Accruals and stock count at year end | `spanish-year-end-closing` |
