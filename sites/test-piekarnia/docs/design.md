# Design: test-piekarnia („Piekarynka nad Zegrzem”)

> Wejście: intake.md (READY), brief.md (READY, 6 podstron / 32 sekcje), research.md, zrzuty L1, L3, R3 z `research-raw/` oraz dwa uzupełnienia od użytkownika przekazane przez managera (26.09.2026): (1) co podoba się w stronach 1, 3, 7; (2) **sekcja „Wyróżniki” [NICE] trafia na podstronę O nas** (dosłownie: „na podstronie o nas”), a nie na Start pod hero.
> Ten dokument **nie zawiera finalnych tekstów**. Teksty pisze writer według „Mapy tekstów”. Wyjątek to fakty wprost z intake, oznaczone jako **„fakt z intake”** ze wskazaniem, gdzie są.

---

## Kierunek i uzasadnienie (z odwołaniem do researchu)

### Kierunek w jednym zdaniu
**„Ciepła piekarnia z rynku”**: duże, ciepłe zdjęcia pieczywa na całą szerokość ekranu z tekstem na przyciemnionej nakładce, kremowe tło, brąz skórki chleba i złoto, szeryfowe nagłówki o książkowym charakterze i okrągławy, czytelny tekst. Sam układ jest spokojny i uporządkowany, z konkretami podanymi od razu: telefon, godziny, wypiek dnia, ceny z alergenami.

### Skąd ten kierunek
1. **Preferencje użytkownika (intake D, mają pierwszeństwo):** styl „ciepły i domowy (drewno, kremowe kolory, swojski klimat)”, kolory „beże, brązy, złoto, kolor skórki chleba”, motyw jasny z automatycznym trybem ciemnym, brak logo (tylko nazwa).
2. **Strony, które się podobają (1, 3, 7) i uzasadnienie użytkownika.** Użytkownik doprecyzował (przekazane przez managera, dosłownie): *„generalnie przykazdej sam overall - uklad strony - fajne zdjecia w tle przy dobrym ukladzie i czcione tekstu”*. W każdej z trzech stron podoba mu się więc **ogólne wrażenie: układ, ładne zdjęcia w tle przy dobrym układzie oraz czcionki**. Poniżej moje obserwacje z zrzutów, czyli **co konkretnie przenoszę** (wzorce, bez kopiowania grafik i tekstów):
   - **L1 Brodzik Naturalnie:** hero ze zdjęciem bochenka na całą szerokość, duży jasny napis bezpośrednio na zdjęciu po lewej, a chleb po prawej. Pod spodem jasny, wyśrodkowany blok treści z szeryfowym brązowym nagłówkiem i krótką kreską-separatorem pod nim. Paleta brąz / karmel / złoto.
     → Przenoszę: **zdjęcie tła w hero z tekstem po lewej stronie**, **szeryfowe nagłówki w kolorze brązu z krótką złotą kreską pod h2**, paletę.
   - **L3 Bracia Kowalscy:** zdjęcie na całą szerokość (drożdżówki) z tekstem na środku, **telefon i adres dużą czcionką w prawym górnym rogu nagłówka**, historia w **układzie zygzakowym „wtedy / dziś”** (tekst obok zdjęcia, na przemian), rząd 3 ikon z krótkimi opisami, prosta, czytelna czcionka bezszeryfowa.
     → Przenoszę: **widoczny telefon i adres w nagłówku**, **zygzak historii 1987 → dziś**, **rzędy ikon** (Wyróżniki), **duże zdjęcia bez ramek**. **Nie przenoszę czerwieni**, bo użytkownik wskazał ciepłe beże, brązy i złoto, a research odradza czerwień jako „marketową” (research: „Bez czerwieni (L3)”). Zobacz pytanie P2.
   - **R3 Breaking Bread:** pas zdjęcia na całą szerokość jako nagłówek strony, pod nim **ciemny pas z instrukcją zamawiania** i **zamówienie w ponumerowanych krokach** (1. data, 2. produkty) w panelu po prawej. Zaokrąglona, czytelna czcionka bezszeryfowa (Mulish lub bardzo podobna).
     → Przenoszę: **nagłówki podstron jako pasy ze zdjęciem**, **ciemny (brązowy) pas z zasadami zamawiania**, **formularz w numerowanych krokach**, **okrągławy krój tekstu (Mulish)**.
3. **Research (wnioski ogólne):** hero ze zdjęciem pieczywa to standard (6/7). Historia jest drugim argumentem (6/7). Luki u konkurencji to cennik z alergenami (0/7), FAQ (0/7), godziny na stronie głównej (2/7) i telefon w nagłówku (1/7), a nasz brief wymaga ich wszystkich, więc projekt je eksponuje. Rekomendacja researchu, którą przyjmuję: szeryfowe ciepłe nagłówki + czytelny tekst w dużym rozmiarze (osoby starsze), umiarkowane zaokrąglenia, tryb ciemny „piekarnia nocą” (czekoladowe tło zamiast czystej czerni).
4. **Czego unikam (błędy z researchu):** baner cookies zasłaniający pół ekranu (L1), hero bez produktu, treść pojawiająca się tylko z animacją (puste miejsca w L1, L3, R1), wyjustowany tekst w wąskich kolumnach, małe obrysowane przyciski „Więcej”, oferta tylko w PDF (L3), długi blok instrukcji w jednym akapicie (R3), czerwony blok zajmujący pół ekranu na mobile (L3).

### Zgodność preferencji z researchem
Preferencje z intake (ciepłe kolory, domowy styl) i rekomendacje researchu są zgodne, więc nie widzę sprzeczności blokującej. Jedyny punkt do potwierdzenia to czerwień z L3 (pytanie P2, nieblokujące: domyślnie jej nie używam, bo nie ma jej w preferencjach kolorów).

---

## Design tokens

### Kolory: tryb jasny (domyślny)
| Token | Hex | Zastosowanie |
|---|---|---|
| `--bg` | `#FBF6EE` | tło strony (kremowe, kolor miąższu) |
| `--surface` | `#FFFDF9` | karty, pola formularzy |
| `--surface-alt` | `#F3E8D7` | sekcje naprzemienne, pasek górny, plakietki alergenów |
| `--text` | `#3B2A1E` | tekst i nagłówki (ciemny brąz) |
| `--text-muted` | `#6B5443` | podpisy, daty, podpowiedzi pól |
| `--primary` | `#8A4B22` | przycisk „Zamów” (tło), linki, ikony (brąz skórki chleba) |
| `--primary-hover` | `#6F3A18` | hover / active przycisku „Zamów” |
| `--on-primary` | `#FFFFFF` | tekst na `--primary` |
| `--accent` | `#C8962E` | przycisk „Napisz do nas” (tło), złota kreska pod h2, tło plakietki „Dziś” |
| `--accent-hover` | `#DDB054` | hover przycisku „Napisz do nas” (rozjaśnienie) |
| `--on-accent` | `#3B2A1E` | tekst na `--accent` |
| `--band` | `#3B2A1E` | ciemny pas „Zasady zamawiania” (wzorzec R3), tekst na nim `--band-text` |
| `--band-text` | `#F5EBDD` | tekst na ciemnym pasie |
| `--border` | `#E3D3BC` | dekoracyjne linie i obramowania kart (bez znaczenia informacyjnego) |
| `--border-input` | `#8C7359` | obramowanie pól formularza, checkboxów i radio (wymóg 3:1) |
| `--diet-bg` | `#E4EFDF` | tło plakietki diety („bezglutenowe (osobna strefa)”, „bez laktozy”) |
| `--diet-text` | `#2F6B3A` | tekst plakietki diety, komunikat sukcesu |
| `--error` | `#A12A1F` | błędy formularza |
| `--focus` | `#3B2A1E` | obrys focus (3 px + odsunięcie 2 px) |
| `--scrim` | `rgba(31,21,16,0.70)` | nakładka na zdjęcia pod tekstem (min. 0.70 pod obszarem tekstu) |
| `--scrim-text` | `#F5EBDD` | tekst na zdjęciach |

### Kolory: tryb ciemny („piekarnia nocą”, `@media (prefers-color-scheme: dark)`)
| Token | Hex | Uwagi |
|---|---|---|
| `--bg` | `#1F1510` | gorzka czekolada |
| `--surface` | `#2B1E16` | karty |
| `--surface-alt` | `#362619` | sekcje naprzemienne, plakietki alergenów |
| `--text` | `#F5EBDD` | kremowy |
| `--text-muted` | `#CDBBA5` | |
| `--primary` | `#D08A52` | przycisk „Zamów” (jasna skórka), linki w treści mają `--accent` |
| `--primary-hover` | `#DDA06E` | rozjaśnienie |
| `--on-primary` | `#1F1510` | w trybie ciemnym tekst na przyciskach jest ciemny |
| `--accent` | `#E0B25A` | „Napisz do nas”, linki, złote kreski |
| `--accent-hover` | `#EBC67A` | |
| `--on-accent` | `#1F1510` | |
| `--band` | `#362619` | + obramowanie górne i dolne 1 px `--accent` |
| `--band-text` | `#F5EBDD` | |
| `--border` | `#4A3626` | dekoracyjne |
| `--border-input` | `#8C7359` | |
| `--diet-bg` | `#2A3A26` | |
| `--diet-text` | `#CFE6C8` | (sukces jako tekst na `--bg`: `#9CCB94`) |
| `--error` | `#F08A7E` | |
| `--focus` | `#E0B25A` | |
| `--scrim` | `rgba(31,21,16,0.70)` | bez zmian |

### Kontrast (WCAG 2.1, liczone ze wzoru na luminancję względną)
| Para | Jasny | Ciemny | Wymóg |
|---|---|---|---|
| `--text` na `--bg` | 12,7 : 1 | 15,2 : 1 | 4,5 ✔ |
| `--text` na `--surface-alt` | 11,3 : 1 | 12,3 : 1 | 4,5 ✔ |
| `--text-muted` na `--bg` | 6,6 : 1 | 9,6 : 1 | 4,5 ✔ |
| `--text-muted` na `--surface-alt` | 5,8 : 1 | 7,8 : 1 | 4,5 ✔ |
| `--on-primary` na `--primary` („Zamów”) | 6,8 : 1 | 6,3 : 1 | 4,5 ✔ |
| `--on-primary` na `--primary-hover` | 9,2 : 1 | 8,0 : 1 | 4,5 ✔ |
| `--on-accent` na `--accent` („Napisz do nas”) | 5,1 : 1 | 9,1 : 1 | 4,5 ✔ |
| `--on-accent` na `--accent-hover` | 6,8 : 1 | 11,0 : 1 | 4,5 ✔ |
| link `--primary` (jasny) / `--accent` (ciemny) na `--bg` | 6,3 : 1 | 9,1 : 1 | 4,5 ✔ |
| link na `--surface-alt` | 5,6 : 1 | 7,4 : 1 | 4,5 ✔ |
| `--diet-text` na `--diet-bg` | 5,4 : 1 | 9,1 : 1 | 4,5 ✔ |
| `--error` na `--bg` | 6,8 : 1 | 7,4 : 1 | 4,5 ✔ |
| sukces na `--bg` | 5,9 : 1 | 9,7 : 1 | 4,5 ✔ |
| `--band-text` na `--band` | 12,7 : 1 | 12,3 : 1 | 4,5 ✔ |
| `--border-input` na `--bg` (element UI) | 4,1 : 1 | 4,0 : 1 | 3,0 ✔ |
| `--focus` na `--bg` | 12,7 : 1 | 9,1 : 1 | 3,0 ✔ |
| `--scrim-text` na zdjęciu pod `--scrim` 0.70 (najgorszy przypadek: biały piksel pod nakładką) | ≥ 5,6 : 1 | ≥ 5,6 : 1 | 4,5 ✔ |

**Uwaga:** `--accent` (złoto) na `--bg` ma tylko 2,5 : 1, więc **nie wolno go używać jako koloru tekstu ani ikon niosących znaczenie** w trybie jasnym. Służy wyłącznie jako tło (z ciemnym tekstem) albo dekoracja (kreski pod h2). Ikony w trybie jasnym mają kolor `--primary`.

### Typografia (Google Fonts, z podzbiorem latin-ext dla polskich znaków)
- **Nagłówki: „Alegreya”** (700; 400 italic do wyróżnień). Humanistyczny szeryf o książkowym, ciepłym charakterze, najbliższy nagłówkom L1, które się podobają. Obsługuje ą, ę, ł, ż, ź.
- **Tekst: „Mulish”** (400, 600, 700). Okrągławy, czytelny bezszeryfowy krój, ten sam charakter co w R3 i zbliżony do prostego sansa L3. Research ostrzega przed cienkimi krojami, dlatego tekst ma min. 400 przy 18 px, a etykiety i przyciski 600–700.
- **Znak słowny (logo tekstowe):** „Piekarynka” w Alegreya 700 italic + „nad Zegrzem” w Mulish 700, wersaliki z rozstrzeleniem 0.08em i mniejszym stopniem. Bez pliku graficznego (intake: brak logo).
- **Skala** (płynna, `clamp`, mobile → desktop):
  | Styl | Rozmiar | Interlinia | Krój |
  |---|---|---|---|
  | h1 (hero) | `clamp(2.25rem, 1.5rem + 3vw, 3.75rem)` | 1.1 | Alegreya 700 |
  | h1 (podstrony) | `clamp(2rem, 1.5rem + 2vw, 3rem)` | 1.15 | Alegreya 700 |
  | h2 | `clamp(1.75rem, 1.4rem + 1.4vw, 2.5rem)` | 1.2 | Alegreya 700 |
  | h3 | `clamp(1.25rem, 1.1rem + 0.6vw, 1.5rem)` | 1.3 | Alegreya 700 |
  | lead | `1.25rem` | 1.55 | Mulish 400 |
  | body | `1.125rem` (18 px) | 1.6 | Mulish 400 |
  | small / podpis / podpowiedź | `1rem` (16 px, **nie mniej**) | 1.5 | Mulish 400 |
  | plakietka alergenu / diety | `0.9375rem` (15 px) | 1.2 | Mulish 600 |
  | cena | `1.25rem` | 1.2 | Mulish 700, `font-variant-numeric: tabular-nums` |
  | przycisk | `1.0625rem` | 1 | Mulish 700 |
  | duża liczba dekoracyjna („1987”, „18 h”) | `clamp(3rem, 2rem + 4vw, 5.5rem)` | 1 | Alegreya 700, kolor `--primary` (jasny) / `--accent` (ciemny) |
