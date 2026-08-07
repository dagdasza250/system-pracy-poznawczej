# SPP v0.5.1 Experimental Value Contract

**Etap programu:** R1 — Minimalny kontrakt wartości  
**Wersja dokumentu:** 1.0  
**Status:** APPROVED_AND_FROZEN  
**Baseline:** `v0.5.1-experimental-baseline`  
**Commit baseline’u:** `c9f48db90506e0fc0fb9082e598ab0b3ef364d32`  
**Data zatwierdzenia R1:** 2026-08-07  
**Decyzja bramki:** `APPROVE & FREEZE R1`  
**Identyfikator zatwierdzającego:** `PROJECT_OWNER`  
**Zakres:** Walidacja poznawcza 02 — indywidualny pilotaż porównawczy  
**Nadrzędna zasada:** ten dokument określa *co jest wartością SPP i co wolno uznać za koszt*. Nie definiuje jeszcze pełnej rubryki, progów GO ani ontologii R2.

---

## 0. Cel kontraktu

R1 zamraża przedmiot przyszłego pomiaru, zanim zostaną dopracowane ontologia, UX eksperymentalny, stabilność i protokół.

SPP v0.5.1 jest traktowany jako **zamrożony instrument eksperymentalny**, a nie jako MVP produktu.

Główna hipoteza wartości brzmi:

> Lepsze myślenie nie wynika wyłącznie z otrzymania inteligentnej odpowiedzi. Powstaje wtedy, gdy człowiek może zobaczyć, kontrolować i korygować drogę od źródła przez interpretację i model do działania.

Badanie nie ma wykazać, czy „SPP działa” w sensie ogólnym. Ma ustalić, **czy i w których wymiarach struktura SPP daje korzyść netto w obecnej klasie spraw w porównaniu z notatkami swobodnymi i standardowym ChatGPT**.

---

## 1. Badany użytkownik

### 1.1. Jednostka badana

Uczestnik pilotażu otrzymuje pseudonim:

**P01**

Tożsamość uczestnika nie jest częścią publicznego kontraktu.

P01:
- jest jedną osobą wykonującą wszystkie sześć właściwych sesji;
- wykonuje po dwie sesje w warunkach A, B i C;
- pracuje na różnych, wcześniej dopasowanych materiałach;
- nie wykonuje więcej niż jednej właściwej sesji dziennie;
- nie wraca do wcześniejszych rezultatów przed zakończeniem pełnej sekwencji, zgodnie z protokołem R5.

### 1.2. Zakres wnioskowania

Pilotaż P01 jest **badaniem eksploracyjnym N=1**.

Może dostarczyć danych o:
- wykonalności metody;
- kierunku potencjalnych różnic;
- kosztach użycia;
- problemach metodologicznych i UX;
- zasadności większej walidacji.

Nie może samodzielnie wykazać skuteczności SPP dla innych użytkowników ani populacji.

---

## 2. Klasa spraw objęta R1

### 2.1. Klasa docelowa pilotażu

R1 dotyczy wyłącznie:

**złożonych, transkrybowanych rozmów wieloperspektywicznych, w których występuje rozbieżność stanowisk lub znaczeń, a analiza ma prowadzić od rekonstrukcji źródła do lepszego modelu problemu i praktycznego działania.**

W szczególności materiał powinien zawierać co najmniej część następujących własności:
- co najmniej dwa stanowiska lub perspektywy;
- pojęcia używane w różnych znaczeniach;
- argumenty, kontrargumenty, wyjątki albo niejawne założenia;
- możliwość pomylenia wypowiedzi źródłowej z interpretacją;
- więcej niż jedną rozsądną interpretację;
- niepewność, sprzeczność lub niepełność informacji;
- możliwość sformułowania praktycznego działania, procedury lub eksperymentu.

### 2.2. Materiał obecnego pilotażu

Walidacja 02 używa sześciu niezmienionych fragmentów jednej naturalnej rozmowy dotyczącej stabilności finansowej, niezależności, pracy, pieniędzy i związanych z nimi różnic perspektyw.

Każdy materiał posiada:
- identyfikator;
- dokładny tekst źródłowy;
- lokalizację w źródle;
- liczbę słów;
- SHA-256.

Materiały są różne między sesjami, aby ograniczyć transfer rozumienia. Ich porównywalność musi zostać formalnie oceniona w R5.

### 2.3. Poza zakresem

R1 nie rozszerza wyniku pilotażu na:
- teksty naukowe;
- dokumenty prawne;
- dokumentację medyczną;
- programowanie;
- uczenie szkolne;
- wiadomości i research internetowy;
- decyzje wysokiego ryzyka;
- wielomiesięczne projekty;
- pracę zespołową lub wieloużytkownikową.

