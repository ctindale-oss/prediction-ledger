# Prediction ledger

Append-only public record of Craig Tindale's explicit forecasts.

The canonical file is `ledger.jsonl`. One JSON object per line. Do not edit a line. A correction is a new line with the same `id` and `supersedes` set. `ledger.csv` and `ledger.json` are derived.

`batches/batch-2026-10-09.json` records the SHA-256 of `ledger.jsonl` for the first batch:

`1b63678f1667007be75c89973a84cfecc5c491c04ff5fb13cc217885dbe24d5a`

`ledger.jsonl.ots` is the OpenTimestamps proof of those bytes, submitted 9 Oct 2026 (Sydney) to public calendars. Bitcoin confirmation is pending until `ots upgrade`. `ledger.jsonl.ots.b64` is the same proof as text.

Stated probabilities and inferred probabilities are scored separately. Inferred calls are a reading of his wording, queued in `inferred-to-confirm.csv` for him to confirm. They are not his skill score.

Scorecard: `scorecard.html`. Method: `SCORING.md`.
