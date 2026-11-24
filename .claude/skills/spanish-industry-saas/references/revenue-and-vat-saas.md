# Revenue and IVA for SaaS companies

## Contents

1. The revenue model in one page
2. Subscriptions and deferred income
3. Setup, onboarding and implementation fees
4. Licences: right to use vs right to access
5. Usage billing, tiers and overages
6. Discounts, free months, credits and refunds
7. Principal vs agent: resellers, marketplaces, app stores
8. Costs of obtaining contracts: sales commissions
9. Foreign currency and bad debts
10. Reconciling ARR and MRR to the ledger
11. IVA: what an electronically supplied service is
12. IVA: the checkout decision
13. IVA: location evidence
14. IVA: invoices and returns
15. Buying foreign SaaS and cloud
16. Ask the user

Sources: PGC NRV 14ª (RD 1/2021), Resolución ICAC 10-02-2021 (RICAC, BOE-A-2021-2155), LIVA (Ley 37/1992, consolidated), RD 1619/2012, Council Implementing Regulation (EU) 282/2011, AEAT pages on electronic services; read 2026-11-24.

---

## 1. The revenue model in one page

| Element | Usual pattern | Rule |
|---|---|---|
| Hosted subscription (SaaS) | Over time, straight-line over the access period | NRV 14.2.1.a; RICAC art. 9.1.a and 11.5 (straight-line when effort is even) |
| Setup fee that only gives access | Spread over the subscription (and longer if renewal is a material right) | RICAC art. 28.5, 27 |
| Distinct implementation or migration service | Separate obligation, over time by progress, or at completion | RICAC arts. 7, 9, 11 |
| On-premise licence, right to use | Point in time, not before the customer can use it | RICAC art. 29.5.b, 29.7 |
| Licence with significant ongoing updates the customer depends on | Over time (right to access) | RICAC art. 29.5.a, 29.6 |
| Usage or overage fees | As usage occurs | RICAC art. 11.4 practical expedient; art. 13 |
| Support and maintenance | Over time | RICAC art. 9.1.a |

## 2. Subscriptions and deferred income

Annual plan 1,200 euros + 21 % IVA, invoiced and collected on 1 October, calendar year-end, Spanish customer:

| Date | Debit | Credit |
|---|---|---|
| 1 Oct, invoice | **430** 1,452 | **705** 1,200; **477** 252 |
| 1 Oct, collection | **572** 1,452 | **430** 1,452 |
| 31 Dec, defer 9 months | **705** 900 | **485** 900 |
| 1 Jan, reverse | **485** 900 | **705** 900 |

Monthly releasing (credit **485**, debit at invoice) is equally valid; month-end systems usually book the invoice to the liability and release 100 euros a month.

**Which account.** PGC **485** *Ingresos anticipados* is defined for income booked in the closing year that belongs to the next. RICAC art. 33.3 presents a contract liability (payment received or due before transfer) under C.V.7 *Anticipos de clientes* (**438**), or under B.V *Periodificaciones a largo plazo* if long term (**181** for long-term advances). Both are used in practice; pick one policy, apply it consistently and disclose contract balances in the notes. Multi-year prepaid deals: the part beyond twelve months is non-current.

**IVA is not deferred.** IVA is due when the instalment is payable (LIVA art. 75.Uno.7º) or on collection of an advance (art. 75.Dos), regardless of the revenue deferral.

## 3. Setup, onboarding and implementation fees

RICAC art. 28.5-28.6: a non-refundable upfront fee is usually an advance for future services and recognised as those services are provided. Administrative set-up activities do not transfer a service and are not a separate obligation.

Decision:
1. Does the setup transfer something the customer can benefit from on its own or with other readily available resources (art. 7.1.a), and is it separately identifiable (7.1.b)? For example, data migration or configuration another provider could have done → **distinct**: separate obligation, recognised as performed (see `spanish-project-accounting`).
2. If not distinct (activation, account provisioning) → combine with the subscription and spread the fee over the expected service period. Extend beyond the initial term if the customer gets a renewal option at a price that is a material right (art. 27, art. 28.5).
3. Allocate the total contract price across obligations by stand-alone selling prices (arts. 16-17), not by the invoice split.

## 4. Licences: right to use vs right to access

