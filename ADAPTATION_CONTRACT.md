# Adaptation contract — HowToLiveBetter-CA

> **Status: DRAFT for review.** This contract governs how the China-source guide
> is rewritten for Canada. **No chapters have been written yet** — nothing in
> `book/` exists. The owner reviews this contract first; writing starts only after approval
> approves it (or approves with edits, which get logged in `docs/decisions.md`).
> Nothing here is published anywhere. No push to GitHub until the owner explicitly
> approves a release.

- **Source corpus:** `eternity4719/HowToLiveBetter` (Unlicense, public domain),
  34 chapters, **641 items** (A=425, B=165, C=51; full counts in `INVENTORY.md`).
  Local source copy: `~/workspace/how-to-live-better/book/`.
- **Target language:** English.
- **Target reader:** a Chinese-speaking newcomer living in Canada. The
  adaptation keeps the "here is the Chinese institution you're used to, here is
  what exists instead" framing where it prevents a real mistake — and deletes
  that framing where the source concept simply doesn't exist.
- **Budget:** $0. Sources are free official publications only.
- **Method base:** `adapting-evidence-based-life-guides` (madkoding/howtolivebetter-cl,
  Unlicense). The benefit-grading table in §5 is localized from its
  `references/item-format.md`; the validator is `scripts/verificar.py`.

---

## 1. Coverage map — what each source chapter becomes

Research completed 2026-09-30 (five primary-source passes, all in `research/`).
Chapters not listed here carry mostly **universal** items (health habits, sleep,
exercise, scams patterns) — they keep their items with portable international
evidence and only need Canadian numbers where a figure appears (e.g. food prices,
screening programs).

| Source chapter | Working title (EN) | Adaptation rule |
|---|---|---|
| 01 不要早死, 02 不要慢慢死, 03 不要浪费精力, 04 不要浪费时间 | Don't die young / Don't die slowly / Don't waste your energy / Don't waste your time | Mostly universal. Re-verify against `health-substitution.md` where a Canadian institution appears. |
| 05 不要浪费钱, 07 没钱的时候怎么活, 12 创业与做生意 | Money chapters | Full rewrite per §2.3. |
| 06 反面清单 | The blacklist | Universal logic; replace China-only examples. |
| 08 别把自己搭进去, 09 法律红线, 10 恋爱结婚, 11 程序员红线, 15 租房买房, 25 人走后 | Law chapters | Full rewrite per §2.5. |
| 13 紧急情况, 21 出国旅行与境外安全 | Emergencies chapters | Full rewrite per §2.1. |
| 14 账号与信息安全 | Accounts & infosec | Universal + CAFC row from §2.1. |
| 16 慢性病, 17 家里有老人, 18 养孩子, 20 刚出生的孩子, 22 怎么放松, 23 学什么技能, 24 看病, 26 网站平台, 27 怀孕和生产, 28 别为外形搞坏身体, 29 重大打击之后, 30 上学以后的孩子, 31 十八岁之后, 32 出国留学, 33 残疾之后, 34 家里常备药 | — | Universal, re-check via `health-substitution.md` for ch.24/16/20/27/33/34; ch.17 (8 items) and ch.18 (6 items) are **merge/expand candidates** — decide at contract review; ch.32 re-anchors to studying *in* Canada. |
| 19 在职离职和工伤, 31 灵活用工 | Work chapters | Full rewrite per §2.2. |

---

## 2. Bucket rules — the five domains

Each bucket below is a **closed rule system** from the 2026-09-30 research.
Writers work from these rules, not from memory of the Chinese original.

### 2.1 Emergencies (`research/emergencies-substitution.md`)

- **911** is the single number for police, fire, ambulance. China splits
  110/120/119 — Canada does not. 911 is emergencies only; non-emergency police
  lines are separate local numbers; **no text-to-911** in most areas.
- **988** is the suicide/crisis line (launched 2023-11-30, **EN/FR only** —
  trap for Chinese speakers). Kids Help Phone exists but was UNVERIFIED.
- **Poison:** 1-844-POISON-X (1-844-764-7669) nationally **except Quebec**,
  which is 1-800-463-5060 (Centre antipoison du Québec).
- **811** is non-urgent health advice; provincial variants exist (SK/MB
  versions UNVERIFIED).
- **Alert Ready** is the national emergency alert system; 72-hour kits are the
  standard preparedness unit.
- **Wildfire is provincial**, not federal: BC *5555, Quebec SOPFEU
  1-800-463-3389 (Alberta wildfire line UNVERIFIED).
