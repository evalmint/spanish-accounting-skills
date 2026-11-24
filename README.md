# Spanish accounting skills

Agent skills for Spanish bookkeeping law, tax and reporting: reference knowledge an AI agent loads when the question comes up.
They work in any agent that reads the Agent Skills format (Claude Code, Codex, Cursor, OpenClaw and others).

Modelled on the Swedish skills in [erp-mafia/accounted-skills](https://github.com/erp-mafia/accounted-skills). Accounts follow the **PGC 2007** (RD 1514/2007, as amended by RD 1/2021). Tax rules are for *territorio común* unless a skill says otherwise; the Basque Country and Navarra (*régimen foral*), Canarias (IGIC) and Ceuta/Melilla (IPSI) are flagged where they differ.

## Install

```bash
npx skills add evalmint/spanish-accounting-skills                      # choose from the list
npx skills add evalmint/spanish-accounting-skills --skill spanish-vat  # one skill
```

Or clone the repository: Claude Code loads `.claude/skills/` when you work inside the directory.

## Skills

| Skill | Covers |
| --- | --- |
| [`spanish-accounting-compliance`](.claude/skills/spanish-accounting-compliance/SKILL.md) | Spanish accounting law and compliance reference for building or checking Spanish bookkeeping |
| [`spanish-asset-accounting`](.claude/skills/spanish-asset-accounting/SKILL.md) | Spanish fixed-asset accounting (inmovilizado) under the PGC 2007 and corporate tax |
| [`spanish-autonomo-tax`](.claude/skills/spanish-autonomo-tax/SKILL.md) | Tax and social security of Spanish autónomos (sole traders, persona física) in territorio común |
| [`spanish-bank-files`](.claude/skills/spanish-bank-files/SKILL.md) | Spanish bank data files and how they feed the books |
| [`spanish-corporate-tax`](.claude/skills/spanish-corporate-tax/SKILL.md) | Spanish Impuesto sobre Sociedades (IS) under Ley 27/2014 (LIS) and RD 634/2015 (RIS), territorio común |
| [`spanish-daily-bookkeeping`](.claude/skills/spanish-daily-bookkeeping/SKILL.md) | Practical booking of everyday Spanish transactions to PGC 2007 accounts with the right IVA and IRPF treatment |
| [`spanish-e-invoicing`](.claude/skills/spanish-e-invoicing/SKILL.md) | Spanish e-invoicing and invoicing-software regimes |
| [`spanish-financial-reporting`](.claude/skills/spanish-financial-reporting/SKILL.md) | Spanish cuentas anuales and their filing |
| [`spanish-industry-construccion`](.claude/skills/spanish-industry-construccion/SKILL.md) | Spanish accounting for construction, building trades and property development (construcción, reformas, promoción) |
| [`spanish-industry-ecommerce`](.claude/skills/spanish-industry-ecommerce/SKILL.md) | Spanish accounting and IVA for online shops (comercio electrónico, tienda online) selling from Spain |
| [`spanish-industry-hosteleria`](.claude/skills/spanish-industry-hosteleria/SKILL.md) | Spanish accounting for hostelería |
| [`spanish-industry-saas`](.claude/skills/spanish-industry-saas/SKILL.md) | Spanish accounting and tax for SaaS and software companies |
| [`spanish-industry-sanidad`](.claude/skills/spanish-industry-sanidad/SKILL.md) | Spanish accounting for healthcare |
| [`spanish-inventory`](.claude/skills/spanish-inventory/SKILL.md) | Spanish inventory accounting (existencias) under the PGC 2007 |
| [`spanish-invoice-compliance`](.claude/skills/spanish-invoice-compliance/SKILL.md) | Spanish invoicing rules under the Reglamento de facturación (RD 1619/2012) for territorio común |
| [`spanish-payroll`](.claude/skills/spanish-payroll/SKILL.md) | Spanish payroll (nómina) for 2025-2026 under territorio común |
| [`spanish-project-accounting`](.claude/skills/spanish-project-accounting/SKILL.md) | Spanish project accounting under PGC 2007 (RD 1/2021) and the Resolución ICAC de 10 de febrero de 2021 on revenue |
| [`spanish-start-company`](.claude/skills/spanish-start-company/SKILL.md) | Guide a founder from idea to a registered Spanish Sociedad Limitada (SL, SLU) and its first month of compliance, one decision per turn |
| [`spanish-travel-expenses`](.claude/skills/spanish-travel-expenses/SKILL.md) | Spanish business travel (gastos de viaje, dietas) for 2026 under territorio común |
| [`spanish-vat`](.claude/skills/spanish-vat/SKILL.md) | Spanish IVA (Impuesto sobre el Valor Añadido) under LIVA (Ley 37/1992) and RIVA (RD 1624/1992), territorio común |
| [`spanish-year-end-closing`](.claude/skills/spanish-year-end-closing/SKILL.md) | Spanish year-end closing (cierre contable) for sociedades (SL, SA) under the PGC or PGC-PYMES, and for autónomos |

## Status

First version, researched against BOE, AEAT, Seguridad Social and ICAC sources as of November 2026. Facts that could not be verified are marked `(unverified)` in the text. Have a *gestor* or *asesor fiscal* review a skill before relying on it in production.

## Checks

`python3 scripts/check_skills.py` validates frontmatter, reference links, contents indexes and every bold PGC account number against `data/pgc-2007-accounts.json`. It does not check whether the accounting is correct. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT. See [LICENSE](LICENSE).