RICAC art. 29:
- A licence sold only together with an online service (the customer accesses content through the service) is part of a single obligation with that service (art. 29.3.b). Pure SaaS is not a licence for this purpose.
- A distinct licence is a **right to access** (over time) if all three hold: the company's activities significantly affect the IP the customer has rights to (change form or functionality, or the customer's benefit depends on them); the customer is exposed to those activities; they do not transfer a separate good or service (art. 29.6). Otherwise it is a **right to use** (point in time), but revenue cannot be recognised before the customer can use the software, for example before a key is provided (art. 29.7).
- Sales- or usage-based royalties on licences: recognised only when the later of the sale/usage or the satisfaction of the obligation occurs (NRV 14.3).

## 5. Usage billing, tiers and overages

Usage fees are variable consideration (art. 13). When the company is entitled to bill an amount that matches the value of the service provided to date, it may recognise that amount (art. 11.4, practical expedient). Committed minimums with true-ups: recognise the minimum over time and the excess as usage occurs, constrained to what is highly probable not to reverse (art. 13.2).

## 6. Discounts, free months, credits and refunds

- **Free months or ramped pricing in a fixed-term contract:** total consideration is spread over the whole service period; the free months carry revenue (allocation of a discount, art. 18).
- **Service-level credits:** variable consideration reducing revenue.
- **Refund rights** (money-back periods): estimate expected refunds; recognise revenue net and a refund liability (art. 24; provision presentation art. 33.4).
- **Bad debts are not refunds:** collectability problems after recognition are impairment expenses (**694** / **490**), not a reduction of revenue (NRV 14.2).

## 7. Principal vs agent: resellers, marketplaces, app stores

RICAC art. 26: the company is principal if it controls the service before it is transferred to the customer. Indicators: primary responsibility for fulfilment, inventory risk, pricing discretion.

- Selling through **Apple App Store or Google Play**: the store typically sets itself as the seller to the end user (commissionaire). Revenue is often the net payout and the IVA is the platform's obligation (Reg. 282/2011 art. 9a presumes the platform supplies in its own name). Read the platform agreement and payout report before deciding; the treatment for accounting and for IVA usually matches but must be checked separately.
- **Resellers** buying at a discount and reselling: the reseller is your customer; your revenue is the price to the reseller.
- **Marketplaces** taking a fee where you remain the seller: gross revenue, platform fee as expense (**623** or **629**).

## 8. Costs of obtaining contracts: sales commissions

Incremental costs of obtaining a contract (commissions paid only on signing) are expensed systematically in line with the transfer of the services, so deferred if recoverable (RICAC art. 21). Practical approach: defer to **480** (or an asset sub-account) and release over the expected customer life, including renewals for which no commensurate commission is paid. Presentation: B.VI *Periodificaciones a corto plazo* or a long-term periodification line (RICAC art. 33.5). Commissions paid on renewals of similar amount relate to the renewal period only.

## 9. Foreign currency and bad debts

