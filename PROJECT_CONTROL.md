# SPP PROJECT CONTROL v1

> **Jedyny kanoniczny zapis aktualnego stanu operacyjnego programu SPP.**  
> Nie zastępuje zamrożonych artefaktów merytorycznych. Odpowiada wyłącznie: **gdzie jesteśmy i co wolno zrobić teraz?**

**CONTROL VERSION:** `1.0`  
**LAST UPDATED:** `2026-08-07 09:19 +02:00`  
**PROGRAM PHASE:** `RESEARCH`  
**STATUS VOCABULARY:** `LOCKED · UNLOCKED · IN_PROGRESS · READY_FOR_SIGNOFF · FROZEN · CLOSED · RETURNED · BLOCKED`

---

## 1. PROGRAM STATE

| Pole | Stan |
|---|---|
| **CURRENT STAGE** | `R2 — Minimalna ontologia eksperymentalna` |
| **CURRENT OPERATION** | `R2.2-A — Relation Inventory Review Gate` |
| **CURRENT STATUS** | `IN_PROGRESS` |
| **LAST FROZEN** | `R2.1 — Canonical Object Dictionary` |
| **NEXT ON PASS** | `R2.2-B — Cardinality & Integrity Contract` |
| **NEXT AFTER FROZEN R2.2** | `R2.3 — Epistemic Status Contract` |

| Etap | Status |
|---|---|
| R0 | `CLOSED / FROZEN` |
| R1 | `CLOSED / FROZEN` |
| R2.1 | `CLOSED / FROZEN` |
| **R2.2-A** | **`IN_PROGRESS`** |
| R2.2-B | `LOCKED` |
| R2.3+ | `LOCKED` |
| R3–R6 / D0 | `LOCKED` |
| Product / AI / Beta / PROD | `LOCKED` |

---

## 2. CURRENT OPERATION

**R2.2-A — Relation Inventory Review Gate**

**OBJECTIVE**  
Zamknąć i zamrozić inwentarz relacji faktycznie istniejących w baseline v0.5.1, zanim zostaną przypisane kardynalności.

**QUESTION**  
Czy wszystkie relacje są poprawnie sklasyfikowane oraz jak rozstrzygamy trzy niejasności blokujące przejście do R2.2-B?

**ACTIVE OUTPUT**  
[`research/R2.2_RELATION_INVENTORY_DRAFT.md`](research/R2.2_RELATION_INVENTORY_DRAFT.md)

**ISSUE REGISTER**  
[`research/R2.2_RELATION_INVENTORY_ISSUES.json`](research/R2.2_RELATION_INVENTORY_ISSUES.json)

---

## 3. CURRENT GATE

### Exit criterion R2.2-A

- [ ] `U01` — rozstrzygnięto domenę `Relation.from/to`;
- [ ] `U02` — rozstrzygnięto typ docelowy `Fragment.contextBeforeIds/contextAfterIds`;
- [ ] `U03` — rozstrzygnięto status `Action.caseId`;
- [ ] wszystkie 30 kandydatów relacji ma jednoznaczną klasyfikację;
- [ ] nie wprowadzono jeszcze kardynalności należących do R2.2-B;
- [ ] baseline `v0.5.1-experimental-baseline` pozostał niezmieniony;
- [ ] Review Gate zakończył się decyzją `APPROVE & FREEZE R2.2-A`.

**GATE STATUS:** `OPEN`

---

## 4. ACTIVE INPUTS / ARTIFACTS

### FROZEN — authoritative

- R0: `v0.5.1-experimental-baseline` · commit `c9f48db90506e0fc0fb9082e598ab0b3ef364d32`
- R1: [`research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md`](research/R1_EXPERIMENTAL_VALUE_CONTRACT_FROZEN.md)
- R1 gate: [`research/R1_GATE_SIGNOFF.json`](research/R1_GATE_SIGNOFF.json)
- R2.1: [`research/R2.1_OBJECT_DICTIONARY_FROZEN.md`](research/R2.1_OBJECT_DICTIONARY_FROZEN.md)
- R2.1 gate: [`research/R2.1_GATE_SIGNOFF.json`](research/R2.1_GATE_SIGNOFF.json)

### REFERENCE — baseline evidence

- JSON Schema v0.5.1
- seed v0.5.1
- frozen application behavior v0.5.1

