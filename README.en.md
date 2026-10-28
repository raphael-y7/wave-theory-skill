<h1 align="center">Wave Theory Skill</h1>

<p align="center"><a href="README.md">中文</a> | English</p>

An AI skill pack for immediate use — it distills the wave-reading methods from Ralph Nelson Elliott's *The Wave Principle* into 15 capability cards that can be triggered individually or combined.

It is not a book summary, nor a reading response — it breaks the reusable methodology in the book into skill modules that can be triggered, executed and tested.

## What these skills solve

- A big advance is running and you cannot say where to sell — the book says "where wave 5 ends decides when investors close and how much they keep", but how to draw the upper channel line, whether a break of it is a top, and how much volume counts as expanded, all have to be put on your own chart
- Your wave count yields several self-consistent alternatives and you cannot tell which to trust — nor how to notice a wrong count (the book has no correction procedure, so the cards stop and show the disagreement honestly)
- A correction has finished and you dare not build a position: is it a zigzag, a flat or an irregular, and what does it warn about the strength of the next move?
- Price makes a new high after your top exit and you cannot tell recovery from a wave-B trap; or the fifth wave never takes out the prior high and you do not know whether to sell at once
- In a bear market you cannot place the current stage and keep buying halfway down; or you hold a position and fear getting off too early, with no "do not sell before the fifth wave" ladder
- You are tempted to apply a book written on 1930s US stocks to today's range-bound markets, illiquid stocks or non-price data — with no gate asking whether wave theory even applies to that instrument

## What was distilled

15 capability cards, organized in the order "pass the gate first, fix the coordinates second, judge the endpoint third, manage the position last":

- **Applicability and charting foundations** (3 cards): `applicability-gate-skill` (applicability gate and stance: the five completeness conditions, trend-market limitation, right-side confirmation), `chart-rules-20` (the 20-rule wave-chart checklist), `multi-timeframe` (multi-timeframe matrix and logarithmic vs arithmetic scale rules)
- **Wave-count coordinate system** (1 card): `wave-labeling-skill` (nine degrees of labeling, subwave decomposition, the slant rule as a validity check)
- **Endpoint location and exit** (4 cards): `wave-five-end-skill` (three-step channel method plus the break/volume/irregular-top triple confirmation), `extension-reversal` (identifying extensions and projecting the two reversals), `failure-irregular-top-skill` (failed fifth and irregular tops: orthodox top vs highest price), `volume-adjudication` (volume verification and resolving pattern ambiguity)
- **Corrections and pattern classification** (2 cards): `correction-classifier-skill` (four-way correction classification and strength warning), `triangle-alternation` (triangle rule set and the alternation rule)
- **Holding and building positions** (2 cards): `recursive-hold-skill` (the six recursive hold/sell rules), `bear-diagnosis-skill` (bear-market stage diagnosis and long-term entry confirmation)
- **Transfer and commentary** (3 cards): `cross-market-sync` (cross-market and cross-series synchrony monitoring), `non-price-series` (three ways to wave-ify non-price series), `commentary-playbook` (the commentator's practical heuristics, not Elliott's own text)

## Two packaging modes: single and pack

The same 15 capability cards are compiled twice, at two granularities. The content is identical; the only difference is how many entries an agent can discover.

| | single (one entry) | pack (compact pack, multiple entries) |
|---|---|---|
| Discoverable entries | **1**: `wave-theory-skill` | **8**: one source router + 7 promoted standalone skills |
| Where the 15 cards live | All inside the entry's `references/capabilities/`, loaded 1–2 at a time by the routing table | 7 high-frequency cards become standalone skills; the other 8 stay in the router's `references/` |
| Triggering | Only the entry description participates in matching; routing happens after entry | The 7 high-frequency capabilities are matched directly, one hop fewer |
| Upgrades | Replace 1 directory | Replace 8 directories |

The 7 cards promoted to standalone skills in the pack:

- `wave-five-end-skill` — fifth-wave endpoint and exit timing
- `wave-labeling-skill` — wave counting and nine-degree labeling
- `recursive-hold-skill` — recursive holding and selling rules
- `correction-classifier-skill` — four-way correction classification and strength warning
- `failure-irregular-top-skill` — failed fifth and irregular tops
- `bear-diagnosis-skill` — bear-market stages and entry points
- `applicability-gate-skill` — the applicability gate and stance

### Which one to install

Pick by the way you work, and **install only one**:

| How you work | Recommended | Why |
|---|---|---|
| You use DSH / Codex / Claude Code with a skills directory and want a clean list | single | Takes 1 slot, loses no capabilities |
| Your daily questions concentrate on "count this wave / where does wave 5 end / should I sell / what kind of correction is this / is this the real top" | pack | Those are exactly the 7 promoted standalone skills, matched directly |
| You distribute to several agents or teammates who pick what they need | pack | They can install only the standalone skills they want |
| You want to install once and maintain one directory | single | Upgrades replace a single directory |

> Both builds come from the same bundle and carry identical capabilities. **Installing both will double-trigger**, so pick one.

## Examples

### Example 1: waves 2 to 4 are complete — how do I fix the exit point?

**User question**

"This rally has run for almost half a year and waves 2, 3 and 4 are done. How do I judge when wave 5 ends, and should I sell?"

**How the skill reasons**

- First `applicability-gate-skill`: the instrument must meet the five completeness conditions (widely held, public market, reliable data, available information, chartable) and be in a trending market — the book explicitly limits wave counting in range-bound markets
- Then `wave-five-end-skill`: confirm the input contract (instrument and operating degree, whether waves 1–4 turning points are identifiable, a high/low bar chart, logarithmic scale for weekly and arithmetic for daily), then run the three channel steps — after wave 4, draw the base line through the wave 2 and wave 4 endpoints and a parallel upper channel line through the wave 3 peak; wave 5 usually ends near that line
- Layer on the triple confirmation: does wave 5 pierce the upper channel line (verify on a log chart for large degrees), does volume expand abnormally on the break (it should exceed any wave of the same degree before it), and the reverse case — failing the line and rolling over means a "weakening" warning
- A holder then uses `recursive-hold-skill` to drill down degree by degree until the innermost fifth wave is exhausted
- Stop conditions: if wave 5 subdivides into five subwaves (an extension) → switch to `extension-reversal`; if wave 5 fails to make a new high → switch to `failure-irregular-top-skill`

**Sample answer**

> Declare the convention first, because the book does not define it and you must: do turning points use closing prices or highs/lows? That choice moves the channel landing zone, and either is fine as long as the whole count uses one. On scale, weekly goes logarithmic and daily arithmetic. Then draw the three steps: the base line through the wave 2 and wave 4 endpoints, a parallel upper channel line through the wave 3 peak — wave 5 will most likely end near that line. That is an exit decision zone, not a precise sell price; the book only says "near", with no quantified tolerance. To confirm the end, read three pieces of evidence together: whether wave 5 pierced the upper channel line (this is a large degree, so re-check on a log chart), whether volume on the break exceeded any wave of the same degree before it, and if it failed the line and rolled over, that is only a weakening warning — reduce, do not liquidate. How much expansion counts as a volume climax has no threshold in the book; you must set that number yourself and write it into the plan. If wave 5 subdivides into five subwaves it is an extension, and an extension is never the end of the move — switch to the two-reversal projection. If wave 5 never made a new high it is a failed fifth: sell near point B, do not wait for a channel break.

### Example 2: a new high after the top exit — recovery or a wave-B trap?

**User question**

"I already sold at the top, and now it has made a new high. Is the trend back? Should I chase it?"

**How the skill reasons**

