# Prediction Ledger Scoring — batch 2026-10-09

## Method
- **Canonical store:** `ledger.jsonl` (one JSON object per line, append-only in spirit).
- **Derived views:** `ledger.csv` and `ledger.json` are regenerated from the jsonl; they are not the proof trail.
- **Corrections:** do not rewrite a line. Append a new line with the same `id` and `"supersedes"` set to identify the prior line; scorers ignore superseded lines.
- **Headline skill:** Brier on **stated** probabilities only, resolved true/false.
- **Inferred Brier:** separate, labelled as a *reading of language*, not Craig's stated skill.
- **Probability map (inferred only):** certain/will/inevitable/guaranteed=0.90; very likely/highly likely=0.80; likely/probably/I expect=0.70; more likely than not=0.60; unlikely=0.30; very unlikely/won't=0.15. Could/might/possible/maybe → not a forecast (unscorable if logged).
- **No 1.0/0.0.** Ranges → midpoint + note.
- **Consensus / edge:** only when a dated consensus number at or before `date_made` was actually found. Never backfill today's market as then-consensus.
- **Consensus-relative score:** mean of (his Brier − consensus Brier) on items with both probabilities and an outcome.
- Today for resolution scope: **2026-10-09** (Australia/Sydney).

## What was searched
1. `/workspace/substack/` — posts.csv (~68 essays) + targeted reads (copper limits, war/El Niño, silver turnstile, El Niño almanac, AI metabolism, AI SaaS, AI lifeline, return of matter, Bessent/gold, copper residual, architecture of financialisation).
2. `/workspace/ctindale_x/all.json` — 124 posts (Jun–Sep 2026); forecast-like subset mined.
3. Commodity/ASX folders (`copper-federation`, `ixr`, `metallium`, `elementos`, `babel-ledger`, `copper-residual`) — sampled; no Craig-authored numeric forecasts logged from assistant briefs.
4. Interviews: MacroVoices #1492 transcript (2026-01-22) opened and quoted; Great Simplification / Blockspace noted, not fully transcribed this pass.
5. Public facts: NOAA CPC ENSO, silver spot (~USD 60 on 2026-10-08), Panama Canal advisories, China H2SO4 export halt, FAO fertiliser commentary, Brent ~USD 104 (2026-10-08).

## What was skipped / not finished
- Full cover-to-cover of all 68 essays.
- X archive before Jun 2026 (not in local all.json).
- Full Great Simplification ep. 207 and Blockspace transcripts.
- Polymarket/Metaculus odds **as of date_made** for most items (current Oct 2026 prices not backfilled).
- OpenTimestamps and GitHub public commit (ledger keeper applies after this batch).

## Counts
| Set | n |
|---|---|
| Total lines logged | 45 |
| Stated probability | 3 |
| Inferred probability | 37 |
| Scorable open | 34 |
| Resolved true | 2 |
| Resolved false | 0 |
| Unresolved (due, evidence insufficient) | 2 |
| Unscorable | 7 |

## Scores
### Headline Brier (stated only)
- **Brier = 0.0625** (n=1)
- Resolved stated items: ['pl-001']

### Inferred Brier (reading of language — NOT skill)
- **Brier = 0.009999999999999995** (n=1)
- Resolved inferred items: ['pl-009']

### Edge vs consensus
- Items with both probs + outcome: 1 → [{'id': 'pl-001', 'his_minus_cons_brier': 0.0, 'edge': 0.0}]
- Mean (his Brier − consensus Brier) = 0.0
- Interpretation: 0 means he matched the consensus he republished (no separate skill claim).

### Direction / timing / magnitude
- direction_result: {'right': 2, 'unresolved': 36, 'n/a': 7}
- timing_result: {'right': 2, 'unresolved': 36, 'n/a': 7}
- magnitude_result: {'n/a': 30, 'unresolved': 15}
- mechanism (resolved only): {'unclear': 1, 'his_reason': 1}
- **Right but early count:** 0
- Unscorable tally: **7**