- Invoices in USD or GBP: record at the spot rate on the transaction date; re-measure monetary items (receivables, cash) at the closing rate; differences to **668**/**768** (PGC NRV 11). Deferred income (**485**/**438**) is non-monetary and stays at the historical rate.
- Impairment of receivables: **694**/**490** (or individual write-offs); tax deductibility follows LIS art. 13.1 (six months overdue and other conditions).

## 10. Reconciling ARR and MRR to the ledger

ARR and MRR are management metrics, not accounting figures. Reconcile monthly:

```
Opening deferred income (485/438)
+ invoices issued in the month (net of IVA)
- revenue recognised in the month (705)
= closing deferred income
```

Then: revenue for the month ≈ MRR active in the month, adjusted for mid-month starts, credits, usage and one-off fees. Differences above a set tolerance are investigated (missing invoices, wrong service periods, discounts booked as expenses).

---

## 11. IVA: what an electronically supplied service is

LIVA art. 69.Tres.4º: services transmitted and received through processing equipment and electronic networks, including website supply and hosting, remote maintenance of programs and equipment, supply of software and updates, images, text, information and databases, music, films, games, distance teaching. Communication by email alone does not make a service electronic. EU detail: Reg. 282/2011 art. 7 and Annex I.

Human-delivered consulting, custom development delivered by people, or training with a live teacher are not TBE (*telecomunicaciones, radiodifusión y electrónicos*) services, even if delivered online; for B2C they follow the general rule (Spanish IVA if the seller is in Spain), with exceptions for the services in art. 69.Dos to non-EU consumers.

## 12. IVA: the checkout decision

For a seller established only in Spain (*territorio de aplicación del impuesto*, TAI).

| # | Question | If yes |
|---|---|---|
| 1 | Customer in Spain (peninsula or Baleares)? | 21 % IVA (LIVA arts. 69.Uno, 90), **477**, modelo 303 |
| 2 | EU business with a VAT number valid in VIES at the date of supply? | Not subject in Spain (art. 69.Uno.1º applies only to customers established in the TAI). Invoice without IVA with the mention "Inversión del sujeto pasivo" (RD 1619/2012 art. 6.1.m); modelo 349 (services key); non-subject box in modelo 303 |
| 3 | EU consumer? Check the threshold: total B2C TBE services plus intra-EU distance sales of goods to the whole EU, net of VAT, did not exceed 10,000 euros last year and has not this year (art. 73.Uno) | Under it: Spanish 21 % (art. 70.Uno.8º). Over it, from the supply that breaks it: destination rate via OSS *régimen de la Unión* (art. 70.Uno.4º.a; art. 163 unvicies ff.). Opting for destination taxation under the threshold binds for at least two calendar years (art. 73.Dos) |
| 4 | Customer outside the EU (business or consumer)? | Not subject to Spanish IVA (AEAT: "No sujeto"; for consumers, a use-and-enjoyment exception may apply to art. 69.Dos services under art. 70.Dos, which do not include TBE services) |
| 5 | Customer in Canarias, Ceuta or Melilla? | Outside the IVA territory (LIVA art. 3): not subject to Spanish IVA. Canarias B2B: the Canarian business self-assesses IGIC (Ley 20/1991 art. 19). Canarias B2C electronic services: located in Canarias for IGIC (Ley 20/1991 art. 17, per secondary sources); the peninsular seller may have to register with the Agencia Tributaria Canaria (unverified, ask an adviser). Ceuta/Melilla: IPSI rules apply (unverified) |

**OSS returns** (*régimen de la Unión*): modelo 369, per calendar quarter, filed and paid during the month after the quarter (LIVA art. 163 duovicies); sales declared in OSS do not go in modelo 303. Register through modelo 035. Output IVA in OSS can be tracked in a sub-account of **477** per country.

**Business status without a VAT number.** If the customer cannot show a valid VAT number, treat it as a consumer unless other evidence of business status exists (Reg. 282/2011 art. 18). Keep the VIES consultation result with the invoice.

## 13. IVA: location evidence

Reg. 282/2011 (as amended by Reg. 1042/2013 and 2017/2459):
- For ordinary SaaS the consumer is located where the supplier identifies on the basis of **two non-contradictory items** of evidence (art. 24b.d), chosen from art. 24f: billing address, IP address or geolocation, bank details or card issuer country, SIM country code, fixed land line location, other commercially relevant information.
- If the supplier's total TBE supplies to other Member States do not exceed **100,000 euros** in the current and preceding year, **one** item from a third party (bank, payment provider) suffices (art. 24b, second paragraph).
- A self-declared country alone is not evidence. Store the evidence per transaction for ten years (OSS record-keeping, art. 63c).

## 14. IVA: invoices and returns

| Item | Rule |
|---|---|
| Invoice content | RD 1619/2012 art. 6; reverse charge mention art. 6.1.m; reference to the non-subject provision for non-EU and Canarias customers is good practice (unverified as mandatory) |
| B2C invoices to EU consumers under OSS | Invoicing follows the rules of the Member State of identification (Spain) |
| Simplified invoices | Possible for B2C up to the art. 4 limits; see `spanish-invoice-compliance` |
| Software | Verifactu-compliant invoicing software from 1 January 2027 for IS taxpayers (RD 1007/2023, RDL 15/2025); see `spanish-e-invoicing` |
| Modelo 349 | Intra-EU B2B services, monthly or quarterly (RIVA art. 81) |

## 15. Buying foreign SaaS and cloud

Services from non-Spanish suppliers to a Spanish business (AWS, Google Workspace from Ireland, US tools): the Spanish company is the taxpayer by reverse charge (LIVA art. 84.Uno.2º). Self-assess 21 %: debit **472**, credit **477**, both in modelo 303; EU purchases also go in modelo 349. Without an ROI registration the EU supplier may charge its own VAT, which is not deductible in modelo 303. Detail in `spanish-daily-bookkeeping`.

## 16. Ask the user

- Which plans exist (monthly, annual, multi-year), and how are they invoiced?
- Are setup or implementation fees charged, and what does the work consist of?
- Any on-premise licences, or only hosted access?
- Which payment provider and checkout tool, and what location evidence and VIES results does it store?
- Total B2C sales to other EU countries last year and this year?
- Any sales through app stores, marketplaces or resellers?
- Commission plan for sales staff?
- Customers in Canarias, Ceuta or Melilla?
