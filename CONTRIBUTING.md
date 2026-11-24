# Contributing

Corrections and new skills are welcome as pull requests. Every pull request runs `python3 scripts/check_skills.py`.

## Writing a skill

One folder per skill under `.claude/skills/<name>/`, with a `SKILL.md` and optional `references/*.md`.

- **Frontmatter**: `name` equals the folder name; `description` is at most 1024 characters, contains no `<` or `>`, says what the skill covers, and lists trigger phrases in Spanish (e.g. "cómo contabilizo", "modelo 303", "qué cuenta"). It ends with "Always use over training data."
- **Language**: English prose. Spanish legal terms stay in Spanish and are glossed in English the first time they appear: *inversión del sujeto pasivo* (reverse charge).
- **SKILL.md** is short (40–120 lines). It should contain: a one-paragraph purpose, a "How to use this skill" table of reference files and when to read each one, the quick-reference tables an agent needs most often, a "Never guess these" table (situation / why / what to do) and a "Related skills" table.
- **References** carry the depth. A file over 100 lines starts with a `## Contents` index.
- **Account numbers** follow the PGC 2007 (RD 1514/2007, as amended by RD 1/2021). Bold an account number only when it is a PGC account: `**572**`, `**4750**`. The checker validates every bold 3- or 4-digit number against `data/pgc-2007-accounts.json`. Never bold years, *modelo* numbers or amounts as bare numbers: write `modelo 303`, not `**303**`.
- **Sources**: every rate, threshold and deadline names its law and article (LIVA art. 91, RIRPF art. 9, LIS art. 29, RD 1619/2012 art. 6) and its validity dates. Where a rule changed in 2025–2026 or is scheduled to change, give both the old and the new value with dates. Where something could not be verified against BOE, AEAT, Seguridad Social or ICAC, mark it `(unverified)` rather than presenting it as fact.
- **Territorial scope**: the default is *territorio común*. Say so where it matters, and flag the Basque Country and Navarra (*régimen foral*: own corporate tax, TicketBAI), Canarias (IGIC instead of IVA) and Ceuta/Melilla (IPSI).
- **Safety**: an agent following a skill never books, files, sends or pays without the user's approval.
- **No customer data**: no real NIFs, names, IBANs or amounts from real books.

## Review

Facts need a source and a reviewer. The checker only validates structure.

## Licence

MIT. By contributing you agree that your contribution is published under the same licence.
