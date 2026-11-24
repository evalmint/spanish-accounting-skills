# Bank Reconciliation (Conciliación Bancaria)

## Contents

- [1. Procedure](#1-procedure)
- [2. Concepto común → likely counterpart](#2-concepto-común--likely-counterpart)
- [3. Matching rules](#3-matching-rules)
- [4. Direct-debit remittances and bills](#4-direct-debit-remittances-and-bills)
- [5. Returns and impagados](#5-returns-and-impagados)
- [6. Card acquiring (TPV) settlements](#6-card-acquiring-tpv-settlements)
- [7. Loans, interest and withholding](#7-loans-interest-and-withholding)
- [8. Foreign currency](#8-foreign-currency)
- [9. Period-end reconciliation statement](#9-period-end-reconciliation-statement)
- [10. Payment status under the B2B e-invoice mandate](#10-payment-status-under-the-b2b-e-invoice-mandate)

PGC 2007 accounts. **572** = Bancos e instituciones de crédito c/c vista, euros; **573** = same in foreign currency.

## 1. Procedure

```
1. Import and validate the statement (norma43-format.md §8 or camt checks).
2. Check continuity: opening balance = previous closing balance per account.
3. De-duplicate against already imported lines.
4. Match each line, in this order:
   a. Exact reference: invoice number / EndToEndId / mandate ID in records 23 or RmtInf
   b. Remittances and batches we generated (pain.001 / pain.008 MsgId, PmtInfId)
   c. Recurring rules (same counterparty and concepto: rent, utilities, Seguridad Social)
   d. Amount + counterparty name + date window against open items (430 / 400 / 410)
5. Propose asientos for matched lines; leave unmatched lines unposted or, with user
   approval, in 555 Partidas pendientes de aplicación.
6. Present for approval. Never post without it.
7. Reconcile the ledger balance of 572 to the bank closing balance (§9).
```

## 2. Concepto común → likely counterpart

A starting point only; the matched document decides.

| Concepto | Haber (money in, debit **572**) | Debe (money out, credit **572**) |
|---|---|---|
| 01 Talones - reintegros | — | **570** cash withdrawal; **400**/**410** cheque paid |
| 02 Ingresos | **570** cash deposited; **430** customer cheque | — |
| 03 Domiciliados - recibos | — | **400**/**410** supplier debit; **628** utilities (if no invoice booked yet); **475** taxes; **476** Seguridad Social |
| 04 Transferencias | **430** customer; **438** advance; **551**/**552** intra-group | **400**/**410** supplier; **465** payroll; **475**/**4750** tax payment |
| 05 Amortización préstamos | — | **520** (short term) / **170** principal; **662** interest |
| 06 Remesas efectos | **4312** remittance collected / **5208** discounted | — |
| 07-09 Valores | **540**/**250** sale; **760** dividends | **540**/**250** purchase |
| 11 Cajero | — | **570** |
| 12 Tarjetas | **430** or a clearing account for TPV settlements; **626** fees netted | **410** / **629** company card spend |
| 13 Extranjero | **430** / **573**; **768** gains | **400** / **573**; **668** losses; **626** fees |
| 14 Devoluciones e impagados | **400**/**410** refund received | **430** / **4315** returned debit; **626** return fee |
| 15 Nóminas - seguros sociales | — | **465** net pay; **476** social security |
| 16 Timbres - corretaje | — | **631** stamp duty; **626** brokerage |
| 17 Intereses - comisiones - gastos | **769** interest earned (net of **473** withholding) | **626** fees; **662** / **669** interest and financial costs |
| 98 Anulaciones | Reverse the original line | Reverse the original line |
| 99 Varios | Investigate | Investigate |

VAT: bank fees and interest are exempt financial services (LIVA art. 20.Uno.18.º); card-acquiring fees too (unverified for every fee type). Some bank charges (e.g. safe-deposit box rental, consultancy) are taxed: check the bank's invoice.

## 3. Matching rules

- **One line, one invoice**: amount equal to the open item and the reference present → match.
- **One line, several invoices**: customer paid a group; RmtInf lists the numbers; split the line.
- **Several lines, one invoice**: partial payments; keep the remainder open.
- **Amount differences**: small differences (bank charges deducted by the payer, rounding) need a rule approved by the user (e.g. ≤ 1 € to **626** / **669**, or keep open). Never write off customer balances without approval.
- **Retentions**: a professional's customer pays net of IRPF; match against the invoice total minus retention; the retention sits in **473** (see `spanish-invoice-compliance`).
- **Date window**: transfers usually arrive within 1-3 business days of the payer's order; direct debits on the due date; card settlements D+1 to D+3.
- **Counterparty names** in records 23 are truncated (66 or 41 characters) and uppercase: use fuzzy matching.

## 4. Direct-debit remittances and bills

Remittance of SEPA direct debits presented for collection (gestión de cobro):

| Step | Debit | Credit |
|---|---|---|
| Remittance sent (optional memo entry) | **4312** Efectos comerciales en gestión de cobro | **430** |
| Bank credits the remittance (one line, concepto 06 or 03) | **572** | **4312** |
| Bank fee for the remittance | **626** | **572** |

Discounted remittance or bills (descuento / anticipo): credit **5208** Deudas por efectos descontados when funds arrive; cancel **5208** against **4311**/**4312** at maturity if paid; interest to **665**.

## 5. Returns and impagados

Returned direct debit (concepto 14), with fee:

| Account | Debit | Credit |
|---|---|---|
| **4315** Efectos comerciales impagados (or **430**) | amount | |
| **626** Servicios bancarios | fee | |
| **572** | | amount + fee |

Then contact the customer (reason code in records 23 / camt RtrInf). If it becomes doubtful, reclassify to **436** and follow the bad-debt rules (`spanish-invoice-compliance` `references/rectificativas.md` §6; `spanish-year-end-closing`). A CORE refund (MD06) within 8 weeks does not cancel the debt: the customer still owes the invoice.

## 6. Card acquiring (TPV) settlements

- Acquirers settle daily totals net of fees or gross with a separate fee line. Match the settlement to the day's card sales (POS Z report or e-commerce payout report), not to individual invoices.
- Use a clearing account (e.g. a **572** subaccount or **555**) for sales charged to cards and not yet settled; the bank line clears it.
- Fee: **626** (or **623** for some processors invoicing as service providers; follow the invoice).
- Marketplace or PSP payouts (Stripe, PayPal, Amazon): reconcile against the provider's settlement report; see `spanish-industry-ecommerce`.

## 7. Loans, interest and withholding

| Event | Debit | Credit |
|---|---|---|
| Loan instalment (concepto 05) | **520** principal; **662** interest | **572** |
| Interest earned on deposits | **572** net; **473** 19 % withholding on capital income (RIRPF art. 90; for companies LIS art. 128 and the RIS) | **769** gross |
| Overdraft / credit line interest | **662** | **572** |
| Account maintenance fee | **626** | **572** |

Reclassify long-term loan principal falling due within 12 months from **170** to **520** at year end (`spanish-year-end-closing`).

## 8. Foreign currency

- A foreign-currency account (**573**) is reconciled in its currency first, then translated. Norma 43 header currency ≠ 978 for these accounts.
- Record 24 gives the original-currency amount of a movement on a euro account (e.g. a USD payment debited in EUR); use it to compute the exchange difference against the invoice booked at its own rate: **668** loss / **768** gain.
- At year end, monetary items in foreign currency are translated at the closing rate (PGC NRV 11.ª).

## 9. Period-end reconciliation statement

```
Balance per bank statement (closing, 33 record)            X
+ Deposits booked in 572 not yet on the statement          +
− Payments booked in 572 not yet on the statement
  (cheques issued, transfers ordered after cut-off)        −
± Bank lines not yet booked (fees, interest, returns)      ±
= Balance per ledger, account 572                           Y
Difference                                                  must be 0
```

- Every reconciling item needs a date and a reference; items older than one month need an explanation.
- Unexplained differences are never posted to a balancing account. Investigate: missing statement days, duplicate imports, entries posted to the wrong bank account, reversed signs.
- Keep the reconciliation and the statement files as justificantes (`spanish-accounting-compliance`).

## 10. Payment status under the B2B e-invoice mandate

From 6 Oct 2027 (> 8 M€) and 6 Oct 2028 (others), the recipient of a B2B e-invoice must report its **full payment and payment date** (plus the due date) to the AEAT Solución Pública de Facturación Electrónica, and the payment state to the issuer, within 4 calendar days excluding weekends and national holidays (RD 238/2026 art. 10, 12; personas físicas ≤ 8 M€ from 6 Oct 2029). The bank reconciliation is the natural trigger: when a supplier invoice is fully matched to a debit line, queue the payment-status message for approval. Details in `spanish-e-invoicing`.
