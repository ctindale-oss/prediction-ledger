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

## Daily intake — 11 Oct 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `f2525b26b1dc6ff01b1d96c750823bd93a746e5eff3dc607d9b74a705201f0ea`. New SHA-256 `f5c58b2c70784a7a49140ea9e9fc8d90380e79cc6573c2bf77f5738f00fdc32a` (74 lines). Batch file `batches/batch-2026-10-11.json`. OpenTimestamps submitted 11 Oct 2026 8:03am Sydney; Bitcoin attestation pending. Batch 1 and batch 2 proofs are now Bitcoin-confirmed (blocks 970534 and 970582).

### Searched
- Substack RSS: no new essay since The Invisible Army (28 Sep 2026). That essay had been missed by the 9 Oct harvest and was read now.
- X @ctindale posts and replies, 10 Oct 2026 7:30am to 11 Oct 8:00am Sydney (8 posts).
- Interviews: none new found.

### New lines (pl-069 to pl-074)
- pl-069, pl-070 (The Invisible Army): online-safety powers spreading abroad; US "probably only till the midterms". Both unscorable.
- pl-071 (X): promised essay on free-market vs Hamilton/Menzies state capitalism "in the next few weeks". Inferred 0.90, due 30 Nov 2026, queued in inferred-to-confirm.csv.
- pl-072, pl-073, pl-074 (X): governments "will choose inflation"; "Bretton Woods 3-4-5"; AUD "hold my beer" vs USD bonds. All unscorable.

Not logged: the market's 10y10y expectation he describes (a reading of investors, not his call); the government's own statement that it will introduce the bill in 2026.

### Resolutions
None due. Earliest open resolution date is 2026-11-30 (pl-071), then 2026-12-31. Scores unchanged: stated Brier 0.0625 (n=1), inferred Brier 0.01 (n=1). Totals: 74 lines, 48 open, 2 resolved true, 0 false, 3 unresolved, 21 unscorable.

## Daily intake — 12 Oct 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `f5c58b2c70784a7a49140ea9e9fc8d90380e79cc6573c2bf77f5738f00fdc32a`. New SHA-256 `935466e6e87487bff4e1ec4e27b1cd34e3c7794c364f9f794f97669c9a96ef0a` (75 lines). Batch file `batches/batch-2026-10-12.json`. OpenTimestamps submitted 12 Oct 2026 8:03am Sydney; Bitcoin attestation pending. Batch 3 proof is now Bitcoin-confirmed (block 970834).

### Searched
- Substack RSS: no new essay since The Invisible Army (28 Sep 2026).
- X @ctindale posts and replies, 11 Oct 2026 7:00am to 12 Oct 8:02am Sydney (4 posts, retweets excluded).
- Interviews: none new found.

### New lines (pl-075)
- pl-075 (X): "What if all apps could be copied perfectly in a few days or weeks ? . That might be the truth in a few months". 'Might' is not a forecast under the word map; logged as unscorable.

Not logged: replies on AI lacking judgment, on a clean-room engineering loophole, and a question to another user; none is a forecast.

### Resolutions
None due. Earliest open resolution date is 2026-11-30 (pl-071), then 2026-12-31. Scores unchanged: stated Brier 0.0625 (n=1), inferred Brier 0.01 (n=1). Totals: 75 lines, 48 open, 2 resolved true, 0 false, 3 unresolved, 22 unscorable.

## Daily intake — 13 Oct 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `935466e6e87487bff4e1ec4e27b1cd34e3c7794c364f9f794f97669c9a96ef0a`. New SHA-256 `8895e407a0cb6de4c7f01cca78185d386b748dcec78e264c546c1efd07a819d2` (79 lines). Batch file `batches/batch-2026-10-13.json`. OpenTimestamps submitted 13 Oct 2026 8:08am Sydney; Bitcoin attestation pending. Batch 4 proof is now Bitcoin-confirmed (block 970983).

