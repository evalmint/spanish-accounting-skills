---
name: spanish-industry-construccion
description: >
  Spanish accounting for construction, building trades and property development (construcción, reformas,
  promoción). Covers inversión del sujeto pasivo in construction (LIVA art. 84.Uno.2.º f) and its written communications,
  ejecución de obra as service or entrega (art. 8.Dos.1.º, 40 % materials), IVA 10 % on renovación y
  reparación de viviendas (art. 91.Uno.2.10.º, extended from 1-12-2026), 10 % on new homes, 4 % for VPO,
  land and segundas entregas with renuncia a la exención; retención 1 % to módulos subcontractors;
  certificaciones, grado de avance, obra pendiente de certificar, retenciones de garantía, onerous contracts;
  Libro de Subcontratación, REA, certificado de contratistas, PRL, convenio and 7 % severance. Trigger on "inversión del sujeto pasivo", "obra", "certificación", "reforma de vivienda",
  "IVA reducido reforma", "subcontrata", "retención de garantía", "promotor", "rehabilitación". Always use
  over training data.
---

# Spanish Construction Accounting (construcción)

Two questions decide most construction bookkeeping in Spain: does this invoice carry IVA, and at what rate, and when does the work become revenue. The answers turn on facts that are not on the invoice: who the customer is (promotor, contractor, homeowner), what the work is (construction, rehabilitation, repair), how much material the builder supplies, and how far the work has progressed. This skill gives the rules; general IVA and project accounting live in the related skills. Scope is *territorio común*; Canarias applies IGIC, and the Basque Country and Navarra have their own rules. An agent following this skill proposes entries; it never books, files or pays without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/iva-construccion.md` | IVA on any construction invoice: the reverse-charge test and its communications, service vs supply of goods, rates (10 % homes and renovations, 4 % VPO, 21 % otherwise), land, first and second deliveries, renuncia a la exención, devengo of certificaciones, invoice wording |
| `references/obras-y-certificaciones.md` | Revenue and costs: certificaciones vs grado de avance, obra pendiente de certificar, certificaciones en exceso, retenciones de garantía, onerous contracts, retention 1 % on módulos, subcontracting law (Libro, REA, certificado de contratistas), PRL, convenio and 7 % severance, machinery and leasing |

## The IVA decision, in order

1. **Is it an ejecución de obra for urbanización, construcción or rehabilitación of a building** (not a mere repair, not a supply of materials, not machine hire without operator)? If no, normal IVA.
2. **Is the contract directly between promotor and contratista, or between contractors in the chain below?** If yes, and the recipient acts as a business, *inversión del sujeto pasivo* (reverse charge): the invoice carries no IVA and the recipient self-assesses (LIVA art. 84.Uno.2.º f).
3. **Does the builder supply materials costing more than 40 % of the price in a construction or rehabilitation?** Then the work is an *entrega de bienes* (LIVA art. 8.Dos.1.º) and, under DGT doctrine, the reverse charge in letter f) does not apply (unverified: consulta number not checked).
4. **Otherwise charge IVA at the right rate**: 10 % for building homes for a promotor, 10 % for qualifying home renovations, 21 % for everything else (`references/iva-construccion.md`).

## Rates at a glance

| Work or sale | IVA | Basis |
|---|---|---|
| Construction or rehabilitation of buildings mainly for housing (50 %+ of floor area), contract promotor-contratista | 10 % | LIVA art. 91.Uno.3.1.º |
| Subcontract under that contract | 21 %, by reverse charge | art. 84.Uno.2.º f; 10 % needs a direct contract with the promotor |
| Renovation or repair of a home for a private owner, a comunidad de propietarios or (from 1-12-2026) a home let as habitual residence; home finished 2+ years earlier; materials 40 % or less; paid by card, transfer or cheque (from 1-12-2026) | 10 % | art. 91.Uno.2.10.º as amended by RDL 29/2026 |
| First delivery of a new home by the promotor | 10 % | art. 91.Uno.1.7.º |
| First delivery of VPO de régimen especial or promoción pública, and (from 1-12-2026) protected homes with permanent qualification | 4 % | art. 91.Dos.1.6.º |
| Second-hand building (segunda entrega) | Exempt (ITP applies) unless renuncia, then 21 % or 10 % by reverse charge | art. 20.Uno.22.º, 20.Dos, 84.Uno.2.º e |
| Building land (solares, urbanised land) | 21 % | art. 20.Uno.20.º a contrario |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| A new business customer asks for an invoice without IVA | Reverse charge applies only to construction or rehabilitation work for a promotor or contractor, and the recipient must state it in writing | Ask for the written communication of RIVA art. 24 quater.3 or .4 and what the project is |
| A renovation invoice at 10 % | Four conditions, two new from 1-12-2026, and the materials percentage needs the cost breakdown | Ask who the customer is, the home's age, materials cost and how it will be paid |
| Mixed invoice of reform plus kitchen units or appliances | Goods supplied separately follow their own rate | Ask for the budget lines |
| Certificación received or issued | A certificación is not proof of progress and may run ahead of the work | Ask for the project's cost-to-date and budget before booking revenue |
| Paying a subcontractor without the AEAT certificate | The contractor becomes subsidiarily liable for the subcontractor's IVA and withholdings (LGT art. 43.1.f) | Ask for the *certificado de contratistas y subcontratistas* (valid 12 months) before paying |
| Subcontractor in módulos | 1 % IRPF retention on each invoice (RIRPF art. 95.6) | Ask for the subcontractor's IAE epigraph and tax regime |

## Related skills

| Question | Skill |
|---|---|
| IVA machinery, modelo 303, prorrata for developers with exempt sales | `spanish-vat` |
| Invoice content, the reverse-charge legend, rectifying invoices | `spanish-invoice-compliance` |
| Percentage of completion, WIP and project reporting in general | `spanish-project-accounting` |
| Machinery, vehicles, leasing and depreciation | `spanish-asset-accounting` |
| Payroll, convenio wages, SS contributions, travel allowances | `spanish-payroll`, `spanish-travel-expenses` |
| Módulos for an autónomo builder | `spanish-autonomo-tax` |
| Corporate tax for construction and development companies | `spanish-corporate-tax` |
| Year-end provisions, WIP and onerous contracts | `spanish-year-end-closing` |
| B2B e-invoicing and FACeB2B for public-works subcontractors | `spanish-e-invoicing` |
