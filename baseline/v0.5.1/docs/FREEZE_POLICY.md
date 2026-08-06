# Polityka zamrożenia SPP v0.5.1

## Status

`FROZEN_FOR_RESEARCH_BASELINE`

## Cel

Zapewnienie, że wyniki sesji R6 odnoszą się do tej samej metody i tej samej implementacji.

## Dozwolone przed pierwszą właściwą sesją

- naprawa błędu uniemożliwiającego uruchomienie, zapis lub eksport;
- instrumentacja wykrywająca awarię bez zmiany treści zadania;
- korekta dokumentacji reprodukcji;
- korekta protokołu wyłącznie przed jego formalnym zamrożeniem w R5.

## Zabronione

- dodawanie nowych operacji analitycznych lub AI;
- zmiana pytań, pól albo struktury warunku C w celu poprawienia wyniku;
- zmiana materiału bez zastosowania zamrożonej reguły zastąpienia;
- poprawianie instrukcji pomiędzy właściwymi sesjami;
- nadpisywanie baseline'u tym samym tagiem;
- ukrywanie błędu albo odchylenia protokołu.

## Procedura koniecznej poprawki

1. Utworzyć osobną gałąź i wersję patch.
2. Opisać błąd, zmianę i wpływ na wyniki.
3. Powtórzyć test reprodukcji.
4. Zdecydować, czy wcześniejsze sesje pozostają porównywalne.
5. Nigdy nie przesuwać istniejącego tagu baseline.

## Odpowiedzialność

Każda zmiana po baseline wymaga jawnego wpisu w changelogu i osobnego hasha release'u.
