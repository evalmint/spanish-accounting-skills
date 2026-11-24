# Aplicación del resultado (application of profit or loss)

## Contents

- [Who decides and when](#who-decides-and-when)
- [Order of allocation for a profit](#order-of-allocation-for-a-profit)
- [Dividend limits](#dividend-limits)
- [Entries: profit](#entries-profit)
- [Entries: dividends and withholding](#entries-dividends-and-withholding)
- [Interim dividends](#interim-dividends)
- [Entries: loss](#entries-loss)
- [Equity below half of capital](#equity-below-half-of-capital)
- [Autónomos](#autónomos)

## Who decides and when

The administrators propose the application with the cuentas anuales (LSC art. 253.1); the junta general decides on it according to the approved balance (LSC art. 273.1), within the first six months (art. 164). The entry is dated on the day of the junta, in the new year. Until then the result stays in **129**. A sole shareholder decides in an acta (LSC art. 15).

## Order of allocation for a profit

| # | Allocation | Rule | Source |
|---|---|---|---|
| 1 | Offset prior losses if they leave equity below capital | Profit goes first to compensate them | LSC art. 273.2 |
| 2 | Reserva legal | 10 % of the year's profit until the reserve reaches at least 20 % of capital | LSC art. 274.1 |
| 2a | SL with capital below 3,000 € | At least 20 % of profit to the reserva legal until reserve + capital reach 3,000 € | LSC art. 4.1 |
| 3 | Statutory reserves | As the bylaws require | LSC art. 273.2 |
| 4 | Reserva de capitalización | Amount of the tax reduction taken (LIS art. 25), separate and non-distributable for 3 years | LIS art. 25.1.b |
| 5 | Reserva de nivelación | Amount of the reduction (LIS art. 105), non-distributable until added back; from the year's profit, or from the first later profits if not possible | LIS art. 105.3 |
| 6 | R&D on the balance sheet | Distributable reserves must at least equal capitalised R&D, or no distribution | LSC art. 273.3 |
| 7 | Dividends, voluntary reserves, remanente | Free, within the limits below | LSC art. 273.2 |

Reserva legal may only offset losses when no other reserves are available, while below 20 % of capital (LSC art. 274.2). After a capital reduction, dividends require the reserva legal to reach 10 % of the new capital (art. 326).

The PGC has no dedicated account for the reservas de capitalización and nivelación. Use a separately titled subaccount within "Otras reservas" (for example under **113** or **114**), so the balance sheet shows them separately as LIS art. 25.1.b requires.

## Dividend limits

| Limit | Source |
|---|---|
| Only from the year's profit or freely distributable reserves | LSC art. 273.2 |
| Equity must not be, or become through the distribution, lower than capital | LSC art. 273.2 |
| Profits recognised directly in equity are not distributable | LSC art. 273.2 |
| Distributable reserves ≥ capitalised R&D | LSC art. 273.3 |
| Paid within 12 months of the resolution; if the junta sets no date, from the day after | LSC art. 276 |
| Equity for these tests includes capital subscribed not called and excludes cash-flow hedge adjustments | Cco art. 36.1.c |
| Right of separation if, after the fifth year since registration, less than 25 % of the prior year's distributable profit is distributed and there were profits in the three previous years (unless bylaws exclude it; listed companies excepted) | LSC art. 348 bis |

## Entries: profit

Profit 80,000 €, capital 30,000 €, reserva legal already 4,000 €, reserva de capitalización 10,000 €, dividend 30,000 €, rest to voluntary reserves:

| Item | Calculation | € |
|---|---|---|
| Reserva legal | 10 % × 80,000 = 8,000, capped at 20 % × 30,000 − 4,000 = 2,000 | 2,000 |
| Reserva de capitalización | Per the IS return | 10,000 |
| Dividend | Junta | 30,000 |
| Voluntary reserves | Rest | 38,000 |

```
Debit  129   Resultado del ejercicio                80,000
Credit 112   Reserva legal                           2,000
Credit 114   Reservas especiales (subaccount Reserva de capitalización)   10,000
Credit 526   Dividendo activo a pagar               30,000
Credit 113   Reservas voluntarias                   38,000
```

Profit not allocated can go to **120** Remanente.

## Entries: dividends and withholding

Dividends paid to resident individuals and companies bear 19 % withholding (LIS art. 128.6.a for corporate recipients; LIRPF art. 101.4 for individuals, unverified), declared on modelo 123 and the annual summary modelo 193. Dividends to a parent with at least 5 % may be exempt from withholding under LIS art. 21 and art. 128.4 (check with `spanish-corporate-tax`).

```
Debit  526   Dividendo activo a pagar               30,000
Credit 4751  Hacienda Pública, acreedora por retenciones practicadas   5,700
Credit 572   Bancos                                 24,300
```
When the withholding is paid: debit **4751**, credit **572**.

## Interim dividends

Allowed by the junta or the administrators if a statement shows sufficient liquidity (included later in the memoria) and the amount does not exceed the profit since year-end, less prior losses, mandatory reserves and the estimated tax on that profit (LSC art. 277).

```
During the year:
Debit  557   Dividendo activo a cuenta               10,000
Credit 526   Dividendo activo a pagar                10,000

At the junta (application of that year's profit):
Debit  129   Resultado del ejercicio                 10,000
Credit 557   Dividendo activo a cuenta               10,000
```
**557** is presented as a deduction from fondos propios until the junta.

## Entries: loss

Loss 25,000 €:
```
Debit  121   Resultados negativos de ejercicios anteriores   25,000
Credit 129   Resultado del ejercicio                  25,000
```
Offsetting with voluntary reserves when decided:
```
Debit  113   Reservas voluntarias                    25,000
Credit 121   Resultados negativos de ejercicios anteriores   25,000
```
Partners can also contribute to cover losses through **118** Aportaciones de socios o propietarios.

## Equity below half of capital

| Rule | Source |
|---|---|
| Losses leaving equity below half of capital are a cause for dissolution unless capital is increased or reduced enough, and unless insolvency must be requested | LSC art. 363.1.e |
| Administrators call a junta within two months | LSC art. 365 |
| Losses of 2020 and 2021 are ignored for this test until the close of the year starting in 2026; losses of 2022-2026 count | RDL 7/2026 art. 30 |
| Equity for this test per Cco art. 36.1.c | Cco art. 36.1.c |

Flag this to the user at every closing where equity is close to half of capital; the decision belongs to the administrators and the junta.

## Autónomos

There is no application of profit. With Cco accounting, the result in **129** is transferred to the owner's capital (**102**), and private withdrawals or contributions run through **550** Titular de la explotación. With libros registro only, the year's net income goes straight to the IRPF return (`spanish-autonomo-tax`).