- Maks. szerokość akapitu: `68ch`. Tekst zawsze wyrównany do lewej, **nigdy wyjustowany** (błąd L4, R2).

### Odstępy (skala 4 px)
`--space-1: 4px`, `--space-2: 8px`, `--space-3: 12px`, `--space-4: 16px`, `--space-5: 24px`, `--space-6: 32px`, `--space-7: 48px`, `--space-8: 64px`, `--space-9: 96px`.
- Pionowy padding sekcji: `--space-7` (mobile) → `--space-9` (desktop ≥1024 px).
- Kontener: `max-width: 1200px`, boczny padding `--space-4` (mobile) / `--space-6` (≥768 px).
- Odstęp w siatkach kart: `--space-5` (mobile) / `--space-6` (desktop).

### Zaokrąglenia i cienie
- `--radius-sm: 6px` (plakietki), `--radius-md: 10px` (przyciski, pola formularza), `--radius-lg: 16px` (karty, zdjęcia w kartach, mapa). Zdjęcia tła na całą szerokość nie mają zaokrągleń.
- `--shadow-1: 0 1px 2px rgba(59,42,30,.08), 0 4px 12px rgba(59,42,30,.08)` (karty). `--shadow-2: 0 8px 24px rgba(59,42,30,.14)` (hover kart, przyklejony pasek).
- Tryb ciemny: cienie zastępuje obramowanie 1 px `--border`.

### Przyciski
- **Dwa równorzędne CTA** (intake B, brief 0.1): ten sam rozmiar, krój, zaokrąglenie i wysokość, oba wypełnione. Różnią się tylko kolorem: **„Zamów”** ma tło `--primary`, **„Napisz do nas”** ma tło `--accent`. Żaden nie jest „drugorzędny” ani tylko obrysowany. W wierszu zawsze kolejność „Zamów”, potem „Napisz do nas”.
- Wymiary: `min-height: 52px`, padding `14px 24px`, `--radius-md`, ikonka 20 px po lewej (opcjonalnie, `aria-hidden`).
- Hover: rozjaśnienie lub przyciemnienie tła wg tokenów `*-hover` + podniesienie `translateY(-1px)`. Active: brak przesunięcia. Focus: `outline: 3px solid var(--focus); outline-offset: 2px`.
- **Przycisk tekstowy / link „więcej”:** tekst `--primary` (jasny) / `--accent` (ciemny), 600, podkreślenie 2 px z odsunięciem, strzałka →. Obszar klikalny min. 44×44 px (błąd L4 z małymi „Więcej”).
- **Na zdjęciach (hero):** te same przyciski, bez zmian kolorów (kontrast liczony względem tła przycisku, nie zdjęcia).

### Ikony
Prosty zestaw liniowy (np. Lucide / Phosphor, licencja MIT, grubość linii 1.75), 24–32 px, kolor `--primary` (jasny) / `--accent` (ciemny). Ikony dekoracyjne mają `aria-hidden="true"`. Proponowane: kłos lub bochenek (1987), klepsydra/zegar (18 h), skreślona fiolka lub listek (bez polepszaczy), tarcza/drzwi (osobna strefa bezglutenowa), furgonetka (dostawa), słuchawka, koperta, pinezka, zegar.

---

## Pokrycie briefu

| Nr | Sekcja z briefu | Priorytet | Uwzględniona? | Gdzie / uwagi |
|---|---|---|---|---|
| 0.1 | Nagłówek i nawigacja | MUST | TAK | wszystkie podstrony: pasek górny z adresem, godzinami na dziś i telefonem + pasek główny ze znakiem słownym, menu i dwoma CTA |
| 0.2 | Stopka | MUST | TAK | wszystkie podstrony, z dosłownym dopiskiem o alergenach i linkiem do cennika |
| 0.3 | Przyklejony pasek akcji na telefonie | NICE | TAK | < 768 px: „Zadzwoń / Zamów / Napisz do nas” |
| 1.1 | Hero | MUST | TAK | Start, zdjęcie tła na całą szerokość |
| 1.2 → O nas | Wyróżniki | NICE | TAK | **Podstrona O nas** (decyzja użytkownika: „na podstronie o nas”), pas 5 haseł z ikonami zaraz pod nagłówkiem podstrony, przed Historią (**miejsce w obrębie podstrony to moja propozycja, do potwierdzenia: P1**) |
| 1.3 | Wypiek dnia | SHOULD | TAK | Start, karta „Dziś” + harmonogram tygodnia |
| 1.4 | Zajawka oferty / specjalności | SHOULD | TAK | Start, 3 karty |
| 1.5 | Zajawka historii | SHOULD | TAK | Start, pas ze zdjęciem tła i dużym „1987” |
| 1.6 | Dla firm (B2B) | SHOULD | TAK | Start, blok z przyciskiem „Napisz do nas” |
| 1.7 | Najnowsze aktualności | SHOULD | TAK | Start, 3 karty |
| 2.1 | Cennik w kategoriach | MUST | TAK | Oferta, 6 kategorii w kolejności z briefu |
| 2.2 | Alergeny przy każdym produkcie | MUST | TAK | Oferta (oraz Start, wszędzie tam, gdzie jest produkt z ceną) |
| 2.3 | Dopisek o śladowych ilościach | MUST | TAK | Oferta (na górze i na dole cennika) + stopka |
| 2.4 | Oznaczenia diet | MUST | TAK | plakietki `--diet-*` |
| 2.5 | Filtr diet | NICE | TAK | Oferta, 4 przełączniki (**otwarte: jak traktować tort, P3**) |
| 2.6 | Przycisk „Zamów” pod cennikiem | MUST | TAK | Oferta, pas na końcu |
| 3.1 | Zasady | MUST | TAK | Zamówienia, ciemny pas w 3 punktach |
| 3.2 | Odbiór i dostawa | MUST | TAK | Zamówienia, 2 karty |
| 3.3 | Płatność | MUST | TAK | Zamówienia, karta + przypomnienie w formularzu |
| 3.4 | Formularz zamówienia | MUST | TAK | Zamówienia, 3 kroki |
| 3.5 | Alternatywa: telefon | MUST | TAK | Zamówienia, blok obok formularza (desktop) / pod nim (mobile) |
| 4.1 | Historia | MUST | TAK | O nas, zygzak 1987 → dziś |
| 4.2 | Jak pieczemy | MUST | TAK | O nas, duże „18 h” + 4 fakty |
| 4.3 | Galeria zdjęć | SHOULD | TAK | O nas, siatka 9 zdjęć |
| 5.1 | Lista wpisów | MUST | TAK | Aktualności, 5 wpisów zastępczych |
| 5.2 | Szablon pojedynczego wpisu | MUST | TAK | osobny plik wpisu (szablon) |
| 5.3 | Kalendarz sezonowy | NICE | TAK | Aktualności, pas 4 kart nad listą (**otwarte: produkt na tłusty czwartek, P4**) |
| 6.1 | Dane kontaktowe | MUST | TAK | Kontakt |
| 6.2 | Pełne godziny otwarcia | MUST | TAK | Kontakt |
| 6.3 | Mapa z dojazdem | MUST | TAK | Kontakt |
| 6.4 | Formularz „Napisz do nas” | MUST | TAK | Kontakt |
| 6.5 | FAQ | SHOULD | TAK | Kontakt, akordeon 8 pytań |

**Razem: MUST 21/21, SHOULD 7/7, NICE 4/4. Nie dodałem żadnych sekcji spoza briefu.**

---

## Struktura strony

### Pliki (propozycja nazw dla codera)
`index.html` (Start), `oferta.html`, `zamowienia.html`, `o-nas.html`, `aktualnosci.html`, `aktualnosci/<slug>.html` (wpisy według jednego szablonu, 5 plików zastępczych), `kontakt.html`.

### 0. Elementy wspólne (każda podstrona)

#### 0.1 Nagłówek i nawigacja [MUST]
- **Cel:** z każdego miejsca jest jedno kliknięcie do zamówienia, wiadomości i telefonu. Adres i godziny widać od razu (osoby starsze, kupujący „po drodze”). Wzorzec: L3 (telefon dużą czcionką w nagłówku).
- **Układ desktop (≥ 1100 px), dwa paski:**
  1. **Pasek górny** (`--surface-alt`, wys. ok. 40 px, tekst 16 px): po lewej pinezka + `g-topbar-address`, na środku zegar + `g-topbar-hours-label` `g-topbar-hours-today`, po prawej **telefon większą czcionką (20 px, 700, kolor `--primary`)**: ikona słuchawki + `g-topbar-phone` jako `tel:+48512345678`.
  2. **Pasek główny** (`--bg`, wys. ok. 80 px, przyklejony do góry przy przewijaniu, `position: sticky`, po przewinięciu cień `--shadow-1`): po lewej znak słowny (`g-wordmark`, link do Startu), na środku menu (6 linków, 17 px, 600; aktywny link podkreślony złotą kreską 3 px i ma `aria-current="page"`), po prawej przyciski `g-cta-order` i `g-cta-write`.
- **Tablet (768–1099 px):** pasek górny zostaje (adres można skrócić do „ul. Rynek 12, Serock”). Pasek główny: znak słowny, oba CTA (mniejszy padding: 12 px 16 px) i przycisk „Menu” (`g-menu-label`) z ikoną hamburgera. Menu rozwija się jako panel pod paskiem.
- **Mobile (< 768 px):** paska górnego nie ma, bo jego treść przechodzi do hero i do stopki. Pasek główny (64 px): znak słowny (mniejszy), okrągły przycisk-telefon 48×48 (`aria-label` = `g-phone-aria`) i przycisk „Menu”. Menu otwiera panel na pełną szerokość z 6 linkami (min. 56 px wysokości każdy), pod nimi oba CTA na pełną szerokość, telefon, adres i godziny na dziś. CTA są też stale dostępne w przyklejonym pasku 0.3.
- **Dostępność:** `g-skip-link` jako pierwszy element (widoczny po focusie). `<nav aria-label="g-nav-aria">`. Przycisk menu ma `aria-expanded` i `aria-controls`, a jego `aria-label` przełącza się między `g-menu-open-aria` / `g-menu-close-aria`. Esc zamyka menu, a focus wraca na przycisk.

#### 0.2 Stopka [MUST]
- `--band` (ciemny brąz) z tekstem `--band-text` w obu trybach (spójne zamknięcie strony, jak ciemne pasy w R3).
- **Desktop:** 4 kolumny: (1) znak słowny w wersji jasnej, `g-footer-tagline`, `g-footer-address`, `g-footer-phone`, `g-footer-email`; (2) `g-footer-hours-title` + `g-footer-hours` (3 wiersze); (3) menu w stopce (`g-footer-nav-aria`, te same 6 linków); (4) `g-footer-social-title` + ikony FB/IG (48×48, `aria-label` z id) oraz ramka z `g-footer-allergen-note` i linkiem `g-footer-allergen-link` (do `oferta.html#alergeny`).
- Pasek na dole: `g-footer-copy`.
- **Mobile:** kolumny jedna pod drugą, kolejność 1 → 2 → 4 → 3. Na dole dodatkowy padding równy wysokości paska 0.3 + `env(safe-area-inset-bottom)`.
- Linki w stopce mają kolor `--accent` (w trybie jasnym `#C8962E` na `#3B2A1E` = 5,1 : 1, w ciemnym `#E0B25A` na `#362619` = 7,4 : 1; oba ≥ 4,5 ✔) i podkreślenie.

#### 0.3 Przyklejony pasek akcji na telefonie [NICE]
- Tylko < 768 px. Przyklejony do dołu, `--surface` z `--shadow-2` i górną linią `--border`, wysokość 64 px + safe-area.
- 3 równe kolumny (ikona 22 px nad etykietą 15 px 700): `g-sticky-call` (`tel:`), `g-sticky-order` (`zamowienia.html#formularz`; wypełnione tło `--primary`), `g-sticky-write` (`kontakt.html#napisz`; wypełnione tło `--accent`). „Zadzwoń” ma tło `--surface` i tekst `--primary`, bo „Zamów” i „Napisz do nas” mają zostać wizualnie równorzędne.
- `<nav aria-label="g-sticky-aria">`. Na stronie Zamówienia „Zamów” przewija do `#formularz`, a na Kontakcie „Napisz do nas” do `#napisz`.

---

### 1. Start (`index.html`) [MUST]

