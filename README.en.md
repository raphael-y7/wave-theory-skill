<h1 align="center">Wave Theory Skill</h1>

<p align="center"><a href="README.md">中文</a> | English</p>

An AI skill pack for immediate use — it distills the wave counting, channel construction and exit rules from R. N. Elliott's *The Wave Principle (Professional Annotated Edition)* into 15 capability cards that can be triggered individually or combined.

It is not a book summary, nor a reading response — it breaks the reusable methodology in the book into skill modules that can be triggered, executed and tested.

## What these skills solve

- How many waves a rally has actually completed and whether it is time to leave: after wave 4, the final channel turns the wave-5 terminus into a geometric location you can restate, instead of a gut-feel top call
- You are already positioned and afraid of selling too early: six recursive holding rules drill down level by level (intermediate → minor → minute → subminute), and you do not sell until the fifth wave of the current degree is complete, confirmed by both a break of the upper channel line and same-degree record volume
- Whether a pullback is a zigzag, a flat or an irregular correction, and what the completed shape implies for the strength of the next move
- After a top, price falls and then makes a new high: is that a fresh advance or a wave-B trap (irregular top / failure), and which high is the orthodox top
- A large-degree decline has run for a year: which of the six bear-market stages are we in, and what confirmation does a long-term entry point need
- Whether this theory even applies to your instrument or this market regime: the five-condition gate plus a "count only in trending markets" filter keep you from forcing wave counts onto a range

## What was distilled

15 capability cards, organized in the order "pass the gate first, build the coordinates second, then locate the terminus and handle exceptions":

- **Preconditions and charting ground rules**: `applicability-gate-skill` (applicability gate and stance of use), `chart-rules-20` (the 20 chart rules checklist)
- **Wave counting and degree coordinates**: `wave-labeling-skill` (wave counting and nine-degree notation)
- **Terminus location and exit**: `wave-five-end-skill` (fifth-wave terminus and ending confirmation: three-step channel method plus a three-part evidence bundle), `recursive-hold-skill` (six recursive holding-and-selling rules)
- **Corrections and exceptional endings**: `correction-classifier-skill` (four-type correction classification and strength warning), `triangle-alternation` (triangles and the alternation rule), `extension-reversal` (extended waves and the two-reversal projection), `failure-irregular-top-skill` (failed fifths and irregular tops)
- **Bear-market diagnosis and entry**: `bear-diagnosis-skill` (bear-market stage diagnosis and long-term entry confirmation)
- **Second evidence chain and edge cases**: `volume-adjudication` (volume verification and ambiguity adjudication), `multi-timeframe` (timeframe selection and chart-scale rules), `cross-market-sync` (cross-market synchrony monitoring), `non-price-series` (three techniques for wave-ifying non-price series), `commentary-playbook` (the annotator's practical heuristics, Zhang Yibo — not Elliott's original text)

## Two packaging modes: single and pack

The same 15 capability cards are compiled twice, at two granularities. The content is identical; the only difference is how many entries an agent can discover.

| | single (one entry) | pack (compact pack, multiple entries) |
|---|---|---|
| Discoverable entries | **1**: `wave-theory-skill` | **8**: one source router + 7 promoted standalone skills |
| Where the 15 cards live | All inside the entry's `references/capabilities/`, loaded one at a time by the router table (at most two across domains) | 7 become standalone skills; the other 8 stay in the router's `references/` |
| Triggering | Only the entry description participates in matching; routing happens after entry | The 7 high-frequency capabilities are matched directly, one hop fewer |
| Upgrades | Replace 1 directory | Replace 8 directories |

The 7 cards promoted to standalone skills in the pack:

- `wave-five-end-skill` — fifth-wave terminus and ending confirmation (three-step channel method plus a three-part evidence bundle)
- `wave-labeling-skill` — wave counting and nine-degree notation
- `recursive-hold-skill` — six recursive holding-and-selling rules
- `correction-classifier-skill` — four-type correction classification and strength warning
- `failure-irregular-top-skill` — failed fifths and irregular tops
- `bear-diagnosis-skill` — bear-market stage diagnosis and long-term entry confirmation
- `applicability-gate-skill` — applicability gate and stance of use

### Which one to install

Pick by the way you work, and **install only one**:

| How you work | Recommended | Why |
|---|---|---|
| You use DSH / Codex / Claude Code with a skills directory and want a clean list | single | Takes 1 slot, loses no capabilities |
| Your daily questions concentrate on "count the waves / where does wave 5 end / should I sell / what correction is this / is that an irregular top / bear-market entry / does this theory even apply" | pack | Those 7 are exactly the promoted standalone skills, matched directly |
| You distribute to several agents or teammates who pick what they need | pack | They can install only the standalone skills they want |
| You want to install once and maintain one directory | single | Upgrades replace a single directory |

> Both builds come from the same bundle and carry identical capabilities. **Installing both will double-trigger**, so pick one.

## Examples

### Example 1: wave 4 just ended — frame the wave-5 terminus and the exit zone in advance

**User question**

"This rally has run a long time. I think waves 2, 3 and 4 are all done. Where does wave 5 end, and when should I clear out?"

**How the skill reasons**

- `wave-five-end-skill` starts with its input contract: instrument and operating degree, wave 1–4 pivots, high-low bar data, and chart scale (log for weekly, arithmetic for daily / 60-minute)
- Then the three-step construction: after wave 2, draw the base line from M to O and a parallel upper channel line through the wave-1 peak N; after wave 3 **discard the old channel regardless of whether it was touched, pierced or never reached**, and redraw the upper line through N–P with a parallel base line through O; after wave 4, connect O–Q as the base line and draw the parallel through the wave-3 peak P to get the final channel
- Wave 5 usually ends near that final upper channel line, and that landing zone is the exit decision area
- Then the three-part evidence bundle: did wave 5 pierce the upper channel line, did volume expand markedly on the break, and the reverse test — no break but a roll-over means a weakening warning

**Sample final answer**

> Settle the convention first, or the channel does not count: whether pivots are taken from closing prices or from highs/lows is undefined in the book, so pick one and remember which one you picked. Then confirm the wave 1–4 pivots are actually identifiable — if they are not, do not force the drawing. At your degree, the final channel is the base line through the wave-2 low O and the wave-4 low Q, with the parallel upper line through the wave-3 peak P; the wave-5 terminus zone sits along that band.
>
> But "near" is a qualitative word — the book gives no tolerance, so do not treat it as an exact sell order. To confirm the ending, check three things: one, did wave 5 pierce the upper channel line (large degrees must be verified on a log chart); two, did volume expand markedly on the break — the book only says a large-degree fifth wave prints volume greater than any earlier wave of the same degree, **it gives no multiple as a threshold, so you have to set that number yourself and write it into your plan**; three, if wave 5 never broke the line and rolled over instead, that is not a normal pause, it is a weakening warning, and the size of the coming correction scales with the degree.
>
> One more trap: breaking the line is not the same as an immediate top — the book says outright that sometimes the fifth wave does not end quickly near the breakout point, so dumping everything on the break misses the last leg. Scale out instead: trim the first tranche after the break plus record volume, and handle the rest with the recursive holding rules level by level. Also note that the book contains no stop-loss procedure and no magnitude algorithm at all; this is decision support, not a closed risk loop.

### Example 2: what kind of correction is this, and is the next move strong or weak

**User question**

"Price has fallen from the top, bounced once, then fell again. Is this a zigzag or a flat? Can it still go up after this?"

**How the skill reasons**

- `correction-classifier-skill` first runs a completeness check: if wave C has not unfolded and the starting point is not fixed, it **stops and refuses to classify** — the author himself says the shape and magnitude of a correction are very hard to forecast while it is forming, so this card is a post-completion warning device, not an ex-ante predictor
- Once the shape is complete, it reads only two relative positions: wave B against the correction's starting point (back to it / beyond it / short of it) and wave C against the wave-A low (new low / level / higher)
- Four outcomes: B clearly below the start and C a new low = zigzag; B back at the start and C level with A = flat; B beyond the start at a new high and C breaking A = irregular (1); B short of a new high and C not breaking A = irregular (2)
- Strength grading: zigzag = ordinary; flat = a longer, stronger move; a correction ending clearly above the wave-a low = super-strong. Bear-market rallies are graded on the same geometry mirrored: B losing the start and C failing = super-weak

**Sample final answer**