**Rule:** PROJECT CONTROL wskazuje artefakty; nie kopiuje ich treści.

---

## 5. SCOPE GUARD

### DO NOW

- review 30 kandydatów relacji;
- rozstrzygnąć `U01`, `U02`, `U03`;
- oddzielać `containment`, `explicit reference`, `semantic edge`, `implementation reference`;
- przygotować inwentarz do `APPROVE & FREEZE R2.2-A`.

### DO NOT DO NOW

- kardynalności `1:1 / 1:N / N:M` — właściciel: `R2.2-B`;
- epistemic status — `R2.3`;
- confidence — `R2.4`;
- provenance — `R2.5`;
- lifecycle / pełna semantyka ModelVersion — `R2.6`;
- naprawa JSON Schema — ocena zgodności: `R2.7`;
- UX / R3 / eksperyment / AI / Product;
- jakakolwiek cicha zmiana baseline’u v0.5.1.

---

## 6. OPEN ISSUES

| Issue | Owner | Status | Blocking current? |
|---|---|---|---|
| `U01 Relation.from/to`: Unit-only czy polymorphic | R2.2-A | `OPEN` | **YES** |
| `U02 Fragment.contextBefore/After`: typ celu | R2.2-A | `OPEN` | **YES** |
| `U03 Action.caseId`: ontologia czy backlink implementacyjny | R2.2-A | `OPEN` | **YES** |
| ModelVersion bez `$defs/modelVersion` | R2.7 | `DEFERRED` | NO |
| `confidence=confirmed` miesza osie znaczeniowe | R2.4 | `DEFERRED` | NO |

**Rule:** problem spoza bieżącego zakresu otrzymuje `OWNER` i `DEFERRED`; nie przerywa CURRENT WORK, jeśli nie jest blokujący.

---

## 7. DECISION / FREEZE REGISTER

| Gate | Zamrożona decyzja | Evidence |
|---|---|---|
| R0 | v0.5.1 = zamrożony instrument eksperymentalny | baseline tag + niezależny `PASS_INDEPENDENT` |
| R1 | V1–V4 są niezależne; C1–C2 są osobnymi kosztami; AI value nie jest wykazana | [`R1_GATE_SIGNOFF.json`](research/R1_GATE_SIGNOFF.json) |
| R2.1 | `Case = container`, `Segment ≠ Fragment`, `Unit(type=hipoteza) ≠ Hypothesis`, `ModelVersion = ontology YES / SCHEMA_GAP` | [`R2.1_GATE_SIGNOFF.json`](research/R2.1_GATE_SIGNOFF.json) |

**Frozen decision nie może zostać zmieniona po cichu.** Konflikt wymaga formalnego `RETURN`.

---

## 8. NEXT TRANSITION

### IF PASS R2.2-A

`R2.2-A → CLOSED / FROZEN`  
`R2.2-B → UNLOCKED / CURRENT`  
`PROJECT CONTROL.currentOperation → R2.2-B`

### IF FAIL R2.2-A

`R2.2-A → IN_PROGRESS`  
`R2.2-B → LOCKED`

### IF LATER PASS + FREEZE COMPLETE R2.2

`R2.2 → CLOSED / FROZEN`  
`R2.3 → UNLOCKED / CURRENT`  
`PROJECT CONTROL.currentOperation → R2.3`

---

## CONTROL INTEGRITY

1. Status `CLOSED / FROZEN` wymaga wskazanego artefaktu bramki/evidence.
2. PROJECT CONTROL wskazuje wyłącznie **kanoniczne frozen artifacts**, nie drafty historyczne — poza jednym aktywnym artefaktem CURRENT OPERATION.
3. Zmiana bramki wymaga natychmiastowej aktualizacji tego pliku.
4. Stare roadmapy, README, raporty i rozmowy **nie mogą nadpisywać STATE_NOW**.
5. `RETURN` musi wskazać: `FROM`, `TO`, `REASON`, `IMPACT`; etap docelowy otrzymuje `RETURNED`, a zależne późniejsze etapy są blokowane do ponownego freeze.
6. PROJECT CONTROL nie zmienia merytoryki automatycznie. Przesunięcie CURRENT następuje wyłącznie po formalnym PASS/FREEZE.

---

**STATE_NOW:** `R2.2-A — Relation Inventory Review Gate · IN_PROGRESS`