- **Abroad:** Global Affairs Canada Emergency Watch, +1 613-996-8885;
  Registration of Canadians Abroad (ROCA); CBSA **CAN$10,000** cash-declaration
  threshold. CICC and dual-nationality wording UNVERIFIED.
- `none` (delete, do not force-fit): 应急管理部， 见义勇为 (as an institution).
- 14 UNVERIFIED items (see file) — none may enter `book/`.

### 2.2 Labour (`research/labour-substitution.md`)

- **Jurisdiction split is the first sentence of every labour item:** ~94% of
  employees are under **provincial** law (Ontario ESA / Quebec LNT); the
  federal Canada Labour Code Part III covers only federally regulated
  industries (banking, telecom, interprovincial/international transport,
  federal Crown corps, uranium mining) — ~6%, ~955,000 workers.
- **There is no general "written labour contract" requirement** (ON or QC).
  ESA/LNT minimums apply with or without a contract. Never port
  "no contract = illegal work".
- **No statutory probation.** Functional stand-in: Ontario ESA s.57 termination
  notice only applies after **3 months** of employment.
- Minimum wage (2026): federal $18.15/hr (2026-04-01); **Ontario $17.95/hr**
  (2026-10-01, was $17.60); **Quebec $16.60/hr** (2026-05-01). Always by
  province of work.
- Overtime thresholds differ: **Ontario 44h/week** at 1.5× (ESA s.22(1));
  **Quebec 40h** at +50%; federal 8h/day, 40h/week at 1.5×. Never merge.
- No-fault dismissal is **legal** with statutory notice/pay in lieu.
  Ontario: 1 week per year of service, max **8 weeks** (ESA s.57).
  Quebec (LNT art.82): <1yr → 1 week; 1–5yr → 2 weeks; 5–10yr → 4 weeks;
  10yr+ → 8 weeks.
- **Ontario severance pay** has a double gate: 5+ years **and**
  (employer global payroll ≥ $2.5M, or 50+ laid off in 6 months) → 1 week/year,
  max **26 weeks**. Quebec: **no statutory severance** (notice only).
- Vacation: Ontario 2 weeks (<5yr) / 3 weeks (5yr+), 4%/6% pay;
  **Quebec 3 weeks at 3 years** (not 5), 4%/6% (arts. 67–69, 74).
- Statutory holidays: Ontario **9** (Family Day, no St-Jean-Baptiste);
  Quebec **8** (St-Jean-Baptiste, no Family Day).
- Parental leave is **unpaid job protection**; the money comes from insurance.
  **Biggest trap in the book: Quebec residents get QPIP, not EI
  maternity/parental — and vice versa.** Ontario: pregnancy leave 17 weeks
  (after 13 weeks service), parental 61/63 weeks. Quebec: maternity 18 weeks,
  paternity 5 weeks (non-transferable), parental up to 65 weeks.
  EI (2026): 55%, cap **$729/week** standard / **$437/week** extended.
- **Non-compete split — write separately:** Ontario **bans** post-2021-10-25
  non-competes (ESA s.67.2, narrow exceptions); Quebec **allows** reasonable
  ones (CCQ art. 2089, UNVERIFIED text).
- Workplace injury: **WSIB (Ontario)** / **CNESST (Quebec)** — employer-funded,
  employee pays $0. Ontario LOE = **85% of net earnings difference**
  (WSIA s.43(2)); a 2026 government proposal to raise to 90% is **not law**.
  Quebec CNESST 2026 average rate $1.54/$100 payroll; claim within **6 months**.
- Sick leave: federal 10 paid days (CLC s.239); Ontario 3 **unpaid** (s.50,
  UNVERIFIED text); Quebec 26 weeks unpaid + first 2 days paid after 3 months
  (art.79.1, UNVERIFIED text).
- Discrimination: federal CHRA ss.7–10; Quebec **Charter art.10 — an exhaustive
  list** (no "etc."), plus art.18.1/18.2 on hiring questions and criminal
  records.
- `none` (delete): 劳动仲裁 (no arbitration commission — Ontario goes to the
  Ministry of Labour ESA claim/OLRB, Quebec to CNESST → TAT; **no
  arbitration-before-litigation requirement**), 五险一金 (unpack into
  CPP/QPP + provincial health + EI + WSIB/CNESST + no housing fund),
  试用期， 视同工伤， 劳动合同到期不续签.
