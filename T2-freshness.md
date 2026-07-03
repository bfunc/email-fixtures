# T2 — Data freshness for migrated components

## Why

The current freshness system (RefreshMonitor) forces every fetching component
into complex custom machinery. Migrated components need a much simpler way to
provide the same user-facing features.

## What

Preserve exactly three user-facing functions, unchanged in behavior:

1. Last-update info and the refresh button.
2. "Data partially unavailable" alert (error handling).
3. Data-inconsistency alert — needed on **one page only**, which will be
   migrated as a whole (see T4).

The background update poller stays as is. Freshness wiring is built into the
standard fetching approach, so teams get it automatically. Old and new
components coexist on the same page indefinitely; the legacy RefreshMonitor
is **not** modified or removed.

## Done when

All three functions work on migrated and mixed pages exactly as today.

