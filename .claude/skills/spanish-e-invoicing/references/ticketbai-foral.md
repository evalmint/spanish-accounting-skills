# TicketBAI, Batuz and Navarra

## Contents

- [1. Why foral territories differ](#1-why-foral-territories-differ)
- [2. TicketBAI in common](#2-ticketbai-in-common)
- [3. Gipuzkoa](#3-gipuzkoa)
- [4. Álava / Araba](#4-álava--araba)
- [5. Bizkaia: TicketBAI inside Batuz](#5-bizkaia-ticketbai-inside-batuz)
- [6. Navarra](#6-navarra)
- [7. B2B e-invoice mandate in foral territories](#7-b2b-e-invoice-mandate-in-foral-territories)
- [8. Which system applies?](#8-which-system-applies)

## 1. Why foral territories differ

Under the Concierto Económico (País Vasco) and the Convenio Económico (Navarra), the Diputaciones Forales and the Hacienda Foral de Navarra regulate and manage corporate tax, IRPF and the management of VAT for taxpayers under their competence. RD 1007/2023 applies only to taxpayers with **domicilio fiscal in territorio común** (RD 1007/2023 art. 1.3). A Basque-domiciled taxpayer uses TicketBAI (and Batuz in Bizkaia), not Verifactu. Competence follows the Concierto's connection points (domicilio fiscal and, for large operators, volume of operations in each territory), so a group can have entities under different systems.

Most foral details below come from the Haciendas Forales' own pages and third-party guides; Diputación pages could not be fetched for this file. Treat the dates as (unverified) unless marked otherwise and confirm in the Boletín Oficial of each territory (BOG, BOTHA, BOB, BON).

## 2. TicketBAI in common

TicketBAI (TBAI) is a joint project of the three Diputaciones Forales and the Basque Government. Shared features (unverified in detail):

- Every invoice (completa or simplificada) is produced by a certified TicketBAI software, registered with the Hacienda Foral, which generates an XML file per invoice **before or at issue**.
- The file is signed electronically (XAdES) and chained: each file includes part of the previous invoice's signature.
- The invoice carries a **TBAI identifier** (built from the issuer NIF, issue date, part of the signature and a CRC) and a QR code linking to the Hacienda Foral's verification service.
- In Gipuzkoa and Álava the file is sent to the Hacienda Foral when issued (real time); in Bizkaia it is reported through the LROE (§5).
- Corrections use the TicketBAI anulación and rectificativa files; nothing is deleted.
- Software developers register their product with the Hacienda Foral; there are differences between the three technical specifications, so a product must be certified per territory.

## 3. Gipuzkoa

- Legal basis: Norma Foral 3/2020 on TicketBAI, and Decreto Foral 32/2020 (reglamento); calendar in its transitional provision (gipuzkoa.eus calendar document).
- Phased by IAE epígrafe: 1 Jul 2022 (tax advisers), 1 Sep 2022, 1 Nov 2022, 1 Apr 2023, and 1 Jun 2023 for the remaining activities (agriculture, livestock, forestry, fishing, other unlisted activities and IAE groups listed) (Gipuzkoa calendar document, created 11 Nov 2021). Later changes for some groups to 2024 are reported by third parties (unverified).
- In force for practically all activities by 2024.

## 4. Álava / Araba

- TicketBAI regulated by Norma Foral and Decreto Foral of the Territorio Histórico de Álava (numbers unverified).
- Phased by sector from late 2022 (first voluntary, then mandatory groups); third-party sources give 1 Dec 2022 as a start and full coverage by 2024 (unverified).

## 5. Bizkaia: TicketBAI inside Batuz

- **Batuz** is Bizkaia's broader anti-fraud strategy with three parts: TicketBAI invoicing software; the **LROE** (*Libro Registro de Operaciones Económicas*), an electronic ledger of income and expenses reported to the Hacienda Foral (modelo 140 for personas físicas with activities, modelo 240 for entities) (unverified model numbers); and pre-filled tax returns built from it.
- Phased introduction from 1 Jan 2024 in half-year windows by taxpayer group, with the last phase (including non-profit entities and remaining professionals) on **1 Jan 2026**, after Norma Foral changes postponed the original 2022 start (third-party sources cite Norma Foral 8/2023; unverified). Bizkaia publishes temporary exemptions for some groups (unverified).
- Tax incentives (deductions for adaptation costs) existed in all three territories during the voluntary periods (unverified).

## 6. Navarra

- RD 1007/2023 does not apply to taxpayers with domicilio fiscal in Navarra (art. 1.3).
- The Hacienda Foral de Navarra announced its own system (referred to as **NaTicket**) within its 2025-2027 anti-fraud plan. As of Nov 2026, no foral regulation with a mandatory start date was found; a draft reportedly targeted 2026 (unverified). Navarra taxpayers have no software-integrity obligation in force until Navarra publishes one.
- Navarra runs its own SII for monthly-period taxpayers; they keep reporting through it (unverified).

## 7. B2B e-invoice mandate in foral territories

- The B2B mandate is commercial law (Ley 56/2007 art. 2 bis; RD 238/2026 issued under Constitution art. 149.1.13.ª) and applies to businesses in all of Spain, foral territories included.
- The Solución Pública de Facturación Electrónica for foral taxpayers works under agreements between the Haciendas Forales and AEAT (RD 238/2026 DA 3.ª; Ley 56/2007 DA 21.ª.7). The concrete arrangement (where a foral taxpayer sends the copia fiel and payment status) was not published as of Nov 2026 (unverified).
- A Basque B2B invoice from 2027-2028 therefore needs TicketBAI **and** the structured e-invoice with copia fiel.

## 8. Which system applies?

```
Domicilio fiscal in territorio común?
  ├─ SII filer?                  → SII (no Verifactu) + B2B mandate
  └─ otherwise                   → Verifactu (1 Jan 2027 IS / 1 Jul 2027 others) + B2B mandate
Domicilio fiscal in Gipuzkoa     → TicketBAI (Gipuzkoa spec) + B2B mandate
Domicilio fiscal in Álava        → TicketBAI (Álava spec) + B2B mandate
Domicilio fiscal in Bizkaia      → TicketBAI + LROE (Batuz) + B2B mandate
Domicilio fiscal in Navarra      → no software-integrity system in force (Nov 2026) + B2B mandate
Canarias / Ceuta / Melilla       → Verifactu (IGIC / IPSI read for VAT) + B2B mandate
```

If the competent administration is unclear (large operators with turnover in several territories, groups), stop and ask for the tax adviser's determination under the Concierto/Convenio.
