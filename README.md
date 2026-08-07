# System Pracy Poznawczej (SPP)

Kanoniczne repozytorium programu SPP.

## Aktualny stan projektu

**Nie jest utrzymywany w README.**

Jedynym kanonicznym źródłem aktualnego stanu operacyjnego programu jest:

➡️ **[SPP PROJECT CONTROL v1](PROJECT_CONTROL.md)**

To tam sprawdzamy:
- gdzie projekt znajduje się teraz;
- jaka operacja jest CURRENT;
- co jest FROZEN / LOCKED;
- jaki artefakt tworzymy;
- jakie jest kryterium wyjścia;
- co zostanie odblokowane po PASS.

README nie może konkurować z PROJECT CONTROL przez przechowywanie własnego statusu etapu.

## Program

**Research → decyzja wartości → Product → badanie AI → beta i replikacja → produkcja**

## Struktura

- `PROJECT_CONTROL.md` — **kanoniczny pulpit stanu operacyjnego**;
- `baseline/` — zamrożone instrumenty eksperymentalne i dokumentacja release'ów;
- `research/` — kontrakty, audyty, bramki i artefakty fazy Research;
- `r0-companion/` — narzędzia niezależnej reprodukcji baseline'u;
- `program/` — mapa programu i materiały planistyczne;
- `docs/` — dokumentacja nadrzędna;
- GitHub history — historia zmian i decyzji.

## Zasada niezmienności

Baseline `v0.5.1-experimental-baseline` nie może być po cichu zmieniany. Każda poprawka wymaga jawnego procesu wersjonowania i kontroli integralności.

Zamrożone artefakty są źródłem prawdy merytorycznej. `PROJECT_CONTROL.md` jest źródłem prawdy o **STATE_NOW**.
