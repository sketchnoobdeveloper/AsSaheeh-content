# AsSaheeh downloadable content

This public repository hosts the optional offline Quran and Hadith content pack
used by the [AsSaheeh Android app](https://github.com/sketchnoobdeveloper/AsSaheeh).
Keeping the compiled corpus in a GitHub Release makes the installer much smaller.

## Content v1

The `content-v1` release contains:

- `offline_library.db` — compiled, read-only import source for the Android app.
- `offline_library.json` — corpus catalog, provenance, counts and database hash.
- `content-manifest.json` — release file sizes and SHA-256 hashes.
- `assaheeh-content-v1-source-json.zip` — unchanged source JSON and sidecars used
  to compile the database; this archive is for reproducibility and is not
  downloaded by the app.
- `THIRD_PARTY_NOTICES.txt` — source and reuse notices.

The Android app downloads the database only after an explicit user action,
checks its exact byte count and SHA-256 hash, imports it transactionally, and
then removes the downloaded staging file. A failed or interrupted download is
not used.

## Important content notice

The catalog and source sidecars are authoritative. Availability in this pack is
not a claim of new scholarly review or new reuse permission. Original source
labels and attribution are preserved; missing content is not invented.
