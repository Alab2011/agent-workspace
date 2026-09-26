# Research: test-piekarnia

> **Status: NIEPEŁNY. Nie udało się przejrzeć ani jednej strony.**
> Każda próba WebFetch (12 z 12) skończyła się błędem `EGRESS_BLOCKED`: proxy sieciowe środowiska blokuje dostęp do tych domen, także do wikipedia.org. Działało tylko WebSearch, które zwraca tytuły, adresy URL i krótkie streszczenia wyników. **Nie widziałem układu, kolorów, typografii ani CTA żadnej strony.** Poniżej jest tylko to, co faktycznie było w wynikach wyszukiwania, z wyraźnym oznaczeniem źródła.

## Brief (jak zrozumiałem zadanie)
- Firma: „Piekarynka nad Zegrzem”, jedna piekarnia rzemieślnicza w Serocku (ul. Rynek 12). Chleb żytni na zakwasie według receptury od 1987 r., 18 h fermentacji, bez polepszaczy, osobna strefa bezglutenowa.
- Strona: wizytówka + blog/aktualności („wypiek dnia”, oferta sezonowa). Cele: zamówienia (torty, większe zamówienia, B2B) i wizerunek (historia rodzinna, tradycja).
- Dwa równorzędne CTA: „Zamów” i „Napisz do nas”.
- Odbiorcy: mieszkańcy okolicy, rodziny, osoby starsze, osoby pracujące w pobliżu.
- Wygląd: ciepły, domowy, beże/brązy/złoto/kolor skórki chleba; jasny motyw z automatycznym trybem ciemnym.
- Zakazy w treści: słowo „ekologiczne”, „najlepsze w okolicy”, „mąka z lokalnych młynów” ani żadne własne deklaracje.
- Zakres researchu (decyzja użytkownika): (1) lokalne piekarnie z okolic Serocka / Zalewu Zegrzyńskiego / Legionowa / Nieporętu, (2) najlepsze piekarnie rzemieślnicze w Polsce jako inspiracja wizualna.

## Przeanalizowane strony

**Przejrzane strony (WebFetch): 0.** Wszystkie poniższe próby zostały zablokowane, więc tych stron nie opisuję:

| Próba pobrania | Wynik |
|---|---|
| https://www.brodziknaturalnie.pl/ | zablokowane (EGRESS_BLOCKED) |
| https://piekarniagrzybki.pl/sklepy-firmowe/piekarnia-legionowo/ | zablokowane |
| https://www.putka.pl/ | zablokowane |
| http://toiowo.eu/jablonna-legionowo-fenomen-malej-piekarni/ | zablokowane |
| https://legionowo.pl/a/piekarnia | zablokowane |
| https://braciakowalscy.pl/ | zablokowane |
| https://mapa.targeo.pl/ (wpis Pychotka, Serock) | zablokowane |
| https://www.sztukamaki.pl/ | zablokowane |
| https://calawmace.pl/ | zablokowane |
| https://kukbuk.pl/artykuly/ranking-najlepsze-piekarnie-w-polsce/ | zablokowane |
| https://en.wikipedia.org/wiki/Piekarniak (test, czy działa cokolwiek) | zablokowane |

### Co widać w samych wynikach wyszukiwania (bez wizyty na stronach)
Poniżej są tylko fakty z tytułów i streszczeń WebSearch. Nie opisują one wyglądu stron.

#### Grupa 1: lokalne piekarnie (Serock, Legionowo, Nieporęt, Zalew Zegrzyński)
- **Serock (Rynek i okolice):** w katalogu Targeo pojawiają się Pychotka (Rynek 16), Cafe Filiżanka (Rynek 3), Cukiernia Sweet Home (Pułtuska 54a) i wpis „Lubaszka – Piekarnia”. W wynikach nie znalazłem własnej strony www żadnej piekarni z Serocka.
- **Brodzik Naturalnie, Legionowo** (brodziknaturalnie.pl): według streszczeń piekarnia na naturalnym zakwasie, bez drożdży, ze starych odmian zbóż. Tytuł strony głównej obiecuje „prawdziwy chleb” z naturalnych składników. Ma osobną podstronę kontaktową i wpisy produktowe (np. zakwas na żurek, cena podana na stronie produktu). Laureat plebiscytu „Orły Piekarnictwa”.
- **Piekarnia Grzybki, Legionowo** (piekarniagrzybki.pl): w strukturze URL widać sekcję „sklepy firmowe”, czyli podstrony poszczególnych punktów (sieć).
- **Putka, Legionowo/Nieporęt** (putka.pl): w wynikach adres, telefon, e-mail i godziny otwarcia (od 6:30 w dni robocze i soboty).
- **Bracia Kowalscy, Wólka Radzymińska / Nieporęt** (braciakowalscy.pl): według streszczenia chleb robiony częściowo ręcznie, z powolną fermentacją, a jako korzyść podają aromat, smak i dłuższą świeżość.
- **Artykuł toiowo.eu „Jabłonna/Legionowo. Fenomen małej piekarni”:** istnieje, ale nie mogłem go przeczytać.
- Lokalne portale z listami piekarni (gdziewlegionowie.pl, jezioro.zegrzynskie.pl, panoramafirm.pl, firmy.net) pokazują, że mieszkańcy szukają piekarni przez katalogi, gdzie liczą się adres, telefon i godziny.