#### 1.1 Hero [MUST]
- **Cel:** w 3 sekundy ma być jasne, że to rzemieślnicza piekarnia z chlebem na zakwasie w Serocku, gdzie jest, do której dziś otwarta i jak zamówić.
- **Zawartość:** `start-hero-eyebrow`, `start-hero-title` (h1), `start-hero-lead` (zakwas, długa fermentacja), `start-hero-cta-order` + `start-hero-cta-write`, a pod nimi linia informacyjna: zegar + `start-hero-hours-label` `start-hero-hours-today` · `start-hero-hours-link`, pinezka + `start-hero-address`. Zdjęcie zastępcze (`start-hero-img-alt`): przekrój/skórka chleba żytniego na zakwasie w ciepłym świetle, na drewnianym blacie.
- **Desktop:** zdjęcie tła na całą szerokość (wzorzec L1/L3, zgodny z tym, co podoba się użytkownikowi), wysokość `min(88vh, 760px)`. Kadr: pieczywo w prawej połowie. **Nakładka gradientowa od lewej**: `--scrim` (0.70) na lewych ~55%, przejście do 0.15 po prawej. Tekst w lewej kolumnie (max 600 px), kolor `--scrim-text`, wyrównany do lewej. Pod h1 krótka złota kreska 64×3 px.
- **Mobile:** zdjęcie tła, wys. min. 560 px, kadr ze środkiem na pieczywie u góry. Nakładka gradientowa od dołu (0.70 w dolnych 65%, gdzie stoi tekst). Oba CTA na pełną szerokość jedno pod drugim (odstęp 12 px), linia informacyjna pod nimi w 2 wierszach.
- **Uwaga:** w HTML zdjęcie wstaw jako `<img>` z `object-fit: cover` i alt (nie jako `background-image`), bo niesie treść („jak wygląda nasz chleb”).

> Wyróżniki (w briefie dotąd 1.2) zostały przeniesione na podstronę O nas decyzją użytkownika. Opis jest w sekcji 4.0.

#### 1.3 Wypiek dnia [SHOULD]
- **Cel:** powód do codziennych odwiedzin (research: „nikt z konkurencji tego nie ma”).
- **Zawartość:** `start-wd-title` (h2) + `start-wd-lead`; **karta „Dziś”**: plakietka `start-wd-today-label` (tło `--accent`, tekst `--on-accent`), zdjęcie (`start-wd-img-alt-1…7` wg dnia), `start-wd-today-name` (h3), `start-wd-today-price`, `g-alg-label` + plakietki alergenów (`start-wd-today-alg`), `start-wd-delivery` (ikonka zegara). Obok **harmonogram tygodnia**: `start-wd-week-title` (h3) i lista 7 wierszy `start-wd-week-1…7` (dzień + nazwa wypieku). Dzisiejszy wiersz jest wyróżniony tłem `--surface-alt`, pogrubieniem i `aria-current="date"`. Pod spodem link `start-wd-link` → Oferta.
- **Desktop:** 2 kolumny 5/7: karta „Dziś” po lewej (zdjęcie u góry, proporcje 4:3), harmonogram po prawej jako tabela lub lista definicji z liniami `--border`.
- **Mobile:** karta „Dziś” na pełną szerokość, pod nią harmonogram.
- **Logika:** dzień tygodnia liczony w strefie `Europe/Warsaw`. Bez JS karta „Dziś” jest ukryta i widać sam harmonogram (bez wyróżnienia), dzięki czemu nic nie kłamie.

#### 1.4 Zajawka oferty / specjalności [SHOULD]
- **Zawartość:** `start-spec-title` (h2) + `start-spec-lead`; 3 karty: chleb żytni na zakwasie, pączek z różą, chałka maślana z kruszonką. Każda karta: zdjęcie (4:3, `--radius-lg` u góry), nazwa (h3), `-desc`, cena, alergeny. Pod kartami link `start-spec-link` → `oferta.html`.
- **Desktop:** 3 kolumny. Karta chleba żytniego może być o 10% wyższa albo mieć plakietkę „od 1987” (hasło z Wyróżników, bez nowych deklaracji), decyzja codera.
- **Mobile:** 1 kolumna. Karty z obrazem u góry, a nie przewijany poziomo karuzel (osoby starsze).
- **Hover (desktop):** `--shadow-2`, zdjęcie `scale(1.03)` w obrębie karty. Cała karta klikalna (link w h3 rozciągnięty pseudo-elementem).

#### 1.5 Zajawka historii [SHOULD]
- **Zawartość:** duża liczba `start-story-year` („1987”), `start-story-title` (h2), `start-story-text`, link `start-story-link` → `o-nas.html`, zdjęcie (`start-story-img-alt`, np. ręce przy cieście w ciepłym świetle; stylizacja „rodzinnego albumu”).
- **Desktop:** **pas ze zdjęciem tła** na całą szerokość (drugi mocny moment zdjęciowy, zgodnie z preferencją „zdjęcia w tle”), wys. ok. 480 px, nakładka `--scrim` od prawej, tekst w prawej kolumnie (lustrzane odbicie hero, rytm lewo-prawo).
- **Mobile:** nakładka od dołu, tekst pod liczbą, wszystko na zdjęciu (min. 480 px).

#### 1.6 Dla firm (B2B) [SHOULD]
- **Zawartość:** `start-b2b-title` (h2), `start-b2b-text` (tylko: kawiarnie, restauracje, sklepy, codzienne poranne dostawy; **bez warunków współpracy**), przycisk `start-b2b-cta` („Napisz do nas”, styl `--accent`, link `kontakt.html#napisz`), zdjęcie (`start-b2b-img-alt`, skrzynki/kosze z pieczywem).
- **Desktop:** tło `--surface-alt`, 2 kolumny: zdjęcie po lewej (`--radius-lg`), tekst po prawej.
- **Mobile:** zdjęcie (16:9) nad tekstem, przycisk na pełną szerokość.

#### 1.7 Najnowsze aktualności [SHOULD]
- **Zawartość:** `start-news-title` (h2), 3 karty z najnowszymi wpisami (treść = `akt-post-1…3`: zdjęcie, data, plakietka kategorii, tytuł, zajawka, link `start-news-more` z `aria-label` wg wzoru `start-news-more-aria`), link `start-news-link` → `aktualnosci.html`.
- **Desktop:** 3 kolumny. **Mobile:** 1 kolumna. Data w `<time datetime="…">`.

---

### 2. Oferta (`oferta.html`) [MUST]

#### Nagłówek podstrony (wspólny wzorzec dla podstron 2–6)
Pas ze zdjęciem tła na całą szerokość (wzorzec R3), wys. 280 px desktop / 200 px mobile, nakładka `--scrim` 0.70 równomierna, h1 + lead wyrównane do lewej w kontenerze, tekst `--scrim-text`. Dla każdej podstrony inne zdjęcie (alt jest pusty `alt=""`, bo zdjęcie pełni tu rolę dekoracyjną, a treść niesie h1).

- **Zawartość:** `oferta-title` (h1), `oferta-lead`.

#### Nawigacja po kategoriach
- Pasek „kotwic” pod nagłówkiem (`<nav aria-label="oferta-catnav-aria">`) z 6 linkami do kategorii (`oferta-cat-*`). Na desktopie jest przyklejony pod paskiem głównym. Na mobile przewija się poziomo, ma chipsy min. 44 px wysokości i widoczny cień krawędzi sygnalizujący przewijanie.

#### 2.5 Filtr diet [NICE] (nad cennikiem)
- `oferta-filter-title` + 4 przełączniki typu chip (`<button aria-pressed>` albo checkboxy stylizowane): `oferta-filter-gf`, `oferta-filter-lf`, `oferta-filter-nuts`, `oferta-filter-sesame`, a także `oferta-filter-reset`. Region `aria-live="polite"` z `oferta-filter-status`. Przy aktywnym filtrze orzechów lub sezamu pojawia się `oferta-filter-trace` (przypomnienie o śladach). Gdy nic nie pasuje: `oferta-filter-empty`.
- **Logika** (dane w atrybutach `data-allergens` / `data-diet`):
  - „bez glutenu”: produkty bez alergenu „gluten” (obecnie tylko chleb bezglutenowy),
  - „bez laktozy”: **wyłącznie produkty z frazą „bez laktozy” w nazwie** (brief 2.4 / odp. 4a), a nie „wszystko bez mleka”,
  - „bez orzechów”: bez „orzechy” i „orzechy (włoskie)”,
  - „bez sezamu”: bez „sezam”,
  - filtry łączą się logicznie przez AND,
  - **tort (alergeny „zależnie od zamówienia”): OTWARTE, pytanie P3.** Do czasu odpowiedzi coder przygotowuje flagę `data-allergens="unknown"`, a zachowanie ustawimy po decyzji.
- Bez JS filtr jest ukryty (`hidden`, odkrywany skryptem), cennik działa w całości.

#### 2.1–2.4 Cennik w kategoriach [MUST]
- **Nad cennikiem** (kotwica `#alergeny`): ramka informacyjna `--surface-alt` z ikoną „i”, zawierająca `oferta-trace-note` (dosłownie) + `oferta-gf-note`.
- **6 kategorii w kolejności z briefu:** Pieczywo, Słodkie wypieki, Wypieki dnia, Sezonowe, Torty i ciasta na zamówienie, Kanapki i przekąski. Każda to `<section>` z h2 (`oferta-cat-*`) i opcjonalną notką (`oferta-cat-dnia-note`, `oferta-cat-sezonowe-note`, `oferta-cat-torty-note`).
- **Wiersz produktu:** nazwa (600) + opcjonalnie `-when` (dzień / okres, `--text-muted`) + plakietki diety → alergeny jako plakietki (`--surface-alt`, `--radius-sm`, np. `gluten` `jaja` `mleko`) → cena wyrównana do prawej (700, tabular-nums).
- **Desktop:** semantyczna `<table>` na kategorię: kolumny `oferta-th-product` | `oferta-th-alg` | `oferta-th-price`, z `<caption>` = nazwa kategorii (h2 może pełnić rolę wizualną, caption `.sr-only`). Linie między wierszami `--border`, wysokość wiersza min. 56 px. Kategorie jedna pod drugą w kolumnie max 960 px (czytelność > gęstość).
- **Mobile:** ta sama tabela przełożona na „karty-wiersze” (CSS: `display: block` dla `tr`): 1. linia to nazwa po lewej i cena po prawej, 2. linia to plakietki alergenów, a nagłówki kolumn są ukryte wizualnie, ale dostępne (`data-label` / `aria-label`).
- **Plakietki diety** (`--diet-bg` / `--diet-text`, ikona listka/tarczy): `oferta-badge-gf` tylko przy chlebie bezglutenowym, `oferta-badge-lf` tylko przy drożdżówce bez laktozy.
- **Tort:** zamiast plakietek alergenów tekst `oferta-p-tort-alg` (fakt: „zależnie od zamówienia, informacja przy składaniu”).
- **Pod cennikiem:** ponownie `oferta-trace-note` (drugie wystąpienie tego samego tekstu, ten sam id).

#### 2.6 Przycisk „Zamów” pod cennikiem [MUST]
- Pas `--surface-alt`: `oferta-cta-title` (h2), `oferta-cta-text` (skrót zasad), przycisk `oferta-cta-order` (`--primary`) → `zamowienia.html#formularz`. Na desktopie wyśrodkowany, na mobile przycisk na pełną szerokość.

---

### 3. Zamówienia (`zamowienia.html`) [MUST]

- **Nagłówek podstrony:** `zam-title` (h1), `zam-lead`.

#### 3.1 Zasady [MUST]
- **Ciemny pas** `--band` (wzorzec R3: instrukcja na ciemnym tle, ale **w punktach zamiast jednego długiego akapitu**). `zam-rules-title` (h2) + 3 punkty z dużymi numerami lub ikonami: `zam-rules-1` (telefon lub formularz), `zam-rules-2` (dzień wcześniej do 14:00), `zam-rules-3` (torty min. 3 dni wcześniej).
- Desktop: 3 kolumny. Mobile: lista pionowa.

#### 3.2 Odbiór i dostawa [MUST] + 3.3 Płatność [MUST]
- 3 karty w rzędzie (desktop) / w kolumnie (mobile), z ikoną u góry:
  - `zam-pickup-title` (h3) + `zam-pickup-text`,
  - `zam-dostawa-title` (h3) + `zam-dostawa-text` (10 km, gratis od 80 zł, poniżej 10 zł). **Nie podajemy dni ani godzin dowozu** (brief 3.2),
  - `zam-pay-title` (h3) + `zam-pay-text` (przy odbiorze lub przy dostawie).
- Karty 3.2 grupuje wspólny nagłówek `zam-delivery-title` (h2). Karta płatności należy do tej samej siatki, a jej h3 wystarcza jako nagłówek sekcji 3.3 (mniej przewijania). Jeśli reviewer uzna, że płatność potrzebuje własnego h2, można go dodać bez zmiany układu.

#### 3.4 Formularz zamówienia [MUST] (kotwica `#formularz`)
- **Desktop:** 2 kolumny 8/4. Po lewej formularz w karcie `--surface`, po prawej przyklejona kolumna (`position: sticky`) z blokiem telefonu 3.5 i skrótem zasad (te same teksty co 3.1, bez nowych id, tylko ponowne użycie `zam-rules-2`, `zam-rules-3`, `zam-f-delivery-cost-hint`). Wzorzec R3: panel zamówienia z boku.
- **Mobile:** 1 kolumna. Formularz, pod nim blok telefonu.
- **Nagłówek:** `zam-form-title` (h2), `zam-form-lead`, `zam-f-required-note`.
- **Kroki** (wzorzec R3: numerowane kroki; `<fieldset>` + `<legend>` z kółkiem-numerem):
  1. `zam-step1-legend`: **Co zamawiasz?** 3 wiersze [`zam-f-product-label` (select, opcja 0 = `zam-f-product-placeholder`, opcje = nazwy produktów z cennika pogrupowane `<optgroup>` wg kategorii) + `zam-f-qty-label` (number, min 1, domyślnie 1)]. Pierwszy wiersz jest wymagany, 2. i 3. opcjonalne. Pod nimi `zam-f-rows-hint`. Kolejność kroków: najpierw produkty, potem data. To świadoma zmiana względem R3, bo termin zależy od produktu (tort = 3 dni).
  2. `zam-step2-legend`: **Kiedy i jak odbierasz?** `zam-f-date-label` (input date) + `zam-f-date-hint` (zasada terminu, aktualizowana dynamicznie, jeśli wybrano tort); radio `zam-f-method-legend`: `zam-f-method-pickup` / `zam-f-method-delivery`; pole `zam-f-address-label` + `zam-f-address-hint` (pojawia się po wybraniu dostawy, CSS `:has()` z fallbackiem „zawsze widoczne”; wymagane tylko przy dostawie); `zam-f-delivery-cost-hint` pod radiami.
  3. `zam-step3-legend`: **Twoje dane.** `zam-f-name-label` (wymagane), `zam-f-phone-label` (wymagane, `type="tel"`, `autocomplete="tel"`), `zam-f-email-label` (opcjonalne, P7), `zam-f-notes-label` (textarea) + `zam-f-notes-hint` (np. do tortu).