> Before answering "can it still go up", check whether your A-B-C is actually complete. If wave C is still falling and the low is not in, classifying now is jumping the gun — the author states that while a correction is forming it is very hard to predict its exact shape or amplitude, so this card is a warning device after completion, not an ex-ante bet.
>
> Assuming C is done, read only two things: whether wave B got back to the correction's starting point, and where wave C sits relative to the wave-A low. If B stayed clearly below the start and C made a new low, that is a zigzag and the following move is ordinary; if B returned to the start and C is roughly level with A, that is a flat, which the book says heralds "a longer period of strong movement".
>
> Two things must be said plainly. First, how to count "back to the start" or "a new low" is not quantified anywhere in the book — you have to agree on a convention beforehand. Second, for "flat = strong" the book can point to exactly one supporting case, the large-degree wave 4 of July 1933 to July 1934, and it is an ex-post label with no frequency statistics. So the strength grade is a warning reference only — not an amplitude forecast, not a price target, and not an entry instruction. And if the decline you are describing is a contracting triangle, that goes to the `triangle-alternation` card, not this four-type classification.

## How these skills were generated

This skill set was generated with the RIA-TV++ pipeline of **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)**, in six stages:

1. **Whole-book understanding (Adler analysis)** — Mortimer Adler's analytical reading method, decomposing the book in four steps: structural, interpretative, critical, applied
2. **Parallel extraction** — several specialized extractors (frameworks, principles, cases, counter-examples, terminology) run at once to pull candidate methodology units out of the source text
3. **Triple-verification screening** — every candidate must pass three tests: at least two independent in-book corroborations (cross-domain), the ability to answer a new question the book never states (predictive power), and not being common sense (distinctiveness)
4. **RIA++ construction** — structured along six dimensions: R (source quotation) / I (restatement in our own words) / A1 (in-book case) / A2 (future trigger scenario) / E (executable steps) / B (boundaries and blind spots)
5. **Zettelkasten linking** — dependency, contrast and combination relations between cards are mapped into a capability index and a routing table
6. **Trigger and output testing** — each card gets trigger blind tests (including decoy prompts: trigger when it should, stay silent when it should not) and output evaluation scenarios; failing cards go back for rework and then a regression pass

The hard part of distilling this book is keeping "what the author claims" separate from "how strong the evidence is": every wave label in the original is drawn on completed price action, and the promise of "forecasting down to the day and hour" is judged undeliverable by the annotator — so every card carries a boundaries-and-blind-spots section that puts "what the book says" and "how much to trust it" in two separate columns.

## Tests and verification

This repository ships the test material from the generation process: `evals/test-prompts.json` is the fixed case set, and `evals/test-results.md` is the item-by-item grading record — method, per-category pass counts and spot checks on execution quality, not a single line saying "all passed".

- **Blind-test method**: 3 independent sub-agents (T1/T2/T3, none involved in distillation) answered holding only the routing table and the relevant capability card; the main process graded against pre-set expectations
- **Actual case count in the case file**: `evals/test-prompts.json` holds 41 cases = 13 trigger + 7 decoy + 6 edge + 15 live execution
- **Per-category pass counts as recorded in the grading file** (quoted from `evals/test-results.md`): should_trigger 22 / 22, should_not_trigger 6 / 6 (zero false activations), edge_case 8 / 8, output_case 15 / 15
- **The counting discrepancy is stated as it is**: the grading record itself claims 39 total cases, while its four category counts add up to 51, and the case file shipped here holds 41. That is a difference in counting conventions in the source material; this repository has not reconciled, rewritten or inferred any pass rate from it
- **Failures and rework**: recorded as none. No expected answer was edited, and no case was dropped from the denominator
- **Quality spot checks**: one blind tester proactively found that the test data's "wave-4 low of 105 below the wave-1 peak of 110" violates the overlap rule, and declared the counting doubt in the deliverable instead of forcing the procedure; for an invalid count the tester gave a "reject" verdict alongside alternative options rather than a single answer

## Repository structure