### Searched
- Substack RSS: one new essay, "Sovereign Black Warrant: India's Existential Material Trap" (12 Oct 2026, 2:00pm Sydney), read in full from the feed.
- X @ctindale posts and replies, 12 Oct 2026 8:02am to 13 Oct 8:06am Sydney (20 posts, retweets excluded).
- X article "Net-Zero by 2050 Came From Computer Models. So Did the Fictional Fantasy Machines That Make It Work." (https://x.com/ctindale/status/2109528525762109557, 12 Oct 2026): could not be read (API returns title only; the web page returns 403). Not yet extracted; retry next run.
- Interviews: none new found.

### New lines (pl-076 to pl-079)
- pl-076 (Substack): "no Indian sintered magnet will come off a line before late 2028." Inferred 0.90 from 'will'; scope fixed to sintered NdFeB on a commercial line; due 30 Sep 2028; queued in inferred-to-confirm.csv. Possible scope conflict flagged in notes (reported IREL samarium-cobalt plant), not verified.
- pl-077 (Substack): solar module sheds "cold within weeks" under an embargo. Conditional, unscorable.
- pl-078 (Substack): "Ten weeks of chemical stock will not outlast an embargo." Conditional, unscorable.
- pl-079 (Substack): "The next shortage will be of things dollars cannot buy." No deadline, unscorable.

Not logged: NALCO administrators' expectation on gallium (their call, not his); the Mines Secretary's stockpile-policy timing (the government's call); X replies on Australia ("We're screwed"), the EU, Frank Knight, e-waste and Bible translation, none a forecast.

### Resolutions
None due. Earliest open resolution date is 2026-11-30 (pl-071), then 2026-12-31. Scores unchanged: stated Brier 0.0625 (n=1), inferred Brier 0.01 (n=1). Totals: 79 lines, 49 open, 2 resolved true, 0 false, 3 unresolved, 25 unscorable.

## Daily intake — 18 Oct 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `84345da4d13374fc67173dc8d334ede1050a1af300f90cb51372ecce7035e990`. New SHA-256 `359766d5d1193e39022c1ca4944275cfa39ce0df34580199c6eca37cf26d86e1` (92 lines). Batch file `batches/batch-2026-10-18.json`. OpenTimestamps submitted 18 Oct 2026 8:04am Sydney; Bitcoin attestation pending. Batch 7 proof (8434..., 86 lines) is now Bitcoin-confirmed (blocks 971468/971474/971480/971484).

### Searched
- Substack RSS: no new essay since Part Two (13 Oct 2026).
- X @ctindale posts and replies, 17 Oct 2026 8:01am to 18 Oct 8:02am Sydney (14 posts).
- Interviews: web search found the Financial Sense Newshour interview with Jim Puplava, "Craig Tindale: Bessent Is the House, Gold Is the Tell" (published 30 Sep 2026), not previously logged. Transcript read in full from the page. Two August podcasts (Kontrarian Korner #144, 19 Aug; NatCon Australia E136, 25 Aug) were also found and are not yet logged; they have summaries only on the open pages, no transcript read yet.

### New lines (pl-086 to pl-091)
- pl-086 (interview): "So I, I see the whole regime changing in the next 12 months. ... It's like Bretton Woods 3 or something like that." Window stated (to 30 Sep 2027) but no measurable event; unscorable as written, as pl-073. Scorable if Craig names the test.
- pl-087 (interview): "short term they can do it three, six, nine months before ... the bond vigilantes ... intervening". Unscorable (undefined event).
- pl-088 (interview): "a lot of these tech stocks will be nationalized eventually ... at much lower prices, and the holders will take the hit." No deadline; unscorable.
- pl-089 (interview): Australia, "we're still going to raise rates into this, into this storm." No window; unscorable.
- pl-090 (interview): central banks' "cult of financialization, cult that's just about to end." Unscorable.
- pl-091 (X, 18 Oct): "it'll take years to move that inertia" on enterprise AI adoption. Unscorable.

Not logged: X reply on Basel II/III risk weights ("every single country that adopted this formula ... had their industrial activity fall by between 50 and 75%"), a claim about the past, not a forecast; X reply recalling 19 Oct 1987 ("it's much worse this time the bankers have financialized the whole economy"), a description of present conditions with no forecast of what or when; replies on AI and blockchain adoption in banks, X visibility, BOM data, a Wright brothers parody and social engineering, none a forecast.

### Resolutions
None newly due. pl-012 and pl-058 remain past due and unresolved. Earliest open resolution date is 2026-11-30 (pl-071). Scores unchanged.

## Daily intake — 20 Oct 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `ad85f1438a6e870028bac5a807053516fba19bba52ebe76f468636c2f5791005`. New SHA-256 `f65fadca3adcf9d879b4dbd3f25fea716f8e09912acc7039cb809d37dc1182da` (104 lines). Batch file `batches/batch-2026-10-20.json`. OpenTimestamps submitted 20 Oct 2026 8:28am Sydney; Bitcoin attestation pending. Batch 9 proof (ad85..., 94 lines) is now Bitcoin-confirmed (block 972057).

### Searched
- Substack: no new essay since 'Same Rules, Different Ruins' (18 Oct 2026).
- X @ctindale posts since the last run: no forecasts.
- Interviews: Bitcoin Magazine Podcast, 'Financial Repression in the Age of Superintelligence' (host Spencer Nichols, published 18 Oct 2026 13:00 UTC, 43 min; YouTube G1Q4ocdwMlc). No human transcript; the Exa page shows only the first three turns, and YouTube captions were blocked (HTTP 429, then bot-check). The episode MP3 was transcribed on the box with faster-whisper (small.en for the full episode, medium.en on the 12 passages quoted); every quoted fragment was checked by script as an exact substring of one of those transcripts (work/src/bm-2026-10-18.*).

### New lines (pl-094 to pl-103)
- pl-094: no default by the US, Australia or Japan; financial repression paid by "domestic players". Unscorable (no date); restates pl-085 with Australia and Japan named.
- pl-095: "a new Treasury-fed accord to manage the yield code ... You'll see this happen in other countries as well." Unscorable (no date or country); overlaps pl-072.
- pl-096: assets stored "next to targets, you're going to lose yours as well"; "heading from the middle game to the end game". Unscorable.
- pl-097: "empires just trade within the empires ... that's what's going to happen". Unscorable.
- pl-098: China's currency has "got to be reciprocal with gold" to become a trading currency. Conditional, unscorable.
- pl-099: "America's next leader is likely to be exactly the same." Inferred 0.70 ('likely'). Test fixed by the ledger keeper and queued in inferred-to-confirm.csv: TRUE if the 2029 US effective tariff rate (gross customs duties ÷ goods imports) is 5.0% or more (2.4% in 2024, 7.7% in 2025); due 31 Mar 2030.
- pl-100: Fourth Turning; the younger generation "are gonna have to rebuild"; "it's going to be crazy". Unscorable.
- pl-101: AI "is not pets.com"; "the first thing it replaces is the coders". Unscorable.
- pl-102: gold, copper and silver "gonna be contested"; silver and copper exchange stock-outs "might"/"may" happen. Unscorable.
- pl-103: his re-run climate models: "what we end up in is the younger driest [Younger Dryas] period ... and everything gets cold". Unscorable.

Not logged: "the government will nationalize it to a certain extent" (restates pl-088, no new date or number); cyborgs in 10–15 years ("I wouldn't make any predictions about it"); bitcoin ("I can't predict that"); IonQ on AWS (relayed company news); repo window, buyback size and "free markets can stop overnight" (statements of what is possible); rare-earth companies "about to start producing" (others' plans, no names); diesel (rhetorical conditional).

### Resolutions
None newly due. pl-012 and pl-058 remain past due and unresolved. Earliest open resolution date is 2026-11-30 (pl-071).

## Daily intake — 22 Oct 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `f65fadca3adcf9d879b4dbd3f25fea716f8e09912acc7039cb809d37dc1182da` (104 lines, now Bitcoin-confirmed in blocks 972217 / 972237). New SHA-256 `f2f01f11dc370f9f6f2723668a0a17b81a3135da102f04a9fd4ef327e4cb6782` (105 lines). Batch file `batches/batch-2026-10-22.json`. OpenTimestamps submitted 22 Oct 2026 8:03am Sydney; Bitcoin attestation pending.

### Searched
- Substack archive API: no new post (latest still 18 Oct 2026, "Same Rules, Different Ruins").
- X posts by @ctindale since the last run: five posts (20 Oct 23:04 UTC to 21 Oct 06:40 UTC).
- Web search for new interviews: none beyond the already-logged 18 Oct 2026 Bitcoin Magazine podcast.

### New
- pl-104 (X, 20 Oct 2026 23:13 UTC): "Folks should keep an eye out for my new essay on how US transitions to gold back bonds , revaluing its reserves and resetting UST & US debt - due out in the next few days". Inferred 0.90 ('due out' read as 'will'); resolves 2026-10-28 against his Substack archive. Queued in inferred-to-confirm.csv.

Not logged: replies on financialisation (state asset sales for income streams), on late-cycle housing versus early-cycle tradeables lending risk, and two replies on the Israel–Gaza exchange with @Frances_Coppola; none is a dated, checkable forecast.

### Resolutions
None due. pl-012 and pl-058 remain unresolved.

## Daily intake — 4 Nov 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `98572c1a06306cb26ccd03a7bb7e8b622a8455cf4ab8ab7940b61d443aca9e35` (114 lines, now Bitcoin-confirmed in blocks 974302 / 974322 / 974343). New SHA-256 `1faffe032d0b26e2a7a16aa4b4f016eab65dc3f8c7a3402fbca964fdf576cd48` (116 lines, 112 active entries). Proof batches/ledger-2026-11-04.jsonl.ots pending.

### Searched
- Substack RSS: one new post, 'Decarbonisation: The Fantasy upon which Net Zero is built.' (3 Nov 2026 06:00 UTC), a republication of the 12 Oct X article already harvested as pl-080 to pl-083.
- X posts by @ctindale since the last run: eleven posts (3 Nov 01:00 UTC to 20:30 UTC).

### New
- pl-111 (Substack): "If the removal machines fail to arrive at the scale the pathways assume, net zero by 2050 is a fantasy. Warming that passes 1.5°C stays above it." Conditional, undated; unscorable.
- pl-112 (X reply to @DawesPoints): "the geopolitical civilisational framework gets more balkanised going forward ... That's why I keep landing on repression and inflation". Undated; unscorable.

Not logged: "on copper alone, the route is implausible" (restates pl-082); X reply to @Mabeytweet that the removal machines "simply don't and can't exist" (restates pl-080); the Zervos energy-risk/bond-yield reply ("I don't think we have the answer to that yet"); Treasury buyback poll thread; Greens/Hutton and Greens/Gaza posts.

### Resolutions
None due. pl-012 and pl-058 remain past due and unresolved.

## Daily intake — 8 Nov 2026 (Australia/Sydney)

Appended only. Prior SHA-256 `3de6d5513c7960431a7d0ebb38d006a25c898947437a2efabbf3a53b7f5a0c00`. New SHA-256 `247631122c6a82dfac434b8d1ee9043b0f1c93019f91eb219d04f159c6e86dd5` (139 lines). Batch file `batches/batch-2026-11-08.json`. OpenTimestamps submitted 8 Nov 2026 about 8am Sydney; Bitcoin attestation pending. Batch 19 proof (3de6..., 132 lines) is Bitcoin-confirmed (blocks 974714/974715/974752/974757).

### Searched
- Substack RSS: no new essay since 5 Nov 2026.
- X @ctindale since 7 Nov 8am Sydney: one two-post Greens thread (Penny Allman-Payne letter, links the existing essay); no forecast.
- Interviews: web search found two interviews earlier intakes missed: the In Gold We Trust report 2026 debate with Luke Gromen (recorded 13 Apr 2026; edited transcript with speaker labels on ingoldwetrust.report, read in full for Craig's turns) and the Investing News Network video interview with Charlotte McLeod (22 Oct 2026; only the two quotes printed on the article page were read, video not transcribed).

### New lines (pl-129 to pl-135), all unscorable as worded
- pl-129 (IGWT): gold revaluation, "probably the most likely it's been in the last 40 years"; read as 0.70, no deadline.
- pl-130 (IGWT): "in order to save the USD, they have to anchor it on some kind of commodity mix"; USD 25,000 gold "isn't hard to imagine" (a possibility, not mapped).
- pl-131 (IGWT): Siemens transformer lead time "that'll blow out to six or seven years"; no date or agreed series.
- pl-132 (IGWT): US magnesium "going to take the US 10 years to fix"; suggested check 13 Apr 2036 via USGS.
- pl-133 (IGWT): "a rotation from hell" out of AI data-centre speculation; no deadline.
- pl-134 (IGWT): conditional copper cut-off "at the end of the year"; context check 31 Dec 2026, not scored.
- pl-135 (INN): "a very significant change in US treasuries, in gold, in international debt, in the value of the dollar"; read as 0.70, no deadline.

Not logged: the Nvidia 250,000 t copper figure for 2028 (a projection he cites); "That “something else” could take the form of war" (a could, kept in pl-132's text).

### Resolutions
None due. Next dated open call pl-071 on 30 Nov 2026. Totals: 139 lines, 135 active, 65 open, 2 resolved true, 3 false, 2 unresolved, 64 unscorable.


## Paid-section reread — 11 Nov 2026 afternoon (Australia/Sydney)

Appended only. Prior SHA-256 `3a4ca4a6d491b0f33ba1d18ae7e2573e6d6a90f8cf34f1b191df72583b3177f7` (141 lines, morning intake). New SHA-256 `f709038b7957b506e75514deb96eff38109c70cff12d6f3161b50d796d77586a` (147 lines). Batch file `batches/batch-2026-11-11-paid.json`. OpenTimestamps submitted 11 Nov 2026 about 9:48am Sydney; Bitcoin attestation pending. Morning 11 Nov proof (3a4ca4a6…) is Bitcoin-confirmed (block 975346). Batch 20 proof (24763112…, 139 lines, 8 Nov) is Bitcoin-confirmed (blocks 974986/974987/975023/975026).

### Why the morning intake missed these
The public Substack page and the X Article both stop at the paywall sentence ("The administration has already used the Commander-in-Chief Clause on military money, but to move money rather than hold it back."). The full published text was read in the afternoon from the essay's published file.

### New lines (pl-138 to pl-143)
- pl-138: "Late in fiscal 2027, a third is likely unless Congress has passed a binding restriction that closes the route. Foreign aid remains the likeliest target." Inferred 0.70 from 'likely'; resolves 31 Oct 2027; queued. If Congress closes the route and no third request is sent, not applicable (not a miss).
- pl-139: "The likeliest pattern is repeated withholding, appeals, rewritten orders and negotiated partial funding deals." Inferred 0.70; resolves 31 Oct 2027; queued.
- pl-140: "The likeliest outcome is a negotiated partial deal, reached after programs the White House opposes have already lost staff, recipients and a year of work." Inferred 0.70; resolves 31 Oct 2027; queued.
- pl-141: officials "will stop saying ‘this is illegal’…"; inferred 0.90; unscorable (no date or measure).
- pl-142: "Least likely is refusing to obey a final, binding court order." Ranking, no number assigned; unscorable.
- pl-143: self-critique — what breaks the advantage of delay (named-account restriction with a release date and a late-rescission ban, or a binding court order before the money expires).

The essay's closing line was already logged as pl-137 from the LinkedIn summary.

### Resolutions
None due. pl-012 and pl-058 remain past due and unresolved.
