# ICLR 2027 acceptance forecast (sealed)

We forecast acceptance for ICLR 2027 submissions before the reviews (2026-11-05) and the final decisions (2026-12-16) were released. The forecast files are sealed: only their fingerprint is public now. The files will be published in the `forecast/` folder of this repository on 2026-12-16, after the decisions are announced.

## What is sealed

- 10,368 ICLR 2027 submissions in 31 research tracks.
- For each paper: the predicted probability of acceptance, a LingEQ value, and its rank within its track.
- LingEQ is derived from the rank of the predicted probability. A higher value means a paper is more likely to be accepted. The maximum is 200.

## Files to be published

- `forecast/predictions_2027.csv`: one row per paper. Columns: `forum_id`, `title`, `link`, `track`, `primary_area`, `p_accept`, `lingeq`, `track_rank`, `track_size`, `area_rank` (rank within the primary area).
- `forecast/README.md`: a short description of the file.

## Fingerprint

SHA-256 of `MANIFEST.sha256`:

```
13261d81b23f41c064c91a9587dc6fd041a1bdc933ff56069e79daf8a891e81d
```

`MANIFEST.sha256` lists the SHA-256 of each forecast file. It reveals nothing about the forecast itself.

## Proof of time

`MANIFEST.sha256.ots` is an OpenTimestamps proof. It anchors the fingerprint in the Bitcoin blockchain and shows that it existed on 2026-11-03, independent of GitHub.

## How to check, once the files are published

1. Each file matches the manifest: `cd forecast && sha256sum -c ../MANIFEST.sha256`
2. The manifest matches the fingerprint above: `sha256sum MANIFEST.sha256`
3. The fingerprint existed on 2026-11-03: upload `MANIFEST.sha256` and `MANIFEST.sha256.ots` at https://opentimestamps.org, or run `ots verify MANIFEST.sha256.ots`
