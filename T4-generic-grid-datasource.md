# T4 — Reusable grid data source for infinite scroll

## Why

Several large tables use AgGrid's infinite-scroll mode through a custom
data-source class tied to the legacy subscription machinery. A recent
prototype proved the query-based replacement works (and found a real
scrolling bug in the process). This ticket turns that prototype into one
small, tested, reusable component all infinite-scroll tables can share.

## What

- A generic query-backed AgGrid data source: fetches one block of rows per
  request, caches blocks, deduplicates and retries automatically.
- Correct end-of-data detection (our list APIs do not return a total row
  count — see T9).
- Unit tests covering the block loading, end detection and cleanup behavior.

## Done when

- The component lives in the shared code area with tests.
- The Cross-Context Override table runs on it in production (the pilot,
  fixing the "rows stop after 100" bug).
