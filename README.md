# Prediction ledger

Append-only public record of Craig Tindale's explicit forecasts.

The canonical file is `ledger.jsonl`. One JSON object per line. Do not edit a line. A correction is a new line with the same `id` and `supersedes` set. `ledger.csv` and `ledger.json` are derived.

`batches/batch-2026-10-09.json` records the SHA-256 of `ledger.jsonl` for the first batch:

`1b63678f1667007be75c89973a84cfecc5c491c04ff5fb13cc217885dbe24d5a`

`ledger.jsonl.ots` is the OpenTimestamps proof of those bytes, submitted 9 Oct 2026 (Sydney) to public calendars. Bitcoin confirmation is pending until `ots upgrade`. `ledger.jsonl.ots.b64` is the same proof as text.

Stated probabilities and inferred probabilities are scored separately. Inferred calls are a reading of his wording, queued in `inferred-to-confirm.csv` for him to confirm. They are not his skill score.

Scorecard: `scorecard.html`. Method: `SCORING.md`.

Update 11 Oct 2026: batch 1 and batch 2 proofs are Bitcoin-confirmed (blocks 970534 and 970582). The ledger is now 74 lines; see `github-parts/README.md` and `batches/batch-2026-10-11.json`. Current SHA-256 `f5c58b2c70784a7a49140ea9e9fc8d90380e79cc6573c2bf77f5738f00fdc32a`, OpenTimestamps pending.

Update 12 Oct 2026: the batch 3 proof (74 lines, `f5c58b2c...`) is Bitcoin-confirmed (block 970834). The ledger is now 75 lines; see `batches/batch-2026-10-12.json`. Current SHA-256 `935466e6e87487bff4e1ec4e27b1cd34e3c7794c364f9f794f97669c9a96ef0a`, OpenTimestamps pending.

Update 13 Oct 2026: the batch 4 proof (75 lines, `935466e6...`) is Bitcoin-confirmed (block 970983). The ledger is now 79 lines; see `batches/batch-2026-10-13.json`. Current SHA-256 `8895e407a0cb6de4c7f01cca78185d386b748dcec78e264c546c1efd07a819d2`, OpenTimestamps pending.

## Daily intake 14 Oct 2026
- SHA-256(ledger.jsonl) = `0dc623597362a34ceb1bd44bbf9b7014c33aa571b5f5ab597dca1036d478cc3a` (85 lines; 84 active after supersede)
- New: pl-080–pl-084 from net-zero X article + Banking Swadeshi Part Two; resolved pl-039 false
- Proof: batches/ledger-2026-10-14.jsonl.ots (Bitcoin pending). Prior batch 8895… now Bitcoin-confirmed (971142+).


## Daily intake 15 Oct 2026
- SHA-256(ledger.jsonl) = `84345da4d13374fc67173dc8d334ede1050a1af300f90cb51372ecce7035e990` (86 lines; 85 active after supersede)
- New: pl-085 (unscorable X reply to Ray Dalio). No call fell due.
- Proof: batches/ledger-2026-10-15.jsonl.ots (Bitcoin pending). Prior batch 0dc6… now Bitcoin-confirmed (blocks 971303/971354/971357).

## Daily intake 18 Oct 2026
- SHA-256(ledger.jsonl) = `359766d5d1193e39022c1ca4944275cfa39ce0df34580199c6eca37cf26d86e1` (92 lines; 91 active after supersede)
- New: pl-086–pl-090 backfilled from the 30 Sep 2026 Financial Sense interview; pl-091 from an 18 Oct X reply. All unscorable as worded. No resolutions.
- Proof: batches/ledger-2026-10-18.jsonl.ots (Bitcoin pending). Prior batch 8434… now Bitcoin-confirmed (blocks 971468–971484).

## Daily intake 19 Oct 2026
- SHA-256(ledger.jsonl) = `ad85f1438a6e870028bac5a807053516fba19bba52ebe76f468636c2f5791005` (94 lines; 93 active after supersede)
- New: pl-092–pl-093 from the 18 Oct 2026 Substack essay 'Same Rules, Different Ruins' (Australian housing-credit cliff; write-down if reweighting is left too late). Both unscorable as worded. No resolutions.
- Proof: batches/ledger-2026-10-19.jsonl.ots (Bitcoin pending). Prior batch 3597… now Bitcoin-confirmed (blocks 971910/971914/971954).

## Daily intake 20 Oct 2026
- SHA-256(ledger.jsonl) = `f65fadca3adcf9d879b4dbd3f25fea716f8e09912acc7039cb809d37dc1182da` (104 lines; 103 active after supersede)
- New: pl-094–pl-103 from the 18 Oct 2026 Bitcoin Magazine Podcast interview 'Financial Repression in the Age of Superintelligence' (host Spencer Nichols), transcribed locally from the episode audio. pl-099 ("America's next leader is likely to be exactly the same") is inferred 0.70, due 31 Mar 2030; the other nine are unscorable as worded. No resolutions.
- Proof: batches/ledger-2026-10-20.jsonl.ots (Bitcoin pending). Prior batch ad85… now Bitcoin-confirmed (block 972057).
