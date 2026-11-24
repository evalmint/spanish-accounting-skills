# Buying From Abroad

How to book invoices from foreign suppliers: services from the EU and outside it, goods from other EU states, imports, and invoices that show foreign VAT. Accounts are **PGC 2007**. The modelo 303 box numbers below are those of the territorio común form; foral forms use other numbers. IVA depth (place of supply, OSS, prorrata) is in `spanish-vat`.

## Contents

- [1. Decision procedure](#1-decision-procedure)
- [2. Services from an EU supplier](#2-services-from-an-eu-supplier)
- [3. Services from a non-EU supplier](#3-services-from-a-non-eu-supplier)
- [4. Goods from another EU state](#4-goods-from-another-eu-state)
- [5. Imports from outside the EU](#5-imports-from-outside-the-eu)
- [6. The supplier charged foreign VAT](#6-the-supplier-charged-foreign-vat)
- [7. Foreign supplier with a Spanish NIF](#7-foreign-supplier-with-a-spanish-nif)
- [8. Supplier lookup](#8-supplier-lookup)
- [9. Withholding on payments to non-residents](#9-withholding-on-payments-to-non-residents)
- [10. Stop and ask](#10-stop-and-ask)

## 1. Decision procedure

1. **Goods or service?** A download, licence, subscription or online advertising is a service. Physical goods shipped to you are goods.
2. **Where is the issuing entity established?** Read the invoice header, not the brand: a US brand may invoice through an Irish entity or a Spanish branch.
3. **What does the invoice show?** Spanish IVA with an ES NIF, foreign VAT, or no VAT with a "reverse charge" mention.
4. **Is the buyer in the ROI?** A Spanish business needs to be registered in the Registro de Operadores Intracomunitarios (census declaration, modelo 036) to have a valid NIF-IVA (ES + NIF) in VIES. Without it, EU suppliers charge their own VAT.
5. **Currency**: convert at the transaction date rate (NRV 11.ª).

### Master table

| Purchase | Supplier | Invoice shows | Treatment | 303 boxes (devengado / deducible) | Also |
|---|---|---|---|---|---|
| B2B service, general rule (LIVA art. 69.Uno.1.º) | EU | No VAT, reverse charge | Autorepercusión under art. 84.Uno.2.º: **477** and **472** | 10–11 / 36–37 | Modelo 349 (key I) |
| B2B service | Non-EU | No VAT | Autorepercusión: **477** and **472** | 12–13 / 28–29 (unverified: see §3) | No 349 |
| Goods shipped from another EU state, both registered | EU | No VAT, intra-EU supply | Intra-EU acquisition (art. 13 and 15): **477** and **472** | 10–11 / 36–37 (38–39 if fixed asset) | Modelo 349 (key A) |
| Goods imported from outside the EU | Non-EU | No VAT; customs DUA shows import IVA | IVA paid to customs (or deferred) is deductible from the DUA | — / 32–33 (34–35 fixed asset) | Duties into the cost |
| Anything | Any | Foreign VAT | Not deductible in the 303; get it corrected or claim it back abroad | — | §6 |
| Anything | Foreign entity with Spanish NIF charging Spanish IVA | Spanish IVA | Domestic purchase: **472** | — / 28–29 | §7 |

Both legs of an autorepercusión appear in the same 303, so a fully taxable business pays nothing net. With a prorrata or a non-deductible cost (art. 95–96), only part of the **472** is deductible and the rest is cost.

## 2. Services from an EU supplier

Place of supply for B2B services is where the recipient is established (LIVA art. 69.Uno.1.º), so the service is taxed in Spain and the Spanish recipient is the taxpayer (art. 84.Uno.2.º). The invoice must carry both VAT numbers and a reverse-charge mention; it is the document that entitles to deduction (LIVA art. 97.Uno.4.º).

**Example: online advertising from an Irish entity, 1,000 €.**

| Cuenta | Debe | Haber |
|---|---|---|
| **627** Publicidad, propaganda y relaciones públicas | 1,000.00 | |
| **472** Hacienda Pública, IVA soportado | 210.00 | |
| **477** Hacienda Pública, IVA repercutido | | 210.00 |
| **410** Acreedores por prestaciones de servicios | | 1,000.00 |

Modelo 303: base 1,000 and cuota 210 in boxes 10 and 11; deductible base and cuota in boxes 36 and 37 (the AEAT's Pre303 notes describe 36–37 as "adquisiciones intracomunitarias de bienes y servicios corrientes"). Report the purchase in modelo 349 with key I.

Accrual: when the service is rendered; for continuous services (subscriptions) at each payment due date, and at least on 31 December for services lasting over a year without payments (LIVA art. 75.Uno.2.º and Uno.7.º).

## 3. Services from a non-EU supplier

Same place-of-supply rule (art. 69.Uno.1.º), same reverse charge (art. 84.Uno.2.º). The invoice will often lack any VAT mention: the obligation exists anyway.

| Cuenta | Debe | Haber |
|---|---|---|
| **629** Otros servicios (e.g. US SaaS) | 500.00 | |
| **472** | 105.00 | |
| **477** | | 105.00 |
| **410** (or **4104** in foreign currency) | | 500.00 |

Modelo 303: base and cuota in boxes 12–13 ("otras operaciones con inversión del sujeto pasivo"); the deductible side is commonly reported in boxes 28–29 (operaciones interiores corrientes). The exact box for the deductible side is (unverified) against the current AEAT instructions; check the year's instructions in the sede before filing. Not reported in modelo 349.

Some non-EU suppliers register for Spanish IVA under the non-Union OSS scheme and charge 21 % to consumers. If they charge Spanish IVA to a business that gave its NIF, ask for an invoice without IVA; IVA charged improperly by a non-established supplier is not deductible.

## 4. Goods from another EU state

An intra-EU acquisition of goods is taxed in Spain when goods are transported from another member state to Spain by or for a business acquirer (LIVA art. 13.1.º and 15). Accrual: when the equivalent domestic supply would accrue; the 349 and 303 period follows the invoice or the 15th of the following month (LIVA art. 76).

| Cuenta | Debe | Haber |
|---|---|---|
| **600** Compras de mercaderías (goods for resale) | 4,000.00 | |
| **472** | 840.00 | |
| **477** | | 840.00 |
| **400** Proveedores (**4004** if foreign currency) | | 4,000.00 |

Freight invoiced by a transport company for intra-EU goods transport is a B2B service taxed where the recipient is established; if the carrier is Spanish, it charges Spanish IVA; if from another EU state, autorepercusión as in §2.

**If the supplier charged its own VAT because our NIF-IVA was missing or not in VIES:** the transaction was not treated as an intra-EU supply. Do not deduct the foreign VAT here: ask for a corrected invoice after registering in the ROI, or reclaim the foreign VAT abroad (§6).

**Goods that stay in another member state** (e.g. bought and resold there, or stored at a fulfilment centre): may create a VAT registration duty in that state. Flag it and see `spanish-industry-ecommerce`.

## 5. Imports from outside the EU

The justificante for the import IVA is the customs document (DUA) or the liquidation issued by customs, not the supplier's invoice (LIVA art. 97.Uno.3.º). The base includes the customs value, duties and costs up to the first destination in Spain (LIVA art. 83).

| Item | Account |
|---|---|
| Supplier's invoice (goods value) | **600** / **400** (or **4004**) |
| Customs duties (aranceles) | **600** (part of acquisition cost, NRV 10.ª 1.1) |
| Freight and insurance to Spain | **600** (or **624** for freight not attributable to stock) |
| Import IVA paid to customs, from the DUA | **472** |
| Customs agent's fee | **623**/**629** with Spanish IVA; duties and IVA the agent advanced are suplidos (no IVA on them) |

**Example:** goods 2,000 € from China; duty 120 €; import IVA 21 % on 2,120 + freight 180 = 2,300 → 483 €. Freight-forwarder invoice: fee 60 + IVA 12.60, plus suplidos (duty 120 + import IVA 483).

| Cuenta | Debe | Haber |
|---|---|---|
| **600** (goods) | 2,000.00 | |
| **400** (supplier) | | 2,000.00 |
| **600** (freight 180 + duty 120) | 300.00 | |
| **629** (agent's fee) | 60.00 | |
| **472** (agent's IVA 12.60 + import IVA 483.00) | 495.60 | |
| **410** (forwarder: 180 + 60 + 12.60 + 120 + 483) | | 855.60 |

(Freight here is invoiced by the forwarder; it is part of the import IVA base under art. 83 and the forwarder does not charge IVA on international transport linked to the import, LIVA art. 64.)

**Deferred import IVA (IVA diferido):** businesses filing monthly (SII or large-company/REDEME) may opt to pay import IVA in the 303 instead of at customs: the import IVA is then declared as devengado in boxes 77 and deducted in 32–33 of the same 303 (RIVA art. 74.1; option in the November census declaration). Ask whether the company has opted.

**Small parcels ≤ 150 €:** since 1 July 2021 imports of low-value consignments are taxed (the 22 € exemption was abolished); the courier or the marketplace's IOSS collects the IVA. A business can deduct import IVA only with the customs document in its name.

## 6. The supplier charged foreign VAT

Foreign VAT is never deducted in the Spanish 303 (LIVA art. 92 only covers Spanish IVA).

| Situation | What happened | What to do |
|---|---|---|
| A. Correctly charged: hotel, restaurant, fuel, event ticket abroad; services taxed where performed | The supply is taxed in the other state | Book the foreign VAT as cost, or reclaim it through the EU refund procedure: modelo 360 filed electronically with the AEAT by 30 September of the following year (LIVA art. 117 bis; Directive 2008/9/EC art. 15) |
| B. Charged by mistake: a B2B service or intra-EU goods where our valid NIF-IVA was not on file | The supplier treated us as a consumer | Ask for a corrected invoice without VAT, then self-assess as in §2 or §4. Until then the VAT is a receivable on the supplier, not deductible |
| C. Supplier registered in Spain charging Spanish IVA | Not foreign VAT | §7 |

Do not self-assess Spanish IVA on top of an invoice that already carries foreign VAT for the same supply unless the invoice is corrected: you would pay twice.

## 7. Foreign supplier with a Spanish NIF

Some multinationals invoice Spanish customers from a Spanish branch or a Spanish VAT registration, charging 21 % IVA. Then the purchase is domestic: deduct the **472** normally, boxes 28–29, no autorepercusión and no 349. Check the issuer's name and NIF on every invoice: the same brand may change entity.

## 8. Supplier lookup

The issuing entity changes over time and differs by product. The table gives what to check, not a fixed answer. Entity names are commonly seen on invoices to Spanish businesses but are (unverified) for any given account: read the invoice.

| Brand | Typical issuer for EU business customers | Expected treatment |
|---|---|---|
| Google Ads, Google Workspace, Google Cloud | Google Ireland Ltd or Google Cloud EMEA Ltd (Ireland) | EU service, reverse charge (§2). Google Ads invoices may show a separate surcharge line for Spain's digital services tax costs; it is part of the advertising cost (unverified) |
| Meta (Facebook, Instagram ads) | Meta Platforms Ireland Ltd | EU service, reverse charge |
| Amazon Web Services | Amazon Web Services EMEA SARL (Luxembourg) or its Spanish branch | If the invoice shows an ES NIF and 21 % IVA, domestic (§7); otherwise reverse charge (§2) |
| Microsoft 365, Azure, LinkedIn ads | Microsoft Ireland Operations Ltd; LinkedIn Ireland | EU service, reverse charge |
| Apple, App Store fees | Apple Distribution International (Ireland) | EU service, reverse charge |
| Adobe | Adobe Systems Software Ireland Ltd | EU service, reverse charge |
| Slack, Zoom, Notion, OpenAI, Anthropic, GitHub and other SaaS | Varies: Irish or Dutch entity, or a US entity | EU → §2; non-EU → §3; Spanish IVA charged → check §3 last paragraph or §7 |
| Stripe, PayPal fees | Irish / Luxembourg entities | Mostly exempt financial services: no IVA to self-assess (`payment-providers.md`) |
| Amazon seller fees | Amazon Services Europe SARL (Luxembourg) or Spanish entity | Taxable service: reverse charge or Spanish IVA as invoiced |
| Airbnb host fees, Booking commission | Irish / Dutch entities | EU service, reverse charge |

## 9. Withholding on payments to non-residents

Payments by a Spanish company to non-residents for certain income obtained in Spain without a permanent establishment (royalties, some technical services, interest, dividends) may require a non-resident income tax retention (IRNR, RDLeg 5/2004 art. 31; modelo 216), reduced or removed by a double tax treaty with the supplier's residence certificate. Ordinary purchases of goods and most SaaS subscriptions are not in scope; licences of software or rights may be. Flag any payment to a non-resident for royalties, licences, interest or individual professional services and see `spanish-corporate-tax`.

## 10. Stop and ask

- The invoice does not say who issued it, or shows a different entity than last month.
- The company has no NIF-IVA in VIES (not in the ROI).
- Foreign VAT on a B2B service.
- A US invoice with US sales tax: not deductible, ask whether it can be removed.
- An import with no DUA in the company's name.
- A licence, royalty or interest payment to a non-resident (possible IRNR retention).
- The business has a prorrata or is exempt (healthcare, education, insurance): the self-assessed IVA is a real cost.

### Sources

LIVA (Ley 37/1992) art. 13, 15, 64, 69, 75, 76, 83, 84, 92, 97, 117 bis; RIVA (RD 1624/1992) art. 74; RD 1619/2012 art. 6; PGC NRV 10.ª and 11.ª; AEAT, Pre303 notas aclaratorias (2023) on boxes 36–37; Directive 2008/9/EC.
