# Norma 43 (Cuaderno 43) File Format

## Contents

- [1. Source and scope](#1-source-and-scope)
- [2. File structure](#2-file-structure)
- [3. Record layouts](#3-record-layouts)
- [4. Field rules](#4-field-rules)
- [5. Conceptos comunes](#5-conceptos-comunes)
- [6. Encoding](#6-encoding)
- [7. SEPA data in records 23 (modalidad 3)](#7-sepa-data-in-records-23-modalidad-3)
- [8. Validation rules](#8-validation-rules)
- [9. Worked example](#9-worked-example)
- [10. Parsing notes](#10-parsing-notes)

## 1. Source and scope

*Información normalizada de cuenta corriente*, Serie normas y procedimientos bancarios nº 43, version June 2012, developed by the Spanish banking associations AEB, CECA and UNACC. It is a voluntary interbank standard, not law; each bank offers it under a bilateral agreement. Names in use: Norma 43, Cuaderno 43, CSB 43, AEB 43, N43. Files usually have extensions `.n43`, `.aeb`, `.csb`, `.q43` or `.txt`.

Three *modalidades* (header position 51):

| Value | Meaning |
|---|---|
| 1 | Ordinary account; movements at the account's office; office origin blank |
| 2 | Movements from several offices; office origin filled |
| 3 | Modalidad 2 plus agreed references (Referencia 1 with check digit, Referencia 2) and normalised SEPA data in records 23 |

Frequency: monthly by default; daily by agreement.

## 2. File structure

```
11  account header                 (one per account block)
  22  movement                     (mandatory, one per movement)
    23  complementary concept      (0-5, codes 01-05)
    24  currency equivalence       (0-1, code 01, only if movement currency ≠ account currency)
  ... more 22 groups
33  account trailer                (one per account block)
... more 11..33 blocks (several accounts in one file)
88  end of file                    (one)
```

## 3. Record layouts

All records are 80 characters. N = numeric, zero-padded left; A = alphanumeric, space-padded right.

### 11 Cabecera de cuenta

| Pos | Len | Fmt | Field |
|---|---|---|---|
| 1-2 | 2 | N | `11` |
| 3-6 | 4 | N | Clave de la entidad (bank code) |
| 7-10 | 4 | N | Clave de oficina (branch) |
| 11-20 | 10 | N | Nº de cuenta |
| 21-26 | 6 | N | Fecha inicial AAMMDD |
| 27-32 | 6 | N | Fecha final AAMMDD |
| 33 | 1 | N | Clave debe/haber of the initial balance: `1` deudor, `2` acreedor |
| 34-47 | 14 | N | Importe saldo inicial (2 implied decimals) |
| 48-50 | 3 | N | Clave de divisa (ISO 4217 numeric) |
| 51 | 1 | N | Modalidad de información (1, 2, 3) |
| 52-77 | 26 | A | Nombre abreviado (account holder) |
| 78-80 | 3 | | Libre (spaces) |

### 22 Principal de movimientos

| Pos | Len | Fmt | Field |
|---|---|---|---|
| 1-2 | 2 | N | `22` |
| 3-6 | 4 | | Libre |
| 7-10 | 4 | N | Clave de oficina origen (blank in modalidad 1) |
| 11-16 | 6 | N | Fecha operación AAMMDD (booking date) |
| 17-22 | 6 | N | Fecha valor AAMMDD (interest value date) |
| 23-24 | 2 | N | Concepto común (§5) |
| 25-27 | 3 | N | Concepto propio (bank's own code) |
| 28 | 1 | N | Clave debe/haber: `1` debe (charge), `2` haber (credit) |
| 29-42 | 14 | N | Importe (2 implied decimals) |
| 43-52 | 10 | N | Nº de documento |
| 53-64 | 12 | N | Referencia 1 (11 digits + check digit; modalidad 3 only) |
| 65-80 | 16 | A | Referencia 2 (modalidad 3 only) |

### 23 Complementario de concepto (up to 5)

| Pos | Len | Fmt | Field |
|---|---|---|---|
| 1-2 | 2 | N | `23` |
| 3-4 | 2 | N | Código dato `01`-`05` |
| 5-42 | 38 | A | Concepto |
| 43-80 | 38 | A | Concepto |

In modalidad 3, SEPA transfers and debits use a different, normalised split of positions 5-80 (§7).

### 24 Equivalencia de importe (optional)

| Pos | Len | Fmt | Field |
|---|---|---|---|
| 1-2 | 2 | N | `24` |
| 3-4 | 2 | N | Código dato `01` |
| 5-7 | 3 | N | Clave divisa origen del movimiento |
| 8-21 | 14 | N | Importe in the original currency |
| 22-80 | 59 | | Libre |

No accounting value; present only when the operation currency differs from the account currency.

### 33 Final de cuenta

| Pos | Len | Fmt | Field |
|---|---|---|---|
| 1-2 | 2 | N | `33` |
| 3-6 | 4 | N | Entidad |
| 7-10 | 4 | N | Oficina |
| 11-20 | 10 | N | Nº de cuenta |
| 21-25 | 5 | N | Nº apuntes debe |
| 26-39 | 14 | N | Total importes debe |
| 40-44 | 5 | N | Nº apuntes haber |
| 45-58 | 14 | N | Total importes haber |
| 59 | 1 | N | Código saldo final: `1` deudor, `2` acreedor |
| 60-73 | 14 | N | Saldo final |
| 74-76 | 3 | N | Clave de divisa |
| 77-80 | 4 | | Libre |

### 88 Fin de fichero

| Pos | Len | Fmt | Field |
|---|---|---|---|
| 1-2 | 2 | N | `88` |
| 3-20 | 18 | N | All `9` |
| 21-26 | 6 | N | Nº de registros (all records in the file, excluding the `88`) |
| 27-80 | 54 | | Libre |

## 4. Field rules

- **Signs** are from the bank's ledger view of the client's account: *debe* = charge to the client (payment out, fee, direct debit), *haber* = credit (incoming transfer, deposit). A *saldo deudor* is an overdraft. Map: `2` → +, `1` → − on the company's **572**.
- **Amounts**: integer cents in 14 digits; `00000000012345` = 123.45.
- **Dates**: two-digit years; interpret as 20YY. Fecha operación drives the asiento date; fecha valor matters for interest and for matching card settlements.
- **Account**: entity + office + account = 18 of the 20 CCC digits; the two control digits (positions 9-10 of the CCC) are missing. To build the IBAN, recompute the CCC control digits (weights 1, 2, 4, 8, 5, 10, 9, 7, 3, 6, mod 11) and then the IBAN check digits (ISO 13616, mod 97) (algorithm from the CCC standard; unverified against a Spanish primary source).
- **Referencia 1** check digit (modalidad 3): weights 2, 3, 4, 5, 6, 7, 8, 9, 2, 3, 4 from the rightmost digit; sum mod 11; remainder 10 → 0 (Cuaderno 43 annex 3). Example: 82546789013 → check digit 8.
- **Libre** positions are spaces.

## 5. Conceptos comunes

Annex 2 of Cuaderno 43:

| Code | Concepto común | Typical content |
|---|---|---|
| 01 | Talones - reintegros | Cheques paid, cash withdrawals at branch |
| 02 | Abonarés - entregas - ingresos | Cash or cheque deposits |
| 03 | Domiciliados - recibos - letras - pagos por su cuenta | Direct debits charged (suppliers, utilities, taxes) |
| 04 | Giros - transferencias - traspasos - cheques | Transfers in and out, internal transfers |
| 05 | Amortizaciones préstamos, créditos, etc. | Loan instalments |
| 06 | Remesas efectos | Remittances of bills / direct debits presented for collection |
| 07 | Suscripciones - div. pasivos - canjes | Securities subscriptions |
| 08 | Div. cupones - prima junta - amortizaciones | Dividends, coupons |
| 09 | Operaciones de bolsa y/o compra/venta valores | Securities trades |
| 10 | Cheques gasolina | Fuel cheques |
| 11 | Cajero automático | ATM |
| 12 | Tarjetas de crédito - tarjetas débito | Card charges and card-acquiring (TPV) settlements |
| 13 | Operaciones extranjero | Foreign payments, FX |
| 14 | Devoluciones e impagados | Returned debits, unpaid bills |
| 15 | Nóminas - seguros sociales | Payroll, Seguridad Social |
| 16 | Timbres - corretaje - póliza | Stamp duty, brokerage, policy fees |
| 17 | Intereses - comisiones - custodia - gastos e impuestos | Interest, fees, custody, charges, withholding |
| 98 | Anulaciones - correcciones asiento | Reversals of earlier entries |
| 99 | Varios | Miscellaneous (banks also use it for Bizum and new products) |

Concepto propio (positions 25-27) is bank-specific; keep a per-bank lookup if you rely on it.

## 6. Encoding

- The spec prescribes EBCDIC for tapes and, for PC media, **ASCII uppercase, code page 850** ("T1000850, Personal computer: multilingual"), character 165 = Ñ; records of 80 bytes, MS-DOS sequential text (CRLF).
- In practice, online banking downloads come in CP850, ISO-8859-1, Windows-1252 or UTF-8, mixed case, sometimes without the final CRLF, sometimes with trailing spaces trimmed (lines shorter than 80).
- Detection order: valid UTF-8 with multi-byte sequences → UTF-8; bytes 0xA5 (Ñ in CP850) or 0xA4 (ñ) → CP850; bytes 0xD1 / 0xF1 → Latin-1/CP1252. Then right-pad lines to 80 before slicing positions.
- Never slice by characters on an undecoded UTF-8 line: a multi-byte Ñ shifts every later field.

## 7. SEPA data in records 23 (modalidad 3)

Cuaderno 43 annex 4 (June 2012) normalises records 23 for SEPA:

**SEPA credit transfers received** (EPC attribute numbers in brackets):

| Código dato | Pos 5-… content |
|---|---|
| 01 | Ordenante name (AT-02) 5-70; ordenante code (AT-10) 71-80 |
| 02 | Ordenante reference / end-to-end (AT-41) 5-39, "No proporcionado" if none; on-behalf-of name (AT-08) 40-80 |
| 03 | Purpose (AT-44) 5-8; category purpose (AT-45) 9-12; remittance info (AT-05) 13-80 |
| 04 | Remittance info continued (AT-05) 5-76 |
| 05 | Free use for beneficiary data (AT-21/24/28/29) 5-80 |

**SEPA direct debits charged**:

| Código dato | Pos 5-… content |
|---|---|
| 01 | Scheme `CORE` or `B2B` (AT-20) 5-8; creditor name (AT-03) 9-78 |
| 02 | Creditor identifier (AT-02) 5-39; mandate reference (AT-01) 40-74 |
| 03 | Purpose (AT-58) 5-8; category purpose (AT-59) 9-12; remittance info (AT-22) 13-80 |
| 04 | Remittance info continued (AT-22) 5-76 |
| 05 | Creditor reference (AT-10) 5-39; debtor / ultimate debtor name (AT-14/15) 40-80 |

The remittance information (AT-05 / AT-22) usually carries the invoice number: the best matching key. Names may be truncated.

## 8. Validation rules

| # | Check | Severity |
|---|---|---|
| 1 | Every line is 80 characters after right-padding; first two characters are a known record type | Error |
| 2 | Order: `11` → `22`(`23`{0,5}`24`?)* → `33`, repeated; one `88` at the end | Error |
| 3 | `23` código dato is 01-05, ascending, max 5 per movement; `24` código dato 01 | Error |
| 4 | Numeric fields contain only digits; dates are valid AAMMDD; fecha inicial ≤ fecha final | Error |
| 5 | `33` entity/office/account equal the `11` of the block; currency equal | Error |
| 6 | Count and sum of `22` with key 1 = `33` nº/total debe; same for key 2 / haber | Error |
| 7 | Saldo final(signed) = saldo inicial(signed) + total haber − total debe | Error |
| 8 | `88` record count = number of lines before it | Error |
| 9 | Fecha operación within [fecha inicial, fecha final] | Warning |
| 10 | Saldo inicial equals the previous file's saldo final for the same account (spec: must coincide) | Warning: gap or overlap |
| 11 | Referencia 1 check digit (modalidad 3) | Warning |
| 12 | Same movement already imported (§10) | Block, ask |

Never "fix" totals by editing the file. Report the exact difference and get a new download.

## 9. Worked example

One account, two movements, EUR, modalidad 3. Fictitious data. Each line is exactly 80 characters (trailing spaces not shown).

```
110049150000001234562701012701312000000010000009783EMPRESA EJEMPLO SL
22    1500270105270105040012000000001210000000000000000000000000FRA2027-0001
2301CLIENTE EJEMPLO SA
2303        FACTURA 2027-0001
22    1500270110270110172101000000000015000000000000000000000000
3300491500000012345600001000000000015000000100000000121000200000001119500978
88999999999999999999000006
```

Reading it:

| Line | Meaning |
|---|---|
| `11` | Bank 0049, branch 1500, account 0000123456, period 1-31 Jan 2027, opening balance acreedor (`2`) 10,000.00, EUR (978), modalidad 3 |
| `22` #1 | Booked and value 5 Jan 2027, concepto común 04 (transfer), haber (`2`) 1,210.00, Referencia 2 "FRA2027-0001" |
| `23 01` | SEPA transfer: ordenante name (AT-02) |
| `23 03` | Purpose and category blank; remittance info (AT-05) "FACTURA 2027-0001" |
| `22` #2 | 10 Jan 2027, concepto común 17 (fees), debe (`1`) 15.00 |
| `33` | 1 debe for 15.00; 1 haber for 1,210.00; closing acreedor 11,195.00 = 10,000.00 + 1,210.00 − 15.00 |
| `88` | 6 records before it |

Asientos: 5 Jan, **572** debit 1,210.00 / **430** credit 1,210.00 (matched to invoice 2027-0001); 10 Jan, **626** debit 15.00 / **572** credit 15.00. Bank fees for financial services are VAT-exempt (LIVA art. 20.Uno.18.º), so no **472**.

## 10. Parsing notes

- Parse into: account (entity, office, account, currency), statement period, opening/closing balances, and movements (dates, concepto común/propio, signed amount, document, references, concept lines joined, original currency amount).
- Duplicate key per movement: account + fecha operación + fecha valor + signed amount + concepto común + nº documento + referencias + hash of the 23 lines, plus an occurrence counter for identical lines in the same file.
- Overlapping downloads (e.g. daily files plus a monthly file) are common; check rule 10 and the duplicate key before posting.
- A file can contain several accounts and currencies (a **573** account for foreign-currency accounts).
- Keep the raw file as the bank justificante for the asientos (conservation per `spanish-accounting-compliance`).
