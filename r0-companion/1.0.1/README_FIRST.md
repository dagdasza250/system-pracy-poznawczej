# SPP v0.5.1 — niezależna reprodukcja bramki R0

Ten zestaw **nie zmienia baseline'u** `v0.5.1-experimental-baseline`. Jest wyłącznie narzędziem, które pozwala drugiej osobie odtworzyć i podpisać test.

## Najkrótsza procedura

1. Rozpakuj cały katalog.
2. Uruchom kontrolę integralności.
3. Uruchom lokalny serwer na porcie `8765`.
4. W panelu wykonuj kroki od 1 do 6.
5. Zamknij przeglądarkę zgodnie z instrukcją restartu, lecz pozostaw serwer włączony.
6. Wygeneruj raport JSON i Markdown.
7. Przekaż oba raporty właścicielowi projektu.

## Ważne

- Używaj portu `8765` przez cały test. `localStorage` jest przypisane do adresu i portu.
- Test powinien być wykonany na czystym profilu lub w nowym profilu przeglądarki.
- Tester nie powinien otrzymywać pomocy podczas przechodzenia procesu.
- Wynik `FAIL` nie może zostać poprawiony ręcznie w raporcie.