- Stop before `failure-irregular-top-skill`: a new high after the top may be wave B, or an extension still forming. Until that ambiguity is resolved the card must not be applied; go to `volume-adjudication` first (shrinking volume favours irregular B, expanding volume favours an extension)
- Once adjudicated as an irregular top, run the three steps of `failure-irregular-top-skill`: wave A = the first pullback low after the top; a rebound above the orthodox top (OT) confirms wave B, labeled "highest price = B, real top = OT"; wave C then unfolds downward in five waves
- Downside target: near the start of the fifth primary wave of the prior advance (a structural reference — the book gives no magnitude formula, and the output must say so)
- Stop conditions: if the rebound never cleared OT it is not an irregular top, so switch to `wave-five-end-skill` for the regular endpoint test; if OT's price and date are missing, ask rather than guess

**Sample answer**

> Do not chase yet. A new high after the top has only two readings, and volume adjudicates first: a new high on shrinking volume leans irregular B (that high is just wave B), a new high on expanding volume leans extension. Assuming an irregular top, your real top has not moved — it is the earlier orthodox top OT, and this new high is only wave B. The book warns that an irregular top from OT to B foreshadows a violent decline, with wave C then unfolding downward in five waves. The target it gives is structural: near the start of the fifth primary wave of the prior advance, not a price computed from a magnitude rule. So the right action is not to chase — either stay flat until wave C completes, or use `bear-diagnosis-skill` to place the current bear-market stage. If, on the other hand, the rebound never cleared OT, this is not an irregular top and you go back to the regular endpoint test. One caveat: without OT's price and date this step cannot be done, so find those two numbers first.

## How these skills were generated

These skills were produced with the **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** RIA-TV++ pipeline, in six stages:

1. **Whole-book comprehension (Adler analysis)** — apply Mortimer Adler's analytical reading method to the book: structure, interpretation, criticism, application
2. **Parallel extraction** — several specialized extractors (frameworks, principles, cases, counter-examples, terminology) mine candidate methodology units from the source text
3. **Triple verification** — every candidate must pass three checks: at least two independent in-book supports (cross-domain), the ability to answer questions the book never explicitly addresses (predictive power), and not being common sense (distinctiveness)
4. **RIA++ construction** — structure each unit along R (quotation) / I (restatement in own words) / A1 (in-book case) / A2 (future trigger scenario) / E (executable steps) / B (boundaries and blind spots)
5. **Zettelkasten linking** — map dependencies, contrasts and combinations between cards, producing the capability index and routing table
6. **Trigger and output testing** — write trigger blind tests (including decoy questions: fire when they should, stay silent when they should not) and output evaluation scenarios for every card; failing cards go back for rework and are re-verified afterwards

This 1938 original carries a layer of modern commentary (marked "【点评】" in the book), and the distillation keeps the two sources separate: Elliott's text supplies the pattern, the degrees and the channel geometry; the commentator's heuristics (right-side confirmation, follow the trend, rest discipline) become a card of their own, `commentary-playbook`, with each item marked as not Elliott's own text and as unverified in evidence level. The boundary fields also come straight from the stage-0 whole-book reading — unfalsifiability risk, the missing magnitude dimension, and volume signals failing exactly when they are most needed are written into each card's (B) field.

## Testing and verification

This repository publishes the test material from the generation process alongside the skills: the trigger and output cases live in the `test-prompts.json` of each skill directory (`single/wave-theory-skill/` plus the 8 skill directories under `pack/`), and the item-by-item scoring log is `test-results.md` at the repository root.

- **Method**: three independent sub-agents ran the blind test, holding only the routing table and the matching capability card and never seeing the expected answers; the main process scored them against expectations
- **41 cases in total** (after de-duplicating the 9 `test-prompts.json` files; the raw sum is 100 because the `pack/` skills reuse the same case set): 13 should_trigger (fire when they should, and route to the right card), 7 should_not_trigger (decoys such as KDJ, P/E and ROE, MACD, stock tips, Fibonacci, the Premier League title — all must stay silent), 6 edge_case (a precise wave-5 target demanded while wave 3 is incomplete, an unfinished wave C, thin-market volume, a zombie stock), and 15 output_case (one per card, each requiring a complete deliverable)
- **Result**: all four categories passed — trigger, decoy, boundary and execution — with no failures, no rework, and no case removed from the denominator
- **Behaviours observed**: the blind tester spotted that the test data violated the overlap rule (wave 4 ending below the wave 1 peak) and declared the counting doubt instead of forcing the procedure; for an invalid count it offered a reject option plus alternatives rather than a single answer; commentary heuristics were labeled by evidence level and marked as not Elliott's text