Takie klasy wymagają osobnych badań.

---

## 3. Problem poznawczy

### 3.1. Problem bazowy

W złożonej rozmowie użytkownik musi przejść od surowego materiału do uzasadnionego rozumienia bez utraty śladu pochodzenia.

Problem obejmuje jednocześnie:
1. odróżnienie tego, co faktycznie zostało powiedziane, od interpretacji;
2. rozpoznanie głównych stanowisk, tez, założeń, niepewności i sprzeczności;
3. rozważenie alternatywnych wyjaśnień;
4. połączenie ważnych wniosków z podstawą źródłową;
5. zbudowanie spójnego modelu problemu;
6. przełożenie modelu na testowalne działanie;
7. możliwość późniejszego odtworzenia, dlaczego dany wniosek lub działanie zostało przyjęte.

### 3.2. Pytanie porównawcze

> Czy w tej klasie spraw struktura SPP v0.5.1 daje lepszy profil wartości poznawczej niż:
> **A — notatki swobodne** oraz **B — standardowa analiza ChatGPT**, przy uwzględnieniu czasu i obciążenia poznawczego?

Warunek C bada **ręczną strukturę SPP bez zintegrowanego silnika AI**.

Dlatego wynik C nie może być interpretowany jako dowód wartości przyszłego „AI SPP”.

---

# 4. Cztery niezależne wartości

Żadna z czterech wartości nie może zastępować pozostałych.

Nie tworzy się jednego ukrytego „score SPP”, który zacierałby różnice między wymiarami.

## V1 — Jakość rozumowania

### Definicja

**Jakość rozumowania** oznacza stopień, w jakim końcowe opracowanie tworzy trafny, źródłowo zgodny, wystarczająco kompletny i epistemicznie ostrożny model badanego problemu.

Obejmuje:
- poprawną rekonstrukcję kluczowych stanowisk;
- rozdzielenie źródła od interpretacji;
- brak dopowiadania faktów spoza materiału;
- rozpoznanie ważnych niepewności i założeń;
- uwzględnienie uzasadnionych alternatywnych interpretacji;
- spójność mechanizmu/modelu;
- adekwatność wniosków do materiału.

### Nie jest tym:
- długość odpowiedzi;
- liczba wygenerowanych punktów;
- stylistyczna płynność;
- pewność tonu;
- zgodność z preferencjami uczestnika.

### Dopuszczalne rodziny miar w R5

Miary R5 dla V1 mogą obejmować m.in.:
- zgodność z materiałem;
- pokrycie kluczowych elementów;
- liczbę twierdzeń niepodpartych;
- jakość rozróżnienia fakt/interpretacja;
- jakość alternatyw;
- spójność modelu;
- niezależną ocenę recenzenta.

## V2 — Audytowalność

### Definicja

**Audytowalność** oznacza zdolność użytkownika lub niezależnego recenzenta do przejścia od ważnego wniosku z powrotem do jego podstawy oraz do zrekonstruowania drogi, którą wniosek powstał.

Obejmuje:
- jawne pochodzenie ważnych twierdzeń;
- możliwość wskazania dokładnego fragmentu źródła;
- odróżnienie źródła, interpretacji, hipotezy i modelu;
- widoczność niepewności;
- możliwość wykrycia twierdzeń bez podstawy;
- możliwość recenzji bez polegania wyłącznie na pamięci autora.

### Nie jest tym:
- sama obecność linków;
- liczba cytatów;
- techniczne posiadanie identyfikatorów bez semantycznego związku.

### Dopuszczalne rodziny miar w R5

Miary R5 dla V2 mogą obejmować:
- odsetek ważnych wniosków z poprawną podstawą źródłową;
- liczbę ważnych wniosków bez podstawy;
- poprawność relacji wniosek ↔ źródło;
- zdolność recenzenta do odtworzenia ścieżki;
- kompletność pochodzenia.

## V3 — Pamięć procesu

### Definicja

**Pamięć procesu** oznacza zdolność późniejszego odzyskania nie tylko końcowego wniosku, lecz również:
- co było podstawą;
- jakie alternatywy rozważano;
- które elementy były niepewne;
- dlaczego wybrano dany model;
- jak model zmieniał się wraz z nowymi danymi.

Jest to właściwość zapisu procesu, nie deklaracja o biologicznej pamięci użytkownika.

### Nie jest tym:
- ilość przechowywanych danych;
- pamiętanie tekstu źródłowego słowo w słowo;
- sam fakt posiadania archiwum.

### Dopuszczalne rodziny miar w R5

