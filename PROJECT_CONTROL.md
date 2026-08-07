# SPP PROJECT CONTROL v1

> **Jedyny kanoniczny zapis aktualnego stanu operacyjnego programu SPP.**  
> Zamrożone artefakty = prawda merytoryczna. PROJECT CONTROL = prawda o `STATE_NOW`.

**CONTROL VERSION:** `1.0`  
**LAST UPDATED:** `2026-08-07 09:36 +02:00`  
**PROGRAM PHASE:** `RESEARCH`  
**STATUS VOCABULARY:** `LOCKED · UNLOCKED · IN_PROGRESS · READY_FOR_SIGNOFF · FROZEN · CLOSED · RETURNED · BLOCKED`

---

## 1. PROGRAM STATE

| Pole | Stan |
|---|---|
| **CURRENT STAGE** | `R2 — Minimalna ontologia eksperymentalna` |
| **CURRENT OPERATION** | `R2.2-A — Relation Inventory Review Gate` |
| **CURRENT STATUS** | `READY_FOR_SIGNOFF` |
| **LAST FROZEN** | `R2.1 — Canonical Object Dictionary` |
| **NEXT ON PASS** | `R2.2-B — Cardinality & Integrity Contract` |
| **NEXT AFTER FROZEN R2.2** | `R2.3 — Epistemic Status Contract` |

| Etap | Status |
|---|---|
| R0 | `CLOSED / FROZEN` |
| R1 | `CLOSED / FROZEN` |
| R2.1 | `CLOSED / FROZEN` |
| **R2.2-A** | **`READY_FOR_SIGNOFF`** |
| R2.2-B | `LOCKED` |
| R2.3+ | `LOCKED` |
| R3–R6 / D0 | `LOCKED` |
| Product / AI / Beta / PROD | `LOCKED` |

---

## 2. CURRENT OPERATION

**R2.2-A — Relation Inventory Review Gate**

**OBJECTIVE**  
Zamknąć i zamrozić inwentarz relacji baseline v0.5.1 przed przypisaniem kardynalności.

**REVIEW RESULT**
- `U01 Relation.from/to` → `UNIT_ONLY`;
- `U02 Fragment.contextBefore/After` → `UNRESOLVED_SCHEMA_GAP`, owner `R2.5/R2.7`;
- `U03 Action.caseId` → `IMPLEMENTATION_REFERENCE / REDUNDANT_BACKLINK`;
- `30/30` kandydatów sklasyfikowanych;
- `27` relacji przechodzi do R2.2-B.

**RC1**  
[`research/R2.2_RELATION_INVENTORY_RC1.md`](research/R2.2_RELATION_INVENTORY_RC1.md)

**REVIEW REPORT**  
[`research/R2.2_A_REVIEW_GATE_REPORT.md`](research/R2.2_A_REVIEW_GATE_REPORT.md)

**ISSUE REGISTER**  
[`research/R2.2_RELATION_INVENTORY_ISSUES.json`](research/R2.2_RELATION_INVENTORY_ISSUES.json)

---

## 3. CURRENT GATE

### Exit criterion R2.2-A

- [x] `U01` rozstrzygnięte;
- [x] `U02` rozstrzygnięte bez zgadywania typu docelowego;
- [x] `U03` rozstrzygnięte;
- [x] 30/30 kandydatów ma jednoznaczną klasyfikację;
- [x] wskazano 27 relacji dla R2.2-B;
- [x] nie przypisano kardynalności;
- [x] baseline pozostał niezmieniony;
- [x] powstały Review Report i RC1;
- [ ] formalna decyzja `APPROVE & FREEZE R2.2-A`.

**GATE STATUS:** `READY_FOR_SIGNOFF`

---

## 4. ACTIVE INPUTS / ARTIFACTS

### FROZEN — authoritative

- R0: `v0.5.1-experimental-baseline` · commit `c9f48db90506e0fc0fb9082e598ab0b3ef364d32`
- R1: [`research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md`](research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md)
- R1 gate: [`research/R1_GATE_SIGNOFF.json`](research/R1_GATE_SIGNOFF.json)
- R2.1: [`research/R2.1_OBJECT_DICTIONARY_FROZEN.md`](research/R2.1_OBJECT_DICTIONARY_FROZEN.md)
- R2.1 gate: [`research/R2.1_GATE_SIGNOFF.json`](research/R2.1_GATE_SIGNOFF.json)

