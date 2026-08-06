# Znane ograniczenia v0.5.1

## Techniczne

1. Aplikacja jest pojedynczym plikiem HTML i zapisuje stan w `localStorage`.
2. Nie ma backendu, synchronizacji, kont ani kontroli dostępu.
3. Dane zależą od profilu i pochodzenia przeglądarki; dlatego release wymaga uruchomienia przez lokalny serwer, nie przez przypadkowy adres `file://`.
4. Nie wykonano pełnych testów wielogodzinnych transkrypcji, bardzo dużych plików, konfliktów współbieżnej edycji ani migracji między schematami.
5. Audyt jest strukturalny, nie ocenia prawdziwości ani adekwatności semantycznej.
6. Warunek B korzysta z zewnętrznego ChatGPT ręcznie; nazwa i tryb modelu muszą zostać zapisane w sesji.
7. Materiały A, B i C różnią się, dlatego trudność materiału pozostaje czynnikiem zakłócającym indywidualny pilotaż.

## Metodologiczne

1. Walidacja 02 w obecnej formie jest indywidualnym pilotażem porównawczym, nie dowodem ogólnej skuteczności.
2. Sześć sesji nie pozwala na stabilne wnioskowanie statystyczne.
3. Efekt uczenia się można ograniczyć, lecz nie usunąć w badaniu jednej osoby.
4. Styl odpowiedzi może ujawnić recenzentowi warunek mimo usunięcia jawnego kodu A/B/C.
5. Wynik działania może zależeć od sytuacji, nie tylko od jakości analizy.

## Zakres

Release jest przeznaczony wyłącznie do fazy badawczej R0–R6. Nie powinien być wdrażany jako produkt ani używany do decyzji wysokiego ryzyka.
