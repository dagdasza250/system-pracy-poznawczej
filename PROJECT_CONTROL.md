# SPP PROJECT CONTROL v1

> **Jedyny kanoniczny zapis aktualnego stanu operacyjnego programu SPP.**  
> Zamrożone artefakty = prawda merytoryczna. PROJECT CONTROL = prawda o `STATE_NOW`.

**CONTROL VERSION:** `1.0`  
**LAST UPDATED:** `2026-08-07 11:09 +02:00`  
**PROGRAM PHASE:** `RESEARCH`  
**STATUS VOCABULARY:** `LOCKED · UNLOCKED · IN_PROGRESS · READY_FOR_SIGNOFF · FROZEN · CLOSED · RETURNED · BLOCKED`

---

## 1. PROGRAM STATE

| Pole | Stan |
|---|---|
| **CURRENT STAGE** | `R2 — Minimalna ontologia eksperymentalna` |
| **CURRENT OPERATION** | `R2.2 — Relations & Cardinalities Final Signoff` |
| **CURRENT STATUS** | `READY_FOR_SIGNOFF` |
| **LAST FROZEN** | `R2.2-A — Relation Inventory` |
| **NEXT ON PASS** | `R2.3 — Epistemic Status Contract` |
| **NEXT IF RETURN** | `R2.2-B — Cardinality & Integrity Contract` |

| Etap | Status |
|---|---|
| R0 | `CLOSED / FROZEN` |
| R1 | `CLOSED / FROZEN` |
| R2.1 | `CLOSED / FROZEN` |
| R2.2-A | `CLOSED / FROZEN` |
| R2.2-B | `READY_FOR_SIGNOFF` |
| **R2.2** | **`READY_FOR_SIGNOFF`** |
| R2.3+ | `LOCKED` |
| R3–R6 / D0 | `LOCKED` |
| Product / AI / Beta / PROD | `LOCKED` |

---

## 2. CURRENT OPERATION

**R2.2 — Relations & Cardinalities Final Signoff**

**OBJECTIVE**  
Podjąć formalną decyzję wobec ukończonego Review R2.2-B i RC1 całego kontraktu relacji, kardynalności oraz integralności.

**REVIEW RESULT**
- `27/27` relacji ma strukturalną kardynalność, owner i regułę integralności;
- `B01` → `SUPERSET_ALLOWED`;
- `B02` → `SELF_LOOP_PROHIBITED`;
- `B03` → `GLOBAL_STATE_UNIQUE`;
- `B04` → `Result.actionId = SOURCE_OF_TRUTH`; `Action.resultIds = optional reverse index`;
- brak blokujących issues;
- baseline v0.5.1 pozostał niezmieniony.

**RC1**
- [`research/R2.2_CARDINALITY_INTEGRITY_CONTRACT_RC1.md`](research/R2.2_CARDINALITY_INTEGRITY_CONTRACT_RC1.md)
- [`research/R2.2_B_RELATION_MATRIX_RC1.json`](research/R2.2_B_RELATION_MATRIX_RC1.json)

**REVIEW**
- [`research/R2.2_B_REVIEW_GATE_REPORT.md`](research/R2.2_B_REVIEW_GATE_REPORT.md)
- [`research/R2.2_B_ISSUES_REVIEWED.md`](research/R2.2_B_ISSUES_REVIEWED.md)

---

## 3. CURRENT GATE

### Exit criterion R2.2

- [x] R2.2-A Relation Inventory zamrożone;
- [x] 27 relacji weszło do R2.2-B;
- [x] allowed ustalone;
- [x] required / structural minimum ustalone;
- [x] min/max cardinality ustalone;
- [x] reference owner ustalony;
- [x] referential integrity ustalona;
- [x] orphan/delete boundary ustalona;
- [x] sharing/cycle rule ustalone tam, gdzie dotyczy;
- [x] schema enforcement sklasyfikowane;
- [x] B01–B04 rozstrzygnięte;
- [x] Review + RC1 przygotowane;
- [x] baseline pozostał niezmieniony;
- [ ] formalna decyzja `APPROVE & FREEZE R2.2`.

**GATE STATUS:** `READY_FOR_SIGNOFF`

---

## 4. ACTIVE INPUTS / ARTIFACTS

### FROZEN — authoritative

