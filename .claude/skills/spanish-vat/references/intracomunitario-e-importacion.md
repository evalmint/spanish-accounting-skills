# Cross-border IVA: intra-EU, imports, exports, OSS

How IVA works when goods or services cross the Spanish IVA border, and which casilla, modelo and PGC account each case uses. General rules are in `vat-reference.md`; the full 303 map is in `modelo-303-casillas.md`. Online-shop specifics (marketplaces, payouts, returns) are in `spanish-industry-ecommerce`.

Sources: LIVA (BOE consolidated 07/10/2026) arts. 3, 8 bis, 9, 9 bis, 13-16, 21, 25, 26, 68-73, 83-84, 163 septiesdecies-octovicies, 167; RIVA (28/02/2026) arts. 9, 13, 74, 78-81; AEAT modelo 303 *Instrucciones 2026*. Checked 2026-11-24.

## Contents

1. [Decision table](#1-decision-table)
2. [Intra-EU supplies of goods (entregas intracomunitarias)](#2-intra-eu-supplies-of-goods-entregas-intracomunitarias)
3. [Intra-EU acquisitions of goods (AIB)](#3-intra-eu-acquisitions-of-goods-aib)
4. [Transfers of own goods, call-off stock, triangulation](#4-transfers-of-own-goods-call-off-stock-triangulation)
5. [Services: place of supply](#5-services-place-of-supply)
6. [Distance sales and OSS/IOSS](#6-distance-sales-and-ossioss)
7. [Imports and the DUA](#7-imports-and-the-dua)
8. [Exports, Canarias, Ceuta and Melilla](#8-exports-canarias-ceuta-and-melilla)
9. [Modelo 349](#9-modelo-349)
10. [Foreign VAT charged by mistake](#10-foreign-vat-charged-by-mistake)
11. [Announced EU changes](#11-announced-eu-changes)

## 1. Decision table

| Operation | Spanish IVA? | Who accounts | 303 casillas | Modelo 349 | PGC |
|---|---|---|---|---|---|
| Sale of goods to EU business with valid VIES number, goods leave Spain | Exempt (art. 25) | Buyer in its country | 59 | Key E | **700** |
| Sale of goods to EU consumer, under €10,000 EU-wide and not opted | Spanish IVA | Seller | 01-09 | No | **700**, **477** |
| Sale of goods to EU consumer above €10,000 | Destination VAT | Seller, via OSS (modelo 369) or registration there | 123 (if OSS) or 120 | No | **700**; destination VAT in a separate liability account (sub-account of **475** or **477**, company choice) |
| Purchase of goods from EU business, goods arrive in Spain | AIB, Spanish IVA self-assessed | Buyer | 10-11 and 36-37 (or 38-39 assets) | Key A | **600**, **472**/**477** |
| B2B service to EU business (general rule) | Not subject in Spain (art. 69.Uno.1º) | Buyer | 59 | Key S | **705** |
| B2B service to non-EU business | Not subject | Buyer | 120 | No | **705** |
| B2B service bought from EU supplier | Spanish IVA by reverse charge | Buyer | 10-11 and 28-29 | Key I | **62x**, **472**/**477** |
| B2B service bought from non-EU supplier | Spanish IVA by reverse charge | Buyer | 12-13 and 28-29 | No | **62x**, **472**/**477** |
| Import of goods from outside the EU (or from Canarias, Ceuta, Melilla) | Import IVA on the DUA | Importer | 32-33 (or 34-35) as deductible; 77 if deferred | No | **472** against **572** or **4750** |
| Export of goods (including to Canarias, Ceuta, Melilla) | Exempt (art. 21) | - | 60 | No | **700** |

Valid VIES check, transport proof and inclusion in modelo 349 are conditions of the art. 25 exemption, not formalities.

## 2. Intra-EU supplies of goods (entregas intracomunitarias)

Exempt under art. 25.Uno when:

1. Goods are dispatched or transported to another member state by the seller, the buyer or a third party on their behalf.
2. The buyer is a business or a legal person not acting as such, with a VAT number from another member state, and has given it to the seller.
3. The seller includes the supply in modelo 349 (art. 25.Uno, second paragraph, since 1 March 2020).

Proof of transport (RIVA art. 13 and Implementing Regulation (EU) 282/2011 art. 45 bis): transport documents (CMR, bill of lading, courier tracking with delivery), insurance, bank payment for transport, buyer's written statement of receipt (for buyer-collected goods, within the 10th day of the following month under the EU presumption). Keep at least two non-contradictory items.

Devengo: the 15th of the month after dispatch, or the invoice date if earlier (art. 75.Uno.8º). The invoice must state the exemption ("Entrega intracomunitaria exenta, art. 25 Ley 37/1992") and both VAT numbers (RD 1619/2012 art. 6).

Not exempt: supplies to buyers whose acquisitions are not subject in their country (art. 14 persons below the threshold, unless they give a VAT number), and goods under REBU.

## 3. Intra-EU acquisitions of goods (AIB)

| Point | Rule |
|---|---|
| What | Goods dispatched from another member state to Spain, bought by a business (art. 13, 15) |
| Base | Consideration paid (art. 82) |
| Rate | Spanish rate of the goods |
| Devengo | When the equivalent domestic supply would be due; VAT is accounted on the 15th of the month after the start of transport, or invoice date if earlier (art. 76) |
| Booking | Debit **600** (or asset), debit **472**; credit **400**, credit **477**. Net zero with full deduction |
| 303 | Base and cuota in 10-11; deductible in 36-37 (current goods) or 38-39 (capital goods) |
| 349 | Key A |
| Non-business acquirers (exempt entities, REAGP farmers, legal persons not acting as business, art. 14) | Not subject while their EU acquisitions stay under €10,000 in the current and previous year, unless they opt; above that they file modelo 309 |
| New means of transport, excise goods | Always subject, even for private persons (modelo 309 for new cars bought by individuals) |

A business in recargo de equivalencia or simplificado that makes an AIB declares it in modelo 309 (RE) or in the 303 (simplificado, casilla 51 and 10-11 equivalents as instructed).

## 4. Transfers of own goods, call-off stock, triangulation

**Transfer of own goods (art. 9.3º).** Moving your own stock from Spain to another member state (to a warehouse, a fulfilment centre) is a deemed intra-EU supply, exempt in Spain, with an AIB in the destination. You need a VAT registration there. Exceptions: goods for installation, temporary use for services, repairs, return within 24 months for temporary use.

**Call-off stock (art. 9 bis).** Goods sent to a known buyer's warehouse in another member state under a consignment agreement: no registration in the destination if the buyer takes them within 12 months, the buyer's identity and VAT number are known when transport starts, and both parties record the goods in a register and in modelo 349 (key specific to consignment). If not taken within 12 months, it becomes a transfer of own goods.

**Triangulation (art. 26.Tres; art. 84.Uno.2º.a and 3º.a):**

| Role of the Spanish company | Treatment |
|---|---|
| Intermediary (buys from A in member state 1, sells to C in member state 3, goods go directly from 1 to 3) | AIB in Spain is exempt (art. 26.Tres) when goods do not enter Spain; the supply to C is taxed in member state 3 with reverse charge by C. Spanish company reports in 349 key T; does not register in state 3 |
| Final buyer in Spain (supplier B is a non-established intermediary) | Spanish buyer self-assesses as recipient (art. 84.Uno.2º.a and 3º.a) |
| Chain transactions (several sales, one transport) | Transport is linked to the supply to the intermediary, unless the intermediary gave the first supplier a Spanish VAT number (art. 68.Dos.1º.B) |

Ask for the full chain, who organises transport and which VAT numbers were quoted before deciding.

## 5. Services: place of supply

**General rules (art. 69):**

| Customer | Place | Spanish invoice |
|---|---|---|
| Business (B2B) | Where the customer is established (art. 69.Uno.1º) | To EU business: no IVA, mention "inversión del sujeto pasivo", customer VAT number; casilla 59 and 349 key S. To non-EU business: no IVA, casilla 120 |
| Consumer (B2C) | Where the supplier is established (art. 69.Uno.2º) | Spanish IVA, with the exceptions below |

**Main exceptions (art. 70.Uno):**

| Service | Place |
|---|---|
| Services connected with real estate (works, architects, letting, hotel accommodation) | Where the property is |
| Passenger transport | Where it takes place, by distance |
| Restaurant and catering | Where performed (on board EU transport: departure point) |
| Admission to cultural, sports, educational events and fairs | Where the event takes place |
| Short-term hire of means of transport (30 days, 90 for vessels) | Where put at disposal |
| B2C telecom, broadcasting and electronically supplied services | Where the consumer is, unless the Spanish supplier's total EU B2C cross-border sales of these services and distance sales of goods stay under €10,000 (art. 73) |
| B2C intermediation, cultural or entertainment services, transport of goods, work on movable goods | Various (art. 70.Uno.3º-7º) |

**Use and enjoyment (art. 70.Dos, as amended by Ley 31/2022 and Ley 13/2023):** services otherwise located outside the EU, Canarias, Ceuta and Melilla are taxed in Spain if effectively used in Spain, but only for (1) art. 69.Dos services (consulting, advertising, IT, legal, financial etc.) to a non-business customer, and (2) hire of means of transport. B2B consulting or advertising bought from outside the EU is not caught by this rule any more; it is a normal reverse charge under art. 84.Uno.2º.a when the Spanish buyer is a business.

**Buying services from abroad:** a Spanish business recipient self-assesses (art. 84.Uno.2º.a). Debit cost and **472**, credit supplier and **477**. EU supplier: casillas 10-11 plus deduction in 28-29, and 349 key I. Non-EU supplier: casillas 12-13 plus 28-29.

Exempt services bought from abroad (insurance, payment services) produce no cuota and no 303 entry, but check the service really is exempt (art. 20.Uno.16º, 18º).

## 6. Distance sales and OSS/IOSS

**Intra-EU distance sales of goods (art. 68.Tres-Cuatro, art. 73):**

| Situation | Place of supply |
|---|---|
| Spanish seller established only in Spain, goods leave from Spain, total EU-wide B2C distance sales plus B2C cross-border electronic/telecom services ≤ €10,000 excluding VAT in the previous year and current year to date, no option | Spain: Spanish IVA in the 303 |
| Above €10,000 (from the sale that exceeds it), or option exercised (minimum two calendar years) | Member state of arrival: destination VAT, declared via OSS Union scheme (modelo 369) or by registering there |
| Goods dispatched from a warehouse outside Spain | €10,000 threshold does not apply; destination VAT from the first euro |
| Excise goods (alcohol, tobacco, energy) to private persons | Always taxed in the member state of arrival (art. 68.Cinco) and excluded from the threshold; excise duty handled separately in the destination |

**OSS (ventanilla única) schemes (LIVA arts. 163 septiesdecies-octovicies):**

| Scheme | For | Return | Deadline | Deduction |
|---|---|---|---|---|
| Union scheme (régimen de la Unión) | EU sellers: intra-EU distance sales of goods; B2C services in member states where the seller is not established; deemed-supplier platforms (domestic supplies under art. 8 bis) | Modelo 369, quarterly, even if nil | By the end of the month after the quarter (art. 163 duovicies.Uno.c) | No deduction in the 369; Spanish input VAT stays in the 303; foreign input via refund procedure (art. 163 tervicies) |
| Non-Union scheme (régimen exterior) | Non-EU businesses selling B2C services in the EU | Modelo 369, quarterly | Same | Same |
| Import scheme (IOSS) | Distance sales of goods imported from third countries in consignments of intrinsic value ≤ €150, excluding excise goods | Modelo 369, monthly | By the end of the following month (art. 163 septvicies) | Same |

Registration: modelo 035 (Orden HAC/610/2021, unverified number). Records: keep ten years (art. 163 duovicies.Uno). Corrections to a filed 369: in a later 369 within three years.

The OSS amounts appear in the Spanish 303 only as information: casilla 123 (not subject in Spain, declared via OSS) or 124 (subject in Spain via IOSS when Spain is the destination).

**Marketplaces (art. 8 bis):** the platform is the deemed supplier for (a) distance sales of imported goods ≤ €150 and (b) supplies within the EU by non-EU sellers to consumers. A Spanish seller on Amazon or eBay is not covered by (b): it remains the supplier of its own goods. See `spanish-industry-ecommerce`.

## 7. Imports and the DUA

| Point | Rule |
|---|---|
| Taxable event | Entry of goods from outside the EU or from Canarias, Ceuta, Melilla into the IVA territory (art. 18) |
| Base | Customs value plus duties, taxes and charges outside Spain and due on import (except IVA), plus ancillary costs (commission, packing, transport, insurance) up to the first place of destination in the EU (art. 83) |
| Document | DUA (*Documento Único Administrativo*) with the customs liquidation; this is the deduction document (art. 97.Uno.2º), not the forwarder's invoice |
| Payment, general | To customs in the customs term; the forwarder often advances it and re-invoices as *suplido* (no IVA on the suplido itself) |
| Deferred import VAT (IVA diferido, RIVA art. 74.1.a) | Only for monthly filers (volume over €6,010,121.04, REDEME, groups). Option by modelo 036 in November for the next year, renewed automatically; renunciation in November, minimum three years. The import VAT is included in casilla 77 of the 303 of the period in which the DUA is received and deducted in the same return (casillas 32-35) |
| Low-value consignments ≤ €150 | IOSS seller collects VAT at sale; or the carrier uses the special arrangement (art. 167 bis) collecting from the customer at delivery |

Booking (deferred VAT, full deduction): debit **472** with credit **4750** (casilla 77); no cash moves. Without deferral: debit **472**, credit **572** or the forwarder's account (**410**) for the suplido.

Customs duty (arancel) is a cost of the goods (PGC: **600** or a sub-account), not a tax account.

**EU customs duty on low-value parcels.** From 1 July 2026 to 1 July 2028 the customs duty relief for consignments ≤ €150 is abolished and a flat €3 duty per item applies (Council Regulation (EU) 2026/382; Commission Delegated Regulation (EU) 2026/1022; European Commission guidance of 8 June 2026). This is customs duty, not IVA, but it enters the IVA import base (art. 83).

## 8. Exports, Canarias, Ceuta and Melilla

| Point | Rule |
|---|---|
| Exemption | Goods dispatched by the seller (or a third party on its behalf) outside the EU, including to Canarias, Ceuta and Melilla (art. 21.1º); goods dispatched by a non-established buyer (art. 21.2º); traveller sales with tax-free procedure (DIVA) |
| Evidence | Export customs declaration (DUA de exportación) with exit confirmation by customs (RIVA art. 9); for postal and courier shipments, the simplified export declaration or the courier's documentation that the shipment left |
| 303 | Casilla 60 |
| Deduction | Input VAT on exported goods stays deductible (art. 94.Uno.1º.b) |
| Canarias side | The Canarian buyer pays IGIC (and possibly AIEM) on import; a B2C seller shipping DDP becomes the importer and must deal with the Canarian tax (ATC) |
| Services to Canarias | Place-of-supply rules treat Canarias as outside the IVA territory: B2B services to a Canarian business are not subject (casilla 120) |

Exports are not in modelo 349.

## 9. Modelo 349

| Point | Rule |
|---|---|
| Content | Intra-EU supplies (E), acquisitions (A), services supplied under art. 69 (S), services acquired (I), triangulation (T), call-off stock movements and replacements, rectifications of earlier periods |
| Period | Monthly; quarterly if EU supplies plus services ≤ €50,000 in the quarter and each of the four previous quarters; switch to monthly from the month the threshold is passed (RIVA art. 81.2) |
| Deadline | 1-20 of the following month; July by 20 September; last period of the year by 30 January (RIVA art. 81) |
| Sanction | €20 per data set (customer/supplier), minimum €300, maximum €20,000 (LGT art. 198.1) |
| Link | Omitting a supply from the 349 can deny the art. 25 exemption |

## 10. Foreign VAT charged by mistake

If an EU supplier charges its own VAT where Spanish reverse charge applies:

- The foreign VAT is not deductible in the 303 (art. 92 refers to Spanish IVA; art. 97 needs a correct invoice).
- Ask the supplier for a corrected invoice without VAT. The EU refund procedure (modelo 360) is for VAT legitimately charged in another member state, not for wrongly charged VAT.
- AEAT and DGT treat the Spanish self-assessment as still due on the correct base (unverified for the base including the foreign VAT; consult DGT doctrine before deciding).
- Electronic services with a VAT line at a foreign rate might be OSS-charged destination VAT for a consumer: check that the supplier has the Spanish company's NIF-IVA (ROI registration).

## 11. Announced EU changes

| Change | Date | Status |
|---|---|---|
| ViDA (Directive (EU) 2025/516): platforms deemed suppliers for short-term accommodation and passenger transport; extended single registration; OSS for transfers of own goods replacing call-off stock | 1 July 2028 (EU) | EU law; Spanish transposition not in LIVA as of 07/10/2026 (unverified details) |
| ViDA digital reporting for intra-EU B2B and e-invoicing | 1 July 2030 (EU) | Not yet transposed |
| EU customs reform: flat €3 duty per item | 1 July 2026 to 1 July 2028 | In force |
