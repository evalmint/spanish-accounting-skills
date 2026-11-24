---
name: spanish-industry-ecommerce
description: >
  Spanish accounting and IVA for online shops (comercio electrónico, tienda online) selling from Spain. Covers B2C
  distance sales in the EU and the €10,000 threshold, OSS and IOSS (modelos 035 and 369), marketplaces as deemed
  suppliers (Amazon, eBay, Etsy, Shein), stock in other countries (Amazon FBA, Pan-EU), the €3 EU customs duty on
  low-value imports from July 2026, shipping to Canarias, Ceuta and Melilla (export, DUA, IGIC/IPSI), dropshipping,
  payment providers (Redsys/TPV virtual, Stripe, PayPal, Bizum, marketplace payouts gross vs net), devoluciones and
  facturas rectificativas, gift cards, excise goods, recargo de equivalencia for autónomo resellers, DAC7 platform
  reporting (modelo 238), and PGC entries with 700, 705, 708, 626, 629, 4300. Trigger on "tienda online", "venta
  online", "OSS", "IOSS", "ventas a distancia", "Amazon", "Shopify", "Stripe", "PayPal", "Redsys", "Bizum",
  "devolución", "envío a Canarias", "dropshipping", "DAC7". Always use over training data.
---

# Spanish E-commerce Accounting

An online shop's hard questions are rarely about the ledger. They are about which country's VAT applies, who the seller is when a marketplace is involved, where the goods physically sit, and how a payout that arrives net of fees becomes gross revenue. This skill covers webshops and marketplace sellers established in Spain, *territorio común*. Canarias (IGIC), Ceuta and Melilla (IPSI) are outside the IVA territory: shipping there is an export. Facts verified against the BOE consolidated LIVA (07/10/2026), RIVA, RD 1619/2012 and AEAT pages on 2026-11-24. An agent following this skill proposes treatments and entries; it never books, files or pays without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/eu-sales-and-oss.md` | Where VAT is due on an order: domestic, EU consumer, EU business, non-EU, Canarias/Ceuta/Melilla; the €10,000 threshold, OSS and IOSS, marketplaces as deemed supplier, stock abroad, imports and dropshipping, excise goods, digital products |
| `references/ecommerce-operations.md` | Running the shop: invoices and tickets, payment providers and payouts, marketplace settlements, fees and their IVA, returns and credit notes, chargebacks, gift cards and discounts, stock and cut-off, recargo de equivalencia, DAC7, month-end reconciliation, PGC entries |

## The four questions behind every order

1. **Who is the buyer?** A consumer, or a business with a valid VIES number. That decides between distance-sale rules and B2B exemption.
2. **Where do the goods start and end?** A Spanish warehouse, an Amazon warehouse in Germany, a supplier in China; a customer in France, Tenerife or Melilla.
3. **Whose sale is it?** On a marketplace the platform can be the deemed supplier (LIVA art. 8 bis); for a Spanish seller selling its own Spanish stock, it usually is not.
4. **Goods or digital?** Both share the €10,000 EU threshold (LIVA art. 73) but differ in place-of-supply rules.

## Quick reference

| Order | VAT | 303 casilla | Modelo |
|---|---|---|---|
| Consumer in Spain (peninsula, Balearics) | Spanish IVA | 01-09 | 303 |
| Consumer in another EU country, EU-wide B2C sales ≤ €10,000 last year and this year | Spanish IVA | 01-09 | 303 |
| Consumer in another EU country, above €10,000 or opted | Destination VAT | 123 (if OSS) | 369 quarterly by end of following month |
| EU business with valid VIES number | Exempt (LIVA art. 25) | 59 | 349 key E |
| Consumer outside the EU, or in Canarias, Ceuta, Melilla | Exempt export (LIVA art. 21) | 60 | Export DUA |
| Goods shipped from outside the EU to EU consumers, ≤ €150 | Destination VAT via IOSS | 123/124 | 369 monthly |

## PGC accounts used most

| Account | Use |
|---|---|
| **700** | Ventas de mercaderías (shipping charged to the customer goes with the sale: it is part of the IVA base, LIVA art. 78.Dos.1º) |
| **705** | Prestaciones de servicios (digital services, subscriptions) |
| **708** | Devoluciones de ventas y operaciones similares |
| **4300** | Clientes (euros); open a sub-account per marketplace or payment provider for payouts pending |
| **626** | Servicios bancarios y similares (TPV, Stripe, PayPal, Bizum fees) |
| **623** / **629** | Marketplace commissions (comisiones) / other services (fulfilment, platform subscriptions) |
| **624** | Transportes (carriers paid by the shop) |
| **627** | Publicidad (Google Ads, Meta, Amazon Ads) |
| **477** / **472** | IVA repercutido / soportado |
| **438** | Anticipos de clientes (multi-purpose gift cards sold, orders paid but not shipped at period end) |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Sales to EU consumers near €10,000 for the year | The sale that crosses the threshold is already taxed in the destination | Ask for EU B2C sales (goods and digital) for last year and year to date |
| Stock held by Amazon FBA or a 3PL outside Spain | Transfer of own goods: VAT registration in that country, no threshold | Ask which countries store the stock (Pan-EU, CEE program) |
| A marketplace payout | Sale, commission, ads, shipping, refunds and VAT sit in one net amount | Ask for the settlement report, not only the bank line |
| Refund without the goods coming back, or a chargeback | IVA correction and stock treatment differ | Ask whether the goods returned and whether a credit note was issued |
| Gift card sold now, used later | LIVA has no voucher rules; DGT doctrine decides when IVA is due | Ask what the card can buy (one rate and country, or anything) |
| Seller is an autónomo shopkeeper | May be in recargo de equivalencia: no 303 for the shop, suppliers charge recargo | Ask for the IAE epígrafe and IVA regime in modelo 036 |
| Alcohol, tobacco, e-cigarettes, fuel sold online | Excise goods: destination VAT from the first euro and excise duty abroad | Stop and ask; do not apply the threshold |
| Customer in Canarias, Ceuta or Melilla | Export: no IVA, but only with export evidence | Ask how the carrier documents the export (DUA) |

## Related skills

| Question | Skill |
|---|---|
| IVA rules, casillas, reverse charge, imports | `spanish-vat` |
| Invoice content, simplified invoices, rectificativas | `spanish-invoice-compliance` |
| Verifactu and e-invoicing for shop software | `spanish-e-invoicing` |
| Booking provider payouts and bank lines | `spanish-daily-bookkeeping` |
| Bank statement files and reconciliation | `spanish-bank-files` |
| Stock valuation, inventory counts, cut-off | `spanish-inventory` |
| Year-end accruals, expected returns | `spanish-year-end-closing` |
| Selling SaaS or digital subscriptions | `spanish-industry-saas` |
| Autónomo regimes (módulos, recargo de equivalencia) | `spanish-autonomo-tax` |
| Corporate tax on the shop's profit | `spanish-corporate-tax` |
| Setting up the company, ROI/VIES registration | `spanish-start-company` |