Miary R5 dla V3 mogą obejmować:
- odroczone odtworzenie toku rozumowania;
- poprawność odzyskania podstaw wniosków;
- odzyskanie wcześniej rozważanych alternatyw;
- czas potrzebny na ponowne wejście w sprawę;
- zgodność rekonstrukcji po czasie z pierwotnym zapisem.

## V4 — Skuteczność działania

### Definicja

**Skuteczność działania** oznacza stopień, w jakim rozumienie powstałe w danym warunku prowadzi do działania, które jest:
1. adekwatne do problemu;
2. konkretne;
3. wykonalne;
4. testowalne;
5. powiązane z modelem;
6. zdolne dostarczyć informacji zwrotnej do aktualizacji modelu.

Właściwa skuteczność wymaga dodatkowo obserwacji rzeczywistego wyniku po zastosowaniu działania.

### Dwa poziomy V4

**V4a — jakość projektu działania**  
Może być oceniona bez wykonania działania.

**V4b — rzeczywisty rezultat działania**  
Może być oceniony wyłącznie wtedy, gdy działanie zostało faktycznie zastosowane i jego wynik zarejestrowany.

### Nie jest tym:
- atrakcyjność rady;
- liczba propozycji;
- ogólne poczucie „przydatności” bez związku z wynikiem.

---

# 5. Dwa koszty

Korzyść nie może być interpretowana bez kosztu jej uzyskania.

## C1 — Koszt czasowy

### Definicja

Czas potrzebny do uzyskania użytecznego rezultatu w danym warunku.

W R5 należy rozróżnić co najmniej:
- czas właściwej sesji;
- przekroczenie limitu;
- opcjonalnie: czas potrzebny później na ponowne wejście w sprawę.

Większa jakość przy bardzo dużym wzroście czasu nie jest automatycznie korzyścią netto.

## C2 — Obciążenie poznawcze

### Definicja

Subiektywny i obserwowalny koszt mentalny wykonania zadania.

Może obejmować:
- wysiłek;
- dezorientację;
- trudność rozumienia struktury;
- potrzebę pamiętania wielu elementów jednocześnie;
- liczbę sytuacji, w których użytkownik nie wie, co zrobić dalej;
- poczucie przeciążenia formularzem lub procedurą;
- odstępstwa od protokołu wywołane trudnością narzędzia.

Obciążenie poznawcze nie może być utożsamiane z samym czasem.

---

# 6. Model decyzji: wektor, nie jeden wynik

Po R6 wynik powinien być zapisany co najmniej jako:

| Wymiar | Wynik |
|---|---|
| V1 Jakość rozumowania | poprawa / brak wyraźnej różnicy / pogorszenie / niejednoznaczne |
| V2 Audytowalność | poprawa / brak wyraźnej różnicy / pogorszenie / niejednoznaczne |
| V3 Pamięć procesu | poprawa / brak wyraźnej różnicy / pogorszenie / niejednoznaczne |
| V4 Skuteczność działania | poprawa / brak wyraźnej różnicy / pogorszenie / niejednoznaczne |
| C1 Koszt czasowy | niższy / podobny / wyższy / niejednoznaczny |
| C2 Obciążenie poznawcze | niższe / podobne / wyższe / niejednoznaczne |

Nie wolno zastąpić tego wektora samym zdaniem:

> „SPP działa.”

Dopuszczalna decyzja D0 powinna wskazywać **dla czego** wydano GO, np.:

> `GO NARROW — poprawa audytowalności złożonych rozmów wieloperspektywicznych przy akceptowalnym wzroście czasu.`

---

# 7. Non-claims — twierdzenia zabronione na podstawie obecnego pilotażu

Niezależnie od wyniku R6, sam indywidualny pilotaż **nie uprawnia** do twierdzenia, że:

1. SPP ogólnie poprawia ludzkie rozumowanie.
2. SPP jest lepszy od notatek dla wszystkich użytkowników i zadań.
3. SPP jest lepszy od ChatGPT dla wszystkich modeli, promptów i klas problemów.
4. Wynik jest przyczynowym dowodem skuteczności dla populacji.
5. Wynik przenosi się na innych użytkowników.
6. Wynik przenosi się na inne klasy źródeł i problemów.
7. Ontologia SPP jest kompletna albo optymalna.
8. Audyt strukturalny gwarantuje poprawność semantyczną.
9. SPP automatycznie chroni użytkownika przed błędami poznawczymi.
10. SPP zwiększa biologiczną pamięć użytkownika.
11. SPP poprawia rzeczywistą skuteczność działania, jeżeli działania nie zostały wykonane i ocenione.
12. Integracja AI przynosi korzyść netto.
13. Przyszły silnik AI v0.6 jest uzasadniony samą strukturą obecnego prototypu.
14. System jest gotowy produkcyjnie, bezpieczny, skalowalny lub odpowiedni do zastosowań wysokiego ryzyka.
15. Brak różnicy w pilotażu N=1 dowodzi braku wartości SPP.
16. Zaobserwowana różnica musi wynikać wyłącznie z SPP — trudność materiałów i efekt uczenia pozostają potencjalnymi zakłóceniami.

