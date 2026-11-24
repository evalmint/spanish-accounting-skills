# Libros obligatorios, legalisation and conservation

## Contents

- [Mercantile books by entity](#mercantile-books-by-entity)
- [What each book contains](#what-each-book-contains)
- [Legalización telemática](#legalización-telemática)
- [Libros registro fiscales](#libros-registro-fiscales)
- [Conservation periods](#conservation-periods)
- [Checklist for a software export](#checklist-for-a-software-export)

## Mercantile books by entity

| Book | Who | Source | Legalised? |
|---|---|---|---|
| Libro Diario | Every empresario | Cco art. 25.1 | Yes, yearly |
| Libro de Inventarios y Cuentas Anuales | Every empresario | Cco art. 25.1 | Yes, yearly |
| Libro de actas | Every mercantile company (juntas, consejo, other collegiate bodies; decisions of the sole shareholder) | Cco art. 26; LSC art. 15 | Yes, yearly |
| Libro registro de socios | SL | LSC art. 104 | Initial book after registration; then only for years with a change |
| Libro registro de acciones nominativas | SA, SCA with registered shares | LSC art. 116 | Same as socios |
| Libro registro de contratos del socio único | Sociedad unipersonal | LSC art. 16.1 | Yes, under the rules for actas |
| Libros de detalle (e.g. *mayor*, subledgers) | Optional | RRM art. 329.2 | Optional |

The *Libro Mayor* (general ledger) is not a compulsory mercantile book, but the Diario must allow the ledger and balances to be produced (Cco art. 25.1).

## What each book contains

**Diario (Cco art. 28.2).** Every transaction, day by day, in date order. A period total (at most a quarter) is allowed if the detail is in other books or registers that agree with it. Each entry in practice carries: date, entry number, accounts (at least at the level the company's chart uses), debit and credit, and a description. Cco art. 29.1 forbids blank spaces, interpolations, crossings-out and erasures; errors are corrected by a new entry as soon as they are noticed.

**Inventarios y Cuentas Anuales (Cco art. 28.1).**

1. Detailed opening balance when the business starts.
2. Trial balances (*balances de comprobación de sumas y saldos*) at least quarterly.
3. The closing inventory (*inventario de cierre*), i.e. a detailed balance of the assets and liabilities at year-end.
4. The cuentas anuales.

**Libro de actas (Cco art. 26.1).** All resolutions of the general and special meetings and other collegiate bodies, with call and constitution data, summary of the debate, interventions whose record was requested, resolutions and voting results.

**Registro de socios / acciones (LSC arts. 104, 116).** Original ownership and every transfer, encumbrance and the identity and address of each holder. Only the person entered is treated as partner.

**Socio único contracts (LSC art. 16).** Each contract in writing, transcribed, and cited individually in the memoria with nature and terms. In the sole shareholder's or the company's insolvency, untranscribed contracts are not enforceable against the estate (art. 16.2).

## Legalización telemática

| Item | Rule | Source |
|---|---|---|
| Which books | All compulsory books, including actas, registro de socios and acciones nominativas | Ley 14/2013 art. 18.1 |
| From when | Years opened from 29-09-2013 | Instrucción DGRN 12-02-2015, Primera |
| Medium | Electronic only; paper books and blank books cannot be legalised for those years | Instrucción, Segunda, Cuarta, Quinta |
| Where | Registro Mercantil of the domicile, filed via registradores.org with an electronic certificate | Ley 14/2013 art. 18.1; Instrucción, Decimosexta |
| Deadline | Within 4 months after year-end (calendar year: by 30 April) | Ley 14/2013 art. 18.1; Cco art. 27.2; RRM art. 333.2 |
| Late filing | Accepted, but the registrar states that it was filed out of time | RRM art. 333.3; Instrucción, Vigesimoprimera |
| Package | One ZIP (Deflate, no encryption, no folders); allowed files XLS/XLSX, WQ1, WK1, DOC/DOCX, RTF, PDF, ODS/ODT; at most 9 files per book type named e.g. DIARIO_001; control files NOMBRES.TXT and DATOS.TXT | Instrucción, Anexo I |
| Fingerprint | SHA-256 hash of each book, base64-encoded, checked by the registrar | Instrucción, Decimoséptima, Decimonovena |
| Actas | Electronic; each year's actas legalised in the 4 months after year-end, with the book's opening and closing dates | Instrucción, Séptima, Octava |
| Socios / acciones | First book after registration with the founders; afterwards a new book only in the 4 months after a year in which ownership changed or an encumbrance was created | Instrucción, Décima |
| Corrections | Send a rectification with a certificate of the administrative body explaining the error plus the corrected file | Instrucción, Decimotercera |
| Never legalised | The first telematic books may include all actas and events since incorporation | Instrucción, Decimoquinta |
| Mid-year | Voluntary legalisation of detail books of actas for shorter periods | Ley 14/2013 art. 18.2 |

Most legalisation software (the registradores' *Legalia* tool or the accounting package) builds the ZIP and hashes. Rules 22, 25 and 26 of the Instrucción were repealed by the Instrucción DGRN of 1-07-2015.

**Autónomos.** RRM art. 329.1 refers to books that empresarios must keep "con arreglo a disposiciones legales". An autónomo who must keep Cco accounting (RIRPF art. 68.2) keeps Diario and Inventarios; whether they must legalise them when not registered at the Registro Mercantil is not settled in the sources checked (unverified). Libros registro fiscales are never legalised at the Registro Mercantil.

**Consequence of not legalising.** No specific fine in the Cco or LSC. The books lose evidential weight (Cco art. 31 leaves their value to the courts), and the failure may count against the company in insolvency and tax disputes. Tax sanctions apply only to tax-book failures (LGT art. 200).

## Libros registro fiscales

| Taxpayer | Books | Source |
|---|---|---|
| IVA, general | Facturas expedidas; facturas recibidas; bienes de inversión; determinadas operaciones intracomunitarias | RIVA art. 62.1 |
| IVA, monthly filers (REDEME, turnover over 6,010,121.04 €, IVA groups) | Same books kept at the AEAT sede through SII (*Suministro Inmediato de Información*) | RIVA art. 62.6 |
| IVA, others | Voluntary SII | RIVA arts. 62.6, 68 bis |
| IVA, régimen simplificado, REAGP, recargo de equivalencia | Exempt from the general books, with exceptions in their rules | RIVA art. 62.2 |
| IRPF, empresarial in estimación directa normal, mercantile activity | Cco accounting | RIRPF art. 68.2 |
| IRPF, empresarial non-mercantile, or estimación directa simplificada | Ventas e ingresos; compras y gastos; bienes de inversión | RIRPF art. 68.3-4 |
| IRPF, professional (any estimación directa) | Ingresos; gastos; bienes de inversión; provisiones de fondos y suplidos | RIRPF art. 68.5 |
| IRPF, estimación objetiva | Keep invoices numbered by date and grouped by quarter; bienes de inversión if amortising | RIRPF art. 68.6-7 |
| IS | Accounting under the Cco; must identify exempt income where relevant | LIS art. 120.1 |

The 6,010,121.04 € volumen de operaciones threshold for monthly filing is in RIVA art. 71.3.1.º (see `spanish-vat`). A single set of IVA and IRPF books may be kept if it meets both sets of requirements (RIVA art. 62.3; AEAT practice).

## Conservation periods

| Rule | Period | Starts | Source |
|---|---|---|---|
| Mercantile | 6 years | Last entry in the books (in practice from the close of each year) | Cco art. 30.1 |
| Tax prescription | 4 years | Day after the end of the voluntary filing period of each return | LGT arts. 66, 67.1 |
| Formal obligations | As long as the related tax debt is not time-barred | | LGT art. 70.1 |
| Compensated or pending BINs, credits, deductions | 10 years for the AEAT to check; afterwards the taxpayer still proves them with the return and the accounts, showing they were deposited at the Registro Mercantil | Day after the filing deadline of the year in which the right arose | LGT art. 66 bis.2-3; LIS art. 26.5 |
| Operations from time-barred years that still affect open years (e.g. amortisation of an old asset) | Until the affected year is time-barred | | LGT art. 70.3 |
| Interruption | Any AEAT action, appeal or taxpayer filing restarts the 4 years | | LGT art. 68 |
| Registro Mercantil's own copy of deposited accounts | 6 years | | LSC art. 280.2 |

Practical rule: keep the books and supporting documents for at least 6 years after the close of each year, and for as long as any BIN or deduction from that year is still being used plus 10 years from the return that generated it. Invoices: see `spanish-invoice-compliance` (RF arts. 19-23).

## Checklist for a software export

- Diario in date order, no gaps in numbering, period totals at most quarterly.
- Quarterly trial balances available for the Inventarios book.
- Closing inventory (detailed balance) and the cuentas anuales as approved.
- Exports in an allowed format (PDF or XLSX is safest), split into at most 9 files per book.
- Actas book covering exactly one year with opening and closing dates.
- SHA-256 hash per book, base64.
- The user signs and files; the agent never files on its own.