## Repository layout

```text
wave-theory-skill/
├── README.md              ← Chinese version
├── README.en.md           ← you are reading this
├── LICENSE                ← MIT
├── BOOK_OVERVIEW.md       ← stage 0 output: Adler whole-book analysis
├── DIGEST.md              ← stage 5 output: reader-facing distilled long-form essay
├── INDEX.md               ← stage 3 output: skill map + dependencies
├── verified.md            ← the 290 units that passed triple verification
├── TEST_SUMMARY.md        ← stage 4 output: stress-test summary
├── CANGJIE_ADAPTATION.md  ← cangjie adaptation notes
├── GITHUB_REPO.md         ← repository metadata
├── test-results.md        ← test result records
├── candidates/            ← stage 1 output: raw candidate pool
│   ├── frameworks.md      ← framework and method candidates
│   ├── principles.md      ← principle / rule / calculation candidates
│   ├── cases.md           ← case candidates from the book
│   ├── counter-examples.md← counter-example and boundary candidates
│   └── glossary.md        ← terminology candidates
├── rejected/              ← stage 1.5 output: rejected units + reasons
├── bundle/                ← compilation source of truth
│   ├── verified.yaml      ← capability metadata, criteria and destinations
│   ├── cards/             ← capability card sources (six sections)
│   └── book/              ← overview.md + glossary.md
├── single/                ← single-mode build (one entry + all capability cards)
│   └── wave-theory-skill/SKILL.md  ← entry: triggers + routing table + loading rules
└── pack/                  ← pack-mode build (one router + 7 promoted skills)
    └── */SKILL.md         ← 8 skills, each shipping a test-prompts.json
```

## Usage

Clone the repository first:

```bash
git clone https://github.com/raphael-y7/wave-theory-skill.git
```

### Install single (recommended first try)

```bash
# macOS / Linux
cp -r wave-theory-skill/single/wave-theory-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\wave-theory-skill\single\wave-theory-skill "$env:USERPROFILE\.agents\skills\"
```

### Install pack

Copy only the directories that contain a `SKILL.md`; do not copy the two JSON files under `pack/` into your skills directory:

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

> `~/.agents/skills` is the DSH skills directory; with another agent, use its own skills directory (for example `~/.claude/skills` for Claude Code).

### How to verify the install

Ask: "Where will wave 5 of this rally roughly end, and when should I sell?" If the agent goes straight into the three-step channel drawing and the break/volume triple confirmation instead of generic "watch your risk, size down" commentary, the install works. With the single build it reads the entry first and then routes to `wave-five-end-skill`; with the pack build that capability is hit directly.

## Sources

- *The Wave Principle* by Ralph Nelson Elliott
- Distilled from the whole book, producing 15 capability cards

## Notice

This repository publishes distilled skills, indexes and rule quick references only. It contains no PDF, EPUB, OCR files, screenshots or full-book transcripts of the source book. Quotations that appear in the capability cards serve solely to attribute methodology and keep the material auditable.

All criteria in the book (the tolerance behind "near" the channel line, the volume threshold for a climax, the "fully drawn" test for triangles, the turnover heuristics, etc.) are case- and experience-based rules without statistical backtesting; some parameters supplied by the commentator (Fibonacci ratios, the 7% turnover figure) were flagged as unverified during distillation. Test them on your own instruments and declare the convention you use. Wave theory itself is contested in academic literature for unfalsifiability, and this repository records that criticism honestly in each card's boundary field (see section 3 of `BOOK_OVERVIEW.md`). Nothing in this repository is investment advice.

## License

[MIT](./LICENSE)
