# Protokół niezależnego testu reprodukcji R0

## Kryterium PASS_INDEPENDENT

Raport zamyka bramkę R0 tylko wtedy, gdy:

1. wszystkie automatyczne kontrole mają wynik PASS;
2. tester potwierdził czysty profil;
3. tester potwierdził brak ustnej pomocy autora;
4. wykonano pełne zamknięcie i ponowne otwarcie przeglądarki;
5. tester potwierdził właściwy ekran aplikacji;
6. raport jest zgodny z rzeczywistym przebiegiem;
7. wybrana rola testera nie jest rolą właściciela projektu.

## Wyniki pośrednie

- `PASS_TECHNICAL_NONINDEPENDENT` — techniczna reprodukcja przeszła, ale tester jest właścicielem projektu. Nie zamyka R0.
- `FAIL_OR_INCOMPLETE` — brak co najmniej jednego elementu wymagającego ponowienia lub wyjaśnienia.

## Zasada niezmienności

Wykrytego błędu nie naprawia się w baseline `v0.5.1-experimental-baseline`. Tworzy się raport, klasyfikuje błąd, a ewentualną poprawkę wydaje jako nowy commit i nową wersję/release.