- **Pod krokami:** `zam-f-pay-note` (bez płatności online), przycisk `zam-f-submit` (`--primary`, pełna szerokość na mobile, min. 260 px na desktopie). Miejsce na klauzulę informacyjną RODO jest zarezerwowane, ale **bez treści do czasu odpowiedzi na P5**.
- **Walidacja** (natywna + JS): komunikaty pod polem (`--error`, ikona, `aria-describedby`, `aria-invalid`), podsumowanie błędów nad formularzem (`zam-f-error-generic`, focus na nim). Pola: `zam-f-err-required`, `zam-f-err-date`, `zam-f-err-date-tort`, `zam-f-err-phone`, `zam-f-err-address`.
- **Reguła daty** (fakt z intake: „najpóźniej dzień wcześniej do 14:00”, „torty z min. 3-dniowym wyprzedzeniem”): najwcześniejsza data = jutro, jeśli teraz jest przed 14:00 (czas Europe/Warsaw), a w przeciwnym razie pojutrze. Jeśli w którymś wierszu wybrano tort, najwcześniejsza data to dziś + 3 dni. **Dokładna interpretacja „3 dni” jest OTWARTA (P6)**, więc coder trzyma ją w jednej stałej.
- **Po wysłaniu:** komunikat `zam-f-success` w ramce sukcesu w miejscu formularza, z focusem na nim (`role="status"`).

#### 3.5 Alternatywa: telefon [MUST]
- Karta `--surface-alt` z dużą ikoną słuchawki: `zam-phone-title` (h2/h3), `zam-phone-text`, numer `zam-phone-number` dużą czcionką (1.5 rem, 700) jako `tel:`, z `aria-label` = `zam-phone-aria`.

---

### 4. O nas (`o-nas.html`) [MUST]

- **Nagłówek podstrony:** `onas-title` (h1), `onas-lead`.

#### 4.0 Wyróżniki [NICE] (w briefie dotąd 1.2, przeniesione na O nas decyzją użytkownika)
- **Cel:** krótkie „dlaczego my” na początku opowieści o piekarni.
- **Miejsce:** zaraz pod nagłówkiem podstrony, przed Historią. To moja propozycja, bo użytkownik wskazał tylko podstronę (P1). Alternatywa to wstawienie ich po „Jak pieczemy” jako podsumowania.
- **Zawartość:** `onas-usp-title` (h2, może być `.sr-only`; w prototypie widoczne), 5 haseł `onas-usp-1` … `onas-usp-5` z ikonami. **Wyłącznie 5 haseł z briefu** (od 1987 r., 18 h fermentacji zakwasu, bez polepszaczy, osobna strefa bezglutenowa, dostawa gratis od 80 zł w promieniu 10 km), bez żadnych innych.
- **Desktop:** karta `--surface` z `--radius-lg` i `--shadow-1` nachodząca −48 px na dół pasa-nagłówka podstrony (wzorzec L1: jasny blok nachodzący na zdjęcie), 5 kolumn: ikona 32 px nad hasłem (17 px 700, wyśrodkowane).
- **Mobile:** karta bez nachodzenia, lista pionowa: ikona po lewej, hasło po prawej (5 wierszy po 56 px).
- **Uwaga o powtórzeniach:** trzy hasła (1987, 18 h, bez polepszaczy) pokrywają się tematycznie z sekcją 4.2 „Jak pieczemy”. Żeby nie było dosłownych powtórzeń, Wyróżniki są krótkimi hasłami (do 8 słów), a 4.2 rozwija je w 1–2 zdaniach. Writer nie powinien kopiować tych samych sformułowań.

#### 4.1 Historia [MUST]
- **Układ zygzakowy „wtedy / dziś”** (wzorzec L3, który podoba się użytkownikowi; research: stylizacja „rodzinnego albumu” wg L4). `onas-hist-title` (h2), potem 2 rzędy:
  1. zdjęcie po lewej (stylizowane na archiwalne: ciepła sepia, biała ramka „polaroid” 12 px, lekki obrót −1.5°; `onas-hist-1-img-alt`) | po prawej duże `onas-hist-1-year` („1987”), `onas-hist-1-title` (h3), `onas-hist-1-text`,
  2. po lewej `onas-hist-2-year` („Dziś”), `onas-hist-2-title` (h3), `onas-hist-2-text` | zdjęcie po prawej, współczesne, pełny kolor (`onas-hist-2-img-alt`).
- Między rzędami pionowa złota linia osi czasu z kropkami przy latach (desktop).
- **Mobile:** każdy rząd = zdjęcie, potem tekst (bez zygzaka), oś czasu jako linia po lewej stronie.

#### 4.2 Jak pieczemy [MUST]
- **Tło:** pas ze zdjęciem tła (zakwas / ciasto w dzieży) z nakładką, na nim po lewej duże `onas-bake-big-number` („18 h”) + `onas-bake-big-label`, po prawej `onas-bake-title` (h2) i `onas-bake-lead`. Pod pasem (na `--bg`) 4 karty faktów z ikonami: `onas-bake-fact-1…4-title` + `-text`. Tematy wyłącznie z briefu 4.2: naturalny zakwas; 18 h fermentacji; ręcznie i tradycyjnie; bez polepszaczy (receptura od 1987 r. może wejść do tekstu karty 1 albo do leadu). **Żadnych innych deklaracji.**
- Desktop: 4 kolumny. Tablet: 2×2. Mobile: 1 kolumna.

#### 4.3 Galeria zdjęć [SHOULD]
- `onas-gal-title` (h2), `onas-gal-lead`. Siatka 9 zdjęć zastępczych: 3 kolumny desktop (pierwsze zdjęcie 2×2, czyli układ „mozaika”), 2 kolumny tablet, 2 kolumny mobile (kwadraty 1:1, odstęp 8 px).
- Tematy (wg briefu): wypieki (1–4), wnętrze (5–6), praca przy piecu (7–9). Każde zdjęcie ma unikalny alt `onas-gal-N-alt`.
- Kliknięcie otwiera zdjęcie w pełnym rozmiarze (zwykły link do pliku). Bez lightboxa i bez JS, można dodać później. `loading="lazy"`, stałe `width/height`, więc nie ma przeskoków ani pustych miejsc (błąd L3).

---

### 5. Aktualności (`aktualnosci.html` + szablon wpisu) [MUST]

- **Nagłówek podstrony:** `akt-title` (h1), `akt-lead`.

#### 5.3 Kalendarz sezonowy [NICE]
- Nad listą wpisów: `akt-cal-title` (h2) i 4 karty w poziomym rzędzie (desktop 4 kolumny, mobile 2×2): każda to ikona, `akt-cal-N-when` (okres, 700) i `akt-cal-N-what` (produkt). Kolejność kart jest taka jak w briefie (tłusty czwartek, 11 listopada, grudzień, Wielkanoc), bez przestawiania na kolejność kalendarzową. **`akt-cal-1-what` (tłusty czwartek) jest OTWARTE (P4).**

#### 5.1 Lista wpisów [MUST]
- `akt-list-title` (h2, może być `.sr-only`). 5 wpisów zastępczych: 1 wypiek dnia (`akt-tag-wd`) + 4 sezonowe (`akt-tag-season`): tłusty czwartek, rogale na 11 listopada, pierniki w grudniu, mazurki na Wielkanoc.
- **Karta wpisu:** zdjęcie 16:9 (`akt-post-N-img-alt`), plakietka kategorii, data `<time>` (`akt-post-N-date`), tytuł h3 (link, `akt-post-N-title`), zajawka (`akt-post-N-excerpt`), link `akt-post-more` z `aria-label` `akt-post-N-more-aria`.
- **Desktop:** pierwszy (najnowszy) wpis szeroki, poziomo (zdjęcie 6/12 + tekst 6/12), pozostałe w siatce 2×2. **Mobile:** 1 kolumna. Bez paginacji (5 wpisów).
- **Uwaga do writera:** rogal świętomarciński jest w ofercie cały rok, a 11 listopada to tylko temat wpisu (brief). Daty wpisów nie mogą być z przyszłości (dziś: 26.09.2026).

#### 5.2 Szablon pojedynczego wpisu [MUST] (`aktualnosci/<slug>.html`)
- Okruszki (`<nav aria-label="wpis-breadcrumb-aria">`: `wpis-breadcrumb-home` › `wpis-breadcrumb-list` › tytuł).
- Nagłówek wpisu **na zdjęciu tła** (wys. 360 px desktop / 240 px mobile, nakładka `--scrim`): plakietka kategorii, h1 (= `akt-post-N-title`), data (= `akt-post-N-date`). Alt zdjęcia wpisu = `akt-post-N-img-alt` (tu zdjęcie niesie treść, więc alt jest niepusty).
- Treść `wpis-N-body` w kolumnie 68ch: akapity, możliwe h2/h3 i lista. Na końcu link `wpis-back-link` ← Aktualności.
- `<title>` = `wpis-N-page-title`, meta description = `wpis-N-meta`.

---

### 6. Kontakt (`kontakt.html`) [MUST]

- **Nagłówek podstrony:** `kont-title` (h1), `kont-lead`.

#### 6.1 Dane kontaktowe [MUST] + 6.2 Pełne godziny [MUST]
- **Desktop:** 2 karty obok siebie.
  - Karta danych (`kont-data-title`, h2): lista z ikonami i etykietami (`kont-address-label` + `kont-address`; `kont-phone-label` + `kont-phone` jako `tel:` z `kont-phone-aria`; `kont-email-label` + `kont-email` jako `mailto:`; `kont-social-label` + `kont-fb` / `kont-ig` z `aria-label`).
  - Karta godzin (`kont-hours-title`, h2): tabela 3 wierszy (`kont-hours-weekdays`, `kont-hours-sat`, `kont-hours-sun`), dzisiejszy wiersz wyróżniony (JS, `aria-current="date"`), pod tabelą `kont-hours-note` (świeże pieczywo od otwarcia, druga dostawa ok. 12:00).
- **Mobile:** karty jedna pod drugą. Telefon jako duży przycisk-link na pełną szerokość.

#### 6.3 Mapa z dojazdem [MUST]
- `kont-map-title` (h2). Pełna szerokość kontenera, wys. 400 px desktop / 300 px mobile, `--radius-lg`. `<iframe>` mapy z `title` = `kont-map-iframe-title` i `loading="lazy"`. Pod mapą przycisk-link `kont-map-route` (otwiera nawigację do „ul. Rynek 12, 05-140 Serock” w nowej karcie, `aria-label` = `kont-map-route-aria`) oraz `kont-map-fallback`.
- **Rekomendacja:** OpenStreetMap (embed) nie wymaga zgody na cookies, a przy Google Maps trzeba by dodać baner zgody (research ostrzega przed banerami cookies zasłaniającymi ekran, L1). Link „Wyznacz trasę” może prowadzić do Google Maps (to zwykły link, bez cookies na naszej stronie). Decyzja techniczna należy do codera/managera, a w razie wątpliwości do użytkownika (P8).

#### 6.4 Formularz „Napisz do nas” [MUST] (kotwica `#napisz`)
- **Desktop:** formularz w jednej kolumnie max 720 px, w karcie `--surface`. FAQ stoi pod nim, bo taka jest kolejność w briefie.
- `kont-form-title` (h2), `kont-form-lead`, `kont-f-required-note`. Pola: `kont-f-name-label` (wymagane), `kont-f-contact-label` + `kont-f-contact-hint` (wymagane; walidacja: poprawny e-mail **albo** telefon), `kont-f-message-label` + `kont-f-message-hint` (textarea, min. 6 wierszy, wymagane). Przycisk `kont-f-submit` (`--accent`, bo to akcja „Napisz do nas”). Komunikaty: `kont-f-success`, `kont-f-error-generic`, `kont-f-err-required`, `kont-f-err-contact`. Miejsce na klauzulę RODO jak w 3.4 (P5).
- Link B2B ze Startu prowadzi tutaj (`#napisz`), a `kont-f-message-hint` może wspomnieć o firmach.

#### 6.5 FAQ [SHOULD]
- `kont-faq-title` (h2). Akordeon na `<details>/<summary>` (działa bez JS, dostępny z klawiatury), 8 pytań `kont-faq-1…8-q` / `-a` na tematy z briefu 6.5 w tej kolejności: termin zamówień, torty, dostawa i koszt, płatność, godziny, alergeny i ślady, chleb bezglutenowy, obsługa firm.
- `summary` min. 56 px, ikona +/− po prawej, linia `--border` między pytaniami. Kolumna max 800 px.

---

## Mapa tekstów

**Legenda typów:** h1/h2/h3 = nagłówek; lead = akapit wprowadzający; p = akapit; etykieta = krótki tekst UI; przycisk / link; alt = tekst alternatywny zdjęcia; aria = `aria-label` lub `title` (niewidoczne); sr = tekst tylko dla czytników (`.sr-only`); meta = `<title>` / meta description.
**„fakt z intake”** = writer przepisuje wartość dokładnie z intake.md we wskazanym miejscu, bez przeredagowania treści merytorycznej (dopuszczalna tylko forma zapisu, np. „pon.–pt.”).
**Zakazy dla wszystkich tekstów (brief):** słowo „ekologiczne”, „najlepsze w okolicy”, „mąka z lokalnych młynów”, „naturalne składniki”, „ręcznie robione z miłością” i **jakiekolwiek nowe deklaracje**. Ton: ciepły, luźny, na „Ty”, w 1. os. l. mn. (rodzina).

