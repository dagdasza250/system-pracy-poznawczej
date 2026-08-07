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
| **CURRENT OPERATION** | `R2.2-B — Cardinality & Integrity Contract` |
| **CURRENT STATUS** | `IN_PROGRESS` |
| **LAST FROZEN** | `R2.2-A — Relation Inventory` |
| **NEXT ON PASS** | `R2.2 Review → APPROVE & FREEZE R2.2` |
| **NEXT AFTER FROZEN R2.2** | `R2.3 — Epistemic Status Contract` |

| Etap | Status |
|---|---|
| R0 | `CLOSED / FROZEN` |
| R1 | `CLOSED / FROZEN` |
| R2.1 | `CLOSED / FROZEN` |
| R2.2-A | `CLOSED / FROZEN` |
| **R2.2-B** | **`IN_PROGRESS`** |
| R2.3+ | `LOCKED` |
| R3–R6 / D0 | `LOCKED` |
| Product / AI / Beta / PROD | `LOCKED` |

---

## 2. CURRENT OPERATION

**R2.2-B — Cardinality & Integrity Contract**

**OBJECTIVE**  
Ustalić kardynalności, właściciela referencji i minimalne reguły integralności dla 27 relacji zamrożonych w R2.2-A.

**QUESTION**  
Dla każdej z 27 relacji: ile obiektów może/musi istnieć po obu stronach, kto przechowuje referencję, jaka integralność jest wymagana i co baseline faktycznie egzekwuje?

**ACTIVE OUTPUTS**
- [`research/R2.2_B_CARDINALITY_INTEGRITY_CONTRACT_DRAFT.md`](research/R2.2_B_CARDINALITY_INTEGRITY_CONTRACT_DRAFT.md)
- [`research/R2.2_B_RELATION_MATRIX_DRAFT.json`](research/R2.2_B_RELATION_MATRIX_DRAFT.json)
- [`research/R2.2_B_ISSUES.md`](research/R2.2_B_ISSUES.md)

---

## 3. CURRENT GATE

### Exit criterion R2.2-B

Dla każdej z 27 relacji musi być jednoznaczne:

- [ ] allowed;
- [ ] required / structural minimum;
- [ ] min cardinality;
- [ ] max cardinality;
- [ ] reference owner;
- [ ] referential integrity;
- [ ] orphan rule;
- [ ] sharing rule;
- [ ] cycle/self-loop rule, gdzie dotyczy;
- [ ] delete/archive boundary;
- [ ] schema enforcement status;
- [ ] zgodność z seedem i ścieżką aplikacji;
- [ ] rozwiązane blokery `B01–B04`;
- [ ] Review + RC1 przygotowane bez zmiany baseline'u.

**GATE STATUS:** `OPEN / DRAFT_FOR_REVIEW`

---

## 4. ACTIVE INPUTS / ARTIFACTS

### FROZEN — authoritative

- R0: `v0.5.1-experimental-baseline` · commit `c9f48db90506e0fc0fb9082e598ab0b3ef364d32`
- R1: [`research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md`](research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md)
- R2.1: [`research/R2.1_OBJECT_DICTIONARY_FROZEN.md`](research/R2.1_OBJECT_DICTIONARY_FROZEN.md)
- R2.2-A: [`research/R2.2_A_RELATION_INVENTORY_FROZEN.md`](research/R2.2_A_RELATION_INVENTORY_FROZEN.md)
- R2.2-A gate: [`research/R2.2_A_GATE_SIGNOFF.json`](research/R2.2_A_GATE_SIGNOFF.json)

### REFERENCE — baseline evidence

- JSON Schema v0.5.1
- seed v0.5.1
- frozen application behavior v0.5.1

---

## 5. SCOPE GUARD

### DO NOW

- pracować wyłącznie na 27 relacjach zamrożonych w R2.2-A;
- rozstrzygać kardynalności, reference ownership i integralność;
- odróżniać `required field` od `non-empty collection`;
- rozwiązać `B01–B04`;
- oznaczać, czego schema nie egzekwuje;
- przygotować R2.2-B do Review i RC1.

### DO NOT DO NOW

