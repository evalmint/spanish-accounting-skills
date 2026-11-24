# Payment Providers, TPV and Marketplaces

How to book sales collected through a card terminal (TPV), Redsys, Stripe, PayPal, SumUp, Bizum or a marketplace, and the provider's fees. Accounts are **PGC 2007**. EU place-of-supply rules for selling to consumers abroad, OSS and the marketplace *deemed supplier* rules are in `spanish-industry-ecommerce` and `spanish-vat`.

## Contents

- [1. The rule: gross revenue, separate fee](#1-the-rule-gross-revenue-separate-fee)
- [2. Where to hold the provider balance](#2-where-to-hold-the-provider-balance)
- [3. Identify the provider and its payout pattern](#3-identify-the-provider-and-its-payout-pattern)
- [4. Worked example A: net payout (Stripe, SumUp, PayPal)](#4-worked-example-a-net-payout-stripe-sumup-paypal)
- [5. Worked example B: bank TPV via Redsys, fee charged separately](#5-worked-example-b-bank-tpv-via-redsys-fee-charged-separately)
- [6. IVA on the provider's fee](#6-iva-on-the-providers-fee)
- [7. Bizum](#7-bizum)
- [8. Refunds, chargebacks, reserves](#8-refunds-chargebacks-reserves)
- [9. Marketplaces](#9-marketplaces)
- [10. Foreign currency](#10-foreign-currency)
- [11. Tips (propinas)](#11-tips-propinas)
- [12. Ask the user](#12-ask-the-user)

## 1. The rule: gross revenue, separate fee

A payment provider is an intermediary, not the customer. The customer owes the full price; the provider owes you the price minus its fee.

| Consequence | Source |
|---|---|
| Revenue and output IVA are on the full price the customer pays, never the payout | LIVA art. 78.Uno: the base is the total consideration "procedente del destinatario o de terceras personas" |
| The fee is a separate expense; income and expenses are not netted | Código de Comercio art. 34.2 and PGC Marco Conceptual, principio de no compensación |
| IVA accrues when the goods are delivered or the service performed (or when an advance is collected), not when the payout lands | LIVA art. 75.Uno and Dos |

A bank line "STRIPE PAYMENTS 1,842.10" is not revenue of 1,842.10. It settles a receivable. Booking the payout as revenue understates both turnover and IVA repercutido.

## 2. Where to hold the provider balance

The PGC has no dedicated account for amounts held by a payment provider. Two defensible choices; pick one per provider and keep it:

| Situation | Account | Why |
|---|---|---|
| The provider holds a balance in an account in your name that you can withdraw (PayPal, Stripe balance, other e-money accounts) | A subaccount of **572** (e.g. 5720009 PayPal) | Functions as a demand account; reconcile it like a bank against the provider's statement |
| The acquirer owes you the day's card sales until settlement (bank TPV) or a marketplace owes you a payout | A subaccount of **440** Deudores (e.g. 4400010 Amazon) | A trade receivable on a party that is not the customer |
| Unidentified receipt you cannot yet attribute | **555** Partidas pendientes de aplicación | Temporary only; clear it before closing |

Do not use **430** for the provider: the customer has already paid. Do not merge providers into one balance: each needs its own subaccount so that every payout reconciles.

## 3. Identify the provider and its payout pattern

| Bank line looks like | Type | Payout normally | Fee arrives as |
|---|---|---|---|
| Bank's own TPV liquidation ("LIQ. TPV", "ABONO COMERCIO"), processed via Redsys | Acquiring bank | Gross or net, depending on the contract with the bank | Monthly charge or deducted per liquidation |
| `STRIPE` | PSP and acquirer (EU entity) | Net of fees | In the balance report; monthly tax invoice |
| `PAYPAL` | E-money institution (EU entity) | Net | Per transaction in the activity report |
| `SUMUP` | Mobile acquirer | Net | Per transaction / per payout |
| `BIZUM` | Interbank instant transfer scheme | Gross (each payment arrives as a transfer) | Bank charges, if any |
| `AMAZON`, `ETSY`, `GLOVO`, `UBER EATS`, `BOOKING` | Marketplace / platform | Net of commission | Monthly invoice for commission and services |

Never assume gross or net from the brand. Open the settlement report and check whether the payout equals the gross sales of the period. If you cannot get a report that splits gross sales, refunds, fees and reserves, ask the user for it; do not book the payout as revenue as a fallback.

## 4. Worked example A: net payout (Stripe, SumUp, PayPal)

An SL sells online to Spanish consumers. Sales for the week: 12,100 € including 21 % IVA (base 10,000, IVA 2,100). Provider fee for the same transactions: 180 €. Payout: 11,920 €.

**Sales (from the sales report or the invoicing system):**

| Cuenta | Debe | Haber |
|---|---|---|
| 5720009 Stripe (subaccount of **572**) | 12,100.00 | |
| **700** Ventas de mercaderías | | 10,000.00 |
| **477** Hacienda Pública, IVA repercutido | | 2,100.00 |

Each sale needs its invoice (simplificada for consumers up to the art. 4 limits, RD 1619/2012) and, from the Verifactu start dates, a compliant billing system record (`spanish-e-invoicing`).

**Fee (from the provider's statement or monthly invoice):**

| Cuenta | Debe | Haber |
|---|---|---|
| **626** Servicios bancarios y similares | 180.00 | |
| 5720009 Stripe | | 180.00 |

**Payout:**

| Cuenta | Debe | Haber |
|---|---|---|
| **572** Bancos (main account) | 11,920.00 | |
| 5720009 Stripe | | 11,920.00 |

Reconciliation per period:

```
opening balance + gross sales − refunds − chargebacks − fees − payouts ± reserve movements = closing balance (= provider's statement)
```

## 5. Worked example B: bank TPV via Redsys, fee charged separately

Redsys is the processing network behind most Spanish bank TPVs; the contract, the liquidation and the *tasa de descuento* (merchant fee) are with the bank. A bar takes 3,300 € in card payments on 30 June (10 % IVA: base 3,000, IVA 300). The bank credits 3,300 € on 1 July and charges 0.5 % (16.50 €) on 5 July.

**30 June, daily sales from the cash register's Z report:**

| Cuenta | Debe | Haber |
|---|---|---|
| 4400001 Banco X, liquidaciones TPV (subaccount of **440**) | 3,300.00 | |
| **700** Ventas de mercaderías | | 3,000.00 |
| **477** Hacienda Pública, IVA repercutido | | 300.00 |

**1 July, liquidation:** **572** / 4400001 for 3,300.00. **5 July, fee:** **626** / **572** for 16.50.

The balance in 4400001 at 30 June (3,300) is a genuine receivable at a period end; it should be zero a few days later. Cash sales the same day go to **570**.

## 6. IVA on the provider's fee

Payment and transfer services are exempt (LIVA art. 20.Uno.18.º, transposing Directive 2006/112 art. 135.1.d). The question is whether each fee line is a payment service or something else.

| Fee line | Usual treatment |
|---|---|
| TPV *tasa de descuento*, card processing, PayPal transaction fee | Exempt financial service: **626**, no IVA |
| Terminal rental, POS software, subscription to the provider's software | Taxable at 21 %: **621** or **629** with **472** |
| Marketplace commission, fulfilment, advertising on the platform | Taxable services: **623**/**627**/**629** with IVA (domestic or reverse charge, §9) |
| Currency conversion margin | Exempt (financial) |
| Chargeback fee | Usually exempt; check the invoice |

When the fee is invoiced by an EU provider without IVA and is an exempt financial service, there is no IVA to self-assess. When the provider's monthly invoice says "reverse charge" for taxable lines (software, fraud tools, tax tools), self-assess IVA as in `foreign-purchases.md`. Read the provider's tax invoice line by line; whether a specific provider classifies a given product as exempt or taxable is provider-specific (unverified for each brand).

## 7. Bizum

- **Bizum between individuals** is a transfer from a private account. If a business collects into the owner's personal Bizum, it is still the business's sale: book the sale normally and record the money as owed by the owner (autónomo: **550**; SL: **551**) until it reaches the business account.
- **Bizum for merchants** (online checkout or "Bizum comercio") is offered by banks through the Redsys gateway; liquidation and fees follow the bank's TPV contract (§5).
- Each Bizum receipt needs to be matched to a sale and its invoice; the bank line alone is not a justificante.

## 8. Refunds, chargebacks, reserves

| Event | Debe | Haber |
|---|---|---|
| Refund to a customer of a sale already booked | **708** Devoluciones de ventas, **477** (reduce output IVA with a factura rectificativa) | Provider subaccount |
| Chargeback (customer disputes), money withdrawn by the provider | **440** or **436** (claim against the customer while disputed) | Provider subaccount |
| Chargeback lost definitively | **650** Pérdidas de créditos comerciales incobrables (or **708** if treated as a cancelled sale with rectificativa) | **440**/**436** |
| Rolling reserve withheld by the provider | Subaccount "reserva" under **440** or **565** Fianzas constituidas a corto plazo | Provider subaccount |

The IVA of a sale is reduced only through a factura rectificativa (LIVA art. 80; RD 1619/2012 art. 15). A chargeback alone does not reduce IVA.

## 9. Marketplaces

Two flows, booked separately:

1. **Your sales to the end customer**: gross revenue and IVA as in §4, with the marketplace's balance as a **440** subaccount. Where the platform is the *deemed supplier* for IVA (LIVA art. 8 bis, mainly non-EU sellers and imports ≤ 150 €), the treatment changes: see `spanish-industry-ecommerce`.
2. **The marketplace's invoice to you** for commissions, fulfilment and advertising: a taxable service. If issued by a Spanish entity with Spanish IVA, deduct the **472**. If issued by an entity in another EU state without IVA, self-assess (autorepercusión, LIVA art. 84.Uno.2.º): **472** and **477** for 21 %, modelo 303 boxes 10–11 and 36–37 (`foreign-purchases.md`), and report it in modelo 349.

Platform payout = your gross sales − commissions − fees − refunds. Book the commission invoice to **623** or **629** (or **627** for advertising) against the **440** subaccount, then clear the subaccount with the payout.

Food delivery platforms and accommodation platforms work the same way; the restaurant or host is the seller to the customer.

## 10. Foreign currency

A payout in USD or GBP converts at the spot rate on the transaction date, or an average rate for at most a month if rates did not move significantly (NRV 11.ª 1.1). At period end, monetary balances (the provider balance, receivables) are revalued at the closing rate; differences go to **668** Diferencias negativas de cambio or **768** Diferencias positivas de cambio (NRV 11.ª 1.2). A provider that converts before paying out gives you euros; its conversion margin is a fee, not an exchange difference.

## 11. Tips (propinas)

Tips paid by card belong to the staff, not to the business, if they are passed on; they are not part of the IVA base when they are voluntary and not part of the price. Book card tips collected to a liability (**465** or a **555**/**440**-type pass-through subaccount) and clear it when distributed. Whether tips paid through payroll are salary is a payroll question (`spanish-payroll`; RIRPF art. 76.1.3.º obliges the employer to withhold when it pays out tips from third parties).

## 12. Ask the user

- Can you export the provider's settlement or payout report for the period?
- Does the bank pay TPV sales gross with a separate monthly fee, or net?
- Who issues the provider's or marketplace's invoice (entity and country), and does it show IVA or "reverse charge"?
- Are any business sales collected into a personal account or personal Bizum?
- Are refunds or chargebacks pending at period end?