### 0. Wspólne (48 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| g-skip-link | Nagłówek | link sr (widoczny po focusie) | 4 słowa | 0.1 |
| g-wordmark | Nagłówek | znak słowny | fakt z intake: nazwa „Piekarynka nad Zegrzem” (intake A) | 0.1 |
| g-wordmark-aria | Nagłówek | aria (link do Startu) | 7 słów | 0.1 |
| g-topbar-address | Pasek górny | etykieta | fakt z intake: adres (intake E „Dane kontaktowe”) | 0.1 |
| g-topbar-hours-label | Pasek górny | etykieta (np. „Dziś:”) | 2 słowa | 0.1 |
| g-topbar-hours-today | Pasek górny | etykieta dynamiczna | fakt z intake: godziny dla bieżącego dnia (intake „Godziny otwarcia”) | 0.1 |
| g-topbar-phone | Pasek górny | link tel | fakt z intake: +48 512 345 678 (intake E) | 0.1 |
| g-phone-aria | Nagłówek mobile | aria przycisku-telefonu | 5 słów + numer | 0.1 |
| g-nav-aria | Nagłówek | aria nav | 3 słowa | 0.1 |
| g-nav-start | Menu | link | fakt z briefu: „Start” | 0.1 |
| g-nav-oferta | Menu | link | fakt z briefu: „Oferta” | 0.1 |
| g-nav-zamowienia | Menu | link | fakt z briefu: „Zamówienia” | 0.1 |
| g-nav-onas | Menu | link | fakt z briefu: „O nas” | 0.1 |
| g-nav-aktualnosci | Menu | link | fakt z briefu: „Aktualności” | 0.1 |
| g-nav-kontakt | Menu | link | fakt z briefu: „Kontakt” | 0.1 |
| g-cta-order | Nagłówek | przycisk | fakt z intake: „Zamów” (intake B) | 0.1 |
| g-cta-write | Nagłówek | przycisk | fakt z intake: „Napisz do nas” (intake B) | 0.1 |
| g-menu-label | Nagłówek | etykieta przycisku | 1 słowo | 0.1 |
| g-menu-open-aria | Nagłówek | aria | 3 słowa | 0.1 |
| g-menu-close-aria | Nagłówek | aria | 3 słowa | 0.1 |
| g-footer-name | Stopka | znak słowny | fakt z intake: nazwa | 0.2 |
| g-footer-tagline | Stopka | p | 12 słów | 0.2 |
| g-footer-address | Stopka | etykieta | fakt z intake: adres | 0.2 |
| g-footer-phone | Stopka | link tel | fakt z intake: telefon | 0.2 |
| g-footer-email | Stopka | link mailto | fakt z intake: kontakt@piekarynkanadzegrzem.pl (przykładowy) | 0.2 |
| g-footer-hours-title | Stopka | h3 | 3 słowa | 0.2 |
| g-footer-hours | Stopka | lista 3 wierszy | fakt z intake: godziny (intake „Godziny otwarcia”), forma skrócona | 0.2 |
| g-footer-social-title | Stopka | h3 | 3 słowa | 0.2 |
| g-footer-fb-aria | Stopka | aria | 8 słów, zawiera @piekarynkanadzegrzem (przykładowy, intake E) | 0.2 |
| g-footer-ig-aria | Stopka | aria | 8 słów, zawiera @piekarynkanadzegrzem (przykładowy, intake E) | 0.2 |
| g-footer-allergen-note | Stopka | p | fakt z intake, dosłownie: dopisek o śladowych ilościach (intake „Alergeny”, pod tabelą) | 0.2 |
| g-footer-allergen-link | Stopka | link | 6 słów | 0.2 |
| g-footer-nav-aria | Stopka | aria nav | 3 słowa | 0.2 |
| g-footer-copy | Stopka | etykieta | 8 słów (rok 2026 + nazwa) | 0.2 |
| g-sticky-aria | Pasek mobile | aria nav | 3 słowa | 0.3 |
| g-sticky-call | Pasek mobile | przycisk | 1 słowo (np. „Zadzwoń”, wg briefu) | 0.3 |
| g-sticky-order | Pasek mobile | przycisk | fakt: „Zamów” | 0.3 |
| g-sticky-write | Pasek mobile | przycisk | fakt: „Napisz do nas” | 0.3 |
| g-alg-label | Wszędzie przy produktach | etykieta (np. „Alergeny:”) | 1 słowo | 2.2 |
| g-alg-gluten | Plakietka | etykieta | fakt z intake: „gluten” | 2.2 |
| g-alg-jaja | Plakietka | etykieta | fakt z intake: „jaja” | 2.2 |
| g-alg-mleko | Plakietka | etykieta | fakt z intake: „mleko” | 2.2 |
| g-alg-orzechy | Plakietka | etykieta | fakt z intake: „orzechy” | 2.2 |
| g-alg-orzechy-wloskie | Plakietka | etykieta | fakt z intake: „orzechy (włoskie)” | 2.2 |
| g-alg-sezam | Plakietka | etykieta | fakt z intake: „sezam” | 2.2 |
| g-alg-gorczyca | Plakietka | etykieta | fakt z intake: „gorczyca” | 2.2 |
| g-new-tab-sr | Linki zewnętrzne | sr | 5 słów (np. informacja o nowej karcie) | 0.2 / 6.1 / 6.3 |
| g-days | Logika dni | lista 7 nazw dni tygodnia | 7 słów (pełne polskie nazwy, pon.–niedz.) | 1.3 / 6.2 |

### 1. Start (66 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| start-page-title | head | meta title | 60 znaków (nazwa + Serock + chleb na zakwasie) | 1 |
| start-meta | head | meta description | 155 znaków | 1 |
| start-hero-eyebrow | Hero | etykieta nad h1 | 5 słów (rzemieślnicza piekarnia, Serock) | 1.1 |
| start-hero-title | Hero | h1 | 8 słów | 1.1 |
| start-hero-lead | Hero | lead | 30 słów (zakwas, długa fermentacja; fakty z intake „Specjalność”) | 1.1 |
| start-hero-cta-order | Hero | przycisk | fakt: „Zamów” | 1.1 |
| start-hero-cta-write | Hero | przycisk | fakt: „Napisz do nas” | 1.1 |
| start-hero-hours-label | Hero | etykieta (np. „Dziś otwarte:”) | 2 słowa | 1.1 |
| start-hero-hours-today | Hero | etykieta dynamiczna | fakt z intake: godziny bieżącego dnia | 1.1 |
| start-hero-hours-link | Hero | link → kontakt.html#godziny | 3 słowa | 1.1 |
| start-hero-address | Hero | etykieta | fakt z intake: adres | 1.1 |
| start-hero-img-alt | Hero | alt | 15 słów | 1.1 |
| start-wd-title | Wypiek dnia | h2 | 4 słowa | 1.3 |
| start-wd-lead | Wypiek dnia | lead | 20 słów | 1.3 |
| start-wd-today-label | Wypiek dnia | plakietka dynamiczna (np. „Dziś, <dzień>”) | 3 słowa | 1.3 |
| start-wd-today-name | Wypiek dnia | h3 dynamiczny | fakt z intake: nazwa wypieku wg dnia (intake „Wypiek dnia, cały tydzień”) | 1.3 |
| start-wd-today-price | Wypiek dnia | cena dynamiczna | fakt z intake: cena z cennika (intake „Oferta z cenami” + „Wypieki dnia spoza cennika”) | 1.3 |
| start-wd-today-alg | Wypiek dnia | plakietki dynamiczne | fakt z intake: alergeny (intake „Alergeny”) | 1.3 |
| start-wd-img-alt-1 | Wypiek dnia | alt (poniedziałek: chleb orkiszowy) | 12 słów | 1.3 |
| start-wd-img-alt-2 | Wypiek dnia | alt (wtorek: bułki z ziarnami) | 12 słów | 1.3 |
| start-wd-img-alt-3 | Wypiek dnia | alt (środa: chleb z żurawiną i orzechami) | 12 słów | 1.3 |
| start-wd-img-alt-4 | Wypiek dnia | alt (czwartek: pączki z różą) | 12 słów | 1.3 |
| start-wd-img-alt-5 | Wypiek dnia | alt (piątek: focaccia z rozmarynem) | 12 słów | 1.3 |
| start-wd-img-alt-6 | Wypiek dnia | alt (sobota: chałka maślana z kruszonką) | 12 słów | 1.3 |
| start-wd-img-alt-7 | Wypiek dnia | alt (niedziela: ciasto drożdżowe z kruszonką) | 12 słów | 1.3 |
| start-wd-delivery | Wypiek dnia | p krótki | 12 słów, fakt z intake: „druga dostawa ok. 12:00” (intake „Godziny otwarcia”) | 1.3 |
| start-wd-week-title | Wypiek dnia | h3 | 4 słowa | 1.3 |
| start-wd-week-1 | Harmonogram | wiersz | fakt z intake: pon. chleb orkiszowy | 1.3 |
| start-wd-week-2 | Harmonogram | wiersz | fakt z intake: wt. bułki z ziarnami | 1.3 |
| start-wd-week-3 | Harmonogram | wiersz | fakt z intake: śr. chleb z żurawiną i orzechami | 1.3 |
| start-wd-week-4 | Harmonogram | wiersz | fakt z intake: czw. pączki z różą | 1.3 |
| start-wd-week-5 | Harmonogram | wiersz | fakt z intake: pt. focaccia z rozmarynem | 1.3 |
| start-wd-week-6 | Harmonogram | wiersz | fakt z intake: sob. chałka maślana z kruszonką | 1.3 |
| start-wd-week-7 | Harmonogram | wiersz | fakt z intake: niedz. ciasto drożdżowe z kruszonką (dokładnie ta nazwa) | 1.3 |
| start-wd-link | Wypiek dnia | link → oferta.html | 4 słowa | 1.3 |
| start-spec-title | Specjalności | h2 | 6 słów | 1.4 |
| start-spec-lead | Specjalności | lead | 25 słów | 1.4 |
| start-spec-1-name | Karta 1 | h3 | fakt z intake: „Chleb żytni na zakwasie” | 1.4 |
| start-spec-1-desc | Karta 1 | p | 20 słów, tylko fakty z intake „Specjalność” (naturalny zakwas, receptura od 1987, 18 h) | 1.4 |
| start-spec-1-price | Karta 1 | cena | fakt z intake: 12 zł | 1.4 |
| start-spec-1-alg | Karta 1 | plakietki | fakt z intake: gluten | 1.4 |
| start-spec-1-img-alt | Karta 1 | alt | 12 słów | 1.4 |
| start-spec-2-name | Karta 2 | h3 | fakt z intake: „Pączek z różą” | 1.4 |
| start-spec-2-desc | Karta 2 | p | 20 słów, fakt: domowa konfitura z róży (intake „Specjalność”) | 1.4 |
| start-spec-2-price | Karta 2 | cena | fakt z intake: 4,50 zł | 1.4 |
| start-spec-2-alg | Karta 2 | plakietki | fakt z intake: gluten, jaja, mleko | 1.4 |
| start-spec-2-img-alt | Karta 2 | alt | 12 słów | 1.4 |
| start-spec-3-name | Karta 3 | h3 | fakt z intake: „Chałka maślana z kruszonką” | 1.4 |
| start-spec-3-desc | Karta 3 | p | 20 słów, tylko fakty z intake | 1.4 |
| start-spec-3-price | Karta 3 | cena | fakt z intake: 9 zł | 1.4 |
| start-spec-3-alg | Karta 3 | plakietki | fakt z intake: gluten, jaja, mleko | 1.4 |
| start-spec-3-img-alt | Karta 3 | alt | 12 słów | 1.4 |
| start-spec-link | Specjalności | link → oferta.html | 4 słowa | 1.4 |
| start-story-title | Zajawka historii | h2 | 7 słów | 1.5 |
| start-story-year | Zajawka historii | liczba dekoracyjna | fakt z intake: „1987” | 1.5 |
| start-story-text | Zajawka historii | p | 45 słów, fakty z intake „Historia” | 1.5 |
| start-story-link | Zajawka historii | link → o-nas.html | 4 słowa | 1.5 |
| start-story-img-alt | Zajawka historii | alt | 15 słów | 1.5 |
| start-b2b-title | Dla firm | h2 | 6 słów | 1.6 |
| start-b2b-text | Dla firm | p | 35 słów, fakty z intake „Dostawa / odbiór” (kawiarnie, restauracje, sklepy, codzienne poranne dostawy). Bez warunków | 1.6 |
| start-b2b-cta | Dla firm | przycisk → kontakt.html#napisz | fakt: „Napisz do nas” | 1.6 |
| start-b2b-img-alt | Dla firm | alt | 12 słów | 1.6 |
| start-news-title | Aktualności | h2 | 5 słów | 1.7 |
| start-news-more | Karty wpisów | link | 2 słowa (np. „Czytaj dalej”) | 1.7 |
| start-news-more-aria | Karty wpisów | aria (wzór: link + tytuł wpisu) | 2 słowa + tytuł | 1.7 |
| start-news-link | Aktualności | link → aktualnosci.html | 4 słowa | 1.7 |

(Karty 1.7 wyświetlają treść `akt-post-1…3-*`, bez osobnych id.)

