# E-commerce operations: payouts, returns, stock, reporting

Running an online shop day to day: documents, payment providers, marketplace settlements, returns, vouchers, stock, recargo de equivalencia, DAC7 and the month-end reconciliation, with PGC 2007 entries. Where VAT is due is in `eu-sales-and-oss.md`; general IVA rules in `spanish-vat`; individual bank lines in `spanish-daily-bookkeeping`.

Sources: LIVA (BOE consolidated 07/10/2026) arts. 75, 78, 80, 89, 96, 148-163; RD 1619/2012 arts. 2-4, 15; Ley 13/2023 and RD 117/2024 (DAC7 transposition; article references unverified); Orden HAC/72/2024 (modelo 238); AEAT modelo 238 FAQ. Checked 2026-11-24. Entries are proposals: the agent never books without the user's approval.

## Contents

1. [Documents: tickets, simplified and full invoices](#1-documents-tickets-simplified-and-full-invoices)
2. [Payment providers](#2-payment-providers)
3. [Marketplace settlements (gross vs net)](#3-marketplace-settlements-gross-vs-net)
4. [IVA on fees and platform costs](#4-iva-on-fees-and-platform-costs)
5. [Returns, refunds and chargebacks](#5-returns-refunds-and-chargebacks)
6. [Discounts, free shipping, gift cards](#6-discounts-free-shipping-gift-cards)
7. [Stock, cut-off and expected returns](#7-stock-cut-off-and-expected-returns)
8. [Autónomo sellers and recargo de equivalencia](#8-autónomo-sellers-and-recargo-de-equivalencia)
9. [DAC7 platform reporting](#9-dac7-platform-reporting)
10. [Month-end reconciliation](#10-month-end-reconciliation)

## 1. Documents: tickets, simplified and full invoices

| Case | Document | Source |
|---|---|---|
| Retail sale to a consumer in Spain, ≤ €3,000 including IVA | Factura simplificada (order confirmation with the legal content can serve) | RD 1619/2012 art. 4.2.a |
| Customer is a business, or asks for a full invoice | Full invoice with NIF and address | RD 1619/2012 art. 2.2.a, art. 6 |
| Intra-EU B2B supply | Full invoice, never simplified | Art. 4.4.a |
| Distance sale to an EU consumer under the Spanish OSS | Simplified allowed | Art. 4.4.b |
| Export (including Canarias) | Full invoice | Art. 2.2.d |
| Refund | Factura rectificativa (simplified allowed when the original was simplified) | Art. 4.1.b, art. 15 |
| Invoicing software | Must meet the Verifactu regulation (RD 1007/2023) from its application date; Shopify/WooCommerce apps and ERPs need a compliant module | See `spanish-e-invoicing` |

Number invoices in series; marketplaces that issue invoices on the seller's behalf (Amazon VAT Calculation Service) need a separate series and a self-billing agreement (RD 1619/2012 art. 5).

## 2. Payment providers

| Provider | What the payout is | Fee IVA treatment (check the invoice) | Booking |
|---|---|---|---|
| Redsys / bank TPV virtual | Card sales settled by the bank daily, usually net of the *tasa de descuento* | Bank card fees are exempt financial services (LIVA art. 20.Uno.18º) | Sale: debit **4300** (sub-account TPV), credit **700**/**477**. Settlement: debit **572** and **626**, credit **4300** |
| Stripe | Balance in Stripe, paid out net of fees in batches | Processing fees normally exempt payment services; other Stripe products (Billing, Radar, Tax) may be taxable services from Ireland: reverse charge, casillas 10-11 | Debit **4300** (Stripe); at payout debit **572**, **626**, credit **4300** |
| PayPal | Balance in PayPal account, transfers to bank | Fees normally exempt | PayPal balance as a sub-account of **572** (e-money account) or **4300**; be consistent |
| Bizum (merchant) | Through the bank, like a transfer | Bank fees exempt | As Redsys |
| Klarna, Aplazame, other BNPL | Provider pays the shop and collects from the customer | Fees: usually exempt credit/payment service; check | Debit **4300** (BNPL), fees **626** |
| Cash on delivery (contra reembolso) | Carrier collects and remits | Carrier fee taxable (21 %) | Debit **4300** (carrier), **624**, **472** |

Never book the payout as revenue. Revenue is the gross order value from the shop platform; the payout clears the provider receivable. Currency payouts: exchange differences to **668**/**768**.

## 3. Marketplace settlements (gross vs net)

For a Spanish seller selling its own goods (no deemed-supplier rule, see `eu-sales-and-oss.md` section 7), the customer's price is the seller's revenue and the platform's deductions are costs.

**Example: Amazon settlement for a period.** Sales to Spanish consumers 1,210 (1,000 + IVA 210); referral fees 150 + IVA; FBA fulfilment fees 80 + IVA; refunds 121 (100 + IVA 21); payout 810.70.

| Account | Debit | Credit |
|---|---|---|
| **4300** (Amazon) | 1,210 | |
| **700** | | 1,000 |
| **477** | | 210 |
| **708** | 100 | |
| **477** | 21 | |
| **4300** (Amazon) | | 121 |
| **623** (referral fees) | 150 | |
| **629** (FBA fulfilment) | 80 | |
| **472** (if the fees carry Spanish IVA) | 48.30 | |
| **4300** (Amazon) | | 278.30 |
| **572** (payout) | 810.70 | |
| **4300** (Amazon) | | 810.70 |

(Figures illustrative; the payout in the report must match the bank. If the fee invoices are issued from Luxembourg without IVA, replace the **472** line with reverse charge: debit **472**, credit **477**, casillas 10-11 and modelo 349 key I.)

Rules:

- Book from the settlement report, not the bank line. The report gives sales by country, refunds, fees, ads and reserves.
- Reserves held by the marketplace stay in the **4300** sub-account until released.
- Sales to other EU countries in the same report follow the distance-sale rules (Spanish IVA under the threshold, OSS above).
- Advertising (Amazon Ads, Google, Meta) goes to **627**, with reverse charge if invoiced from another member state.

## 4. IVA on fees and platform costs

| Supplier (typical) | Likely treatment | 303 |
|---|---|---|
| Spanish entity invoicing with Spanish IVA | Deductible input | 28-29 |
| EU entity (Ireland, Luxembourg, Netherlands) invoicing without IVA: Shopify, Google, Meta, Amazon (if invoiced from Luxembourg), Etsy | Intra-EU service: reverse charge | 10-11 and 28-29; 349 key I |
| Non-EU entity (US, UK, China) | Reverse charge | 12-13 and 28-29 |
| Exempt financial services (card processing) | No IVA, no 303 entry | - |
| Invoice shows foreign VAT by mistake | Not deductible; ask for a corrected invoice | - |

The shop's NIF-IVA must be registered in the ROI (VIES) for EU suppliers to invoice without VAT; register with modelo 036.

## 5. Returns, refunds and chargebacks

| Event | IVA | Entry |
|---|---|---|
| Goods returned, refund paid | Factura rectificativa; reduce base in the period of the rectification (LIVA art. 80.Dos, art. 89); casillas 14-15 negative | Debit **708**, debit **477**; credit **4300**/**572**. Stock back: if perpetual inventory, debit **300**, credit **610** (or note for the year-end count) |
| Refund without return (goodwill, damaged item kept) | Treat as a discount after sale: rectificativa | Debit **708** (or **706** for price discounts), debit **477**; credit **572** |
| Partial refund for late delivery | Same | Same |
| Chargeback, goods delivered, customer does not pay | No base reduction unless the bad-debt conditions of art. 80.Cuatro are met (one year or six months, claim, notice to AEAT within a month) | Debit **4300** (disputed) or **436**; consider impairment **694**/**490** at year end |
| Chargeback won | Reverse the dispute entry | |
| Return of an OSS sale | Correct the destination VAT in the 369 of the period (or later 369 within three years) | Debit **708** and the OSS liability; credit **4300** |
| Return of an export (Canarias) | Re-import; ask the carrier for documents | |

Customer refunds of shipping costs follow the goods.

## 6. Discounts, free shipping, gift cards

| Case | Treatment |
|---|---|
| Discount code at checkout | Reduces the base (LIVA art. 78.Tres.2º); book net sale in **700** or gross with **706**/**709** per policy |
| Free shipping | No separate income; shipping cost to **624** |
| Shipping charged | Part of the sale base and rate (art. 78.Dos.1º); book in **700** (sub-account) |
| Loyalty points redeemable for goods | Part of revenue deferred under the ICAC revenue resolution (Resolución ICAC de 10 de febrero de 2021); IVA when the goods are delivered (unverified DGT doctrine for each scheme) |
| Gift card (*tarjeta regalo*) | LIVA contains no voucher rules: the EU Voucher Directive (2016/1065) has not been transposed (no provision found in LIVA consolidated 07/10/2026). DGT doctrine applies the single-purpose / multi-purpose distinction: a card usable for one product type at one rate in Spain is taxed when sold; a card usable for anything is taxed when redeemed (unverified: confirm the DGT consulta applicable). Book the unredeemed card in **438** until redeemed |
| Expired unredeemed card | Income (**759**); IVA treatment per DGT doctrine (unverified) |

## 7. Stock, cut-off and expected returns

| Point | Rule |
|---|---|
| Valuation | Cost (purchase price plus import duties, the €3 EU flat duty on low-value imports from 1 July 2026, freight in); non-recoverable taxes included, deductible IVA excluded (PGC NRV 10ª). See `spanish-inventory` |
| Stock at fulfilment centres | Still the shop's stock: include Amazon FBA and 3PL inventory, by country, in the year-end count; reconcile with the provider's report |
| Goods in transit to customers at year end | Revenue when control passes (usually delivery); goods shipped and not delivered on 31 December may still be stock (ICAC Res. 10 February 2021, unverified detail) |
| Expected returns (right of return) | Under the ICAC revenue resolution, revenue is recognised net of expected returns, with a refund liability and an asset for the goods expected back (unverified account; see `spanish-year-end-closing`) |
| Damaged or unsellable returns | Write down (**693**/**390**) or derecognise; no IVA self-supply for destroyed goods with evidence |
| Periodic inventory | Purchases in **600**; year end: **610** against **300** |

## 8. Autónomo sellers and recargo de equivalencia

| Situation | Treatment | Source |
|---|---|---|
| Autónomo retailer (individual) buying goods and selling them unchanged, more than 80 % to consumers | Compulsory recargo de equivalencia for those products: suppliers charge IVA plus recargo; the seller charges customers normal IVA and files no 303 for this activity | LIVA arts. 148-149, 154; RIVA art. 59 |
| A shop selling online only | Still a retailer if the conditions are met; the channel does not matter | Art. 149 |
| Retailer buys stock from another EU country or imports | Pays IVA and recargo itself: modelo 309 for intra-EU acquisitions; at customs for imports | Art. 154.Uno |
| Retailer's own transformation (printing, assembling) | Not RE for those products; general regime as a separate sector | Art. 149.Uno.1º |
| Selling to an RE retailer (B2B wholesale webshop) | Charge recargo on top of IVA; casillas 16-24 of the 303 | Art. 161 |
| RE retailer making distance sales to other EU countries above €10,000 | Interaction with OSS not covered here (unverified); ask an adviser | |
| Companies (S.L.) | Never in RE | Art. 148.Uno |

## 9. DAC7 platform reporting

| Point | Rule |
|---|---|
| Who reports | Platform operators (marketplaces, rental and service platforms) report their sellers' identity and income to the tax authority; Spanish platforms through modelo 238 |
| Legal basis | Directive (EU) 2021/514 (DAC7), transposed by Ley 13/2023 and RD 117/2024; modelo 238 approved by Orden HAC/72/2024 |
| Deadline | Annual, during January of the year after the reported year (AEAT modelo 238 FAQ) |
| Sellers excluded | Sellers of goods with fewer than 30 sales and no more than €2,000 of consideration in the year (DAC7 definition of excluded seller) |
| What the seller should do | Give the platform its NIF and address; reconcile the platform's DAC7 figures with its own books, since AEAT cross-checks them against modelo 303 and income tax |

## 10. Month-end reconciliation

1. **Orders vs revenue.** Export orders from the shop platform (Shopify, WooCommerce, PrestaShop) by country, rate and channel; agree to **700** and **477** by rate.
2. **Providers.** Each **4300** provider sub-account should hold only payouts in transit at month end; agree with the Stripe/PayPal/Redsys reports.
3. **Marketplaces.** Agree each settlement report: sales, refunds, fees, ads, reserves, payout.
4. **Refunds.** Each refund has a rectificativa and appears in casillas 14-15.
5. **EU threshold.** Update cumulative EU B2C sales against €10,000 (or confirm OSS registration).
6. **OSS liability.** Per country, equals the 369 for the quarter.
7. **Stock.** Agree warehouse and fulfilment-centre reports with the stock records; check transfers between countries.
8. **Fees.** Every foreign fee invoice has reverse charge in casillas 10-11 or 12-13.
9. **Canarias/export.** Every exempt export has carrier export evidence.
10. **303 tie-out.** **472**, **477** cleared to **4750** or **4700**; modelo 349 matches casillas 59 and 10.
