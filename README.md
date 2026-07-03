# Epic: Modern data fetching — paved road, gradual adoption

Our frontend fetches data through custom, home-grown services that are hard
to maintain and slow every new feature down. TanStack Query is the industry
standard that does the same job out of the box.

The legacy services are used in hundreds of places across many team areas, so
a central rewrite is not realistic. Instead, this epic delivers a **paved
road**: shared building blocks, one verified example for every fetching
pattern, and a guardrail that blocks new legacy usage. Teams then migrate
their own areas at their own pace.

**Out of scope:** mass migration and deletion of the legacy services. A
future decommission epic starts once adoption is complete — tracked by a
visible counter (T6).

## Tickets

- T1 — Foundations
- T2 — Data freshness for migrated components
- T3 — Reusable infinite-scroll grid data source
- T4 — Reference examples (one per pattern)
- T5 — Cookbook and adoption guide
- T6 — Adoption tracking and rollout