### 2. Oferta (104 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| oferta-page-title | head | meta title | 60 znaków | 2 |
| oferta-meta | head | meta description | 155 znaków (cennik z alergenami) | 2 |
| oferta-title | Nagłówek | h1 | 5 słów | 2 |
| oferta-lead | Nagłówek | lead | 30 słów | 2.1 |
| oferta-catnav-aria | Kotwice | aria nav | 3 słowa | 2.1 |
| oferta-cat-pieczywo | Kategoria | h2 | fakt z briefu: „Pieczywo” | 2.1 |
| oferta-cat-slodkie | Kategoria | h2 | fakt z briefu: „Słodkie wypieki” | 2.1 |
| oferta-cat-dnia | Kategoria | h2 | fakt z briefu: „Wypieki dnia” | 2.1 |
| oferta-cat-sezonowe | Kategoria | h2 | fakt z briefu: „Sezonowe” | 2.1 |
| oferta-cat-torty | Kategoria | h2 | fakt z briefu: „Torty i ciasta na zamówienie” | 2.1 |
| oferta-cat-kanapki | Kategoria | h2 | fakt z briefu: „Kanapki i przekąski” | 2.1 |
| oferta-cat-dnia-note | Kategoria | p krótki | 15 słów (dostępne w konkretne dni) | 2.1 |
| oferta-cat-sezonowe-note | Kategoria | p krótki | 15 słów (okresy: grudzień, Wielkanoc) | 2.1 |
| oferta-cat-torty-note | Kategoria | p krótki | 20 słów, fakt z intake: min. 3-dniowe wyprzedzenie | 2.1 |
| oferta-th-product | Tabela | nagłówek kolumny | 1 słowo | 2.1 |
| oferta-th-alg | Tabela | nagłówek kolumny | 1 słowo | 2.2 |
| oferta-th-price | Tabela | nagłówek kolumny | 1 słowo | 2.1 |
| oferta-badge-gf | Plakietka diety | etykieta | fakt z briefu 2.4: „bezglutenowe (osobna strefa)” | 2.4 |
| oferta-badge-lf | Plakietka diety | etykieta | fakt z briefu 2.4: „bez laktozy” | 2.4 |
| oferta-trace-note | Nad i pod cennikiem | p | fakt z intake, dosłownie: dopisek o śladowych ilościach (intake „Alergeny”) | 2.3 |
| oferta-gf-note | Nad cennikiem | p krótki | 20 słów, fakt z intake: chleb bezglutenowy pieczony w osobnej strefie (intake odp. 27) | 2.4 |
| oferta-filter-title | Filtr | etykieta | 3 słowa | 2.5 |
| oferta-filter-gf | Filtr | chip | 3 słowa (bez glutenu) | 2.5 |
| oferta-filter-lf | Filtr | chip | 3 słowa (bez laktozy) | 2.5 |
| oferta-filter-nuts | Filtr | chip | 3 słowa (bez orzechów) | 2.5 |
| oferta-filter-sesame | Filtr | chip | 3 słowa (bez sezamu) | 2.5 |
| oferta-filter-reset | Filtr | przycisk | 3 słowa | 2.5 |
| oferta-filter-status | Filtr | sr (aria-live), wzór z liczbą | 5 słów | 2.5 |
| oferta-filter-empty | Filtr | p | 12 słów | 2.5 |
| oferta-filter-trace | Filtr | p krótki | 20 słów (przypomnienie o śladach; może cytować dopisek) | 2.5 / 2.3 |
| oferta-cta-title | Pas „Zamów” | h2 | 8 słów | 2.6 |
| oferta-cta-text | Pas „Zamów” | p | 25 słów, fakty z intake „Zamówienia z wyprzedzeniem” | 2.6 |
| oferta-cta-order | Pas „Zamów” | przycisk | fakt: „Zamów” | 2.6 |

**Produkty w cenniku (22 produkty × 3 id + 5 id `-when` = 71 id).** Wszystko to fakty z intake: nazwa i cena z intake „Oferta z cenami” (tabela główna oraz „Wypieki dnia spoza powyższego cennika”), alergeny z intake „Alergeny”, przypisanie do kategorii z briefu „Fakty z wejścia”. Podsekcje briefu: 2.1 (nazwa, cena) i 2.2 (alergeny).

| Kategoria | Nazwa (id) | Cena (id) | Alergeny (id) | Dodatkowo |
|---|---|---|---|---|
| Pieczywo | oferta-p-chleb-zytni-name | oferta-p-chleb-zytni-price | oferta-p-chleb-zytni-alg | |
| Pieczywo | oferta-p-chleb-pszenny-name | oferta-p-chleb-pszenny-price | oferta-p-chleb-pszenny-alg | |
| Pieczywo | oferta-p-bagietka-name | oferta-p-bagietka-price | oferta-p-bagietka-alg | |
| Pieczywo | oferta-p-kajzerka-name | oferta-p-kajzerka-price | oferta-p-kajzerka-alg | |
| Pieczywo | oferta-p-grahamka-name | oferta-p-grahamka-price | oferta-p-grahamka-alg | |
| Pieczywo | oferta-p-chleb-orkiszowy-name | oferta-p-chleb-orkiszowy-price | oferta-p-chleb-orkiszowy-alg | |
| Pieczywo | oferta-p-chleb-bezglutenowy-name | oferta-p-chleb-bezglutenowy-price | oferta-p-chleb-bezglutenowy-alg | + plakietka `oferta-badge-gf` |
| Pieczywo | oferta-p-focaccia-name | oferta-p-focaccia-price | oferta-p-focaccia-alg | |
| Pieczywo | oferta-p-chalka-name | oferta-p-chalka-price | oferta-p-chalka-alg | |
| Słodkie wypieki | oferta-p-paczek-name | oferta-p-paczek-price | oferta-p-paczek-alg | |
| Słodkie wypieki | oferta-p-drozdzowka-ser-name | oferta-p-drozdzowka-ser-price | oferta-p-drozdzowka-ser-alg | |
| Słodkie wypieki | oferta-p-rogal-name | oferta-p-rogal-price | oferta-p-rogal-alg | dostępny cały rok (brief), bez oznaczenia sezonu |
| Słodkie wypieki | oferta-p-szarlotka-name | oferta-p-szarlotka-price | oferta-p-szarlotka-alg | cena „8 zł/kawałek” |
| Słodkie wypieki | oferta-p-drozdzowka-bez-laktozy-name | oferta-p-drozdzowka-bez-laktozy-price | oferta-p-drozdzowka-bez-laktozy-alg | + plakietka `oferta-badge-lf` |
| Wypieki dnia | oferta-p-bulka-ziarna-name | oferta-p-bulka-ziarna-price | oferta-p-bulka-ziarna-alg | `oferta-p-bulka-ziarna-when` (wtorek) |
| Wypieki dnia | oferta-p-chleb-zurawina-name | oferta-p-chleb-zurawina-price | oferta-p-chleb-zurawina-alg | `oferta-p-chleb-zurawina-when` (środa) |
| Wypieki dnia | oferta-p-ciasto-drozdzowe-name | oferta-p-ciasto-drozdzowe-price | oferta-p-ciasto-drozdzowe-alg | `oferta-p-ciasto-drozdzowe-when` (niedziela). Nazwa zawsze „ciasto drożdżowe z kruszonką”, cena „6 zł / kawałek” |
| Sezonowe | oferta-p-pierniki-name | oferta-p-pierniki-price | oferta-p-pierniki-alg | `oferta-p-pierniki-when` (grudzień). Nazwa z „opakowanie 250 g” |
| Sezonowe | oferta-p-mazurek-name | oferta-p-mazurek-price | oferta-p-mazurek-alg | `oferta-p-mazurek-when` (Wielkanoc) |
| Torty i ciasta | oferta-p-tort-name | oferta-p-tort-price | oferta-p-tort-alg | cena „od 120 zł”, alergeny: fakt „zależnie od zamówienia, informacja przy składaniu” |
| Kanapki i przekąski | oferta-p-kanapka-jajeczna-name | oferta-p-kanapka-jajeczna-price | oferta-p-kanapka-jajeczna-alg | (alergeny obejmują „gorczyca”) |
| Kanapki i przekąski | oferta-p-zapiekanka-name | oferta-p-zapiekanka-price | oferta-p-zapiekanka-alg | |

### 3. Zamówienia (51 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| zam-page-title | head | meta title | 60 znaków | 3 |
| zam-meta | head | meta description | 155 znaków | 3 |
| zam-title | Nagłówek | h1 | 5 słów | 3 |
| zam-lead | Nagłówek | lead | 30 słów | 3 |
| zam-rules-title | Zasady | h2 | 5 słów | 3.1 |
| zam-rules-1 | Zasady | punkt | 15 słów, fakt z intake: telefonicznie (+48 512 345 678) lub przez formularz | 3.1 |
| zam-rules-2 | Zasady | punkt | 15 słów, fakt z intake: najpóźniej dzień wcześniej do 14:00 | 3.1 |
| zam-rules-3 | Zasady | punkt | 15 słów, fakt z intake: torty okolicznościowe min. 3 dni wcześniej | 3.1 |
| zam-delivery-title | Odbiór i dostawa | h2 | 5 słów | 3.2 |
| zam-pickup-title | Karta odbioru | h3 | 3 słowa | 3.2 |
| zam-pickup-text | Karta odbioru | p | 20 słów, fakt z intake: odbiór osobisty w piekarni + adres | 3.2 |
| zam-dostawa-title | Karta dostawy | h3 | 3 słowa | 3.2 |
| zam-dostawa-text | Karta dostawy | p | 25 słów, fakt z intake: promień 10 km, gratis od 80 zł, poniżej 10 zł. Bez dni i godzin | 3.2 |
| zam-pay-title | Karta płatności | h3 | 3 słowa | 3.3 |
| zam-pay-text | Karta płatności | p | 15 słów, fakt z briefu (odp. 5a): przy odbiorze lub przy dostawie | 3.3 |
| zam-form-title | Formularz | h2 | 5 słów | 3.4 |
| zam-form-lead | Formularz | lead | 20 słów | 3.4 |
| zam-step1-legend | Krok 1 | legend | 4 słowa | 3.4 |
| zam-step2-legend | Krok 2 | legend | 5 słów | 3.4 |
| zam-step3-legend | Krok 3 | legend | 3 słowa | 3.4 |
| zam-f-product-label | Krok 1 | etykieta pola | 2 słowa | 3.4 |
| zam-f-product-placeholder | Krok 1 | opcja 0 selecta | 3 słowa | 3.4 |
| zam-f-qty-label | Krok 1 | etykieta pola | 1 słowo | 3.4 |
| zam-f-rows-hint | Krok 1 | podpowiedź | 15 słów | 3.4 |
| zam-f-date-label | Krok 2 | etykieta pola | 4 słowa | 3.4 |
| zam-f-date-hint | Krok 2 | podpowiedź dynamiczna (2 warianty: zwykły / tort) | 20 słów, fakt z intake: terminy | 3.4 / 3.1 |
| zam-f-method-legend | Krok 2 | legend radia | 4 słowa | 3.4 |
| zam-f-method-pickup | Krok 2 | etykieta radia | 4 słowa | 3.4 |
| zam-f-method-delivery | Krok 2 | etykieta radia | 4 słowa (z „do 10 km”) | 3.4 |
| zam-f-address-label | Krok 2 | etykieta pola | 2 słowa | 3.4 |
| zam-f-address-hint | Krok 2 | podpowiedź | 12 słów | 3.4 |
| zam-f-delivery-cost-hint | Krok 2 | podpowiedź | 20 słów, fakt z intake: gratis od 80 zł, poniżej 10 zł, promień 10 km | 3.4 / 3.2 |
| zam-f-name-label | Krok 3 | etykieta pola | 3 słowa | 3.4 |
| zam-f-phone-label | Krok 3 | etykieta pola | 1 słowo | 3.4 |
| zam-f-email-label | Krok 3 | etykieta pola | 3 słowa (z oznaczeniem „opcjonalnie”, P7) | 3.4 |
| zam-f-notes-label | Krok 3 | etykieta pola | 2 słowa | 3.4 |
| zam-f-notes-hint | Krok 3 | podpowiedź | 15 słów (np. do tortu) | 3.4 |
| zam-f-required-note | Formularz | p krótki | 8 słów | 3.4 |
| zam-f-pay-note | Formularz | p krótki | 15 słów, fakt z briefu: płatność przy odbiorze / dostawie, bez płatności online | 3.4 / 3.3 |
| zam-f-submit | Formularz | przycisk | 3 słowa | 3.4 |
| zam-f-success | Formularz | komunikat | 30 słów (nie obiecywać terminu odpowiedzi, bo nie ma go w intake) | 3.4 |
| zam-f-error-generic | Formularz | komunikat | 20 słów | 3.4 |
| zam-f-err-required | Formularz | błąd pola | 6 słów | 3.4 |
| zam-f-err-date | Formularz | błąd pola | 20 słów, fakt: dzień wcześniej do 14:00 | 3.4 |
| zam-f-err-date-tort | Formularz | błąd pola | 20 słów, fakt: torty min. 3 dni | 3.4 |
| zam-f-err-phone | Formularz | błąd pola | 10 słów | 3.4 |
| zam-f-err-address | Formularz | błąd pola | 10 słów | 3.4 |
| zam-phone-title | Telefon | h2/h3 | 6 słów | 3.5 |
| zam-phone-text | Telefon | p | 20 słów (bez godzin przyjmowania telefonów, których nie ma w intake) | 3.5 |
| zam-phone-number | Telefon | link tel | fakt z intake: +48 512 345 678 | 3.5 |
| zam-phone-aria | Telefon | aria | 5 słów + numer | 3.5 |

