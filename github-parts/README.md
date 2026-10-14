# Ledger bytes

`ledger.jsonl` in the repo root was an incomplete upload and is not the record.

The canonical file is the concatenation, in order, of `github-parts/ledger-01.jsonl`, `ledger-02.jsonl`, and so on.

SHA-256 of ledger-01..13 (68 lines, 9 Oct 2026): `f2525b26b1dc6ff01b1d96c750823bd93a746e5eff3dc607d9b74a705201f0ea`

The first 45 lines of that concatenation are batch 1.
SHA-256: `1b63678f1667007be75c89973a84cfecc5c491c04ff5fb13cc217885dbe24d5a`
Those lines are also stored as `github-parts/batch1-01.jsonl` onward.
Proof: `batches/ledger-2026-10-09-batch1.jsonl.ots` (already in the repo as the earlier ots file) and `batches/ledger-2026-10-09-substack.jsonl.ots.b64` for the full 68-line file.

Daily intake 11 Oct 2026 added `ledger-14.jsonl` (pl-069 to pl-074). SHA-256 of ledger-01..14: `f5c58b2c70784a7a49140ea9e9fc8d90380e79cc6573c2bf77f5738f00fdc32a`. Proof: `batches/ledger-2026-10-11.jsonl.ots.b64` (Bitcoin block 970834).

Daily intake 12 Oct 2026 added `ledger-15.jsonl` (pl-075). SHA-256 of ledger-01..15: `935466e6e87487bff4e1ec4e27b1cd34e3c7794c364f9f794f97669c9a96ef0a`. Proof: `batches/ledger-2026-10-12.jsonl.ots.b64` (Bitcoin block 970983).

Daily intake 13 Oct 2026 added `ledger-16.jsonl` (pl-076 to pl-079). SHA-256 of ledger-01..16: `8895e407a0cb6de4c7f01cca78185d386b748dcec78e264c546c1efd07a819d2`. Proof: `batches/ledger-2026-10-13.jsonl.ots.b64` (Bitcoin confirmation pending).

To check:

    cat github-parts/ledger-*.jsonl | sha256sum

Daily intake 14 Oct 2026 added `ledger-17.jsonl` (pl-039 resolution + pl-080 to pl-084). SHA-256 of ledger-01..17: `0dc623597362a34ceb1bd44bbf9b7014c33aa571b5f5ab597dca1036d478cc3a`. Proof: `batches/ledger-2026-10-14.jsonl.ots.b64` (Bitcoin confirmation pending). Batch 5 (8895...) now Bitcoin-confirmed (blocks 971142/971147/971177).

Daily intake 15 Oct 2026 added `ledger-18.jsonl` (pl-085). SHA-256 of ledger-01..18: `84345da4d13374fc67173dc8d334ede1050a1af300f90cb51372ecce7035e990`. Proof: `batches/ledger-2026-10-15.jsonl.ots.b64` (Bitcoin confirmation pending). Batch 6 (0dc6...) now Bitcoin-confirmed (blocks 971303/971354/971357).
