# Przekazanie R0 niezależnemu testerowi

## Tester otrzymuje

- kompletny Companion Kit 1.0.1;
- instrukcję `README_FIRST.md`;
- lokalny panel reprodukcji;
- dokładną kopię plików baseline’u;
- automatyczne sprawdzenie SHA-256;
- generator raportu JSON i Markdown.

## Tester zwraca

1. raport JSON;
2. raport Markdown;
3. opis każdego błędu lub otrzymanej pomocy;
4. informację, czy test wykonano bez pomocy autora.

## Decyzja

Tylko `PASS_INDEPENDENT` może formalnie zamknąć R0. `PASS_TECHNICAL_NONINDEPENDENT` nie zamyka bramki.
