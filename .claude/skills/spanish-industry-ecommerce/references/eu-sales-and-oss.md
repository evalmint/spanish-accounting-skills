# E-commerce: where VAT is due, OSS and IOSS

Where IVA (or foreign VAT) is due on each kind of online order, which scheme carries it, and how it is booked under the PGC 2007. General IVA mechanics (casillas, reverse charge, import VAT) are in `spanish-vat`; invoice content in `spanish-invoice-compliance`. This file covers only what is specific to selling online across borders.

Sources: LIVA (BOE consolidated 07/10/2026) arts. 3, 8 bis, 9.3º, 20 bis, 21, 25, 68, 70, 73, 163 septiesdecies-octovicies, 167 bis; RIVA; RD 1619/2012 art. 4; AEAT modelo 303 *Instrucciones 2026*; European Commission guidance on the temporary flat duty on low-value imports (8 June 2026). Checked 2026-11-24.

## Contents

1. [What changed for Spanish webshops in 2025-2026](#1-what-changed-for-spanish-webshops-in-2025-2026)
2. [Master decision table](#2-master-decision-table)
3. [Sales to consumers in Spain](#3-sales-to-consumers-in-spain)
4. [Distance sales to consumers in other EU countries](#4-distance-sales-to-consumers-in-other-eu-countries)
5. [OSS: the Union scheme (modelo 369)](#5-oss-the-union-scheme-modelo-369)
6. [Stock held outside Spain](#6-stock-held-outside-spain)
7. [Marketplaces as deemed supplier](#7-marketplaces-as-deemed-supplier)
8. [Goods from outside the EU: IOSS, imports, dropshipping](#8-goods-from-outside-the-eu-ioss-imports-dropshipping)
9. [Canarias, Ceuta, Melilla and non-EU customers](#9-canarias-ceuta-melilla-and-non-eu-customers)
10. [B2B sales to EU businesses](#10-b2b-sales-to-eu-businesses)
11. [Excise goods](#11-excise-goods)
12. [Digital products and services](#12-digital-products-and-services)
13. [Ask the user before booking](#13-ask-the-user-before-booking)

## 1. What changed for Spanish webshops in 2025-2026

| Change | Date | Source |
|---|---|---|
| Food rates back to permanent levels (4 % basics and olive oil, 10 % other food); temporary 0/2/5/7.5 % ended | 1 January 2025 | RDL 4/2024 |
| EU customs duty relief for consignments ≤ €150 abolished; temporary flat duty of €3 per item | 1 July 2026 to 1 July 2028 | Council Regulation (EU) 2026/382; Commission Delegated Regulation (EU) 2026/1022 |
| Product identifiers mandatory in customs data for low-value consignments | 1 November 2026 (as reported by the Commission; unverified in the legal text) | European Commission news, 29 June 2026 |
| B2B e-invoicing obligation scheduled (does not cover B2C web sales) | 12 months (volume > €8 million) and 24 months (others) from Orden HAC/1028/2026, in force 6 October 2026: about October 2027 / October 2028 | RD 238/2026; see `spanish-e-invoicing` |
| Verifactu for invoicing software | Corporate taxpayers before 1 January 2027, others before 1 July 2027 per RD 1007/2023 as amended by RDL 15/2025; a further postponement to October 2028 has been reported but not found in the BOE consolidated text (unverified) | See `spanish-e-invoicing` |
| ViDA: wider single VAT registration via OSS, transfer of own goods in OSS | 1 July 2028 (EU law, Directive (EU) 2025/516); not yet in LIVA | Plan, do not apply yet |

## 2. Master decision table

`Ship from` is where the goods physically start.

| Buyer | Destination | Ship from | VAT due where | Scheme | 303 casilla | Account |
|---|---|---|---|---|---|---|
| Consumer | Spain (peninsula, Balearics) | Spain | Spain | 303 | 01-09 | **700**, **477** |
| Consumer | Other EU | Spain, under €10,000 EU-wide | Spain | 303 | 01-09 | **700**, **477** |
| Consumer | Other EU | Spain, above €10,000 or opted | Destination | OSS (369) or local registration | 123 (OSS) / 120 (local) | **700**; destination VAT to a liability sub-account outside the 303 totals |
| Consumer | Other EU | Warehouse in another EU country | Destination (no threshold) | OSS if shipped cross-border; local return if same-country delivery | 123 or 120 | Same |
| Consumer | Canarias, Ceuta, Melilla, non-EU | Spain | Exempt export | Export evidence | 60 | **700** |
| Consumer | EU | Outside EU, ≤ €150 | Destination | IOSS (369 monthly) or customer pays at import | 123/124 | **700** |
| Consumer | EU | Outside EU, > €150 | Import VAT at destination | Customer imports (DAP) or seller imports (DDP, registration in destination) | - | **700** |
| Business with valid VIES number | Other EU | Spain | Exempt intra-EU supply, buyer self-assesses | 349 key E | 59 | **700** |
| Business | Spain | Spain | Spain | 303 (full invoice) | 01-09 | **700**, **477** |

## 3. Sales to consumers in Spain

- Spanish IVA at the product's rate (21 %, 10 % food, 4 % basic food, books and some health products; see `spanish-vat`). Shipping charged follows the goods: it is part of the base (LIVA art. 78.Dos.1º), and with mixed-rate baskets is apportioned (DGT doctrine).
- Retail sales to consumers may be documented with a *factura simplificada* up to €3,000 including IVA (RD 1619/2012 art. 4.2.a), or €400 for other operations (art. 4.1.a). If the customer asks for a full invoice with NIF, issue it.
- Devengo is when goods are put at the customer's disposal (delivery), not when paid; an order paid before shipping is an advance: IVA is due on payment (LIVA art. 75.Dos). Most shops simply invoice at payment, which meets the advance rule.

## 4. Distance sales to consumers in other EU countries

**The €10,000 threshold (LIVA art. 73):** one EU-wide figure, excluding VAT, adding together intra-EU distance sales of goods and B2C cross-border telecom, broadcasting and electronic services.

| Point | Rule |
|---|---|
| Who can use it | Sellers established only in Spain and shipping from Spain (art. 68.Tres.b) |
| Test | Previous calendar year and current year. If the previous year exceeded €10,000, destination VAT from 1 January. If crossed during the year, destination VAT applies to the sale that crosses it and all later sales (art. 73.Uno, second paragraph) |
| Option | Destination taxation from the first euro; minimum two calendar years (art. 73.Dos) |
| Not available | Goods dispatched from another member state (art. 73.Uno, third paragraph); excise goods (art. 68.Cinco); new means of transport |
| Below the threshold | Spanish IVA in the 303, as a domestic sale |
| Above | Destination country's rate and rules; Spain: not subject (casilla 123 via OSS, or 120 if registered locally) |

**Rates:** apply the destination country's rate for the product. Check the European Commission's TEDB database or the destination authority; do not use Spanish rates.

**Invoices:** distance sales under OSS follow Spanish invoicing rules, and a simplified invoice is allowed only when the Union OSS is used (RD 1619/2012 art. 4.4.b). Without OSS, the sale is located abroad and invoicing follows the destination's rules (RD 1619/2012 art. 2.3).

## 5. OSS: the Union scheme (modelo 369)

| Point | Rule | Source |
|---|---|---|
| Registration | Modelo 035 at the AEAT (Spain as member state of identification) before the first quarter of use | LIVA art. 163 duovicies; Orden HAC/610/2021 (unverified number) |
| Scope | All intra-EU distance sales of goods and B2C services in member states where the seller is not established. Once registered, all such sales go through OSS (no picking) | Art. 163 unvicies |
| Return | Modelo 369, quarterly, also when nil | Art. 163 duovicies.Uno.c |
| Deadline | During the month after the quarter: 1-30 April, 1-31 July, 1-31 October, 1-31 January | Same |
| Payment | In euros, within the filing period, referenced to the return | Art. 163 duovicies.Uno.d |
| Corrections | In a later 369, within three years of the original deadline | Same |
| Input VAT | Spanish input VAT stays in the 303; foreign input VAT is recovered by the EU refund procedure (modelo 360) | Art. 163 tervicies |
| Records | Ten years, available to any member state | Art. 163 duovicies |
| Spanish 303 | Informative casilla 123 | AEAT Instrucciones 2026 |

**Booking an OSS sale** (French consumer, €100 + 20 % FR VAT, paid by card):

| Account | Debit | Credit |
|---|---|---|
| **4300** (sub-account Stripe/Redsys payouts) | 120 | |
| **700** | | 100 |
| OSS VAT liability (company sub-account, e.g. 4750.OSS.FR) | | 20 |

At the 369 payment: debit the OSS liability, credit **572**. Keep OSS liabilities separate from **477** so they do not distort the 303 reconciliation.

## 6. Stock held outside Spain

| Situation | Treatment |
|---|---|
| Moving own stock to a warehouse in another member state (Amazon FBA DE/FR/IT/PL/CZ, a 3PL) | Deemed intra-EU supply in Spain (art. 9.3º), exempt, casilla 59 and 349; AIB in the destination. VAT registration in the destination is required |
| Selling from that warehouse to a local consumer | Domestic sale in that country: local VAT return, not OSS |
| Selling from that warehouse to a consumer in a third member state | Distance sale: OSS (no €10,000 threshold applies) |
| Selling from that warehouse to a Spanish consumer | Distance sale arriving in Spain (art. 68.Tres.a): Spanish IVA. Whether a Spanish-established seller declares it in its 303 or in OSS is not settled here (unverified); ask an adviser |
| Call-off stock to a known B2B customer | Simplification of art. 9 bis, 12 months; not available for marketplace warehouses |
| Amazon Pan-EU | Stock moves between countries are transfers of own goods; each move needs entries on both sides and the 349 |

Ask for the fulfilment provider's inventory movement reports by country every month.

## 7. Marketplaces as deemed supplier

LIVA art. 8 bis makes the platform (*interfaz digital*) the deemed supplier when it facilitates:

| Case | Deemed supplier? |
|---|---|
| Distance sales of goods imported from outside the EU in consignments ≤ €150 | Yes: the platform charges and declares the VAT (IOSS) |
| Supplies within the EU by a seller not established in the EU to a consumer | Yes: the underlying seller's supply to the platform is exempt (art. 20 bis) |
| Spanish seller selling its own goods on Amazon, eBay, Etsy, Zalando | No: the Spanish seller remains the supplier, charges and declares VAT itself |

For a Spanish seller, the marketplace is a service provider: its commissions are a cost, and the sale price paid by the customer is the seller's revenue (gross). See `ecommerce-operations.md` section 3.

Platforms must also report sellers under DAC7 (see `ecommerce-operations.md` section 9).

## 8. Goods from outside the EU: IOSS, imports, dropshipping

| Case | Treatment |
|---|---|
| Spanish shop imports stock from China, then sells | Import by the shop: DUA, import IVA (deductible, casillas 32-33), customs duty as cost (**600**). The €3 per item flat duty applies to low-value consignments imported from 1 July 2026 |
| Dropshipping: supplier ships from China directly to an EU consumer, consignment ≤ €150, Spanish shop sells on its own site | Distance sale of imported goods. Shop registers for IOSS (modelo 035, monthly 369) and charges destination VAT at checkout; import is then VAT-exempt (LIVA art. 66.4º for imports into Spain). Without IOSS, the consumer pays import VAT and the carrier's fee at delivery (special arrangement, art. 167 bis) |
| Same via a marketplace | The marketplace is deemed supplier (art. 8 bis.a): it collects VAT; the shop's sale to the platform is exempt |
| Consignment > €150 | IOSS not available. Either the consumer imports (DAP) or the shop imports in the destination (DDP) and must register there |
| Excise goods | Excluded from IOSS |
| Dropshipping from a Spanish supplier to a Spanish consumer | Two domestic sales: supplier to shop (IVA, deductible) and shop to consumer (IVA) |
| Dropshipping from an EU supplier to a Spanish consumer | The supplier is making a distance sale into Spain (if it ships on its own behalf) or a chain transaction arises; ask who organises transport and which VAT numbers were quoted |

IOSS is optional for the seller; it applies per consignment of intrinsic value ≤ €150 (value of goods excluding transport and insurance unless included in the price).

## 9. Canarias, Ceuta, Melilla and non-EU customers

| Point | Rule |
|---|---|
| IVA | Exempt export (LIVA art. 21.1º), because Canarias, Ceuta and Melilla are outside the IVA territory (art. 3) |
| Evidence | Export customs declaration (DUA de exportación) with exit confirmed, or the carrier's export documentation for postal/courier shipments. Without evidence, charge Spanish IVA |
| 303 | Casilla 60 |
| Customer side | Pays IGIC (Canarias) or IPSI (Ceuta, Melilla) and the carrier's customs fees on import, unless the shop sells DDP, in which case the shop becomes the importer and deals with the Canarian or local tax administration |
| Small consignments into Canarias | The Canarias import regime has its own thresholds and simplifications (unverified figures; ask the carrier or the Agencia Tributaria Canaria) |
| Pricing | Show prices without IVA for these destinations at checkout; showing Spanish IVA and then not charging it creates refund disputes |
| Non-EU customers (UK, Switzerland, US) | Same export logic; the destination's import VAT and duties apply; some destinations (UK ≤ £135, Switzerland, Norway VOEC) require foreign registration for low-value B2C (outside this skill) |

## 10. B2B sales to EU businesses

| Point | Rule |
|---|---|
| Condition | Buyer's VAT number valid in VIES at the date of supply, goods transported to another member state, supply included in modelo 349 (LIVA art. 25) |
| Invoice | Full invoice, no IVA, both VAT numbers, mention of the exemption (RD 1619/2012 art. 6.1.j); no simplified invoice (art. 4.4.a) |
| Checkout | A B2B checkout must validate the VAT number in VIES and keep the consultation record |
| 303 / 349 | Casilla 59; 349 key E |
| Invalid number | Treat as a consumer sale (distance-sale rules) |

## 11. Excise goods

Wine, beer, spirits, tobacco, e-liquids with nicotine (taxed in Spain since 2025 under the Impuesto sobre el Tabaco y otros productos, unverified scope) and energy products:

- Intra-EU sales to consumers are always taxed in the member state of arrival (LIVA art. 68.Cinco); they do not count for the €10,000 threshold.
- Excise duty is also due in the destination, usually through a tax representative under the excise rules (Ley 38/1992 and the destination's law).
- Excluded from IOSS and from recargo de equivalencia for some products (RIVA art. 59.2).
- Stop and ask before selling excise goods cross-border.

## 12. Digital products and services

| Product | Place of supply | Note |
|---|---|---|
| E-books, digital newspapers | B2C: customer's member state if over €10,000 (shared threshold), else Spain; B2B: customer's country | Spanish rate 4 % (LIVA art. 91.Dos.1.2º) |
| Downloads, streaming, apps, online courses without live teacher | Same | Electronically supplied services, 21 % in Spain |
| Live online classes, webinars | B2C: depends on the nature (education or event); check art. 70.Uno.3º and 7º | Ask |
| Customer location evidence | Two non-contradictory items (billing address, IP, bank country, SIM) under Implementing Regulation (EU) 282/2011 art. 24 ter | Keep with the order |

Details for subscriptions and SaaS are in `spanish-industry-saas`.

## 13. Ask the user before booking

1. EU B2C sales (goods and digital) last year and year to date, by country.
2. Is the shop registered in OSS (modelo 035) or IOSS? From which date?
3. Where is stock held (own warehouse, 3PL, Amazon FBA, which countries)?
4. Which sales channels: own site (Shopify, WooCommerce, PrestaShop), Amazon, eBay, Etsy, others?
5. Does the shop ship to Canarias, Ceuta, Melilla or outside the EU, and with which carrier and incoterm (DAP/DDP)?
6. Does any supplier ship directly to customers (dropshipping), and from where?
7. Are any products excise goods or at reduced rates?
8. Is the seller a company or an autónomo, and which IVA regime is in its modelo 036 (general, recargo de equivalencia)?
