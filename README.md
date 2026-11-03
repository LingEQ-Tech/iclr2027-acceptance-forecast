# ICLR 2027 acceptance forecast (sealed)

We forecast acceptance for ICLR 2027 submissions before the reviews (2026-11-05) and the final decisions (2026-12-16) were released. The forecast file is sealed: only its fingerprint is public now. The file will be published in this repository on 2026-12-16, after the decisions are announced.

## What is sealed

- 10,368 ICLR 2027 submissions in 31 research tracks.
- For each paper: the predicted probability of acceptance, a LingEQ value, and its rank within its track.
- LingEQ gives each paper a value of up to 200; a higher value means the paper is more likely to be accepted.
- Within each track, papers are ranked by their LingEQ value (papers with the same value are ordered by their predicted probability).

## File to be published

`predictions_2027.csv`: one row per paper. Columns: `forum_id`, `title`, `link`, `track`, `primary_area`, `p_accept`, `lingeq`, `track_rank`, `track_size`, `area_rank` (rank within the primary area).

## Fingerprint

SHA-256 of `predictions_2027.csv`:

```
4052e12ee062b851fa02d22e4481453feffa8488ec59f125ed01450122cfd37b
```

## Proof of time

`predictions_2027.csv.ots` is an OpenTimestamps proof. It anchors the fingerprint in the Bitcoin blockchain and shows that it existed on 2026-11-03, independent of GitHub.

## How to check, once the file is published

1. The file matches the fingerprint: `sha256sum predictions_2027.csv`
2. The fingerprint existed on 2026-11-03: upload `predictions_2027.csv` and `predictions_2027.csv.ots` at https://opentimestamps.org, or run `ots verify predictions_2027.csv.ots`

## History

The first commits of this repository sealed the same data file together with a description file (fingerprint of `MANIFEST.sha256`, whose list already contained the hash above). On 2026-11-03 the seal was reduced to the data file alone.
