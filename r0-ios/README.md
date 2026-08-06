# SPP v0.5.1 — R0 iOS Verifier

Mobilny wariant niezależnej reprodukcji R0 dla iPhone/iOS.

## Cel

Pozwala wykonać kontrolę baseline’u bez `localhost`, Terminala i skryptów START. Verifier jest hostowany jako zwykła strona HTTPS, natomiast badane pliki pozostają lokalne na urządzeniu i są wybierane przez systemowy selektor Pliki.

## Pliki wymagane na iPhonie

1. `SPP_v0.5.1_experimental_baseline_release.zip`
2. `SPP_v0.5.1_seed.json` lub identyczny `SPP_v0.5.1_snapshot_initial.json`
3. `SPP_v0.5.1_wersja_eksperymentalna.html`

Verifier porównuje SHA-256 tych artefaktów z zamrożonym baseline’em.

## Procedura

1. Utwórz osobny profil Safari `SPP R0` lub przynajmniej rozpocznij od wyczyszczonego stanu R0.
2. Otwórz hostowany verifier przez HTTPS.
3. Wybierz pełny ZIP baseline’u z aplikacji Pliki i sprawdź SHA-256.
4. Wybierz snapshot JSON i sprawdź wersję, schemaVersion i liczebności.
5. Wybierz zamrożony plik aplikacji HTML.
6. Uruchom kontrolę; verifier odtwarza snapshot do localStorage i wykonuje ścieżkę `dashboard → walidacja → dashboard`.
7. Zamknij kartę/Safari i otwórz tę samą stronę ponownie w tym samym profilu Safari.
8. Uruchom kontrolę trwałości.
9. Uzupełnij rolę testera i oświadczenia.
10. Pobierz raport JSON i Markdown.

## Interpretacja

- `PASS_INDEPENDENT` — wszystkie kontrole przeszły i tester deklaruje niezależność; raport może zamknąć R0.
- `PASS_TECHNICAL_NONINDEPENDENT` — warstwa techniczna przeszła, ale tester nie jest niezależny lub nie spełniono oświadczeń; R0 pozostaje otwarte.
- `FAIL_OR_INCOMPLETE` — co najmniej jedna wymagana kontrola nie przeszła.

## Prywatność

Strona nie wysyła ZIP-a, snapshotu ani aplikacji do GitHuba. Pliki są odczytywane przez File API w przeglądarce, a hashe liczone przez Web Crypto. Do repozytorium trafił wyłącznie kod verifiera oraz publiczne identyfikatory release’u/hashów.

## Zamrożony baseline

- tag: `v0.5.1-experimental-baseline`
- commit: `c9f48db90506e0fc0fb9082e598ab0b3ef364d32`
- release SHA-256: `e72504ad446a309929caec4d47ea73e177a76ef962ad4fba59c52488bf4adfe9`
