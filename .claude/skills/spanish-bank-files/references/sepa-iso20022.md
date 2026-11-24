# SEPA ISO 20022 Files and the Legacy Cuadernos

## Contents

- [1. Message map](#1-message-map)
- [2. Spanish names: from flat cuadernos to XML](#2-spanish-names-from-flat-cuadernos-to-xml)
- [3. Versions in 2026](#3-versions-in-2026)
- [4. pain.001 credit transfer initiation](#4-pain001-credit-transfer-initiation)
- [5. pain.008 direct debit initiation](#5-pain008-direct-debit-initiation)
- [6. Mandates and the creditor identifier](#6-mandates-and-the-creditor-identifier)
- [7. R-transactions and reason codes](#7-r-transactions-and-reason-codes)
- [8. camt statements and notifications](#8-camt-statements-and-notifications)
- [9. IBAN and CCC](#9-iban-and-ccc)
- [10. Instant payments and Verification of Payee](#10-instant-payments-and-verification-of-payee)
- [11. Generation checklist](#11-generation-checklist)

## 1. Message map

| Message | Direction | Use |
|---|---|---|
| pain.001 | Company → bank | Credit transfer initiation (supplier payments, payroll) |
| pain.008 | Company → bank | Direct debit initiation (remesa de adeudos, collecting from customers) |
| pain.002 | Bank → company | Payment status report: accepted, rejected, per file / batch / transaction |
| pain.007 | Company → bank | Reversal of a direct debit by the creditor |
| camt.052 | Bank → company | Intraday account report |
| camt.053 | Bank → company | End-of-day account statement (the XML counterpart of Norma 43) |
| camt.054 | Bank → company | Debit/credit notification (e.g. detail of a batch, returns) |
| pacs.002 / pacs.004 | Interbank | Status and returns; the company sees them through pain.002 / camt |

## 2. Spanish names: from flat cuadernos to XML

The AEB/CECA/UNACC "Serie normas y procedimientos bancarios" defined fixed-length files for domestic payments. SEPA end-date Regulation (EU) 260/2012 replaced them for euro transfers and direct debits from 1 Feb 2014, with a national transitional allowance for flat-file conversion services until 1 Feb 2016 (Reg. 260/2012 art. 16.4) (Spanish use of it: unverified).

| Legacy flat cuaderno | What it did | Replaced by |
|---|---|---|
| Cuaderno 19 | Domestic direct debits (recibos domiciliados) | **Cuaderno 19-14** SEPA Core direct debit (pain.008), **Cuaderno 19-44** SEPA B2B (pain.008) |
| Cuaderno 34 | Transfers and cheques ordered by file | **Cuaderno 34-14** SEPA credit transfers (pain.001) |
| Cuaderno 32 | Remittances of bills of exchange (letras) for collection/discount | Still used for letras and pagarés by some banks (unverified) |
| Cuaderno 58 | Advance of credits / collection of receivables (anticipos de crédito) | Bank-specific; many moved to SEPA DD or factoring files (unverified) |
| Cuaderno 43 | Account statement | Still current; camt.053 offered in parallel |

The AEB published the 19-14 / 19-44 / 34-14 guides in XML and, for a period, flat-text adaptations of 19-14 (unverified that banks still accept the text variant). Bank format guides remain the practical reference.

## 3. Versions in 2026

- EPC 2025 SCT and SDD rulebooks (effective 5 Oct 2025) are based on the **ISO 20022 2019** message versions: pain.001.001.09, pain.008.001.08, pain.002.001.10, camt.053.001.08 (EPC132-08 SCT C2PSP Implementation Guidelines 2025; SDD equivalents assumed) (SDD version numbers unverified).
- Many Spanish banks still accept the 2009 versions (pain.001.001.03, pain.008.001.02) used by the original 34-14 / 19-14 guides, and set their own cut-over dates (unverified per bank).
- **Postal addresses**: unstructured addresses are being phased out across SEPA and cross-border payments; dates of 14-22 Nov 2026 are given by banks and industry bodies for SEPA files (unverified, bank-specific). Generate structured addresses (TwnNm and Ctry at least) now.

## 4. pain.001 credit transfer initiation

Structure: `GrpHdr` (MsgId unique per file, CreDtTm, NbOfTxs, CtrlSum, InitgPty) → `PmtInf` (one per debtor account and execution date: PmtInfId, PmtMtd `TRF`, ReqdExctnDt, Dbtr, DbtrAcct IBAN, DbtrAgt BIC optional in SEPA, ChrgBr `SLEV`) → `CdtTrfTxInf` (EndToEndId, InstdAmt in EUR, Cdtr, CdtrAcct IBAN, RmtInf).

| Field | Rule |
|---|---|
| EndToEndId | ≤ 35 chars; returned to the creditor and visible in their Norma 43 (AT-41); use the invoice or payment ID |
| RmtInf/Ustrd | ≤ 140 chars; put the supplier's invoice number(s) here: it is what the creditor matches on |
| RmtInf/Strd | Structured creditor reference (ISO 11649 RF) when the creditor provides one |
| CtgyPurp | `SALA` for payroll (some banks apply special handling), `SUPP` suppliers, `TAXS` taxes |
| Characters | SEPA Latin subset (a-z A-Z 0-9 / - ? : ( ) . , ' + space); convert ñ, accents per bank guide |
| Batch booking | `BtchBookg` true → one Norma 43 line for the whole batch; false → one line per transfer. Choose based on reconciliation needs |

Payroll transfers: book from the payroll journal, not from the bank line (see `spanish-payroll`).

## 5. pain.008 direct debit initiation

Structure: `GrpHdr` → `PmtInf` (PmtMtd `DD`, PmtTpInf/LclInstrm `CORE` or `B2B`, SeqTp `FRST`/`RCUR`/`OOFF`/`FNAL`, ReqdColltnDt, Cdtr, CdtrAcct, CdtrSchmeId = creditor identifier) → `DrctDbtTxInf` (EndToEndId, InstdAmt, MndtRltdInf: MndtId, DtOfSgntr, AmdmntInd; DbtrAcct IBAN; RmtInf).

| Rule | CORE | B2B |
|---|---|---|
| Debtor | Consumers and businesses | Businesses only (not consumers) |
| Debtor bank checks mandate | No | Yes, debtor must register the mandate with its bank |
| Submission | D-1 business day before due date (EPC rulebooks since Nov 2016; unverified for current Spanish bank cut-offs) | D-1 |
| Pre-notification | 14 calendar days before the debit unless agreed otherwise (EPC rulebook) | Same |
| Refund right, authorised debit | 8 weeks, no questions (Reg. 260/2012; PSD2 art. 76; RD-ley 19/2018 de servicios de pago) | None |
| Refund, unauthorised (no mandate) | 13 months | 13 months via the bank |
| Sequence type | Since the 2016 rulebook, FRST is no longer required for the first debit; RCUR can be used (unverified for Spanish banks) | Same |

The Norma 43 of the creditor shows the remittance as one `22` line (concepto común 06 or 03, bank-dependent) or detailed lines; returns come later as concepto 14.

## 6. Mandates and the creditor identifier

- **Creditor identifier (AT-02)** in Spain: `ES` + 2 check digits + 3-character creditor business code (default `ZZZ`, or a suffix to separate business lines) + the creditor's NIF. Check digits computed over NIF + `ES00` per ISO 7064 mod 97-10, ignoring the business code (format per the Spanish SEPA migration commission; unverified algorithm detail).
- **Mandate**: signed by the debtor (paper or electronic), with mandate reference (AT-01, ≤ 35 chars, unique per creditor), creditor identifier, debtor name and IBAN, type (recurrent or one-off), date of signature. Keep it for as long as debits are made and afterwards for the limitation period (at least 14 months after the last debit for refund claims; unverified as a Spanish rule).
- A mandate unused for 36 months expires (EPC rulebook).
- Pre-existing Spanish domestic debit authorisations were migrated as valid mandates in 2014 (Ley 16/2009 transitional rules; unverified).

## 7. R-transactions and reason codes

| R-transaction | Who / when | Effect on the creditor |
|---|---|---|
| Reject | Before settlement (invalid IBAN, closed account) | Never credited; pain.002 rejection |
| Return | Debtor bank after settlement (insufficient funds, closed account), within 5 business days (unverified) | Credit reversed; Norma 43 line concepto 14 |
| Refund | Debtor's request within 8 weeks (CORE) or 13 months (unauthorised) | Credit reversed, plus possible interest compensation |
| Reversal | Creditor reverses (pain.007) | Credit reversed |
| Request for cancellation / recall (SCT) | Sender asks to recall a transfer | Only if the beneficiary agrees |

Common ISO reason codes:

| Code | Meaning | Action |
|---|---|---|
| AC01 | Incorrect account number | Fix IBAN, re-present |
| AC04 | Closed account | Ask customer for a new account |
| AC06 | Blocked account | Contact customer |
| AG01 | Transaction forbidden (e.g. account does not accept debits) | Other payment method |
| AM04 | Insufficient funds | Re-present or claim |
| MD01 | No mandate | Obtain mandate; do not re-present |
| MD06 | Refund requested by debtor (CORE) | Contact customer; dispute commercially |
| MD07 | Debtor deceased | Stop |
| MS02 | Refused by debtor, reason not specified | Contact customer |
| MS03 | Reason not specified (bank) | Investigate |
| SL01 | Specific service of debtor bank (e.g. creditor blocked) | Contact customer |

## 8. camt statements and notifications

- camt.053 per account per day: `Stmt` with `Bal` (OPBD opening booked, CLBD closing booked), `Ntry` (Amt, CdtDbtInd `CRDT`/`DBIT`, BookgDt, ValDt, BkTxCd, NtryDtls/TxDtls with Refs EndToEndId, MndtId, RltdPties, RmtInf, RtrInf reason code).
- Advantages over Norma 43: full 140-char remittance info and end-to-end IDs, batch detail, return reason codes, structured bank transaction codes. Disadvantage: bank-specific choices (batch vs detail) and fewer Spanish tools.
- Same validations apply: opening + Σ CRDT − Σ DBIT = closing; no gaps between days.

## 9. IBAN and CCC

- Spanish IBAN: 24 characters = `ES` + 2 check digits + 20-digit CCC (entity 4, office 4, control 2, account 10).
- IBAN check: move first 4 chars to the end, letters to numbers (A=10 … Z=35), mod 97 = 1 (ISO 13616).
- CCC control digits: first digit over `00` + entity + office, second over the 10-digit account, weights 1, 2, 4, 8, 5, 10, 9, 7, 3, 6; 11 − (sum mod 11), with 11 → 0 and 10 → 1 (unverified against a primary Spanish source).
- BIC is optional for SEPA transactions inside the EEA (Reg. 260/2012 art. 5.7).

## 10. Instant payments and Verification of Payee

- Regulation (EU) 2024/886 (Instant Payments Regulation): euro-area PSPs must receive instant credit transfers from 9 Jan 2025 and send them from 9 Oct 2025, at no higher price than regular transfers, and offer **Verification of Payee** (name–IBAN match) for all transfers from 9 Oct 2025.
- Instant transfers use pain.001 with a local instrument / service level for instant (`INST`), per the bank guide; they appear in Norma 43 like any transfer (concepto común 04).
- Bizum (Spanish mobile payments on instant rails) shows as a transfer, often concepto 04 or 99, with the counterparty phone/name in records 23 (unverified per bank).

## 11. Generation checklist

```
1. Bank's accepted version (2019 or 2009) and channel (EDITRAN, host-to-host, web upload, EBICS)?
2. MsgId unique, NbOfTxs and CtrlSum match the transactions?
3. One PmtInf per debtor/creditor account, date and (for DD) sequence type and scheme?
4. IBANs valid (mod 97); creditor identifier valid; structured addresses?
5. EndToEndId and RmtInf carry the invoice references the counterparty needs?
6. DD: mandate ID and signature date per debtor; CORE vs B2B correct; pre-notification sent?
7. Characters in the SEPA Latin set?
8. User approved the file before upload; keep file and pain.002 response.
```