### 4. O nas (42 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| onas-page-title | head | meta title | 60 znaków | 4 |
| onas-meta | head | meta description | 155 znaków | 4 |
| onas-title | Nagłówek | h1 | 5 słów | 4 |
| onas-lead | Nagłówek | lead | 25 słów | 4 |
| onas-usp-title | Wyróżniki | h2 (może być sr) | 5 słów | Wyróżniki (dotąd 1.2) |
| onas-usp-1 | Wyróżniki | hasło | 6 słów, fakt z briefu: od 1987 r. (ta sama receptura chleba żytniego) | Wyróżniki |
| onas-usp-2 | Wyróżniki | hasło | 6 słów, fakt: 18 h fermentacji zakwasu | Wyróżniki |
| onas-usp-3 | Wyróżniki | hasło | 4 słowa, fakt: bez polepszaczy | Wyróżniki |
| onas-usp-4 | Wyróżniki | hasło | 5 słów, fakt: osobna strefa bezglutenowa | Wyróżniki |
| onas-usp-5 | Wyróżniki | hasło | 8 słów, fakt: dostawa gratis od 80 zł (w promieniu 10 km) | Wyróżniki |
| onas-hist-title | Historia | h2 | 6 słów | 4.1 |
| onas-hist-1-year | Historia | liczba dekoracyjna | fakt z intake: „1987” | 4.1 |
| onas-hist-1-title | Historia | h3 | 6 słów | 4.1 |
| onas-hist-1-text | Historia | p | 50 słów, fakty z intake „Historia” (Józef Kowalczyk, przepisy z rodzinnej wsi, przez lata doskonalił) | 4.1 |
| onas-hist-1-img-alt | Historia | alt | 15 słów (zdjęcie zastępcze, **nie opisywać go jako prawdziwego zdjęcia założyciela**) | 4.1 |
| onas-hist-2-year | Historia | etykieta dekoracyjna | 1 słowo („Dziś”) | 4.1 |
| onas-hist-2-title | Historia | h3 | 6 słów | 4.1 |
| onas-hist-2-text | Historia | p | 50 słów, fakty z intake: syn i wnuczka, ręcznie, tradycyjnie, bez sztucznych polepszaczy | 4.1 |
| onas-hist-2-img-alt | Historia | alt | 15 słów | 4.1 |
| onas-bake-title | Jak pieczemy | h2 | 5 słów | 4.2 |
| onas-bake-lead | Jak pieczemy | lead | 30 słów | 4.2 |
| onas-bake-big-number | Jak pieczemy | liczba dekoracyjna | fakt z intake: „18 h” | 4.2 |
| onas-bake-big-label | Jak pieczemy | etykieta | 8 słów (fermentacja zakwasu) | 4.2 |
| onas-bake-fact-1-title | Fakt 1 | h3 | 4 słowa (naturalny zakwas) | 4.2 |
| onas-bake-fact-1-text | Fakt 1 | p | 20 słów (może zawierać: ta sama receptura od 1987 r.) | 4.2 |
| onas-bake-fact-2-title | Fakt 2 | h3 | 4 słowa (18 h fermentacji) | 4.2 |
| onas-bake-fact-2-text | Fakt 2 | p | 20 słów | 4.2 |
| onas-bake-fact-3-title | Fakt 3 | h3 | 4 słowa (ręcznie, tradycyjnie) | 4.2 |
| onas-bake-fact-3-text | Fakt 3 | p | 20 słów | 4.2 |
| onas-bake-fact-4-title | Fakt 4 | h3 | 4 słowa (bez polepszaczy) | 4.2 |
| onas-bake-fact-4-text | Fakt 4 | p | 20 słów | 4.2 |
| onas-gal-title | Galeria | h2 | 4 słowa | 4.3 |
| onas-gal-lead | Galeria | lead | 15 słów | 4.3 |
| onas-gal-1-alt | Galeria | alt (wypieki) | 12 słów | 4.3 |
| onas-gal-2-alt | Galeria | alt (wypieki) | 12 słów | 4.3 |
| onas-gal-3-alt | Galeria | alt (wypieki) | 12 słów | 4.3 |
| onas-gal-4-alt | Galeria | alt (wypieki) | 12 słów | 4.3 |
| onas-gal-5-alt | Galeria | alt (wnętrze) | 12 słów | 4.3 |
| onas-gal-6-alt | Galeria | alt (wnętrze) | 12 słów | 4.3 |
| onas-gal-7-alt | Galeria | alt (praca przy piecu) | 12 słów | 4.3 |
| onas-gal-8-alt | Galeria | alt (praca przy piecu) | 12 słów | 4.3 |
| onas-gal-9-alt | Galeria | alt (praca przy piecu) | 12 słów | 4.3 |

### 5. Aktualności (42 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| akt-page-title | head | meta title | 60 znaków | 5 |
| akt-meta | head | meta description | 155 znaków | 5 |
| akt-title | Nagłówek | h1 | 4 słowa | 5 |
| akt-lead | Nagłówek | lead | 25 słów | 5 |
| akt-cal-title | Kalendarz | h2 | 5 słów | 5.3 |
| akt-cal-1-when | Kalendarz | etykieta | fakt z intake: „tłusty czwartek” | 5.3 |
| akt-cal-1-what | Kalendarz | p krótki | **OTWARTE (P4)**: intake nie wskazuje produktu | 5.3 |
| akt-cal-2-when | Kalendarz | etykieta | fakt z intake: „11 listopada” | 5.3 |
| akt-cal-2-what | Kalendarz | p krótki | fakt z intake: rogale | 5.3 |
| akt-cal-3-when | Kalendarz | etykieta | fakt z intake: „grudzień” | 5.3 |
| akt-cal-3-what | Kalendarz | p krótki | fakt z intake: pierniki | 5.3 |
| akt-cal-4-when | Kalendarz | etykieta | fakt z intake: „Wielkanoc” | 5.3 |
| akt-cal-4-what | Kalendarz | p krótki | fakt z intake: mazurki | 5.3 |
| akt-list-title | Lista | h2 (może być sr) | 3 słowa | 5.1 |
| akt-tag-wd | Plakietka kategorii | etykieta | fakt z intake: „Wypiek dnia” | 5.1 |
| akt-tag-season | Plakietka kategorii | etykieta | 2 słowa | 5.1 |
| akt-post-1-title | Wpis 1 (wypiek dnia) | h3 (h1 we wpisie) | 10 słów | 5.1 / 5.2 |
| akt-post-1-date | Wpis 1 | data | format „DD miesiąc RRRR”, nie z przyszłości | 5.1 / 5.2 |
| akt-post-1-excerpt | Wpis 1 | p | 25 słów | 5.1 |
| akt-post-1-img-alt | Wpis 1 | alt | 12 słów | 5.1 / 5.2 |
| akt-post-1-more-aria | Wpis 1 | aria | 2 słowa + tytuł | 5.1 |
| akt-post-2-title | Wpis 2 (tłusty czwartek) | h3 | 10 słów | 5.1 / 5.2 |
| akt-post-2-date | Wpis 2 | data | jw. | 5.1 / 5.2 |
| akt-post-2-excerpt | Wpis 2 | p | 25 słów | 5.1 |
| akt-post-2-img-alt | Wpis 2 | alt | 12 słów | 5.1 / 5.2 |
| akt-post-2-more-aria | Wpis 2 | aria | 2 słowa + tytuł | 5.1 |
| akt-post-3-title | Wpis 3 (rogale na 11 listopada) | h3 | 10 słów | 5.1 / 5.2 |
| akt-post-3-date | Wpis 3 | data | jw. | 5.1 / 5.2 |
| akt-post-3-excerpt | Wpis 3 | p | 25 słów (rogal jest cały rok) | 5.1 |
| akt-post-3-img-alt | Wpis 3 | alt | 12 słów | 5.1 / 5.2 |
| akt-post-3-more-aria | Wpis 3 | aria | 2 słowa + tytuł | 5.1 |
| akt-post-4-title | Wpis 4 (pierniki w grudniu) | h3 | 10 słów | 5.1 / 5.2 |
| akt-post-4-date | Wpis 4 | data | jw. | 5.1 / 5.2 |
| akt-post-4-excerpt | Wpis 4 | p | 25 słów | 5.1 |
| akt-post-4-img-alt | Wpis 4 | alt | 12 słów | 5.1 / 5.2 |
| akt-post-4-more-aria | Wpis 4 | aria | 2 słowa + tytuł | 5.1 |
| akt-post-5-title | Wpis 5 (mazurki na Wielkanoc) | h3 | 10 słów | 5.1 / 5.2 |
| akt-post-5-date | Wpis 5 | data | jw. | 5.1 / 5.2 |
| akt-post-5-excerpt | Wpis 5 | p | 25 słów | 5.1 |
| akt-post-5-img-alt | Wpis 5 | alt | 12 słów | 5.1 / 5.2 |
| akt-post-5-more-aria | Wpis 5 | aria | 2 słowa + tytuł | 5.1 |
| akt-post-more | Karty wpisów | link | 2 słowa | 5.1 |

### 5.2 Szablon wpisu (19 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| wpis-breadcrumb-aria | Okruszki | aria nav | 2 słowa | 5.2 |
| wpis-breadcrumb-home | Okruszki | link | fakt z briefu: „Start” | 5.2 |
| wpis-breadcrumb-list | Okruszki | link | fakt z briefu: „Aktualności” | 5.2 |
| wpis-back-link | Stopka wpisu | link | 4 słowa | 5.2 |
| wpis-1-page-title | Wpis 1 | meta title | 60 znaków | 5.2 |
| wpis-1-meta | Wpis 1 | meta description | 155 znaków | 5.2 |
| wpis-1-body | Wpis 1 | treść (akapity) | 250 słów, tylko fakty z intake (harmonogram wypieku dnia) | 5.2 |
| wpis-2-page-title | Wpis 2 | meta title | 60 znaków | 5.2 |
| wpis-2-meta | Wpis 2 | meta description | 155 znaków | 5.2 |
| wpis-2-body | Wpis 2 | treść | 200 słów (P4: bez przypisywania produktu do czasu odpowiedzi) | 5.2 |
| wpis-3-page-title | Wpis 3 | meta title | 60 znaków | 5.2 |
| wpis-3-meta | Wpis 3 | meta description | 155 znaków | 5.2 |
| wpis-3-body | Wpis 3 | treść | 200 słów (cena i alergeny rogala z intake) | 5.2 |
| wpis-4-page-title | Wpis 4 | meta title | 60 znaków | 5.2 |
| wpis-4-meta | Wpis 4 | meta description | 155 znaków | 5.2 |
| wpis-4-body | Wpis 4 | treść | 200 słów (pierniki: 250 g, 18 zł, alergeny z intake) | 5.2 |
| wpis-5-page-title | Wpis 5 | meta title | 60 znaków | 5.2 |
| wpis-5-meta | Wpis 5 | meta description | 155 znaków | 5.2 |
| wpis-5-body | Wpis 5 | treść | 200 słów (mazurek kajmakowy: 45 zł, alergeny z intake) | 5.2 |