- Hotlines: Ontario 1-800-531-5551 (UNVERIFIED — re-check before print),
  federal Labour Program 1-800-641-4049, CNESST 1-844-838-0808, EI
  1-800-206-7218.
- 13 UNVERIFIED items (see file) — none may enter `book/`.

### 2.3 Money & benefits (`research/money-substitution.md`)

- Tax filing: CRA T1 annually; **Quebec files twice** (federal T1 + provincial
  TP-1 to Revenu Québec). Federal BPA **$16,452** (2026); lowest marginal rate
  **14%** (Bill C-4, 2026 — **not 15%**); first bracket to **$58,523**.
  Mortgage interest on a principal residence is **not deductible**.
- RRSP 2026 cap **$33,810** (18% of prior-year earned income, less pension
  adjustment); TFSA 2026 **$7,000**/year. RRSP = deductible in / taxed out;
  TFSA = after-tax in / tax-free out.
- EI regular: 55%, 2026 MIE **$68,900**, max **$729/week**, 14–45 weeks,
  420–700 insurable hours; **employer must issue ROE** (electronic: 5 calendar
  days after pay period).
- CPP 2026: YMPE **$74,600**, YAMPE **$85,000**, rate **5.95%** (cap $4,230.45);
  max retirement at 65 **$1,507.65/month**; early −0.6%/month (max −36% at 60);
  late +0.7%/month (max +42% at 70). **QPP (Quebec): 6.3%** — separate row.
- OAS (2026 Q3): 65–74 **$751.97/month**, 75+ **$827.17/month**; full pension
  needs 40 years residence after 18 (min 10 years at 1/40); clawback starts at
  **$93,454** net income (2025). GIS single max **$1,123.17/month**.
- CCB (2026-07–2027-06): <$6 **$8,157/year**, 6–17 **$6,883/year**; full below
  **$38,237** family net income.
- ⚠️ **Naming trap: the GST/HST credit no longer exists.** Since July 2026 it
  is the **Canada Groceries and Essentials Benefit (CGEB)** — +25% over 5
  years, one-time 50% top-up 2026-06-05. Never write "GST/HST credit" as
  current.
- CWB (from July 2026): single max **$1,665**, family max **$2,869**.
  Ontario Works single max **$733/month**. Bank of Canada inflation target
  **2%** (1–3% band).
- `none` (delete): 住房公积金， 医保个人账户/家庭共济， 失信名单，
  信用卡透支利率上限， QDII/境外汇款额度， 就业困难人员认定，
  "¥120,000/¥400 no-filing threshold".
- 14 UNVERIFIED items (see file) — including all Quebec social-assistance
  2026 amounts (aide sociale / solidarité sociale / revenu de base):
  **re-check on quebec.ca before any of these enter `book/`.**

### 2.4 Health (`research/health-substitution.md`)

- Provincial plans, **no national card**: **OHIP** (Ontario, no waiting period
  since 2026), **RAMQ** (Quebec, up-to-3-month wait even for citizens).
  BC = balance + 2 months, Alberta = 3rd month of arrival.
- **Quebec: prescription drug insurance is mandatory** — public RAMQ plan or
  compliant private plan, no opting out (verbatim rule).
- 120 → **911**. 811 variants by province. Health Canada = drug/device
  regulator (NOC); PHAC = public health; NACI + provincial schedules for
  **free routine vaccines** (StatCan).
- Quebec: **$300 child eyewear** benefit. CDCP: household income **<$90,000**.
- `none` (delete): 挂号 (appointment/triage system), 分级诊疗 (tiered care),
  体检 (annual physical as a system), 120.
- 5 UNVERIFIED items (see file) — including Ontario ambulance fees
  ($45/$240, needs Reg. 552 text).

### 2.5 Law (`research/law-substitution.md`)

- **911** for police; **no 公安/派出所** — policing is municipal/provincial
  (OPP, Sûreté du Québec) or federal (RCMP, everywhere except ON/QC;
  contracts expire 2032-03-31).
- Fraud: **Criminal Code s.380** — the **$5,000** dividing line; 14 years max
  over $5,000; **2-year minimum** over $1 million.
- Sexual offences: **s.271** — up to 10 years (14 if complainant <16);
  summary max is now **two years less a day** (2026, c.19, s.29 — old guides
  say 18 months). Age of consent **16** (s.150.1, close-in-age exceptions;
  never under trust/authority/dependency). China's 14 does **not** transfer.