### Calibration by domain
| domain | n_resolved | mean_p | fraction_true | Brier | note |
|---|---|---|---|---|---|
| asx-equity | 0 | None | None | None | no resolved scorable items |
| climate | 1 | 0.75 | 1.0 | 0.0625 | calibration not meaningful (n<8) |
| copper | 0 | None | None | None | no resolved scorable items |
| energy | 0 | None | None | None | no resolved scorable items |
| geopolitics | 0 | None | None | None | no resolved scorable items |
| gold | 0 | None | None | None | no resolved scorable items |
| other | 1 | 0.9 | 1.0 | 0.01 | calibration not meaningful (n<8) |
| rare-earths | 0 | None | None | None | no resolved scorable items |

## Batch proof (local)
- File: `batches/batch-2026-10-09.json`
- SHA-256(`ledger.jsonl`) = `1b63678f1667007be75c89973a84cfecc5c491c04ff5fb13cc217885dbe24d5a`
- OpenTimestamps calendars accepted this digest on 9 Oct 2026 at 7:56am Sydney. Proof file: ledger.jsonl.ots. Bitcoin attestation pending. Public repo: https://github.com/ctindale-oss/prediction-ledger.

## Top open claims still running

- **pl-003** (gold, due 2027-09-08): Where will it trade Silver will trade above $90 an ounce within twelve months. Physical demand will drive it.
- **pl-004** (copper, due 2028-12-31): By 2028, demand (>30 Mt) outstrips likely supply (~28-29 Mt) by roughly 1 to 2 million tonnes.
- **pl-029** (climate, due 2027-02-28): WMO puts persistence through February 2027 near 100%.
- **pl-016** (other, due 2027-12-31): AI Won't Nuke SaaS: Why the White-Collar Apocalypse Is Just Tech Bros' Dreaming Nonsense These white-collar Armageddon stories are nonsense
- **pl-027** (climate, due 2027-12-31): Global heat into 2027 — High. The WMO outlook supports continued warmth as El Niño’s influence carries beyond its expected late-2026 peak.

## Second batch — full Substack harvest (2026-10-09)

Appended only. Prior lines were not rewritten. Prior SHA-256 remains `1b63678f1667007be75c89973a84cfecc5c491c04ff5fb13cc217885dbe24d5a`. New SHA-256 is `f2525b26b1dc6ff01b1d96c750823bd93a746e5eff3dc607d9b74a705201f0ea`, not yet OpenTimestamped. Batch file: `batches/batch-2026-10-09-substack.json`.

