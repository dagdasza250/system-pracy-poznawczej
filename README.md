# System Pracy Poznawczej (SPP)

Kanoniczne repozytorium programu SPP.

## Program

**Research → decyzja wartości → Product → badanie AI → beta i replikacja → produkcja**

Aktualny etap: **R0.5 — niezależny test reprodukcji i podpisanie bramki R0**.

Do zamknięcia R0:
- baseline v0.5.1 jest zamrożony;
- artefakty techniczne R0.1–R0.4 są ukończone;
- Companion Kit 1.0.1 jest gotowy;
- oczekiwany jest niezależny test `PASS_INDEPENDENT`.

Do tego czasu **R1, R2–R6, Product i AI pozostają zablokowane**.

## Struktura

- `baseline/v0.5.1/` — zamrożony instrument eksperymentalny i dokumentacja release'u;
- `r0-companion/1.0.1/` — narzędzie niezależnej reprodukcji;
- `program/` — kanoniczna mapa etapów i status bramek;
- `docs/` — dokumentacja nadrzędna;
- GitHub Issues — bramki i jawne blokery programu.

## Zasada niezmienności

Baseline `v0.5.1-experimental-baseline` nie może być po cichu zmieniany. Każda poprawka wymaga nowego commita i jednoznacznie nowej wersji/release'u oraz ponownej kontroli integralności i reprodukcji.
