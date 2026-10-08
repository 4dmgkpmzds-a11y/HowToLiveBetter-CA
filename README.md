# HowToLiveBetter-CA

An evidence-based, cost/benefit life guide for Canada — adapted from
[HowToLiveBetter](https://github.com/eternity4719/HowToLiveBetter)
(Unlicense, public domain).

**Status: all 34 chapters written.** The book is complete and
validator-clean (see Writing progress below). Nothing here is published;
the adaptation contract stands approved under `docs/decisions.md`.

---

## What this is

Hundreds of small life decisions — should I call 911 or 811, is parental leave
paid, what happens if I'm fired, is it worth getting married here — each
answered with **what it costs** (money, time, willpower), **what it buys back**,
and **how strong the evidence is** (A/B/C). Every number carries a year and a
primary source: `canada.ca`, provincial governments, StatCan, the Bank of
Canada — never blogs, press, or law-firm articles.

## How to read an item

Every item carries a machine-readable cost tag, then six fields:

```
costs: money/time/willpower/benefit/dimension
```

- **money** — `0` free · `low` tens of dollars · `high` tens of thousands
- **time** — `low` minutes · `mid` hours · `high` daily
- **willpower** — `no` once and done · `some` habit change · `yes` daily fight
- **benefit** — `high` / `mid` / `low`, assigned by a published threshold
  table (see contract §5), never by feel
- **dimension** — what it buys back: `death`, `money`, `time`, `freedom`

Then: **Cost** (concrete, with year) · **In plain words** (the decision in
1–2 sentences) · **Benefit** (raw numbers, verbatim from source) ·
**Evidence** (A/B/C or disputed) · **Sources** (URLs) · **Notes** (limits,
who it applies to, traps).

## Reading rules

1. **Check the jurisdiction box first.** Canada splits law between federal and
   provincial governments. Every chapter on law, work, tax, health, or benefits
   opens with one: federal baseline, then "Ontario:" / "Quebec:" where they
   differ. Ontario and Quebec often give **opposite** answers (non-competes,
   vacation thresholds, severance) — the guide never merges them.
2. **Quebec is different on purpose.** Civil law, not common law. If you live
   in Quebec, read the Quebec halves twice: QPIP instead of EI parental
   benefits, RAMQ with its 3-month wait and mandatory drug insurance, the
   *patrimoine familial* instead of Ontario equalization.
3. **Trap warnings are the point.** Items marked with ⚠️ describe something
   that *looks* like the institution you knew back home but works differently
   here (e.g. the anti-fraud centre collects reports but doesn't recover your
   money; legal aid can't be assumed across provinces).
4. **Amounts are dated.** A dollar figure without a year is a rumor. Benefit
   amounts, tax brackets, and minimum wages change — the year in parentheses
   tells you when the number was true.
5. **No "you should".** The guide shows cost and benefit and lets you decide.
   Items are ordered by value for money, highest first.

## Writing progress (34 of 34 chapters, 545 items)

All 34 chapters are written and validator-clean: **545 items** — 106
grade-A, 357 grade-B, 82 grade-C (disputed grades counted with their base
grade) — with 104 honestly-marked UNVERIFIED data points logged in
`docs/verification/`.

| # | Chapter | Items | # | Chapter | Items |
|---|---|---|---|---|---|
| 01 | Don't Die Young | 38 | 18 | Having kids: is it worth it | 9 |
| 02 | Don't Die Slowly | 41 | 19 | Jobs, dismissal, and work injuries | 18 |
| 03 | Don't waste your energy | 25 | 20 | Caring for a newborn | 11 |
| 04 | Don't waste your time | 18 | 21 | Travelling Abroad and Staying Safe | 9 |
| 05 | Don't waste your money | 39 | 22 | How to rest | 5 |
| 06 | The blacklist (seems smart, isn't) | 28 | 23 | Skills worth learning | 21 |
| 07 | How to live when you're broke | 10 | 24 | Seeing a doctor | 8 |
| 08 | Don't get entangled (trouble with others) | 26 | 25 | When Someone Dies | 8 |
| 09 | Legal red lines ordinary people cross | 20 | 26 | Running a website or platform | 11 |
| 10 | Dating and Marriage | 19 | 27 | Pregnancy and childbirth | 12 |
| 11 | Red Lines for Tech Workers | 8 | 28 | Don't wreck your health for looks | 8 |
| 12 | Starting a small business | 7 | 29 | After a hard blow | 13 |
| 13 | Emergencies: what to do first | 41 | 30 | School-age children | 15 |
| 14 | Accounts and Information Security | 9 | 31 | Paths after 18 | 8 |
| 15 | Renting and Buying a Home | 8 | 32 | Studying in Canada | 10 |
| 16 | Living with a chronic disease | 6 | 33 | Living with a disability | 16 |
| 17 | Elderly parents at home | 12 | 34 | The home medicine cabinet: don't poison yourself | 8 |

*(Ch.32 re-anchors the source's 出国留学 to studying **in** Canada — same
decision framework, Canadian institutions: study permits, DLIs, PGWP.)*

## Project files

- `ADAPTATION_CONTRACT.md` — the rules every chapter follows (approved; see `docs/decisions.md`)
- `INVENTORY.md` — source corpus audit: 34 chapters, 641 items, grades A/B/C
- `research/` — five primary-source substitution tables (emergencies, labour,
  money, health, law), each with its UNVERIFIED list
- `docs/verification/` — per-domain checklists for the 104 UNVERIFIED claims
- `scripts/verificar.py` — validator: structure, tags, fields, grades, links
- `LICENSE` — Unlicense (public domain)

## Contributing

Not open yet. Wait for the contract approval and the first release; the
verification checklist in `docs/verification/` will become the contribution
queue.