- R0: `v0.5.1-experimental-baseline` · commit `c9f48db90506e0fc0fb9082e598ab0b3ef364d32`
- R1: [`research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md`](research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md)
- R2.1: [`research/R2.1_OBJECT_DICTIONARY_FROZEN.md`](research/R2.1_OBJECT_DICTIONARY_FROZEN.md)
- R2.2-A: [`research/R2.2_A_RELATION_INVENTORY_FROZEN.md`](research/R2.2_A_RELATION_INVENTORY_FROZEN.md)
- R2.2-A gate: [`research/R2.2_A_GATE_SIGNOFF.json`](research/R2.2_A_GATE_SIGNOFF.json)

### CURRENT — reviewed RC1

- [`research/R2.2_CARDINALITY_INTEGRITY_CONTRACT_RC1.md`](research/R2.2_CARDINALITY_INTEGRITY_CONTRACT_RC1.md)
- [`research/R2.2_B_RELATION_MATRIX_RC1.json`](research/R2.2_B_RELATION_MATRIX_RC1.json)
- [`research/R2.2_B_REVIEW_GATE_REPORT.md`](research/R2.2_B_REVIEW_GATE_REPORT.md)

---

## 5. SCOPE GUARD

### DO NOW

- podjąć wyłącznie decyzję `APPROVE & FREEZE R2.2` albo `RETURN FOR REVISION R2.2`;
- w razie PASS utworzyć frozen contract, gate evidence, hash i zaktualizować PROJECT CONTROL.

### DO NOT DO NOW

- nie rozpoczynać R2.3 przed PASS R2.2;
- nie otwierać R2.5 provenance, R2.4 confidence, R2.6 lifecycle ani R2.7 schema repair;
- nie zmieniać frozen R2.2-A;
- nie zmieniać baseline'u v0.5.1;
- nie przechodzić do R3, eksperymentu, AI ani Product.

---

## 6. OPEN ISSUES

### Blocking current

**NONE**

### Deferred

| Issue | Owner | Status |
|---|---|---|
| Unit→Fragment semantic minimum | R2.5 | `DEFERRED` |
| Hypothesis support/challenge semantic minimum | R2.5 | `DEFERRED` |
| Fragment context target semantics | R2.5 + R2.7 | `DEFERRED` |
| lifecycle delete/archive + Result→ModelVersion trigger | R2.6 | `DEFERRED` |
| ModelVersion `$defs` gap | R2.7 | `DEFERRED` |
| `confidence=confirmed` | R2.4 | `DEFERRED` |

---

## 7. DECISION / FREEZE REGISTER

| Gate | Zamrożona decyzja | Evidence |
|---|---|---|
| R0 | v0.5.1 = zamrożony instrument eksperymentalny | baseline tag + `PASS_INDEPENDENT` |
| R1 | V1–V4 niezależne; C1–C2 osobne; AI value niewykazana | [`R1_GATE_SIGNOFF.json`](research/R1_GATE_SIGNOFF.json) |
| R2.1 | `Case=container`; `Segment≠Fragment`; `Unit(type=hipoteza)≠Hypothesis`; ModelVersion = ontology YES / schema gap | [`R2.1_GATE_SIGNOFF.json`](research/R2.1_GATE_SIGNOFF.json) |
| R2.2-A | 30 kandydatów sklasyfikowanych; 27 do R2.2-B; `Relation=UNIT_ONLY`; context IDs deferred; `Action.caseId` implementation-only | [`R2.2_A_GATE_SIGNOFF.json`](research/R2.2_A_GATE_SIGNOFF.json) |

R2.2-B decisions są **reviewed, ale nie frozen do czasu decyzji całego R2.2**.

---

## 8. NEXT TRANSITION

### IF APPROVE & FREEZE R2.2

`R2.2 → CLOSED / FROZEN`  
`R2.3 → UNLOCKED / CURRENT`  
`PROJECT CONTROL.currentOperation → R2.3 — Epistemic Status Contract`

### IF RETURN FOR REVISION R2.2

`R2.2-B → IN_PROGRESS`  
`R2.2 → OPEN`  
`R2.3 → LOCKED`

---

## CONTROL INTEGRITY

1. `CLOSED / FROZEN` wymaga artefaktu bramki/evidence.
2. PROJECT CONTROL wskazuje kanoniczne frozen artifacts oraz reviewed RC1 bieżącej bramki.
3. Po każdej decyzji bramki PROJECT CONTROL jest aktualizowany natychmiast.
4. Stare roadmapy, README, raporty i rozmowy nie mogą nadpisywać `STATE_NOW`.
5. `RETURN` wymaga `FROM`, `TO`, `REASON`, `IMPACT`.
6. Przesunięcie CURRENT następuje wyłącznie po formalnym PASS/FREEZE.

---

**STATE_NOW:** `R2.2 — Relations & Cardinalities Final Signoff · READY_FOR_SIGNOFF`