### CURRENT — pending freeze

- [`research/R2.2_RELATION_INVENTORY_RC1.md`](research/R2.2_RELATION_INVENTORY_RC1.md)
- [`research/R2.2_A_REVIEW_GATE_REPORT.md`](research/R2.2_A_REVIEW_GATE_REPORT.md)

### REFERENCE

- JSON Schema v0.5.1
- seed v0.5.1
- frozen application behavior v0.5.1

---

## 5. SCOPE GUARD

### DO NOW

- review RC1 i Review Report;
- podjąć decyzję `APPROVE & FREEZE R2.2-A` albo `RETURN FOR REVISION R2.2-A`.

### DO NOT DO NOW

- nie rozpoczynać kardynalności — `R2.2-B` nadal `LOCKED`;
- nie rozstrzygać provenance `R2.5`, confidence `R2.4`, lifecycle `R2.6` ani naprawy schema `R2.7`;
- nie przechodzić do R3, eksperymentu, AI ani Product;
- nie zmieniać baseline'u v0.5.1.

---

## 6. OPEN ISSUES

| Issue | Owner | Status | Blocking current? |
|---|---|---|---|
| target `Fragment.contextBefore/After` | R2.5 + R2.7 | `DEFERRED` | NO |
| ModelVersion bez `$defs/modelVersion` | R2.7 | `DEFERRED` | NO |
| Result → ModelVersion jako lifecycle trigger, bez direct ID | R2.6 | `DEFERRED` | NO |
| `confidence=confirmed` miesza osie | R2.4 | `DEFERRED` | NO |

**CURRENT BLOCKERS:** none merytoryczne. Pozostaje formalny sign-off.

---

## 7. DECISION / FREEZE REGISTER

| Gate | Zamrożona decyzja | Evidence |
|---|---|---|
| R0 | v0.5.1 = zamrożony instrument eksperymentalny | baseline tag + `PASS_INDEPENDENT` |
| R1 | V1–V4 niezależne; C1–C2 osobne; AI value niewykazana | [`R1_GATE_SIGNOFF.json`](research/R1_GATE_SIGNOFF.json) |
| R2.1 | `Case=container`; `Segment≠Fragment`; `Unit(type=hipoteza)≠Hypothesis`; ModelVersion = ontology YES / schema gap | [`R2.1_GATE_SIGNOFF.json`](research/R2.1_GATE_SIGNOFF.json) |

R2.2-A decisions są **reviewed, ale jeszcze nie frozen**.

---

## 8. NEXT TRANSITION

### IF APPROVE & FREEZE R2.2-A

`R2.2-A → CLOSED / FROZEN`  
`R2.2-B → UNLOCKED / CURRENT`  
`PROJECT CONTROL.currentOperation → R2.2-B`

### IF RETURN FOR REVISION R2.2-A

`R2.2-A → IN_PROGRESS`  
`R2.2-B → LOCKED`

### AFTER LATER FREEZE COMPLETE R2.2

`R2.2 → CLOSED / FROZEN`  
`R2.3 → UNLOCKED / CURRENT`

---

## CONTROL INTEGRITY

1. `CLOSED / FROZEN` wymaga artefaktu bramki/evidence.
2. PROJECT CONTROL wskazuje kanoniczne frozen artifacts oraz jeden aktywny RC/current artifact.
3. Po każdej decyzji bramki PROJECT CONTROL jest aktualizowany natychmiast.
4. Stare roadmapy, README, raporty i rozmowy nie mogą nadpisywać `STATE_NOW`.
5. `RETURN` wymaga `FROM`, `TO`, `REASON`, `IMPACT`.
6. Przesunięcie CURRENT następuje wyłącznie po formalnym PASS/FREEZE.

---

**STATE_NOW:** `R2.2-A — Relation Inventory Review Gate · READY_FOR_SIGNOFF`