### 6. Kontakt (57 id)
| id | Sekcja | Typ | Maks. długość | Podsekcja briefu |
|----|--------|-----|---------------|------------------|
| kont-page-title | head | meta title | 60 znaków | 6 |
| kont-meta | head | meta description | 155 znaków | 6 |
| kont-title | Nagłówek | h1 | 4 słowa | 6 |
| kont-lead | Nagłówek | lead | 20 słów | 6 |
| kont-data-title | Dane | h2 | 4 słowa | 6.1 |
| kont-address-label | Dane | etykieta | 1 słowo | 6.1 |
| kont-address | Dane | tekst | fakt z intake: ul. Rynek 12, 05-140 Serock | 6.1 |
| kont-phone-label | Dane | etykieta | 1 słowo | 6.1 |
| kont-phone | Dane | link tel | fakt z intake: +48 512 345 678 | 6.1 |
| kont-phone-aria | Dane | aria | 5 słów + numer | 6.1 |
| kont-email-label | Dane | etykieta | 1 słowo | 6.1 |
| kont-email | Dane | link mailto | fakt z intake: kontakt@piekarynkanadzegrzem.pl (przykładowy) | 6.1 |
| kont-social-label | Dane | etykieta | 2 słowa | 6.1 |
| kont-fb | Dane | link | fakt z intake: Facebook @piekarynkanadzegrzem (przykładowy) | 6.1 |
| kont-fb-aria | Dane | aria | 8 słów | 6.1 |
| kont-ig | Dane | link | fakt z intake: Instagram @piekarynkanadzegrzem (przykładowy) | 6.1 |
| kont-ig-aria | Dane | aria | 8 słów | 6.1 |
| kont-hours-title | Godziny | h2 | 3 słowa | 6.2 |
| kont-hours-weekdays | Godziny | wiersz | fakt z intake: pon.–pt. 6:00–19:00 | 6.2 |
| kont-hours-sat | Godziny | wiersz | fakt z intake: sob. 6:30–15:00 | 6.2 |
| kont-hours-sun | Godziny | wiersz | fakt z intake: niedz. 7:00–13:00 | 6.2 |
| kont-hours-note | Godziny | p krótki | fakt z intake: świeże pieczywo codziennie od otwarcia, druga dostawa ok. 12:00 | 6.2 |
| kont-map-title | Mapa | h2 | 4 słowa | 6.3 |
| kont-map-iframe-title | Mapa | aria (`title` iframe) | 10 słów, z adresem | 6.3 |
| kont-map-route | Mapa | przycisk-link | 3 słowa | 6.3 |
| kont-map-route-aria | Mapa | aria | 10 słów (z informacją o nowej karcie) | 6.3 |
| kont-map-fallback | Mapa | p krótki | 15 słów | 6.3 |
| kont-form-title | Formularz | h2 | fakt: „Napisz do nas” | 6.4 |
| kont-form-lead | Formularz | lead | 20 słów | 6.4 |
| kont-f-name-label | Formularz | etykieta pola | 1 słowo | 6.4 |
| kont-f-contact-label | Formularz | etykieta pola | 4 słowa (telefon lub e-mail) | 6.4 |
| kont-f-contact-hint | Formularz | podpowiedź | 10 słów | 6.4 |
| kont-f-message-label | Formularz | etykieta pola | 1 słowo | 6.4 |
| kont-f-message-hint | Formularz | podpowiedź | 15 słów (może wspomnieć o firmach B2B) | 6.4 / 1.6 |
| kont-f-required-note | Formularz | p krótki | 8 słów | 6.4 |
| kont-f-submit | Formularz | przycisk | 3 słowa | 6.4 |
| kont-f-success | Formularz | komunikat | 25 słów (bez obietnicy czasu odpowiedzi) | 6.4 |
| kont-f-error-generic | Formularz | komunikat | 20 słów | 6.4 |
| kont-f-err-required | Formularz | błąd pola | 6 słów | 6.4 |
| kont-f-err-contact | Formularz | błąd pola | 12 słów | 6.4 |
| kont-faq-title | FAQ | h2 | 5 słów | 6.5 |
| kont-faq-1-q | FAQ | pytanie (summary) | 12 słów: termin zamówień | 6.5 |
| kont-faq-1-a | FAQ | odpowiedź | 40 słów, fakt z intake: dzień wcześniej do 14:00, telefon lub formularz | 6.5 |
| kont-faq-2-q | FAQ | pytanie | 12 słów: torty | 6.5 |
| kont-faq-2-a | FAQ | odpowiedź | 40 słów, fakt z intake: min. 3 dni, od 120 zł za 1,5 kg, alergeny zależnie od zamówienia | 6.5 |
| kont-faq-3-q | FAQ | pytanie | 12 słów: dostawa i koszt | 6.5 |
| kont-faq-3-a | FAQ | odpowiedź | 40 słów, fakt z intake: 10 km, gratis od 80 zł, poniżej 10 zł, odbiór osobisty | 6.5 |
| kont-faq-4-q | FAQ | pytanie | 12 słów: płatność | 6.5 |
| kont-faq-4-a | FAQ | odpowiedź | 30 słów, fakt z briefu: przy odbiorze lub przy dostawie, bez płatności online | 6.5 |
| kont-faq-5-q | FAQ | pytanie | 12 słów: godziny | 6.5 |
| kont-faq-5-a | FAQ | odpowiedź | 40 słów, fakt z intake: godziny + druga dostawa ok. 12:00 | 6.5 |
| kont-faq-6-q | FAQ | pytanie | 12 słów: alergeny i ślady | 6.5 |
| kont-faq-6-a | FAQ | odpowiedź | 40 słów, fakt z intake: alergeny przy każdym produkcie + dosłowny dopisek o śladach | 6.5 |
| kont-faq-7-q | FAQ | pytanie | 12 słów: chleb bezglutenowy | 6.5 |
| kont-faq-7-a | FAQ | odpowiedź | 40 słów, fakt z intake: osobna strefa, 16 zł, alergeny: jaja. Uwaga: dopisek o śladach orzechów i sezamu obowiązuje też tutaj, więc nie pisać „bez alergenów” | 6.5 |
| kont-faq-8-q | FAQ | pytanie | 12 słów: obsługa firm | 6.5 |
| kont-faq-8-a | FAQ | odpowiedź | 40 słów, fakt z intake: kawiarnie, restauracje, sklepy, codzienne poranne dostawy, kontakt przez formularz. Bez warunków | 6.5 |

### Podsumowanie liczby id
| Grupa | Liczba id |
|---|---|
| 0. Wspólne | 48 |
| 1. Start | 66 |
| 2. Oferta (33 w tabeli ogólnej + 71 w tabeli produktów) | 104 |
| 3. Zamówienia | 51 |
| 4. O nas (w tym 6 id Wyróżników) | 42 |
| 5. Aktualności | 42 |
| 5.2 Szablon wpisu | 19 |
| 6. Kontakt | 57 |
| **Razem** | **429** |

`page-title` i `meta-description` są dla każdej podstrony (6 × 2) oraz dla każdego z 5 wpisów (5 × 2).

---

## Responsywność i interakcje

### Punkty przełamania (mobile-first)
| Zakres | Nazwa | Najważniejsze zmiany |
|---|---|---|
| < 480 px | mały telefon | 1 kolumna, CTA na pełną szerokość, przyklejony pasek 0.3 |
| 480–767 px | telefon | galeria i kalendarz sezonowy w 2 kolumnach |
| 768–1099 px | tablet | pasek górny widoczny, oba CTA w nagłówku, menu pod przyciskiem „Menu”, siatki 2-kolumnowe, bez paska 0.3 |
| ≥ 1100 px | desktop | pełne menu, siatki 3–5 kolumn, formularz 8/4 z przyklejoną kolumną |

Urządzenia są „po równo” (intake C), więc oba widoki projektuję z tą samą starannością, a prototyp pokazuje oba (zwężenie okna).

### Interakcje
- **Menu mobilne/tabletowe:** przycisk „Menu” z hamburgerem → panel wysuwany z góry (`transform: translateY`, 200 ms ease-out). Pod panelem przyciemnienie tła, Esc i klik w tło zamykają panel, focus pozostaje w panelu (focus trap), a po zamknięciu wraca na przycisk. Bez JS: menu widoczne jako lista pod znakiem słownym.
- **Pasek główny** przyklejony (`position: sticky`) i po przewinięciu > 40 px dostaje cień. Pasek górny przewija się razem ze stroną.
- **Hover (tylko `@media (hover: hover)`):** przyciski wg tokenów, karty z podniesieniem i `--shadow-2`, powiększenie zdjęć w kartach do 1.03, linki z grubszym podkreśleniem.
- **Focus:** zawsze widoczny (`:focus-visible`), 3 px `--focus` + 2 px odsunięcia, również na chipach filtra, `summary` FAQ i kartach.
- **FAQ:** `<details>/<summary>`, ikona +/− obracana CSS-em.
- **Filtr oferty:** natychmiastowe ukrywanie wierszy (`hidden`), komunikat w `aria-live`. Kategoria, w której nic nie zostało, zwija się do nagłówka z notką `oferta-filter-empty`.
- **Wypiek dnia / godziny na dziś:** wyliczane w przeglądarce (Europe/Warsaw), bez migotania: domyślny HTML to wersja bez „dziś”, a JS ją wzbogaca.
- **Animacje:** tylko przejścia 150–250 ms na hover i menu. **Żadnych animacji pojawiania się treści przy przewijaniu** (w L1, L3 i R1 dawały puste miejsca). `@media (prefers-reduced-motion: reduce)` wyłącza przejścia i `scale`.
- **Zdjęcia tła:** `<img>` + `object-fit: cover` (alt zgodnie z mapą; dekoracyjne pasy podstron `alt=""`), `srcset` 480 / 960 / 1600 / 2400 px, hero `fetchpriority="high"`, reszta `loading="lazy"` z wymiarami. Kadry z punktem ciężkości (`object-position`) ustawionym osobno dla mobile i desktop.
- **Formularze:** wielkie pola (min. 52 px wysokości, 18 px tekstu), etykiety zawsze nad polem (nie placeholder zamiast etykiety), `autocomplete` (name, tel, email, street-address), `inputmode="tel"`.
- **Tryb ciemny:** wyłącznie automatyczny (`prefers-color-scheme`), bez przełącznika, zgodnie z intake D. `color-scheme: light dark` w `:root`, żeby natywne kontrolki (date, select) też się przełączały. Zdjęcia bez zmian, a nakładki są te same.

---

## Uwagi dla codera

1. **Tokeny:** zdefiniuj wszystkie kolory z sekcji „Design tokens” jako zmienne CSS w `:root` i nadpisz je w `@media (prefers-color-scheme: dark)`. Nie wpisuj hexów bezpośrednio w komponentach. **Złoto `--accent` w trybie jasnym nigdy jako kolor tekstu na jasnym tle.**
2. **Fonty:** Google Fonts `Alegreya:ital,wght@0,700;1,400;1,700` i `Mulish:wght@400;600;700`, `display=swap`, `subset latin-ext` (polskie znaki), `preconnect` do fonts.googleapis.com i fonts.gstatic.com. Fallback: `Georgia, serif` / `system-ui, sans-serif`.
3. **Jedno źródło danych produktów:** nazwy, ceny, alergeny, kategorie i przypisanie „wypieku dnia” do dni trzymaj w jednym miejscu (np. obiekt JS lub `data-*` generowane z jednej listy). Z niego powinny korzystać cennik, karta „Dziś”, harmonogram, karty specjalności i select w formularzu zamówienia. Dzięki temu cena nie rozjedzie się między stronami. Teksty dostarczy writer według id z mapy tekstów, a fakty muszą zgadzać się 1:1 z intake.md.
4. **Filtr „bez laktozy”** działa tylko na produktach z frazą „bez laktozy” w nazwie (brief 2.4 / odp. 4a), a nie na podstawie braku „mleko”. Tort ma flagę `unknown`, a jego zachowanie w filtrze czeka na odpowiedź (P3).
5. **Reguły daty** w formularzu zamówienia zapisz jako stałe (`ORDER_CUTOFF_HOUR = 14`, `CAKE_MIN_DAYS = 3`). Interpretacja „3 dni” jest otwarta (P6). Czas licz w `Europe/Warsaw` (np. `Intl.DateTimeFormat` z `timeZone`). Nie blokuj dni tygodnia, bo intake nie podaje dni dowozu.
6. **Wysyłka formularzy:** sposób wysyłki (usługa formularzy, własny backend, mailto) nie wynika z briefu, więc manager musi go ustalić z użytkownikiem (P8). Do tego czasu zrób formularze z pełną walidacją i komunikatem sukcesu w trybie demo.
7. **Mapa:** preferowany embed OpenStreetMap (brak cookies stron trzecich, więc bez baneru zgody). Link „Wyznacz trasę” jako zwykły link zewnętrzny z `rel="noopener"` i informacją o nowej karcie (`g-new-tab-sr`).
8. **Zdjęcia zastępcze:** jednolite proporcje (hero 16:9 desktop / 4:5 mobile, karty 4:3, wpisy 16:9, galeria 1:1), ciepła tonacja. Źródło (np. darmowe zdjęcia na licencji CC0 albo neutralne placeholdery) potwierdza manager (P9). Plik nazwij tak, żeby było jasne, że to placeholder (`placeholder-hero.jpg`).
9. **Bez banerów zasłaniających treść.** Jeśli coś będzie wymagało zgody na cookies (np. mapa Google), baner ma być mały, przy dolnej krawędzi i nie może zasłaniać CTA ani paska 0.3.
10. **Dane przykładowe** (e-mail, FB, IG) wstaw tak jak w intake, ale w kodzie oznacz je komentarzem `<!-- DANE PRZYKŁADOWE -->`, żeby łatwo było je podmienić.
11. **Semantyka:** jeden `h1` na stronę, landmarki `header / nav / main / footer`, cennik jako `<table>` (na mobile przestylowana), godziny jako `<table>` lub `<dl>`, daty w `<time>`, telefon `tel:+48512345678`, adres w `<address>`. Dane strukturalne `schema.org/Bakery` (nazwa, adres, telefon, godziny) w JSON-LD na Starcie i Kontakcie, tylko z faktami z intake.
12. **Wydajność:** bez frameworków, statyczny HTML/CSS + mały JS (menu, wypiek dnia, godziny na dziś, filtr, walidacja). Obrazy w WebP/AVIF z fallbackiem JPG.
13. **Czego nie robić:** nie dodawaj sekcji spoza briefu (np. opinii klientów, newslettera, kafli szybkich akcji z L2), nie dodawaj przełącznika motywu, nie używaj karuzel ani animacji przy przewijaniu.

---

## Otwarte pytania (do przekazania użytkownikowi przez managera)
- **P1.** Wyróżniki (5 haseł z ikonami) są na podstronie O nas, zgodnie z Twoją decyzją. W którym miejscu tej podstrony? Proponuję zaraz pod nagłówkiem, przed Historią. Alternatywa: po „Jak pieczemy”. Trzy hasła (1987, 18 h, bez polepszaczy) tematycznie powtarzają się z „Jak pieczemy”. Czy takie powtórzenie jest OK?
- **P2.** Z Braci Kowalskich (strona 3) przenoszę układ (telefon w nagłówku, historia „wtedy / dziś”, duże zdjęcia), ale **nie czerwień**, bo w preferencjach kolorów podałeś beże, brązy i złoto. Czy tak zostaje?
- **P3.** Filtr diet w Ofercie: jak traktować **tort** (alergeny „zależnie od zamówienia”)? a) ukrywać go przy każdym aktywnym filtrze, b) pokazywać zawsze z dopiskiem „alergeny ustalamy przy zamówieniu”, c) inaczej.
- **P4.** W kalendarzu sezonowym (i we wpisie) przy **tłustym czwartku** intake nie wymienia produktu. Czy wpisać „pączki” (np. pączki z różą z oferty), czy zostawić sam termin?
- **P5.** Formularze zbierają dane osobowe (imię, telefon, adres). Czy dodać krótką klauzulę informacyjną RODO / link do polityki prywatności? Brief takiej sekcji nie ma, więc zostawiłem tylko miejsce.
- **P6.** Torty „z min. 3-dniowym wyprzedzeniem”: czy np. zamawiając w poniedziałek, najwcześniejszy odbiór to czwartek? Czy godzina 14:00 dotyczy też tortów?
- **P7.** W formularzu zamówienia telefon jest wymagany, a e-mail opcjonalny. Czy tak może być?
- **P8.** (techniczne, dla managera) Jak mają być wysyłane formularze i jaka mapa (OpenStreetMap bez cookies czy Google Maps z banerem zgody)?
- **P9.** (techniczne, dla managera) Skąd zdjęcia zastępcze: darmowe zdjęcia stockowe (CC0) czy neutralne szare placeholdery?
