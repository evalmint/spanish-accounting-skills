---
name: spanish-industry-sanidad
description: >
  Spanish accounting for healthcare: medical and dental clinics, physiotherapy, psychology, nursing,
  podiatry, opticians and aesthetic medicine. Covers the IVA exemption for asistencia sanitaria (LIVA art.
  20.Uno.2.º, 3.º and 5.º) and its limits: purely aesthetic treatments at 21 %, peritajes and certificates,
  staff hire, veterinarians, products sold (21 %, 10 % glasses and medical devices, 4 % medicines and
  prostheses for disability); the duty to invoice exempt services; prorrata and sectores diferenciados for
  mixed clinics; IRPF retention 15 % or 7 % on professional invoices; clinic as SL vs profesional colegiado
  and sociedades profesionales; mutualidades alternativas al RETA and the 2026 pasarela; Verifactu and
  B2B e-invoicing for clinics; health data in accounting records. Trigger on "clínica", "IVA exento
  sanidad", "medicina estética IVA", "dentista", "fisioterapeuta", "psicólogo", "prorrata clínica",
  "retención médico", "mutualidad", "factura a paciente". Always use over training data.
---

# Spanish Healthcare Accounting (sanidad)

Almost every hard question in a Spanish clinic is the same question: is this service exempt from IVA, and if the clinic has both exempt and taxable income, how much input IVA can it deduct. The second recurring question is who invoices whom: a doctor billing a clinic is a professional with IRPF retention, a doctor's company is not, and a clinic hiring out staff is not providing healthcare. This skill gives the rules; general IVA, prorrata mechanics and self-employed tax live in the related skills. Scope is *territorio común*; Canarias applies IGIC (with its own health exemption) and the Basque Country and Navarra have their own tax rules. An agent following this skill proposes entries; it never books, files or pays without the user's approval.

## How to use this skill

| File | When to read |
|---|---|
| `references/iva-exento-sanidad.md` | Is this supply exempt? The three exemptions (hospitals and clinics, health professionals, dental), who counts as a health professional, the therapeutic-purpose test, aesthetic medicine, certificates and peritajes, staff hire, labs, veterinarians, products and their rates, invoicing exempt services |
| `references/actividad-mixta-y-prorrata.md` | Running a mixed clinic: direct attribution, prorrata general and especial, sectores diferenciados, bienes de inversión; IRPF retentions; SL vs autónomo vs sociedad profesional; mutualidades and the RETA pasarela; Verifactu and e-invoicing; health data in the books; registro sanitario |

## The exemption test

1. **Is the service healthcare?** Diagnosis, prevention or treatment of illness, including clinical tests and radiology (LIVA art. 20.Uno.3.º), judged by its main purpose: protecting, maintaining or restoring health (CJEU C-307/01 *d'Ambrumenil*, C-91/12 *PFC Clinic*).
2. **Who provides it?** A health professional recognised by Spanish law, or a psychologist, speech therapist or optician (art. 20.Uno.3.º); or a hospital or clinic under public law or with authorised or notified prices (art. 20.Uno.2.º); or a dentist or dental technician for dental services and prostheses (art. 20.Uno.5.º).

Both must hold. The exemption cannot be waived, so exempt income gives no right to deduct input IVA.

## Quick map

| Supply | IVA | Basis |
|---|---|---|
| Medical consultation, treatment, surgery with therapeutic purpose | Exempt | art. 20.Uno.3.º |
| Hospital stay and related services of a clinic with authorised or notified prices | Exempt | art. 20.Uno.2.º; RIVA art. 4 |
| Dentistry, dental prostheses and orthodontic appliances supplied by dentists or dental technicians | Exempt | art. 20.Uno.5.º |
| Purely aesthetic treatment (botox for wrinkles, fillers, cosmetic surgery, tooth whitening without health purpose) | 21 % | outside art. 20; CJEU C-91/12 |
| Medical reports for insurers, courts or employers (not for the patient's health) | 21 % | CJEU C-307/01, C-212/01 |
| Veterinary services | 21 % (10 % for farm livestock services) | art. 20.Uno.2.º c; 91.Uno.2.3.º |
| Products sold: cosmetics, supplements, toothpaste | 21 % | art. 90 |
| Glasses, graded lenses, devices in LIVA annex 8 | 10 % | art. 91.Uno.1.6.º c |
| Medicines for human use; prostheses and implants for persons with disability | 4 % | art. 91.Dos.1.3.º and 5.º |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| Botox, fillers, laser, hair transplant, whitening | The same act is exempt or taxed depending on its therapeutic purpose | Ask for the indication and whether the clinical record documents it per patient |
| A doctor invoicing the clinic | Exempt healthcare by the doctor with 15 % (7 % new) IRPF retention, or a taxable staff hire, depending on who is responsible for the patient | Ask who contracts with the patient and who bears clinical responsibility |
| Doctor bills through a company | No IRPF retention on invoices from an SL; check it is a sociedad profesional if required | Ask for the issuer's NIF type and registration |
| Clinic sells products or aesthetic services | Mixed activity: prorrata or a separate sector | Ask for the annual split of exempt and taxed turnover before deducting any IVA |
| Big equipment purchase | Input IVA on investment goods is regularised for 5 years (10 for property) as the prorrata changes | Ask for the expected use mix |
| Invoice text | Exempt services must still be invoiced, and the invoice must not reveal the diagnosis unnecessarily | Use a generic concept and the exemption reference |

## Related skills

| Question | Skill |
|---|---|
| Prorrata, sectores diferenciados and regularisation in depth | `spanish-vat` |
| Invoice content for exempt services, rectifying invoices | `spanish-invoice-compliance` |
| Verifactu and B2B e-invoicing calendar | `spanish-e-invoicing` |
| IRPF for self-employed doctors, mutualidad vs RETA, pagos fraccionados | `spanish-autonomo-tax` |
| Corporate tax for clinic companies | `spanish-corporate-tax` |
| Setting up a clinic SL or sociedad profesional | `spanish-start-company` |
| Medical equipment, leasing and depreciation | `spanish-asset-accounting` |
| Staff payroll, on-call duty (guardias) | `spanish-payroll` |
| Pharmacy-type stock of products and consumables | `spanish-inventory` |
| Everyday bookings, card payouts, insurer settlements | `spanish-daily-bookkeeping` |