### What was opened
- Essay files on disk: **68** (posts.csv has 69 rows because The Return of Matter is listed twice against one file). All 68 were scanned for will / by 20xx / percent / forecast language, then the hits were read.
- Could not read: **none**.
- Essays that produced new lines this pass: **20**.
- Already in batch 1, re-read, no additional explicit forecast: **5** (Copper Limits to Growth, Metabolism of AI, AI Won't Nuke SaaS, Architecture of Financialisation, Bessent / gold).
- Skipped after the scan as having no explicit forecast: **43**.

Third-party point forecasts he cites but does not adopt in his own voice were not logged (IEA 82% by 2035, S&P 10 Mt by 2040, Argus HVO shortfall, TBAC funding gap, Silver Institute ounce balances, Hormuz scenario branches). Vague calls were logged as unscorable, not dropped.

### New lines
- New claims: **23** (`pl-046` through `pl-068`).
- Of which stated: 1 (`pl-051`, the 69% RONI figure). Inferred: 19. Unscorable: 9.
- One due item, `pl-058` (the delivered-cost model "in the coming weeks"), is **unresolved**. It was not found in the local archive or on a web search, and that is not proof it was never published.
- No new claim was resolved true or false. Copper at $15,000 (`pl-046`) has not printed: LME high about USD 14,875/t on 10 Sep 2026.

### Scores on ALL non-superseded rows
No superseded lines.

| Set | n |
|---|---|
| Total lines | 68 |
| Stated probability | 4 |
| Inferred probability | 56 |
| Scorable open | 47 |
| Resolved true | 2 |
| Resolved false | 0 |
| Unresolved (due, evidence insufficient) | 3 |
| Unscorable | 16 |

- **Stated Brier = 0.0625** (n=1). Resolved stated: ['pl-001'].
- **Inferred Brier = 0.009999999999999995** (n=1). Resolved inferred: ['pl-009']. This is a reading of language, not his skill.
- Edge vs consensus: n=1, mean (his Brier − consensus Brier) = 0.0. Items: [{'id': 'pl-001', 'his_minus_cons_brier': 0.0, 'edge': 0.0}].
- direction_result: {'right': 2, 'unresolved': 50, 'n/a': 16}
- timing_result: {'right': 2, 'unresolved': 50, 'n/a': 16}
- magnitude_result: {'n/a': 47, 'unresolved': 21}
- mechanism (resolved only): {'unclear': 1, 'his_reason': 1}
- Right but early: 0
- Unscorable tally: **16**

### Calibration by domain
| asx-equity | 0 | None | None | None | no resolved scorable items |
| climate | 1 | 0.75 | 1.0 | 0.0625 | calibration not meaningful (n<8) |
| copper | 0 | None | None | None | no resolved scorable items |
| energy | 0 | None | None | None | no resolved scorable items |
| geopolitics | 0 | None | None | None | no resolved scorable items |
| gold | 0 | None | None | None | no resolved scorable items |
| other | 1 | 0.9 | 1.0 | 0.01 | calibration not meaningful (n<8) |
| rare-earths | 0 | None | None | None | no resolved scorable items |

Calibration is not meaningful in any domain: every domain has n_resolved < 8.

### Essays skipped as no explicit forecast
- a-castle-lookout-doesnt-wait-for.txt
- anthropic-an-attempted-coup.txt
- article-the-missing-mechanism-in.txt
- australias-proposed-cgt-reforms-why.txt
- blood-bifurcation.txt
- decoding-trump-on-irans-electrical.txt
- dismantling-gender-norms-the-un-blueprint.txt
- earth-rotation-residuals-as-an-early.txt
- five-contracts-one-river.txt
- global-system-failure.txt
- how-australias-esafety-commissioner.txt
- how-shipping-effluent-may-intensify.txt
- how-to-read-this-series.txt
- money-broke-physics-the-framework.txt
- south-africa-the-rainbow-nation-taught.txt
- stepping-outside-the-fiat-frame-gold.txt
- stop-using-ai-for-answers-start-using.txt
- sydneys-fast-track-housing-machine.txt
- systemic-risk-a-12-order-cascading.txt
- the-accounting-illusion-supply-constraints.txt
- the-age-of-consequences-is-here-only.txt
- the-amputation-algorithm.txt
- the-calculus-of-american-blindness.txt
- the-chokepoint-mandate-the-global.txt
- the-discipline-of-peace.txt
- the-dorian-gray-of-threadneedle-street.txt
- the-great-silencing-how-australias.txt
- the-hard-bifurcation-the-convergence.txt
- the-hidden-disease-how-a-handful.txt
- the-hidden-subsidy-who-owns-the-chemistry.txt
- the-importance-of-being-obsolencent.txt
- the-new-serfdom-how-central-bankers.txt
- the-next-evolution-in-human-logic.txt
- the-original-mind-virus-ricardo.txt
- the-reserve-currency-trap-the-mechanics.txt
- the-revenge-of-matter-chinas-commodity.txt
- the-sovereignty-spread.txt
- thoughts-on-making-life-easier.txt
- trumps-material-mandate-reforming.txt
- what-the-2000-fishing-boats-were.txt
- where-we-are-today-the-mechanics.txt
- why-young-adults-are-less-reliable.txt
- you-cannot-unsee-the-loops.txt