- Impaired driving: **s.320.14**, 80 mg/100 mL within 2 hours — **no
  饮酒/醉酒 two-tier**; provinces add administrative penalties below 80.
- Good Samaritan: Ontario **Good Samaritan Act, 2001 s.2(1)** protects
  volunteer rescuers from ordinary negligence (not gross negligence).
  **Quebec reverses it: Charter art.2 imposes a duty to rescue** — failing to
  help when you safely could is itself a violation.
- Protection: federal **s.810 peace bond** (fear on reasonable grounds,
  up to 12 months); Ontario FLA **s.46 restraining order** (2025 amendment
  **not in force** — do not cite); Quebec **ordonnance civile de protection**
  (C.p.c. art.509, form SJ-1318-2).
- Fraud reporting: **CAFC 1-888-495-8501** — collects intelligence, **does not
  investigate or recover money** (unlike China's 反诈中心）; also report to
  local police + Equifax/TransUnion.
- Border: **CBSA** examines (Border Watch 1-888-502-9060); **IRCC** issues
  documents — separate doors. Driver/vehicle: **ServiceOntario** (ON) /
  **SAAQ** (QC); Ontario plates renew automatically; Quebec plates stay with
  the vehicle; SAAQ fines are **not** payable at SAAQ points.
- Courts: **no 检察院** — Crown prosecutors (provincial AGs / PPSC / DPCP in
  Quebec); victims are witnesses, not parties.
- Small claims: **Ontario $50,000** (from 2025-10-01, O. Reg. 42/25 — most
  Chinese guides still say $35,000); **Quebec $15,000**.
- Legal aid is **provincial**: LAO (Ontario, income <$45,440 for 1–4-person
  families, assets <$15,000, 2025-03-31–2028); Quebec CSJ (single ≤$29,302/yr,
  2025-05-31 indexation; contributory stream $100–$800).
- **Quebec notaires** are the closest thing to 公证处 (authentic acts, wills,
  marriage contracts, can solemnize marriages); outside Quebec a "notary
  public" only witnesses signatures — **do not equate**.
- Marriage: **no 民政局**. Ontario = municipal **marriage licence**
  (expires in 3 months) + authorized officiant + 2 witnesses. Quebec =
  **20-day publication** of avis de mariage + authorized celebrant (notaries,
  mayors, even a designated friend) + ceremony within 3 months after day 20.
- Divorce: **Divorce Act (federal)** — court order only, **no 协议离婚**;
  1-year separation is the no-fault ground.
- Property: **Ontario FLA s.5 — equalization of net family properties**
  (value, not 50/50 title; **married spouses only**). **Quebec: patrimoine
  familial** (CCQ arts. 414–426, equal sharing of net value) + default
  **société d'acquêts** regime. ⚠️ **In both provinces, unmarried
  (common-law/de facto) partners get no property sharing and nothing on
  intestacy** — the single most dangerous trap for newcomer couples.
  (Quebec 2024 "union parentale" regime: exists, details UNVERIFIED.)
- Intestacy: Ontario preferential share **$350,000** (deaths on/after
  2021-03-01; + 1/2 or 1/3 of residue); Quebec: spouse takes 1/2 of family
  patrimony first, then **spouse 1/3 / children 2/3**.
- Limitation: Ontario **2 years from discovery** (Limitations Act, 2002 s.4);
  Quebec **3 years** (CCQ art. 2925). Sexual assault: Ontario no limitation
  (s.16(1)(h.1)); Quebec **30 years** (art. 2926.1).
- Rent: Ontario guideline **2.1% for 2026** (cap 2.5%; 90 days' notice;
  once/12 months) — **no cap on units first occupied after 2018-11-15**.
  Quebec TAL 2026: base **3.1%** (negotiation tool, not automatic).
- Credit: **no government-run credit system** — two private bureaus,
  **Equifax Canada and TransUnion Canada**; check both.
- Consumer: Ontario **Consumer Protection Ontario** 1-800-889-9768
  (**mediates**, cannot order refunds; the Consumer Protection Act, 2023 is
  **not in force** — cite the 2002 Act). Quebec **OPC** (licensing + enforcement).
- `none` (delete): 居委会/村委会， 妇联， 自首 (as a statutory concept —
  early guilty plea is only a common-law mitigating factor), 受案回执，
  国家赔偿 (as a general scheme), 民政局 marriage registration.
- 12 UNVERIFIED items (see file) — none may enter `book/`.

---

## 3. Master substitution table (China → Canada)

Condensed from the five research files. "Trap" = a near-equivalent that will
mislead a Chinese reader; these must be stated explicitly in the item's
`Notes`. Full citations live in `research/<domain>-substitution.md`.

| Chinese institution | Canada equivalent | Trap / Quebec difference |
|---|---|---|
| 110 / 120 / 119 | **911** (all three) | 911 emergencies only; no text-to-911 |
| 心理危机干预热线 | **988** (EN/FR only — trap for Chinese speakers) | Launched 2023-11-30 |
| 中毒急救 | 1-844-POISON-X; **Quebec: 1-800-463-5060** | — |
| 非急诊医疗咨询 | **811** (provincial variants) | SK/MB versions UNVERIFIED |
| 突发公共事件预警 | **Alert Ready**; 72-hour kits | — |
| 应急管理部 | **none** (wildfire is provincial: BC *5555, QC SOPFEU 1-800-463-3389) | — |
| 见义勇为 (institution) | **none**; Ontario Good Samaritan Act s.2(1) shields rescuers; **Quebec Charter art.2: duty to rescue** | QC reverses the rule |
| 境外求助 | GAC +1 613-996-8885, ROCA; CBSA CAN$10,000 declaration | CICC / dual-nationality wording UNVERIFIED |
| 12333 劳动热线 | ON 1-800-531-5551 (UNVERIFIED); federal 1-800-641-4049; QC CNESST 1-844-838-0808 | Re-check numbers at write time |
| 劳动合同 (mandatory written) | **none** — ESA/LNT minimums apply regardless | Never write "no contract = illegal" |
| 试用期 (statutory) | **none** — ON: s.57 notice only after 3 months | — |
| 最低工资 | Fed $18.15; **ON $17.95** (2026-10-01); **QC $16.60** (2026-05-01) | By province of work |
| 加班费 | ON 44h @1.5×; QC 40h @+50%; federal 8h/day 40h/week @1.5× | Never merge thresholds |
| 无故解雇违法 | **Legal** with statutory notice/pay in lieu | ON max 8 wks; QC scale 1/2/4/8 wks |
| N+1 经济补偿 | ON severance: 5yr **and** ($2.5M payroll or 50+ laid off), max 26 wks; **QC: none** | Common-law reasonable notice exists but needs a lawsuit |
| 带薪年假 | ON 2 wks (<5yr) / 3 wks (5yr+); **QC 3 wks at 3yr** | QC threshold is 3yr, not 5 |
| 法定节假日 | ON **9** (Family Day, no St-Jean); QC **8** (St-Jean, no Family Day) | — |
| 产假 (paid by employer) | **Unpaid job protection**; money from EI/QPIP | QC paternity 5 wks non-transferable |
| 生育津贴 | EI 55% cap $729/$437 (non-QC); **QC: QPIP only** | Biggest trap: EI↔QPIP are mutually exclusive |
| 五险一金 | **none** — unpack: CPP/QPP + provincial health + EI + WSIB/CNESST | No housing fund; group benefits are voluntary |
| 失业保险金 | EI regular 55%, $729/wk max, 14–45 wks; employer issues ROE | Voluntary quit/misconduct usually disqualifies |
| 工伤 | **WSIB** (ON, LOE 85% net) / **CNESST** (QC, employer-funded, claim ≤6 mo) | 90% proposal is not law |
| 劳动仲裁 | **none** — ON Ministry of Labour claim/OLRB; QC CNESST → TAT; no arbitration-first | Deadlines short (QC 45 days) |
| 竞业协议 | **ON: banned** (post-2021-10-25); **QC: allowed if reasonable** | Write separately — opposite rules |
| 病假 | Federal 10 paid; ON 3 unpaid; QC 26 unpaid + 2 paid | Do not merge |
| 个税汇算 | CRA T1; **QC files TP-1 too**; BPA $16,452; rate **14%** | No ¥120k/¥400 no-filing threshold |
| 专项附加扣除 (房贷利息) | **none** — principal-residence mortgage interest not deductible | — |
| 住房公积金 | **none** | FHSA/RRSP are voluntary savings, not 公积金 |
| 医保个人账户/家庭共济 | **none** | — |
| 个人养老金 | **RRSP** ($33,810) + **TFSA** ($7,000/yr) | Deduct-in/taxed-out vs tax-free |
| 职工养老保险 | **CPP** (5.95%, max $1,507.65/mo at 65) / **QPP** (6.3%) | Early −0.6%/mo, late +0.7%/mo |
| 基础养老金 | **OAS** 65–74 $751.97 / 75+ $827.17; 40yr residence = full; clawback $93,454 | Quarterly-indexed |
| 低收入老人补贴 | **GIS** single max $1,123.17/mo | Income-tested |
| 儿童福利 | **CCB** <$6 $8,157/yr; 6–17 $6,883/yr | Full below $38,237 family income |
| GST/HST credit | **CGEB** (renamed July 2026, +25%) | Never write "GST/HST credit" as current |
| 低收入工薪补贴 | **CWB** single $1,665 / family $2,869 | — |
| 低保 | **Ontario Works** $733/mo single (QC amounts UNVERIFIED) | No 户口-style threshold |
| 存款保险 ¥500k | **CDIC $100,000** per category per institution | Secondary-sourced — flag at write time |
| 失信名单 | **none** | — |
| 信用卡利率上限 | **none** | — |
| 省级医保卡/挂号/分级诊疗/体检 | **OHIP** (ON, no wait) / **RAMQ** (QC, ≤3-mo wait, mandatory drug insurance) | No 挂号/分级诊疗/体检 equivalents |
| 12315 | ON Consumer Protection Ontario 1-800-889-9768 (mediates only); QC **OPC** (enforces) | CPA 2023 not in force — cite 2002 Act |
| 96110 / 国家反诈中心 | **CAFC** 1-888-495-8501 — collects, **does not investigate/recover** | + local police + Equifax/TransUnion |
| 公安/派出所/交警/车管所 | Municipal/OPP/SQ/RCMP policing; **ServiceOntario** / **SAAQ** for licences | No single 公安； fines not payable at SAAQ |
| 检察院 | **none** — Crown prosecutors (DPCP in QC) | Victims are witnesses |
| 律师/12348 | **LAO** (ON) / **CSJ** (QC) — provincial, different thresholds | — |
| 公证处 | **QC notaires** (closest); rest of Canada "notary public" ≠ 公证处 | Do not equate |
| 民政局 (marriage) | **none** — ON licence + officiant; QC 20-day publication + celebrant | — |
| 协议离婚 | **none** — court order only (Divorce Act), 1yr separation | — |
| 夫妻共同财产 | ON **FLA s.5 equalization** (married only); QC **patrimoine familial** + société d'acquêts | **Unmarried partners: no sharing, no intestacy — in both provinces** |
| 法定继承 | ON $350,000 preferential share; QC spouse 1/3 / children 2/3 | Unmarried = nothing without a will |
| 诉讼时效 | ON **2yr** from discovery; QC **3yr** (art.2925) | Sexual assault: ON none / QC 30yr |
| 小额诉讼 | ON **$50,000** (2025-10-01); QC **$15,000** | Old guides say $35,000 — outdated |
| 征信系统 | **Equifax Canada + TransUnion Canada** (private) | Check both |
| 居委会/村委会/妇联 | **none** | — |
| 自首 | **none** as statutory concept (early plea = common-law mitigation only) | — |
| 受案回执/国家赔偿 | **none** (file number; Crown liability only) | — |

---

## 4. Item format (English)

Every item in `book/` is one Markdown file (or one section) carrying a
machine-readable cost tag followed by six fields. The validator
(`scripts/verificar.py`) enforces this; tag keys are English, positional,
exactly five — the parser depends on order and count.

### 4.1 Cost tag

`costs: money/time/willpower/benefit/dimension`

| Key | Values | Meaning (localized to Canada) |
|---|---|---|
| money | `0` / `low` / `high` | `0` free or saves money; `low` tens of dollars, or up to ~a day's wage per month; `high` tens of thousands of dollars or a significant recurring cost |
| time | `low` / `mid` / `high` | `low` minutes or incidental; `mid` hours once, or hours weekly; `high` daily |
| willpower | `no` / `some` / `yes` | `no` once and done; `some` change a habit or tolerate discomfort; `yes` fight an ingrained habit daily |
| benefit | `high` / `mid` / `low` | Assigned mechanically — see §5. Never by intuition. |
| dimension | `death` / `money` / `time` / `freedom` | What the item mainly buys back. Not comparable across dimensions. |

### 4.2 Fields

| Field | Content | Rules |
|---|---|---|
| `Cost` | What it takes from your pocket and your day | Concrete Canadian amounts **with the year**; time in minutes/days. Example: "$45 per ambulance ride in Ontario (2026)". |
| `In plain words` | 1–2 sentences translating `Benefit` for a non-statistician | No RR/HR/OR/CI/cohort/meta-analysis vocabulary. No number absent from `Benefit`/`Cost`. No hedging loss, no marketing words. Write for someone deciding in 5 seconds. |
| `Benefit` | The numbers, raw, with intervals | **Verbatim from the source.** Never "simplified". The validator diffs the number sets between this field and `In plain words` — a new number here is a new unsourced claim. |
| `Evidence` | `A`, `B`, `C`, or `X (disputed)` | Grading rules in §6. Disputed items keep both sides. |
| `Sources` | Primary sources with URLs | At least one URL per item; statute article numbers and DOIs where applicable. |
| `Notes` | Limits, who it applies to, traps, what it omits | Expected in practice. This is where jurisdiction ("Ontario only"), traps ("Quebec residents use QPIP, not EI"), and `UNVERIFIED` markers live. |

Body ≤ 10 lines beyond the tag; longer explanations go to a separate
long-read document under `docs/`.

### 4.3 Ordering

Within a chapter, order by value for money, highest first. Never publish a
ratio tier by hand — synthesize it from the benefit level plus the three cost
dimensions (that is how the search page does it), so ranking stays consistent
when an item is edited.

---

## 5. Mechanical benefit grading (localized thresholds)

Assigned from the item's own `Benefit` by threshold — **never by intuition**.
This keeps rankings comparable across hundreds of items written by different
people. When the numbers genuinely cannot decide it, judge and **write the
justification in `Notes`**; "not enough data" is not an acceptable reason alone.

| Dimension | `high` | `mid` | `low` |
|---|---|---|---|
| `death` | relative reduction ≥ 20% | 10–20% | < 10%, or surrogate endpoint only |
| `money` | ≥ **$50,000 CAD** cumulative | $5,000–$50,000 CAD | < $5,000 CAD |
| `freedom` | avoids a **criminal conviction** | avoids **detention or a fine** | avoids **civil litigation** |
| `time` | hours **daily** | hours **weekly** | **once** |

**Localization note (why money differs from the method's reference table):**
the reference table's money tiers (millions / hundreds of thousands / tens of
thousands) were scaled to its source economy. The CA edition uses cumulative
lifetime CAD: $50k+ (high) ≈ a year of maximum EI + a year of CCB-scale
benefits, i.e. life-changing money for a newcomer household; $5k–$50k (mid)
≈ a major one-time benefit (e.g. a year of OAS+GIS ≈ $22k); <$5k (low) ≈
routine savings and rebates. Documented here so the scale is auditable, not
felt.

---

## 6. Sourcing and evidence rules

1. **Primary sources only:** `canada.ca`, CRA/Service Canada/ESDC pages,
   `ontario.ca` / Ontario e-Laws, `quebec.ca` / `*.gouv.qc.ca` /
   `legisquebec.gouv.qc.ca`, `laws-lois.justice.gc.ca`, StatCan, CIHI, Bank of
   Canada. **Never** press, blogs, law-firm articles, or aggregators — they
   are leads, not sources.
2. **Every number carries a year** (e.g. "(2026)"). Quarterly-indexed figures
   (OAS/GIS/CPP amounts) carry the quarter too. **Every dollar figure is
   re-anchored at write time** — the research is dated 2026-09-30; amounts
   change (minimum wage, tax brackets, benefit caps).
3. **Statute sections are quoted verbatim** (English or French original).
   Article numbers must match the quoted text.
4. **Evidence grades:**
   - `A` — systematic reviews / meta-analyses / official statistics with
     published methodology (e.g. StatCan, CIHI, CRA tables).
   - `B` — single authoritative studies, government program rules stated as
     fact (most bureaucratic items: "EI pays 55%" is B, not A — it's a rule,
     not a finding).
   - `C` — expert consensus, official guidance without published data,
     reasonable inference clearly marked.
   - `X (disputed)` — keep both sides; the source had 4 such items
     (2×A, 1×B, 1×C).
5. **Portable international evidence is fine** where the mechanism is
   biological, not bureaucratic (the source already cites NHTSA, WHO, Lancet).
   Only the *institutional wrapper* gets replaced.
6. **B-heavy chapters need full re-verification:** ch.13 Emergencies is
   31/42 B — every item re-checked, no carry-over assumptions.

---

## 7. Federal-vs-provincial rule (with Quebec flags)

1. **Every chapter touching law, labour, tax, health, or benefits opens with
   a jurisdiction box:** federal baseline + "Ontario:" / "Quebec:" where they
   differ. ~94% of employees are provincially regulated; say so once per
   chapter, then mark the exceptions.
2. **Where Ontario and Quebec give opposite answers, write two items or one
   item with two clearly labelled halves — never one merged sentence.**
   Known opposites: non-compete clauses (banned vs allowed), vacation 3-week
   threshold (5yr vs 3yr), minimum wage, overtime threshold (44h vs 40h),
   severance (conditional vs none), drug insurance (voluntary vs mandatory),
   rescue (no duty vs duty), property on divorce (equalization vs patrimoine
   familial), small-claims limit ($50k vs $15k).
3. **Quebec is civil law; the rest is common law.** Never apply a common-law
   concept (e.g. "common-law marriage gives property rights") to Quebec, and
   never present a Quebec institution (notaire, TAL, CNESST) as Canada-wide.
4. **The EI/QPIP mutual-exclusion warning appears in every item that mentions
   parental/maternity benefits.** It is the highest-frequency trap in the book.
5. Hotline and agency phone numbers are **re-verified at write time** from the
   primary source — numbers change.

---

## 8. Hard prohibitions

1. **No translated statutes.** Quote the English or French original. A
   paraphrase is marked as paraphrase.
2. **No ported Chinese numbers.** A fine, a deadline, a benefit amount, a
   threshold from the Chinese original is deleted unless a Canadian primary
   source confirms an equivalent figure. "About the same" is not confirmation.
3. **Never invent a figure.** If the number isn't in a primary source, the
   item carries `UNVERIFIED` and does not enter `book/` (§9).
4. **No moralizing, no "you should".** Show cost and benefit; let the reader
   decide. Drop exclamation marks and decoration.
5. **No new numbers in `In plain words`.** The validator diffs number sets;
   a percentage invented for readability is a fabricated claim.
6. **`none` means none.** Where the research says no Canadian equivalent
   exists (五险一金， 劳动仲裁， 居委会， 民政局， 失信名单， …), the item is
   deleted or rewritten from scratch — never force-fit a lookalike.
7. **No Apply/click-bait patterns** — this guide informs; it never funnels
   readers to services. (No affiliate links, no "sign up here".)
8. **Grading by gut is forbidden** (§5). Intuition-based `high`/`low` will be
   caught at review; the threshold table is the only authority.

---

## 9. UNVERIFIED marker and verification log

- Any claim that could not be confirmed on a primary source is marked
  **`UNVERIFIED`** in the item's `Notes`, with the specific gap named
  (e.g. "`UNVERIFIED`: Quebec aide sociale 2026 monthly amount — quebec.ca
  page not found 2026-09-30").
- **UNVERIFIED items do not enter `book/`.** They wait in
  `docs/verification/` as one file per domain
  (`emergencies.md`, `labour.md`, `money.md`, `health.md`, `law.md`),
  each a checklist: claim → what was tried → what's missing → retry date.
- Counts from the 2026-09-30 research: emergencies **14**, labour **13**,
  money **14**, health **5**, law **12** — **58 total**.
  The single largest cluster is Quebec social-assistance 2026 amounts
  (aide sociale / solidarité sociale / revenu de base): **re-check quebec.ca
  before any of these enter `book/`.**
- A verification pass clears a marker only by citing the primary source;
  the log records the URL and date. `scripts/verificar.py --urls` probes
  every cited link; dead links fail the build.

---

## 10. Open decisions (for the owner at contract review)

1. **Thin chapters:** ch.17 (8 items, elderly parents) and ch.18 (6 items,
   having kids) are merge/expand candidates. Merge into neighbours, or expand
   with Canada-specific items (e.g. CCB, child-care benefit rules)?
2. **Disputed items (4):** keep the source's both-sides treatment, or drop?
3. **Release form:** GitHub repo + GitHub Pages (free), English only for v1?
   French/Chinese editions later?
4. **Custom domain** (~$20/yr, optional) — only cost in the whole project.

---

## 11. What "done" looks like

- [ ] This contract approved by the owner (decision logged in `docs/decisions.md`)
- [ ] All 58 UNVERIFIED items cleared or formally dropped
- [ ] 34 chapters in `book/`, every item with cost tag + six fields
- [ ] `scripts/verificar.py` exits 0 (structure) and `--urls` exits 0 (links)
- [ ] Quebec flags and EI/QPIP warnings present wherever required
- [ ] `docs/verification/` empty (all markers cleared)
- [ ] The owner approves the release; only then push to GitHub