---

# 8. Warunki porównawcze objęte kontraktem

R1 przyjmuje trzy odrębne warunki:

**A — Notatki swobodne**  
Samodzielna analiza bez struktury SPP i bez AI.

**B — Standardowy ChatGPT**  
Standardowa analiza przez ChatGPT według ustalonego promptu, bez struktury SPP i bez integracji API z SPP.

**C — SPP v0.5.1 offline**  
Ręczna praca w strukturze SPP, bez zintegrowanego silnika AI.

Kontrakt bada więc przede wszystkim:

> **wartość struktury pracy poznawczej SPP**, a nie wartość modelu AI osadzonego w SPP.

---

# 9. Reguła mapowania wszystkich przyszłych miar

Każda miara, która ma wpływać na interpretację R6 lub decyzję D0, musi posiadać identyfikator rodzica:

- `V1.*` — jakość rozumowania
- `V2.*` — audytowalność
- `V3.*` — pamięć procesu
- `V4.*` — skuteczność działania
- `C1.*` — koszt czasowy
- `C2.*` — obciążenie poznawcze

## Zakaz miar osieroconych

Miara bez jawnego przypisania do jednego z sześciu konstruktów:
- nie może być wynikiem głównym;
- nie może wpływać na GO / GO NARROW / SIMPLIFY / RETURN / STOP;
- musi zostać usunięta albo zdefiniowana przed zamrożeniem R5.

Miara może mieć więcej niż jednego rodzica tylko wtedy, gdy w R5 zostanie zapisane:
- który konstrukt jest główny;
- jaki jest konstrukt pomocniczy;
- dlaczego nie powoduje to podwójnego liczenia.

---

# 10. Granica R1 / R5

R1 **nie ustala jeszcze**:
- dokładnej rubryki punktowej;
- wag;
- progów istotności;
- progów GO;
- kolejności sesji;
- formalnego dopasowania materiałów;
- sposobu postępowania z brakującymi danymi;
- instrukcji recenzenta;
- finalnych operacjonalizacji każdej miary.

To należy do R5.

R1 zamraża wyłącznie:
- przedmiot badania;
- sześć konstruktów;
- ich definicje;
- zakres wnioskowania;
- zakazane interpretacje;
- zasadę mapowania pomiarów.

---

# 11. Bramka R1

R1 może zostać oznaczone `CLOSED` tylko wtedy, gdy wszystkie poniższe warunki mają odpowiedź TAK:

- [x] Uczestnik pilotażu jest określony jako P01.
- [x] Klasa spraw jest jednoznacznie zawężona.
- [x] Problem poznawczy jest określony.
- [x] V1 ma definicję i granice.
- [x] V2 ma definicję i granice.
- [x] V3 ma definicję i granice.
- [x] V4 ma definicję i granice.
- [x] C1 ma definicję.
- [x] C2 ma definicję.
- [x] Non-claims są zaakceptowane.
- [x] Przyjęto wektorowy model wyniku.
- [x] Przyjęto zakaz miar osieroconych.
- [x] Potwierdzono, że R1 nie zmienia ontologii ani aplikacji v0.5.1.
- [x] Dokument został podpisany przed rozpoczęciem R2.

---

# 12. Podpis R1 — zapis finalny

**Decyzja:** `APPROVE & FREEZE`  
**Identyfikator osoby zatwierdzającej:** `PROJECT_OWNER`  
**Data:** `2026-08-07`  
**Źródło decyzji:** jawne polecenie właściciela projektu: `APPROVE & FREEZE R1`  
**Uwagi / warunki zatwierdzenia:** brak.

## Skutek bramki

`R1 → CLOSED`  
`R2 → UNLOCKED`

Od tej chwili treść R1 jest punktem odniesienia dla R2–R6. Zmiana definicji V1–V4, C1–C2, klasy spraw, zakresu wnioskowania albo non-claims wymaga formalnego `RETURN` do R1, nowej wersji dokumentu oraz ponownego zamrożenia przed dalszym badaniem.

R2 jest odblokowane, ale nie zostało rozpoczęte przez sam fakt zatwierdzenia R1.