#### Grupa 2: piekarnie rzemieślnicze w Polsce (inspiracja)
- **Cała w Mące, Warszawa-Żoliborz** (calawmace.pl, Instagram @calawmacepiekarnia): według streszczeń kilka lokalizacji, godziny podane per punkt, ok. 20 h fermentacji, właścicielka (piekarka i fotografka) jako twarz marki. Znana z jagodzianek i chałki.
- **Breaking Bread, Kraków** (breakingbread.dodla.pl): według streszczenia zakwas pszenny i żytni, zimna fermentacja ok. 16 h. Liczba godzin fermentacji pojawia się jako argument, tak jak nasze 18 h.
- **Sztuka Mąki, Grodzisk Mazowiecki** (sztukamaki.pl): tytuł strony to „Mikro Piekarnia Rzemieślnicza – Chleb na Zakwasie”, w nazwie od razu specjalność.
- **Bardzo Dobry Chleb** (sklep.bardzodobrychleb.pl): ma sklep internetowy.
- Rankingi i przewodniki (kukbuk.pl, label-magazine.com, twojstyl.pl, stronakuchni.pl, krakowfood.pl): istnieją, ale nie mogłem ich przeczytać.

## Wspólne wzorce w branży
Z samych wyników wyszukiwania (to są sygnały, nie obserwacje stron):
1. **Konkretne liczby jako argument jakości:** godziny fermentacji (16 h, ok. 20 h), naturalny zakwas, brak drożdży lub polepszaczy. To pasuje do naszych 18 h i receptury od 1987 r.
2. **Twarz / historia za marką:** właściciel lub rodzina jako element komunikacji (Cała w Mące, Bracia Kowalscy już w nazwie).
3. **Dane praktyczne na pierwszym planie:** adres, telefon, godziny otwarcia. Tak lokalne piekarnie występują w katalogach i portalach.
4. **Specjalność w tytule strony / nazwie** (Sztuka Mąki: „Chleb na Zakwasie”).
5. **Podstrona kontaktowa i podstrony punktów** (Brodzik, Grzybki).

**Nie jestem w stanie** ustalić wzorców wizualnych (układ sekcji, kolory, typografia, CTA), bo nie widziałem żadnej strony.

## Rekomendacje dla designera
- **Sekcje obecne u większości konkurencji: NIE DA SIĘ USTALIĆ (0 przejrzanych stron, więc 0/0).** Nie podaję liczb typu „6/7”, bo byłyby zmyślone. Z wyników wyszukiwania wynika tylko tyle, że u kilku firm istnieją: podstrona kontakt (Brodzik: 1 potwierdzony URL), godziny otwarcia (Putka, Cała w Mące: 2 w streszczeniach), podstrony punktów sprzedaży (Grzybki: 1), sklep online (Bardzo Dobry Chleb: 1). To nie jest porównanie sekcji.
- **Kierunek wizualny:** brak danych z researchu. Designer powinien oprzeć się na intake (ciepły, domowy, beże/brązy/złoto, skórka chleba, jasny + auto-ciemny).
- **Pomysły na wyróżnienie się (z briefu i sygnałów z wyszukiwania, do weryfikacji):**
  - W Serocku w wynikach nie znalazłem żadnej piekarni z własną stroną www, więc już porządna strona z ofertą, cenami i godzinami może być wyróżnikiem (do potwierdzenia po normalnym researchu).
  - Liczby na widoku: „18 h fermentacji”, „od 1987”, „druga dostawa ok. 12:00”, „dostawa gratis od 80 zł”.
  - „Wypiek dnia” na każdy dzień tygodnia jako żywy element strony głównej.
  - Alergeny przy każdym produkcie i osobna strefa bezglutenowa. W wynikach nie widziałem, by lokalna konkurencja to eksponowała (ale stron nie widziałem).
  - Rodzinna historia (trzy pokolenia) jako sekcja wizerunkowa.

**Rekomendacja dla managera:** powtórzyć research w środowisku z dostępem do sieci (albo poprosić użytkownika o zezwolenie na te domeny w ustawieniach sieci środowiska), zanim designer oprze się na tej sekcji.

## Źródła (lista linków)
Linki z wyników WebSearch (żadnego nie udało się otworzyć):
- https://mapa.targeo.pl/pychotka-rynek-16-05-140-serock~4641535/cukiernia-piekarnia/adres
- https://mapa.targeo.pl/cafe-filizanka-rynek-3-serock~10331073/cukiernia-piekarnia/adres
- https://mapa.targeo.pl/cukiernia-sweet-home-pultuska-54a-05-140-serock~5330268/cukiernia-piekarnia/adres
- https://mapa.targeo.pl/lubaszka-piekarnia-serock-powiat-legionowski/kategoria/3271/0921645
- https://brodziknaturalnie.pl/
- https://brodziknaturalnie.pl/kontakt-z-brodzik-naturalnie/
- https://legionowo.pl/a/piekarnia
- https://piekarniagrzybki.pl/sklepy-firmowe/piekarnia-legionowo/
- https://www.putka.pl/
- https://braciakowalscy.pl/
- http://toiowo.eu/jablonna-legionowo-fenomen-malej-piekarni/
- https://gdziewlegionowie.pl/aktualnosci/lista-piekarni-w-legionowie-gdzie-kupic-pieczywo-w-legionowie/
- https://jezioro.zegrzynskie.pl/wybierz-relaks/przy-stole/kawiarnie-i-cukiernie,s-3
- https://calawmace.pl/
- https://www.instagram.com/calawmacepiekarnia/
- https://breakingbread.dodla.pl/
- https://www.sztukamaki.pl/
- https://sklep.bardzodobrychleb.pl/zakwas/
- https://kukbuk.pl/artykuly/ranking-najlepsze-piekarnie-w-polsce/
- https://label-magazine.com/lifestyle/artykuly/najlepsze-piekarnie-rzemieslnicze-ktore-warto-odwiedzic-w-2026-roku
