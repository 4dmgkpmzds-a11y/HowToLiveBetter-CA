# Source inventory — HowToLiveBetter (China) → HowToLiveBetter-CA

Source: `eternity4719/HowToLiveBetter` (Unlicense, public domain), shallow-cloned 2026-09-30.
Local copy of the source corpus: `~/workspace/how-to-live-better/book/`.

**Totals: 34 chapters, 641 items.**
- Evidence grades: A = 425 (incl. 2 disputed), B = 165 (incl. 1 disputed, 1 special), C = 51 (incl. 1 disputed).
- Every item (641/641) carries the machine-readable cost tag; item numbering is contiguous
  (1…N) in every chapter; every item has all six fields.

## Per-chapter counts

| # | Source chapter (CN) | Working title (EN) | Items | A | B | C |
|---|---|---|---|---|---|---|
| 01 | 不要早死 | Don't die young | 38 | 27 | 11 | 0 |
| 02 | 不要慢慢死 | Don't die slowly | 42 | 32 | 10 | 0 |
| 03 | 不要浪费精力 | Don't waste your energy | 25 | 5 | 17 | 3 |
| 04 | 不要浪费时间 | Don't waste your time | 18 | 4 | 12 | 2 |
| 05 | 不要浪费钱 | Don't waste your money | 45 | 24 | 10 | 11 |
| 06 | 反面清单 | The blacklist (seems smart, isn't) | 28 | 15 | 10 | 3 |
| 07 | 没钱的时候怎么活 | How to live when you're broke | 21 | 15 | 5 | 1 |
| 08 | 别把自己搭进去 | Don't get entangled (trouble with others) | 44 | 34 | 9 | 1 |
| 09 | 普通人容易踩的法律红线 | Legal red lines ordinary people cross | 23 | 22 | 1 | 0 |
| 10 | 恋爱和结婚划不划算 | Dating and marriage: is it worth it | 20 | 13 | 6 | 1 |
| 11 | 程序员和技术人容易踩的红线 | Red lines for tech workers | 17 | 12 | 4 | 1 |
| 12 | 创业与做生意 | Starting and running a business | 23 | 18 | 3 | 2 |
| 13 | 紧急情况 | Emergencies: what to do first | 42 | 8 | 31 | 3 |
| 14 | 账号与信息安全 | Accounts and information security | 9 | 5 | 0 | 4 |
| 15 | 租房与买房 | Renting and buying a home | 9 | 8 | 0 | 1 |
| 16 | 得了慢性病之后怎么活 | Living with a chronic disease | 9 | 7 | 0 | 2 |
| 17 | 家里有老人 | Elderly parents at home | 8 | 4 | 2 | 2 |
| 18 | 养孩子划不划算 | Having kids: is it worth it | 6 | 3 | 0 | 3 |
| 19 | 在职离职和工伤 | Jobs, dismissal, and work injuries | 17 | 13 | 2 | 2 |
| 20 | 刚出生的孩子怎么带 | Caring for a newborn | 12 | 8 | 2 | 2 |
| 21 | 出国旅行与境外安全 | Travelling abroad and staying safe | 11 | 8 | 0 | 3 |
| 22 | 怎么放松 | How to rest | 11 | 10 | 1 | 0 |
| 23 | 学什么技能划算 | Which skills are worth learning | 23 | 17 | 4 | 2 |
| 24 | 看病 | Seeing a doctor | 12 | 12 | 0 | 0 |
| 25 | 人走了以后要办什么 | What to do when someone dies | 10 | 10 | 0 | 0 |
| 26 | 做一个网站或平台 | Running a website or platform | 11 | 10 | 0 | 1 |
| 27 | 怀孕和生产 | Pregnancy and childbirth | 16 | 15 | 1 | 0 |
| 28 | 别为了外形把身体搞坏 | Don't wreck your health for looks | 8 | 5 | 3 | 0 |
| 29 | 遭遇重大打击之后 | After a hard blow | 13 | 9 | 3 | 1 |
| 30 | 上学以后的孩子 | School-age children | 15 | 6 | 9 | 0 |
| 31 | 十八岁之后有哪几条路 | Paths after 18 | 16 | 16 | 0 | 0 |
| 32 | 出国留学 | Studying abroad | 10 | 10 | 0 | 0 |
| 33 | 残疾之后怎么活 | Living with a disability | 20 | 17 | 3 | 0 |
| 34 | 家里的常备药别吃出事 | The home medicine cabinet: don't poison yourself | 9 | 3 | 6 | 0 |
| | **Total** | | **641** | **425** | **165** | **51** |

## Real item schema (extracted, not assumed)

Heading: `### N. <verb-first imperative>` — numbering restarts per chapter, contiguous from 1.

Cost tag (mandatory, first non-empty line after the heading, invisible on GitHub):

```html
<!-- 成本标签: 钱=0 时间=少 毅力=否 收益=大 口径=死亡率 -->
```

Observed vocabulary (all 641 items):

| Key (CN) | EN meaning | Values (count) |
|---|---|---|
| 钱 | money | `0` (512) · `少` low (103) · `多` high (26) |
| 时间 | time | `少` low (503) · `中` mid (112) · `多` high (26) |
| 毅力 | willpower | `否` no (331) · `些` some (261) · `是` yes (49) |
| 收益 | benefit | `大` high (342) · `中` mid (261) · `小` low (38) |
| 口径 | dimension | `金钱` money (239) · `死亡率` mortality (218) · `自由` freedom (109) · `时间` time (75) |

Fields, in fixed order (all present in every item):

1. `成本` — Cost: what it takes from pocket and day (local amounts with year).
2. `说人话` — Plain-language line: benefit restated for a non-statistician.
3. `收益` — Benefit: raw numbers with intervals, verbatim from source.
4. `证据等级` — Evidence grade: `A`, `B`, `C`, with rare variants `A（争议）` (2),
   `B（争议）` (1), `C（争议）` (1), `B（指南强推荐，但底层证据等级低）` (1).
5. `来源` — Sources: primary sources with URLs (DOIs, WHO/NHTSA publications,
   Chinese statutes with article numbers).
6. `备注` — Notes (optional in spec, present in practice): limits, applicability,
   disputes, pending-verification notes.

Body is short (≤ ~10 lines beyond the tag); longer explanations live in `docs/`.

## Notes for the adaptation

- The most country-specific chapters (heaviest replacement load): 07, 08, 09, 10, 15,
  19, 24, 25 — laws, benefits, procedures, agencies.
- The most portable chapters (mostly universal evidence): 01, 02, 22, 27, 31, 32.
- Chapter 13 (emergencies) is B-heavy (31/42): procedural, needs full re-verification
  against Canadian sources, not just re-grading.
- Thin chapters (17, 18 — 8 and 6 items) are candidates for merging or expansion
  during adaptation; volume is not a goal.
- Disputed-grade items (4 total) must carry their counter-evidence into the CA version.
- The source already cites international evidence (NHTSA, WHO, Lancet) in health
  chapters — those items port with numbers intact; only the China-specific
  prevalence/context lines get replaced.