```text
wave-theory-skill/
├── README.md                      ← you are here (Chinese)
├── README.en.md                   ← English version
├── LICENSE                        ← MIT
├── BOOK_OVERVIEW.md               ← whole-book understanding (Adler four-step breakdown, stage 0 output)
├── verified.md                    ← triple-verification conclusions: verified method units and evidence inventory
├── single/                        ← single-entry mode
│   └── wave-theory-skill/
│       ├── SKILL.md               ← entry: trigger conditions + routing table + loading rules
│       ├── BUILD_MANIFEST.json    ← build manifest and file hashes
│       └── references/
│           ├── overview.md        ← whole-book overview
│           ├── capability-index.md  ← full intent and keyword index (all 15 cards registered)
│           ├── cheatsheet.md      ← decision-rule quick reference
│           ├── glossary.md        ← glossary
│           └── capabilities/      ← the 15 capability cards
├── pack/                          ← multi-entry mode (compact pack)
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── wave-theory-skill-router/
│   │   ├── SKILL.md               ← source routing entry
│   │   └── references/            ← the 15 cards + index, called internally by the router
│   ├── wave-five-end-skill/
│   │   └── SKILL.md
│   ├── wave-labeling-skill/
│   │   └── SKILL.md
│   ├── recursive-hold-skill/
│   │   └── SKILL.md
│   ├── correction-classifier-skill/
│   │   └── SKILL.md
│   ├── failure-irregular-top-skill/
│   │   └── SKILL.md
│   ├── bear-diagnosis-skill/
│   │   └── SKILL.md
│   └── applicability-gate-skill/
│       └── SKILL.md
└── evals/                          ← trigger blind tests and output evaluation material
    ├── test-results.md             ← per-item grading and quality spot checks
    └── test-prompts.json           ← the 39 fixed cases (trigger / decoy / edge / execution)
```

## How to use

Clone the repository first:

```bash
git clone https://github.com/raphael-y7/wave-theory-skill.git
```

### Install single (try this one first)

```bash
# macOS / Linux
cp -r wave-theory-skill/single/wave-theory-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\wave-theory-skill\single\wave-theory-skill "$env:USERPROFILE\.agents\skills\"
```

### Install pack

Copy only the directories that contain `SKILL.md`, and do not copy the two json files under `pack/` into your skills directory:

```bash
# macOS / Linux
cd wave-theory-skill/pack
cp -r wave-theory-skill-router \
      wave-five-end-skill \
      wave-labeling-skill \
      recursive-hold-skill \
      correction-classifier-skill \
      failure-irregular-top-skill \
      bear-diagnosis-skill \
      applicability-gate-skill ~/.agents/skills/
```

```powershell
# Windows
$pack = ".\wave-theory-skill\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('wave-theory-skill-router','wave-five-end-skill','wave-labeling-skill','recursive-hold-skill','correction-classifier-skill','failure-irregular-top-skill','bear-diagnosis-skill','applicability-gate-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` is the DSH skills directory; with another agent, use that agent's own skills directory (Claude Code, for example, uses `~/.claude/skills`).

### How to confirm it is installed

Ask "wave 4 is done — draw the channel and give me the wave-5 terminus and the exit zone", and see whether the agent goes straight into the three-step channel construction and the evidence bundle, instead of handing you a generic "watch your risk and position sizing". With single installed it reads the entry first and then routes to a card; with pack installed, `wave-five-end-skill` is matched directly by its description.

## Source

- *The Wave Principle (Professional Annotated Edition)* by Ralph Nelson Elliott (US), translated by Duan Huiqing, annotated by Zhang Yibo; original edition 1938, Chinese edition published by Posts & Telecom Press (Century Classics of Stock Investing series)
- The whole book yields 15 capability cards
- The original sample is US equities from 1854 to 1938, concentrated in the Dow Jones Industrial Average of 1921–1938; there is not a single A-share case. Migrating to A-shares requires re-calibrating degree correspondence, volume conventions and the T+1 rule yourself
- Annotator material (Zhang Yibo's views inside the `commentary-playbook` card and the passages marked 【点评】 in other cards) is not Elliott's original text; each item is tagged with its source level inside the card

## Disclaimer

This repository publishes only the distilled skills, indexes and rule quick-reference material. It contains no PDF, EPUB, OCR files, screenshots or full-book transcript of the original. Quotations inside the capability cards serve only to attribute methodology and keep it auditable.

All numeric criteria in the book (the tolerance of "near" in channel work, record-volume multiples, correction-classification boundaries, the 7% turnover figure and so on) are case-based and empirical generalizations; the original provides no statistical backtesting, and many thresholds are not given in the book at all. Test them on your own instrument and declare the convention you use. Nothing in this repository constitutes investment advice.

## License

[MIT](https://opensource.org/licenses/MIT)
