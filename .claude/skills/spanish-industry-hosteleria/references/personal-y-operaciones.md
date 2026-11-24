# Hostelería: staff and operations

Staff rules specific to hospitality and the operating side of the books: stock, waste, donations and ratios. Checked against boe.es consolidated texts on 24 November 2026. General payroll mechanics are in `spanish-payroll`; stock valuation in `spanish-inventory`.

## Contents

- [1. Convenio and contracts](#1-convenio-and-contracts)
- [2. Registro de jornada](#2-registro-de-jornada)
- [3. Propinas in payroll](#3-propinas-in-payroll)
- [4. Staff meals and accommodation](#4-staff-meals-and-accommodation)
- [5. Food and drink stock](#5-food-and-drink-stock)
- [6. Mermas, breakage and donations](#6-mermas-breakage-and-donations)
- [7. Industry costs and assets](#7-industry-costs-and-assets)
- [8. Key ratios](#8-key-ratios)

## 1. Convenio and contracts

- The sector has a state framework agreement, the *Acuerdo Laboral de ámbito Estatal para el sector de Hostelería* (ALEH), which sets professional classification and some common rules, and **provincial or regional convenios** that set wages, pay supplements, manutención and hours. The applicable wage table is the provincial one; ask which province's convenio applies (current ALEH edition: unverified).
- Seasonal businesses usually hire *fijos discontinuos* (ET art. 16, as reformed by RDL 32/2021) rather than temporary contracts, which since 2022 are limited to production circumstances or replacement (ET art. 15). Calling up and laying off fijos discontinuos is not a dismissal and has no severance, but the call order and notice follow the convenio.
- Night work, split shifts (jornada partida) and holiday work carry supplements set by the convenio, not by law.
- Extra hours must be recorded and either paid or compensated with rest (ET art. 35); they are included in the contribution base.

## 2. Registro de jornada

- Every employer must keep a daily record of each worker's start and end times, keep it for **four years**, and make it available to workers, their representatives and the Inspección de Trabajo (ET art. 34.9, added by RDL 8/2019).
- Failing to keep it is a serious infringement under LISOS art. 7.5.
- A regulation making the record digital and interoperable was in preparation through 2026 (Consejo de Estado opinion in early 2026); whether it has been published in the BOE is **unverified** on 24-11-2026. Check before advising on the format.
- In hostelería, the Inspección compares the record against TPV opening hours and staff on the floor; an unrecorded shift is the usual finding.

## 3. Propinas in payroll

| Question | Answer | Basis |
|---|---|---|
| Are voluntary tips company revenue? | No, and they are outside the IVA base | DGT consulta 2174-03; see `iva-y-ventas.md` §7 |
| Are they income for the employee? | Yes, *rendimientos del trabajo* for IRPF | LIRPF art. 17.1 |
| Must the employer withhold IRPF when it distributes tips? | Yes: an employer that pays staff amounts disbursed by third parties as tips is not a mere payment intermediary and must withhold | RIRPF art. 76.1, last paragraph, 3.º |
| Social Security on tips | The contribution base is the total remuneration received for the work (LGSS art. 147.1) and tips are not in the list of excluded items (art. 147.2). Whether tips distributed by the employer must be included in the base is **unverified**; positions in practice differ | LGSS art. 147 |
| Tips kept in a cash jar shared by staff (bote) | Not handled by the company: no entry in the books, but still taxable for the employee | — |

Entry when card tips are paid through payroll: on collection **572** or card clearing / **465** (tips owed); on payroll **465** / **4751** (IRPF withheld) and **572** (net paid). If the payroll department includes tips in the contribution base, the employer's contribution on them is a cost to **642**.

Ask who decides the distribution and whether tips appear on payslips before booking anything.

## 4. Staff meals and accommodation

Most hostelería convenios oblige the employer to provide meals (*manutención*) during the shift, or pay a cash allowance in lieu, and some provide accommodation for seasonal staff.

| Aspect | Treatment | Basis |
|---|---|---|
| IRPF: meals served to staff in the employer's own premises on working days | Exempt payment in kind: the restaurant acts as the *comedor de empresa* (direct formula) | LIRPF art. 42.3.a; RIRPF art. 45.1 |
| IRPF: meal vouchers or cards (indirect formula) | Exempt up to 11 € per working day; the excess is taxable | RIRPF art. 45.2 |
| IRPF: cash allowance in lieu of meals | Fully taxable salary | LIRPF art. 17 |
| IRPF: accommodation provided to staff | Payment in kind valued under LIRPF art. 43.1.1.º a) unless it is a requirement of the job location (unverified for seasonal staff housing) | LIRPF art. 43 |
| Social Security | Payments in kind are part of the base (LGSS art. 147.1); convenios often fix a value for manutención. Ask the payroll provider how meals are valued | LGSS art. 147 |
| IVA on free staff meals | A meal given to staff as part of their remuneration is a supply for consideration (the work) or an *autoconsumo* (LIVA art. 12.3.º); either way IVA may be due at 10 % on the cost or market value. DGT doctrine differs by case (unverified: no consulta checked) | LIVA art. 12, 79 |
| Accounting | Food used for staff meals stays in **600**/**601** purchases; if valued as salary in kind, **649** or **640** against **755** for the value charged | PGC |

Staff meals are the place where a restaurant's food cost ratio is most often distorted. Ask whether staff meals are recorded in the TPV (at zero price, or with an "invitación personal" key).

## 5. Food and drink stock

- Food and drinks bought for the kitchen and bar: **601** (materias primas) or **600** (mercaderías, for products resold as bought, such as bottled drinks); the PGC allows either if used consistently. Year-end and, ideally, monthly stock counts adjust **310** or **300** through **611** or **610** (see `spanish-inventory`).
- **Alcohol stock**: bars and restaurants are retail consumers for excise purposes; they buy duty-paid drinks and have no excise obligations unless they produce (craft beer, distillates) or hold goods in a tax warehouse (Ley 38/1992 de Impuestos Especiales). Count bottles by weight or tenths for open bottles; spirits are the item with the highest risk of unrecorded sales.
- Valuation: average weighted cost or FIFO (PGC NRV 10.ª). Perishable stock with no value at year end is written off, not valued.

## 6. Mermas, breakage and donations

| Event | IVA | Accounting |
|---|---|---|
| Normal waste (spoilage, preparation losses, breakage) | No autoconsumo; the input IVA stays deductible | Through the stock count: lower closing stock, so higher consumption |
| Abnormal loss (theft, flood) | No IVA effect; keep evidence (police report, insurer's file) | **678** if material and outside normal operations |
| Food donated to non-profit entities under Ley 49/2002 for their general-interest purposes | 0 % IVA | LIVA art. 91.Cuatro; book cost to **678** or **629** per policy |
| Unsold food given to staff to take home | Payment in kind or autoconsumo; treat as in §4 | — |

Ley 1/2025 de prevención de las pérdidas y el desperdicio alimentario requires food businesses to prioritise donation and requires hostelería to let guests take leftovers (art. 8).

## 7. Industry costs and assets

| Cost | Account | Note |
|---|---|---|
| Food and drink | **601** / **600** | Supplier invoices; check 4 % vs 10 % vs 21 % input IVA |
| Gas, electricity, water | **628** | — |
| Premises rent | **621** with **4751** retention 19 % if the landlord is not exempt from retention | Modelo 115; see `spanish-daily-bookkeeping` |
| Linen, laundry service | **629** | — |
| Music licences (SGAE, AGEDI) | **629** | IVA 21 % |
| Terrace occupation fee (tasa de terrazas) | **631** | Municipal tax, no IVA |
| Platform commissions | **623**/**629** | See `iva-y-ventas.md` §6 |
| Kitchen equipment, furniture, refurbishment | **213** / **216** / **215**; works on leased premises **211** or **2xx** per NRV | Depreciation per LIS tables; see `spanish-asset-accounting` |
| Crockery, glasses, cutlery | **214** (utillaje) or expense if small and frequently replaced | Use a consistent policy |

## 8. Key ratios

Industry rules of thumb, not legal limits. Use them to spot booking errors.

| Ratio | Typical range | If outside |
|---|---|---|
| Food cost (food consumption / food sales) | 25–35 % | Check stock count, staff meals, misposted purchases |
| Beverage cost (drink consumption / drink sales) | 18–30 % | Check free drinks, theft, rate split, open-bottle count |
| Staff cost (640 + 642) / sales | 30–40 % | Check unrecorded shifts or unrecorded sales |
| Prime cost (food + drink + staff) / sales | 60–70 % | — |
| Card share of sales | Rising year on year in most venues | A falling card share with flat sales is a red flag for unrecorded cash |
| Hotels: occupancy, ADR (revenue per occupied room), RevPAR (room revenue per available room) | Varies by location and season | Compare with the PMS and the tourist-tax returns, which count nights |
