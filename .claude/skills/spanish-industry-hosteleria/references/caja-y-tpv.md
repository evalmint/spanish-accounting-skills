# Hostelería: caja diaria, Z-report and TPV

How a restaurant, bar or hotel turns the till into bookkeeping, and what the till software must do under Verifactu or TicketBAI. Checked against boe.es consolidated texts on 24 November 2026.

## Contents

- [1. From Z-report to asiento](#1-from-z-report-to-asiento)
- [2. Card settlements and other payment methods](#2-card-settlements-and-other-payment-methods)
- [3. Cash differences, float and withdrawals](#3-cash-differences-float-and-withdrawals)
- [4. Libro registro de facturas expedidas](#4-libro-registro-de-facturas-expedidas)
- [5. Factura simplificada and full invoices](#5-factura-simplificada-and-full-invoices)
- [6. The TPV as a SIF: Verifactu and TicketBAI](#6-the-tpv-as-a-sif-verifactu-and-ticketbai)
- [7. Cash limits](#7-cash-limits)
- [8. Small bars in módulos](#8-small-bars-in-módulos)
- [9. Daily checklist](#9-daily-checklist)

## 1. From Z-report to asiento

The *informe Z* (end-of-day closing) gives total sales per IVA rate and per payment method, and resets the day counters. The *informe X* is an intermediate reading that resets nothing. Book from the Z, never from the X.

Worked day (illustrative figures, IVA-inclusive):

| Z-report line | Amount |
|---|---|
| Sales at 10 % (base 1,800.00 + IVA 180.00) | 1,980.00 |
| Sales at 21 % (take-away alcohol; base 100.00 + IVA 21.00) | 121.00 |
| Total sales | 2,101.00 |
| Paid in cash | 601.00 |
| Paid by card | 1,400.00 |
| Meal cards (Edenred-type) | 100.00 |
| Card tips (not sales) | 45.00 |

| Debit | Credit | Amount |
|---|---|---|
| **570** Caja | | 601.00 |
| Card clearing (sub-account of **555**, or **572** if settled same day) | | 1,445.00 |
| **440** Meal-card company | | 100.00 |
| | **705** Prestaciones de servicios | 1,800.00 |
| | **700** Ventas de mercaderías | 100.00 |
| | **477** IVA repercutido 10 % | 180.00 |
| | **477** IVA repercutido 21 % | 21.00 |
| | Staff tips (sub-account of **465** or **555**) | 45.00 |

Many restaurants book all sales to **705** with a sub-account for take-away; that is acceptable if the IVA split per rate is kept.

Hotels: room revenue accrues per night stayed, not at checkout. For stays crossing a month-end, accrue nights to **705** against **4309** (pending invoice) and invoice at checkout. Advance payments and deposits go to **438** and trigger IVA when received (LIVA art. 75.Dos).

## 2. Card settlements and other payment methods

- **Bank TPV (datáfono)**: the acquirer pays the gross amount and charges the commission separately, or pays net. Book the gross sale on the Z-report date and the commission to **626** (financial service, exempt under LIVA art. 20.Uno.18.º, so no **472**). Clear the card-clearing account with the payout.
- **Bizum, PayPal, Stripe** (online bookings): same pattern; see `spanish-daily-bookkeeping` for the provider settlement files and `spanish-bank-files` for Norma 43 matching.
- **Delivery platforms**: gross sales from the platform report, not the bank payout (see `iva-y-ventas.md` §6).
- **Unpaid bills of a regular customer or company (cuenta de cliente)**: **4300** instead of cash; issue a full invoice if the customer is a business.

Reconcile the card-clearing balance weekly. A residual balance is either a missing payout, a chargeback or a tip not yet paid to staff.

## 3. Cash differences, float and withdrawals

| Event | Entry |
|---|---|
| Cash short against the Z (descuadre) | **678** Gastos excepcionales (or **659** Otras pérdidas en gestión corriente) / **570** |
| Cash over | **570** / **778** (or **759**) |
| Float (fondo de caja) left in the drawer | No entry; it stays in **570** |
| Cash deposited at the bank | **572** / **570** |
| Small purchases paid from the till (ice, bread) | **600**/**602**/**629** + **472** / **570**, with the ticket kept |
| Owner of an SL takes cash | **551** / **570**, never an expense |

A systematic shortage is a control issue, not an accounting one. Ask before booking repeated differences.

## 4. Libro registro de facturas expedidas

Simplified invoices (tickets) may be recorded as a daily summary entry (*asiento resumen*) per date, with the base and quota per rate and the first and last ticket numbers, provided the tickets do not require the customer's identification and all are accrued within the same calendar month (RIVA art. 63.4). Full invoices and rectifying invoices are recorded individually (RIVA art. 63.6). A Verifactu system or SII produces the records automatically.

## 5. Factura simplificada and full invoices

| Rule | Detail | Basis |
|---|---|---|
| General limit for a factura simplificada | 400 € IVA included | RD 1619/2012 art. 4.1.a |
| Raised limit for restaurants, bars, cafés, horchaterías, chocolaterías and similar, and the supply of food and drinks for consumption on the spot | 3,000 € IVA included | RD 1619/2012 art. 4.2.e |
| Dance halls and discos | 3,000 € | art. 4.2.f |
| Hotel accommodation | Not listed in art. 4.2, so the 400 € limit applies to room invoices (unverified reading: confirm whether AEAT accepts hotels under "establecimientos similares") | art. 4 |
| Customer is a business and asks for an invoice | Must issue a full invoice or a *factura simplificada cualificada* with the customer's NIF and address (to deduct IVA) | RD 1619/2012 art. 2.2, 7.2 |
| B2B e-invoicing obligation (RD 238/2026) | Simplified invoices are excluded unless they are *cualificadas* under art. 7.2 | RD 238/2026 art. 4.1 |

The restaurant guest who wants to deduct a business meal needs a full or qualified simplified invoice; see `spanish-invoice-compliance`.

## 6. The TPV as a SIF: Verifactu and TicketBAI

A TPV or PMS that issues tickets and invoices is a *sistema informático de facturación* (SIF) under RD 1007/2023, which develops LGT art. 29.2.j.

| Point | Rule | Basis |
|---|---|---|
| Who | IS taxpayers, IRPF taxpayers with business activity, IRNR with permanent establishment, entidades en atribución de rentas, if they use software to invoice (even partly) | RD 1007/2023 art. 3.1 |
| Excluded | Businesses keeping their IVA books through SII (RIVA art. 62.6); taxpayers with *domicilio fiscal* in the Basque Country or Navarra, which apply their own systems | RD 1007/2023 art. 3.3 and art. 1.3 of the Reglamento |
| Deadline, companies (IS) | Systems adapted before 1-1-2027 | RD 1007/2023 DF 4.ª, as amended by RDL 15/2025 |
| Deadline, others (autónomos) | Before 1-7-2027 | same |
| Deadline, software vendors | Products must already be compliant (nine months from Orden HAC/1177/2024) | DF 4.ª |
| Modes | "Verifactu" (records sent to AEAT in real time) or "no Verifactu" (chained, signed records kept locally with an event log) | RD 1007/2023 art. 15–16 |
| Ticket content | Each ticket carries a QR code and, in Verifactu mode, the legend "VERI*FACTU" | RD 1007/2023 and Orden HAC/1177/2024 |

Practical points for hostelería:
- **Mesa abierta / pre-bill**: a pre-bill printed for the guest is not an invoice. Ask the vendor how the software records voids and changes after the pre-bill; deleting lines after printing is exactly what the rules target.
- **Several TPVs and an online ordering app**: each issuing system must comply, and numbering series must not overlap.
- **Old cash registers** (non-programmable, no software) fall outside RD 1007/2023, but the obligation to issue and keep tickets remains.
- **Basque Country**: TicketBAI (Araba, Bizkaia under Batuz, Gipuzkoa) applies instead of Verifactu, under each Diputación's Norma Foral; it has been mandatory for hostelería for some years. Navarra has its own system. Ask where the establishment is before choosing the software requirements.

See `spanish-e-invoicing` for the full calendar, the B2B e-invoicing phases (12 and 24 months after Orden HAC/1028/2026, in force 6-10-2026) and the technical detail.

## 7. Cash limits

Payments in cash where one party is a business or professional are capped at 1,000 € (or the equivalent in foreign currency), and 10,000 € where the payer is an individual not resident in Spain for tax purposes and not acting as a business (Ley 7/2012 art. 7, as amended by Ley 11/2021). A wedding banquet or a large group bill paid in cash above the limit exposes both parties to a fine of 25 % of the amount paid. Splitting the payment does not avoid the limit.

## 8. Small bars in módulos

An autónomo running a bar or café may be in *estimación objetiva* (módulos) for IRPF and the *régimen simplificado* for IVA, with tax computed on indices such as staff, tables and electricity rather than real profit. Hostelería activities are covered by the annual Orden de módulos.

- The exclusion thresholds were raised to 250,000 € (and 125,000 € for invoicing to businesses) up to 2024 by LIRPF DT 32.ª. The extensions for 2025 and 2026 were made by real decretos-leyes that the Congreso later derogated (RDL 9/2024, RDL 16/2025, RDL 2/2026). Whether 250,000 € or the statutory 150,000 € applies for 2025 and 2026 is **unverified**; AEAT guidance and the BOE consolidated text diverge. Check `spanish-autonomo-tax` before relying on either figure.
- A bar in módulos is still obliged to issue tickets or invoices when asked (RD 1619/2012 art. 3.1.c), and its TPV falls under Verifactu from 1-7-2027.
- A bar run through an SL is never in módulos.

## 9. Daily checklist

1. Print the Z-report and keep it with the day's card-terminal closing.
2. Check that the Z totals per payment method match the cash counted and the card-terminal batch.
3. Book the asiento from the Z (§1), separating tips.
4. Record purchases paid from the till with their tickets.
5. Weekly: reconcile the card-clearing account, platform settlements and meal-card statements.
6. Monthly: check the IVA split per rate against menu and TPV configuration; review cash differences.
