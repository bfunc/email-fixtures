# T1 — Foundations

## Why

Set the ground rules once, so every migration done by any team behaves
consistently.

## What

- Standard library setup with sensible defaults.
- A one-page conventions document (naming, keys come from the existing
  managed keys/URLs repository — no hardcoded values).
- A shared test helper so migrated components are easy to test.
- A lint guard: existing legacy usages are grandfathered, **new** legacy
  usage is blocked. The shrinking grandfather list doubles as the adoption
  metric.

## Done when

Setup, conventions, test helper and lint guard are merged; one existing
component proves the setup works.
