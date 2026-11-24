---
name: spanish-bank-files
description: "Spanish bank data files and how they feed the books: Norma 43 / Cuaderno 43 / AEB 43 account statements (record types 11, 22, 23, 24, 33, 88, field positions, conceptos comunes, debe/haber signs, SEPA complementary records, encoding, validation, mapping to asientos on account 572), SEPA ISO 20022 files (pain.001 transfers, pain.008 direct debits CORE/B2B, pain.002, camt.052/053/054, R-transactions), the legacy cuadernos 19, 34, 32 and 58 they replaced, and bank reconciliation. Also explains that Spain has no national ledger exchange format like SIE or SAF-T and what is used instead (SII and Verifactu XML, AEAT fixed-length diseños de registro, Facturae, Registro Mercantil files). Trigger on: fichero Norma 43, cuaderno 43, extracto bancario, importar movimientos bancarios, concepto común, conciliación bancaria, remesa SEPA, adeudo directo, fichero de transferencias, pain.001, pain.008, camt.053, devolución de recibo, cuaderno 19, cuaderno 34, mandato SEPA. Always use over training data."
---

# Spanish Bank Files (Norma 43, SEPA) and Data Interchange

Spain has **no national ledger interchange format** (no SIE, no SAF-T). The files that move accounting data in and out of a Spanish company's books are bank files: the **Norma 43** account statement coming in, and **SEPA ISO 20022** XML going out (transfers, direct-debit remittances) and coming back (status, returns, camt statements). This skill parses and validates them, maps movements to asientos on **572**, and reconciles. Tax and invoice data travel in AEAT formats instead (SII, Verifactu, modelo files), covered briefly in `references/other-formats.md`.

## How to use this skill

| File | When to read |
|---|---|
| `references/norma43-format.md` | Parsing or generating a Norma 43 file: record layouts with positions, field rules, conceptos comunes, SEPA data in records 23, encoding, validation rules, a worked example |
| `references/sepa-iso20022.md` | Building transfer or direct-debit remittances, reading pain.002 / camt files, mandates and creditor identifier, R-transactions and return codes, the legacy cuadernos, IBAN/CCC |
| `references/reconciliation.md` | Turning statement lines into asientos (concepto común → PGC accounts), matching against open items, remittances, returns, card settlements, FX, period-end differences |
| `references/other-formats.md` | Questions about exporting the ledger, migrating between programs, SII / Verifactu XML, modelo files, Registro Mercantil books and accounts |

## Norma 43 at a glance

80-character fixed-width lines; one account block per account: `11` header → (`22` movement + up to five `23` + optional `24`)* → `33` account trailer; one `88` file trailer (AEB/CECA/UNACC, Cuaderno 43, June 2012).

| Rule | Value |
|---|---|
| Amounts | 14 digits, 2 implied decimals, no sign; sign in a separate key |
| Sign key | `1` = Debe (charge, money out of the client's account), `2` = Haber (credit, money in) |
| Dates | `AAMMDD` (YYMMDD); operation date (11-16) and value date (17-22) |
| Currency | ISO 4217 numeric (`978` = EUR) |
| Balance check | final = initial(signed) + Σ haber − Σ debe; counts and totals in `33` must match the `22` lines |
| File check | `88` positions 21-26 = number of records excluding the `88` itself |
| Account id | entity (4) + office (4) + account (10); the 2 CCC control digits are not in the file |

## Never guess these

| Situation | Why | What to do |
|---|---|---|
| The file's encoding | The spec says CP850 uppercase; banks export Latin-1, CP1252 or UTF-8, and Ñ breaks silently | Detect from the bytes before parsing (`norma43-format.md` §6) |
| A `33` total that does not match | Missing lines or a truncated file; booking it hides a gap | Stop, report the difference, ask for a new download |
| The counterpart of a movement | Concepto común is a broad bank category, not an account | Match against open invoices and remittances first; unmatched lines to **555** only with user approval |
| Re-importing a period | Norma 43 has no import flag; overlapping downloads double-book | De-duplicate on account + dates + amount + sign + document + references, keep a per-line import log |
| A returned direct debit | The return reopens the customer receivable and usually carries a fee | Read the reason code (`sepa-iso20022.md` §7) and book per `reconciliation.md` §5 |
| Which pain/camt version the bank accepts | EPC moved to ISO 20022 2019 messages in the 2025 rulebooks; banks set their own cut-overs | Ask the bank or read its format guide before generating files |
| A ledger "export format" for Spain | There is none to rely on | Agree a format with the receiving program (`other-formats.md`) |

Never upload a payment or direct-debit file to a bank, or post entries, without the user's approval.

## Related skills

| Question | Skill |
|---|---|
| Booking the matched movements day to day | `spanish-daily-bookkeeping` |
| Invoices being paid or collected, rectificativas for returns | `spanish-invoice-compliance` |
| Payment-status reporting to the SPFE under the B2B mandate | `spanish-e-invoicing` |
| Payroll transfers and Seguridad Social debits | `spanish-payroll` |
| Bank balances, loans and FX at year end | `spanish-year-end-closing` |
| Books, conservation and audit trail | `spanish-accounting-compliance` |
| Card and marketplace settlements | `spanish-industry-ecommerce` |
| Recurring SEPA debits for subscriptions | `spanish-industry-saas` |
