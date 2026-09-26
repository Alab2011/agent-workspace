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
_w toku_

### researcher
_w toku_
