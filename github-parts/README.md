# Ledger bytes

`ledger.jsonl` in the repo root was an incomplete upload and is not the record.

The canonical file is the concatenation, in order, of `github-parts/ledger-01.jsonl`, `ledger-02.jsonl`, and so on.

SHA-256 of ledger-01..13 (68 lines, 9 Oct 2026): `f2525b26b1dc6ff01b1d96c750823bd93a746e5eff3dc607d9b74a705201f0ea`

The first 45 lines of that concatenation are batch 1.
SHA-256: `1b63678f1667007be75c89973a84cfecc5c491c04ff5fb13cc217885dbe24d5a`
Those lines are also stored as `github-parts/batch1-01.jsonl` onward.
Proof: `batches/ledger-2026-10-09-batch1.jsonl.ots` (already in the repo as the earlier ots file) and `batches/ledger-2026-10-09-substack.jsonl.ots.b64` for the full 68-line file.

Daily intake 11 Oct 2026 added `ledger-14.jsonl` (pl-069 to pl-074). SHA-256 of ledger-01..14: `f5c58b2c70784a7a49140ea9e9fc8d90380e79cc6573c2bf77f5738f00fdc32a`. Proof: `batches/ledger-2026-10-11.jsonl.ots.b64`.

To check:

    cat github-parts/ledger-*.jsonl | sha256sum
