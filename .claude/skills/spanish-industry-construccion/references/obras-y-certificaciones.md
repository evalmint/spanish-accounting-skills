# Construction: works, certificaciones and site obligations

Revenue recognition for construction contracts, the balance-sheet items peculiar to the sector, and the subcontracting, tax-liability and labour rules that drive costs. Checked against boe.es consolidated texts on 24 November 2026.

## Contents

- [1. Revenue: grado de avance under the PGC](#1-revenue-grado-de-avance-under-the-pgc)
- [2. Certificaciones vs revenue: the two balancing accounts](#2-certificaciones-vs-revenue-the-two-balancing-accounts)
- [3. Retenciones de garantía](#3-retenciones-de-garantía)
- [4. Onerous contracts and post-completion costs](#4-onerous-contracts-and-post-completion-costs)
- [5. Developers (promotoras)](#5-developers-promotoras)
- [6. Paying subcontractors: retention, certificate, liability](#6-paying-subcontractors-retention-certificate-liability)
- [7. Ley 32/2006: subcontracting limits, REA and Libro](#7-ley-322006-subcontracting-limits-rea-and-libro)
- [8. Prevención de riesgos laborales](#8-prevención-de-riesgos-laborales)
- [9. Convenio, contracts and the 7 % severance](#9-convenio-contracts-and-the-7--severance)
- [10. Machinery, vehicles and leasing](#10-machinery-vehicles-and-leasing)
- [11. Monthly checklist](#11-monthly-checklist)

## 1. Revenue: grado de avance under the PGC

The PGC 2007 recognition rule for revenue (NRV 14.ª, rewritten by RD 1/2021) and the ICAC Resolución de 10 de febrero de 2021 on revenue apply to construction contracts. Revenue from a contract is recognised **over time**, by stage of completion, when one of the over-time criteria is met; a construction on the customer's land, or a building the customer controls as it is built, normally qualifies.

| Step | What to do |
|---|---|
| Identify the contract and its performance obligations | A single building is usually one obligation; separate obligations only if distinct |
| Determine the price | Include agreed modifications (*modificados*, reformados) once approved; variable amounts (penalties, bonuses) only if highly probable not to reverse |
| Measure progress | Output method (measured units, surveys) or input method (costs incurred / total estimated costs). Exclude costs that do not reflect progress, such as materials delivered to site not yet installed |
| Cannot measure reliably | Recognise revenue only up to the costs incurred that are expected to be recovered |
| Expected loss | Recognise the full expected loss at once (§4) |

The *Adaptación sectorial del PGC a las empresas constructoras* (Orden de 27 de enero de 1993) still applies where it does not contradict the PGC 2007 (RD 1514/2007 DT 5.ª) and is the usual source for sector sub-accounts (unverified: its continuing application after RD 1/2021 should be confirmed with ICAC guidance). Small companies on the PGC Pymes (RD 1515/2007) apply the same principle.

Corporate tax follows the accounting result (LIS art. 10.3 and 11.1); see `spanish-corporate-tax`. General project mechanics are in `spanish-project-accounting`.

## 2. Certificaciones vs revenue: the two balancing accounts

The *certificación de obra* is the periodic (usually monthly) statement of work executed, signed by the *dirección facultativa* and accepted by the client. It is a billing document, not proof of the stage of completion. Compare cumulative revenue by stage of completion with cumulative amounts certified:

| Situation | Entry at month or year end | Account |
|---|---|---|
| Revenue earned exceeds amounts certified (*obra ejecutada pendiente de certificar*) | Debit the asset, credit revenue | **4309** Clientes, facturas pendientes de formalizar / **705** |
| Amounts certified exceed revenue earned (*certificaciones en exceso*, *obra certificada por anticipado*) | Debit revenue, credit the liability | **705** / **438** Anticipos de clientes |
| Advance received before work starts (*anticipo de obra*) | Cash in, liability | **572** / **438** and **477** (IVA accrues on receipt, LIVA art. 75.Dos) |
| Certificación invoiced | Receivable and revenue (subject to the adjustments above) | **430** / **705** and **477** |

Reverse the balancing entries at the start of the next period, or keep them as running balances, consistently. Disclose contract balances in the notes (PGC model notes on revenue).

## 3. Retenciones de garantía

Clients usually withhold a percentage of each certificación (commonly 5 %) until reception of the works and the end of the guarantee period.

- The retention is part of the receivable, not a discount: book the full certificación to **430** and transfer the retained part to a separate sub-account, for example "4300xxxx Clientes, retenciones de garantía". The PGC 2007 has no specific account for it (unverified: the 1993 sector adaptation's sub-account numbering was not checked).
- Retentions due in more than 12 months are non-current; reclassify them out of current receivables in the balance sheet (PGC model, *deudores comerciales no corrientes*).
- Retentions the company withholds from its subcontractors: the mirror image in a sub-account of **400** or **410**, reclassified as non-current when appropriate.
- If the client disputes defects, assess impairment (**694** / **490**) or a provision for repairs (§4).
- IVA on the retention accrues with the invoice of the certificación, not on release (see `iva-construccion.md` §6).

## 4. Onerous contracts and post-completion costs

| Item | Treatment | Accounts |
|---|---|---|
| Contract where total estimated costs exceed total revenue | Recognise the full expected loss as soon as it is probable | **6954** / **4994** Provisión por contratos onerosos |
| Costs to finish already-certified work, site clearance, final settlement | Provision at year end if not accrued | **695** / **4999** |
| Guarantee repairs after delivery (*garantía decenal* exposure under Ley 38/1999 LOE art. 17, one-, three- and ten-year periods) | Provision based on experience if probable and estimable | **695** / **4999** or a long-term provision under **14** |
| Excess provision released | Reverse | **4994**/**4999** / **7954** |

## 5. Developers (promotoras)

- Buildings under construction for sale are **inventory**, not fixed assets: land and construction costs to **33** (productos en curso) and finished units to **35**, through **71** variation accounts. Borrowing costs can be capitalised on inventory that takes more than a year to be ready (PGC NRV 10.ª 1).
- Sale revenue is recognised on transfer of control, normally at delivery of the keys or deed, not on reservations or pre-sale instalments, which go to **438**.
- A developer with exempt second-hand sales or residential rentals has mixed IVA: apply prorrata (see `spanish-vat`).

## 6. Paying subcontractors: retention, certificate, liability

| Rule | Detail | Basis |
|---|---|---|
| IRPF retention 1 % | Payments by a business to an autónomo in *estimación objetiva* (módulos) for activities listed in RIRPF art. 95.6.2.º, which include carpentry and metal structures, albañilería y pequeños trabajos de construcción (IAE 501.3), installations and plumbing (504.1 to 504.3), and other construction trades | RIRPF art. 95.6 |
| Declaring the retention | Modelo 111 (monthly or quarterly) and annual modelo 190; book to **4751** | RIRPF art. 108 |
| Autónomo in estimación directa | No retention on business activities (only professional activities carry 15 %/7 %) | RIRPF art. 95.1, 95.6 |
| Certificado de contratistas y subcontratistas | A business that contracts works or services within its main activity is subsidiarily liable for the subcontractor's IVA and withholdings on that work unless the subcontractor gives a specific AEAT certificate issued in the 12 months before each payment. AEAT issues or refuses it within three days | LGT art. 43.1.f |
| Social Security and wages | The main contractor is jointly liable for Social Security debts the subcontractor incurred during the contract, claimable for three years after the work ends, and for wage debts for one year after (ET art. 42.2). Request the TGSS *certificación negativa por descubiertos* in writing; if TGSS does not issue it within 30 days, the requesting company is released for Social Security (ET art. 42.1) | ET art. 42 |
| Ley 32/2006 breaches | Joint liability for labour and Social Security obligations of the subcontractor in breach | Ley 32/2006 art. 7.2 |

Ask for the subcontractor's IAE epigraph, tax regime and the two certificates before the first payment, and diary their expiry.

## 7. Ley 32/2006: subcontracting limits, REA and Libro

Ley 32/2006, de 18 de octubre, reguladora de la subcontratación en el sector de la construcción, developed by RD 1109/2007.

| Requirement | Detail | Basis |
|---|---|---|
| Own organisation | Contractors and subcontractors must have their own production organisation, assume business risk and direct their workers | art. 4.1 |
| PRL training and organisation | Accredited by a sworn declaration | art. 4.2.a, 4.3 |
| Registro de Empresas Acreditadas (REA) | Registration with the regional labour authority of the registered office, valid nationwide | art. 4.2.b, 6 |
| Permanent staff | At least 30 % of the workforce on indefinite contracts for businesses habitually contracted on construction sites | art. 4.4 |
| Chain limit | Promotor → contratista → up to three levels of subcontractors; the third subcontractor and autónomos cannot subcontract; labour-only subcontractors cannot subcontract | art. 5.2 |
| Libro de Subcontratación | Each contractor keeps one per site, on site, recording every subcontract in order, level, scope, dates and PRL plan delivery | art. 8.1 |
| Vigilance | Contractors must check their subcontractors' REA registration and compliance with the chain limits | art. 7.1 |

These are not accounting rules, but a breach creates a liability that the year-end review should consider, and the REA and Libro are what an inspection or main contractor asks for first.

## 8. Prevención de riesgos laborales

Construction sites require a *estudio* or *estudio básico de seguridad y salud* in the project, a *plan de seguridad y salud* by each contractor, a safety coordinator where several companies work, and the opening notice of the work centre (RD 1627/1997 and Ley 31/1995). PRL costs (external prevention service, PPE, training) are operating costs: prevention service to **623** or **629**, PPE to **602** or **629**. Workers need sector PRL training under the convenio; the *Tarjeta Profesional de la Construcción* (TPC) accredits it.

## 9. Convenio, contracts and the 7 % severance

- The **VII Convenio General del Sector de la Construcción** (BOE 23-9-2023, term 2022–2026, salary increases for 2025 and 2026 agreed by later actas published in the BOE) sets the framework; provincial convenios set the wage tables. Whether a VIII convenio has been signed for 2027 is unverified.
- **Contrato indefinido adscrito a obra** (Ley 32/2006 DA 3.ª, as amended by RDL 32/2021): when the work ends, the employer must offer relocation, after training if needed. If the worker refuses or cannot be relocated, the contract may end for reasons inherent to the worker with **7 % severance** calculated on the salary concepts in the convenio tables accrued over the whole contract, or more if the state convenio provides it (DA 3.ª.6).
- Accounting: accrue the 7 % monthly as the right is earned, debit **641** (or **640** per policy) and credit a liability (a sub-account of **465**, or a provision under **142** where timing or amount is uncertain). Ask the payroll provider which concepts enter the base.
- Construction carries higher accident and occupational disease contribution rates than most sectors (tarifa de primas, Ley 42/2006 DA 4.ª, by CNAE code; exact current rates unverified here, see `spanish-payroll`).
- Travel and site allowances (dietas, plus de distancia): see `spanish-travel-expenses`.

## 10. Machinery, vehicles and leasing

- Plant and machinery **213**, vehicles **218**, small tools **214**; depreciation per LIS official tables (see `spanish-asset-accounting`).
- Finance leases (most construction machinery leasing): asset at the present value of payments against **174**/**524**; interest to **662** (PGC NRV 8.ª). IVA is charged on each instalment.
- Machinery hire without operator is a rental (21 %, no reverse charge); with operator for construction works it may be an ejecución de obra under the reverse charge (see `iva-construccion.md` §2).
- Machinery used on a site is a contract cost for measuring progress (depreciation allocated by use).

## 11. Monthly checklist

1. Update estimated total cost and revenue per contract; recompute stage of completion.
2. Compare with cumulative certifications; post **4309** or **438** balances.
3. Check new modificados are approved before including them in the price.
4. Review loss-making contracts; post or update the **4994** provision.
5. Move retenciones de garantía to their sub-accounts; reclassify those due beyond 12 months at year end.
6. For each subcontractor paid: reverse-charge treatment, 1 % retention if módulos, AEAT certificate in date, REA registration, entry in the Libro de Subcontratación.
7. Accrue 7 % severance for indefinite site contracts.
