# SPP — Program Status

## Research phase

- R0 — `CLOSED`
- R1 — `CLOSED / FROZEN`
- R2 — `OPEN`
  - R2.1 — `CLOSED / FROZEN`
  - R2.2 — `IN PROGRESS`
    - R2.2-A Relation Inventory — `DRAFT_FOR_REVIEW`
    - R2.2-B Cardinality & Integrity Contract — `NOT STARTED`
  - R2.3 — `LOCKED`
  - R2.4 — `LOCKED`
  - R2.5 — `LOCKED`
  - R2.6 — `LOCKED`
  - R2.7 — `LOCKED`
  - R2.8 — `LOCKED`
  - R2.9 — `LOCKED`
- R3 — `LOCKED`
- R4 — `LOCKED`
- R5 — `LOCKED`
- R6 — `LOCKED`
- D0 — `LOCKED`

## Product / AI / beta / production

- P0–P7 — `LOCKED`
- A0–A2 — `LOCKED`
- B0–B2 — `LOCKED`
- PROD — `LOCKED`

## Current operation

**R2.2-A — Relation Inventory Review Gate**

R2.2 has formally started. The first relation inventory has been produced from the frozen v0.5.1 JSON Schema, seed and application behavior without modifying the baseline.

The inventory currently identifies 30 relation candidates and separates structural containment, explicit ID references, semantic `Relation(from,type,to)` edges, and implementation-only references.

Before R2.2-B can start, the R2.2-A Review Gate must resolve three questions:

1. whether `Relation.from/to` are Unit-only endpoints or polymorphic;
2. the target type of `Fragment.contextBeforeIds/contextAfterIds`;
3. whether `Action.caseId` is canonical ontology or only a redundant implementation backlink.

Until these decisions are reviewed and frozen:

- R2.2-A remains `DRAFT_FOR_REVIEW`;
- R2.2-B remains `NOT STARTED`;
- R2.3 and R3 remain `LOCKED`;
- the frozen `v0.5.1-experimental-baseline` remains unchanged.
