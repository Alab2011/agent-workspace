# Notatki treningowe

Wnioski z próbnych przebiegów pipeline'u. Poprawki promptów wprowadzamy dopiero po akceptacji użytkownika.

Statusy: `PROPOSED` (zaproponowana) → `APPROVED` (zaakceptowana, czeka na wprowadzenie) → `APPLIED` (wprowadzona).

## Przebieg 1: `sites/test-piekarnia/` (lokalna piekarnia)

### informator
Przebiegi: 4. Otwarte pytania: 29 → 8 → 2 → 0 (READY).

Co działało dobrze:
- Pytania pogrupowane A–F z propozycjami odpowiedzi i trafnymi pytaniami branżowymi (alergeny, torty, sezonowość).
- Wyłapywał sprzeczności między odpowiedziami (np. „przykładowe dane” a podany telefon) i luki (produkty spoza cennika, brak alergenów).
- Niczego nie rozstrzygał sam (zasada 7). Nieaktualne odpowiedzi przekreślał, zamiast je usuwać.

| # | Problem | Poprawka promptu | Status |
|---|---------|------------------|--------|
| I-1 | Propozycja odpowiedzi „c) rzemieślnicza (…, mąki ekologiczne)” przemyciła fakt, którego użytkownik nie podał. Potrzebna była dodatkowa runda pytań. | Propozycje odpowiedzi zawierają tylko kategorie, nigdy fakty o firmie (składniki, certyfikaty, obietnice). | APPROVED |
| I-2 | Opcje „wymyślcie sami” (nazwa, miasto, alergeny, wypiek dnia) kłócą się z zasadą „nie zmyślamy faktów” i nie wskazują, kto miałby zmyślać. | Usunąć opcje „wymyślcie sami”. Dopuścić tylko „użyjcie danych przykładowych” przy danych kontaktowych, z oznaczeniem PRZYKŁADOWE. | APPROVED |
| I-3 | 29 pytań na start to dużo dla klienta. | Oznaczać pytania kluczowe (⭐), a resztę opisać jako „opcjonalne, jeśli wiesz”. | APPROVED |

### interpreter
Przebiegi: 4 (+1 po kontroli konfliktu). Pytania: 5 → 2 → 0 (READY).
- ✅ Pytał tylko o luki, nie powtarzał pytań informatora.
- ✅ Wyłapał niejednoznaczną odpowiedź „3a” na pytanie z trzema podpunktami i niczego nie rozstrzygnął sam.

| # | Problem | Poprawka promptu | Status |
|---|---------|------------------|--------|
| P-1 | Pytanie z podpunktami (a/b/c) i odpowiedź jedną literą dały niejednoznaczność, potrzebna była dodatkowa runda. | Każdy podpunkt dostaje własny numer (3, 4, 5 zamiast 3a, 3b, 3c). Dotyczy informatora i interpretera. | PROPOSED |

### researcher
Przebiegi: 3. Dwa pierwsze nieudane (WebFetch → EGRESS_BLOCKED), trzeci w wariancie B1 (manager pobrał strony i zrobił zrzuty).
- ✅ Za każdym razem uczciwie raportował 0 przejrzanych stron, nie zmyślał statystyk „x/N” i nie nadpisał pliku gorszą wersją.
- ✅ W B1 przeanalizował 7/8 stron. Stronę z ekranem anty-botowym odrzucił, a braki na zrzutach uzupełniał z HTML, z oznaczeniem źródła.
- Środowisko: patrz sekcja „Przygotowanie środowiska” w `pipeline.md`.

### manager (ja)
| # | Problem | Reguła | Status |
|---|---------|--------|--------|
| M-1 | Odpowiedź „nie mam zakazanych kolorów” trafiła tylko do interpretera, a do intake nie. Powstały dwa rozbieżne źródła prawdy. | Każdy fakt od użytkownika najpierw trafia przez informatora do `intake.md`, a dopiero potem do innych agentów. | APPLIED (poprawione w intake) |