- nie zmieniać katalogu 30 relacji R2.2-A bez formalnego RETURN;
- nie rozstrzygać semantycznych minimów provenance — owner `R2.5`;
- nie projektować epistemic status — `R2.3`;
- nie projektować confidence — `R2.4`;
- nie definiować pełnego lifecycle/archive — `R2.6`;
- nie naprawiać JSON Schema — `R2.7`;
- nie przechodzić do R3, eksperymentu, AI ani Product;
- nie zmieniać baseline'u v0.5.1.

---

## 6. OPEN ISSUES

| Issue | Owner | Status | Blocking current? |
|---|---|---|---|
| `B01 Case.sourceIds`: exact set czy nadzbiór źródeł Episode | R2.2-B | `OPEN` | **YES** |
| `B02 Relation self-loop`: globalny zakaz czy zależny od typu | R2.2-B | `OPEN` | **YES** |
| `B03 ID uniqueness`: globalna czy case-local | R2.2-B | `OPEN` | **YES** |
| `B04 Action↔Result`: potwierdzić source of truth / reverse index | R2.2-B | `OPEN` | **YES** |
| Unit→Fragment semantic minimum | R2.5 | `DEFERRED` | NO |
| Hypothesis support/challenge semantic minimum | R2.5 | `DEFERRED` | NO |
| Fragment context target semantics | R2.5 + R2.7 | `DEFERRED` | NO |
| lifecycle delete/archive + Result→ModelVersion trigger | R2.6 | `DEFERRED` | NO |
| ModelVersion `$defs` gap | R2.7 | `DEFERRED` | NO |
| `confidence=confirmed` | R2.4 | `DEFERRED` | NO |

---

## 7. DECISION / FREEZE REGISTER

| Gate | Zamrożona decyzja | Evidence |
|---|---|---|
| R0 | v0.5.1 = zamrożony instrument eksperymentalny | baseline tag + `PASS_INDEPENDENT` |
| R1 | V1–V4 niezależne; C1–C2 osobne; AI value niewykazana | [`R1_GATE_SIGNOFF.json`](research/R1_GATE_SIGNOFF.json) |
| R2.1 | `Case=container`; `Segment≠Fragment`; `Unit(type=hipoteza)≠Hypothesis`; ModelVersion = ontology YES / schema gap | [`R2.1_GATE_SIGNOFF.json`](research/R2.1_GATE_SIGNOFF.json) |
| R2.2-A | 30 kandydatów sklasyfikowanych; 27 do R2.2-B; `Relation=UNIT_ONLY`; context IDs deferred; `Action.caseId` implementation-only | [`R2.2_A_GATE_SIGNOFF.json`](research/R2.2_A_GATE_SIGNOFF.json) |

**Frozen decision nie może zostać zmieniona po cichu. Konflikt wymaga formalnego RETURN.**

---

## 8. NEXT TRANSITION

### IF R2.2-B REVIEW PASS

`R2.2-B → READY_FOR_SIGNOFF`  
`R2.2 → READY_FOR_SIGNOFF`  
formalna decyzja: `APPROVE & FREEZE R2.2` albo `RETURN FOR REVISION R2.2`

### IF APPROVE & FREEZE R2.2

`R2.2 → CLOSED / FROZEN`  
`R2.3 → UNLOCKED / CURRENT`  
`PROJECT CONTROL.currentOperation → R2.3`

### IF R2.2-B REVIEW FAIL

`R2.2-B → IN_PROGRESS`  
`R2.3 → LOCKED`

---

## CONTROL INTEGRITY

1. `CLOSED / FROZEN` wymaga artefaktu bramki/evidence.
2. PROJECT CONTROL wskazuje kanoniczne frozen artifacts oraz aktywne artefakty CURRENT OPERATION.
3. Po każdej decyzji bramki PROJECT CONTROL jest aktualizowany natychmiast.
4. Stare roadmapy, README, raporty i rozmowy nie mogą nadpisywać `STATE_NOW`.
5. `RETURN` wymaga `FROM`, `TO`, `REASON`, `IMPACT`.
6. Przesunięcie CURRENT następuje wyłącznie po formalnym PASS/FREEZE.

---

**STATE_NOW:** `R2.2-B — Cardinality & Integrity Contract · IN_PROGRESS`
