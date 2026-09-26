# Research: test-piekarnia („Piekarynka nad Zegrzem”)

## Brief (jak zrozumiałem zadanie)
- **Firma:** „Piekarynka nad Zegrzem”, jedna piekarnia rzemieślnicza w Serocku (ul. Rynek 12). Założona w 1987 r. przez Józefa Kowalczyka, dziś prowadzą ją syn i wnuczka.
- **Wyróżnik merytoryczny:** chleb żytni na naturalnym zakwasie, receptura od 1987 r., 18 h fermentacji, bez polepszaczy, osobna strefa bezglutenowa, dostawa gratis od 80 zł (promień 10 km). **Nie wolno** pisać „ekologiczne”, „najlepsze w okolicy”, „mąka z lokalnych młynów” ani dodawać własnych deklaracji.
- **Rodzaj strony:** wizytówka + aktualności („wypiek dnia” na każdy dzień tygodnia, oferta sezonowa).
- **Cele:** zbieranie zamówień (torty, pieczywo na imprezy, B2B) i budowa wizerunku (historia rodzinna, tradycja).
- **Główna akcja:** dwa równorzędne przyciski: „Zamów” (formularz zamówienia) i „Napisz do nas”.
- **Odbiorcy:** mieszkańcy, rodziny, osoby starsze oraz osoby pracujące w pobliżu (szybki zakup, śniadanie). Urządzenia: mniej więcej po równo desktop i mobile.
- **Wygląd:** ciepły, domowy, kremowy, drewno. Kolory: beże, brązy, złoto, kolor skórki chleba. Motyw jasny z automatycznym trybem ciemnym. Brak logo, jest tylko nazwa.
- **Ton:** ciepły, luźny, na „Ty”. Tylko język polski.
- **Wymagane funkcje:** formularz kontaktowy, formularz zamówień, mapa, galeria, FAQ, cennik z pełną listą alergenów przy każdym produkcie, godziny otwarcia.
- **Strony wzorcowe od użytkownika:** brak („nie mam przykładów”) ani stron, których należy unikać. Dlatego analizuję wyłącznie strony wybrane przez managera (grupa lokalna + grupa rzemieślnicza).

## Uwagi metodologiczne
- Analiza opiera się na materiałach pobranych przez managera (zrzuty desktop 1440×900, całe strony do 5000 px, mobile 390×844 oraz surowy HTML). Sam nie otwierałem tych stron (WebFetch zablokowany w środowisku).
- **R4 (bardzodobrychleb.pl) nie został przeanalizowany**: wszystkie trzy zrzuty i HTML pokazują tylko ekran weryfikacji anty-botowej („Please wait while your request is being verified…”, tytuł HTML „One moment, please...”). Nie ma na nich żadnej treści strony.
- **R1 (calawmace.pl)**: poniżej pierwszego ekranu zrzut całej strony jest prawie pusty (szare i jasnofioletowe prostokąty). Treść pojawia się z animacją przy przewijaniu (atrybuty `data-aos` w HTML), więc zrzut jej nie złapał. Sekcje R1 poniżej hero opisuję na podstawie HTML, a kolorów tych sekcji nie oceniam.
- **R2 (sztukamaki.pl)**: podobnie, sekcja „Moje chleby” na zrzucie pokazuje tylko szare napisy (Klasyk, Żytni, Chałka, Rodzinny) bez zdjęć. Prawdopodobnie zdjęcia się nie doczytały.
- **R3 (breakingbread.dodla.pl)**: to strona systemu zamówień (dodla.pl), a nie klasyczna wizytówka. Lista produktów na zrzucie się nie załadowała (widać kręcący się wskaźnik ładowania).
- **L1 (brodziknaturalnie.pl)**: baner cookies zasłania lewy dolny róg pierwszego ekranu na desktopie i dolną połowę ekranu na mobile. Środkowa część strony (ok. 2500–3000 px) jest pusta, a zrzut kończy się na nagłówku „Opinie naszych klientów” (limit 5000 px), więc stopki nie widziałem.
- **L2 (putka.pl)**: zrzut kończy się na sekcji historii (limit 5000 px), stopki nie widziałem.
- **L3 (braciakowalscy.pl)**: na zrzucie całej strony od ok. 3200 px jest pusto (galeria i logotypy doczytują się przy przewijaniu). Dalsze sekcje (galeria, „Sprzedajemy”, kontakt w stopce) opisuję na podstawie HTML.
- W sumie **faktycznie przeanalizowałem 7 z 8 stron** (N = 7). Wszystkie liczby „x/7” poniżej dotyczą tylko tych 7 stron. Jeśli coś wynika tylko z HTML, zaznaczam to.

---

## Przeanalizowane strony

### GRUPA LOKALNA (okolice Serocka / Legionowa / Zalewu Zegrzyńskiego)

### L1. Brodzik Naturalnie (Legionowo): https://www.brodziknaturalnie.pl/
- **Układ sekcji (od góry):** nagłówek z logo na środku i menu po obu stronach (O nas, Artykuły | Produkty, Kontakt) oraz okrągła ikonka koszyka „Sklep” → slider hero (bochenek na tle jutowego worka, duży napis w wersalikach, pod nim podtytuł, 3 kropki slidera) → białe pudełko z nagłówkiem, krótkim wstępem o piekarni i 4 kartami z ikonami (stare odmiany zbóż, własny zakwas, linia keto), każda z obrysowanym przyciskiem „Sprawdź…” → ramka „Dlaczego używamy…” z dłuższym tekstem i wyróżnioną ramką przerywaną → pusty obszar (treść się nie doczytała) z niewielkim blokiem „Prawdziwy chleb” i linkiem „Sprawdź nasze produkty” → pas z teksturą juty i hasłem → „Z pradawnych odmian zbóż”: 4 kafle ze zdjęciami kłosów i podpisami → „Nasze produkty”: szachownica 2×2 (karmelowe kafle z tekstem na przemian ze zdjęciami) → „Opinie naszych klientów” (tu kończy się zrzut).
- **Kolory / typografia:** białe tło, jasnoszare tło z delikatną teksturą, brązowe i karmelowe akcenty (kafle w kolorze skórki chleba), złoto-pomarańczowe przyciski, czerwona linia oddzielająca sekcje. Nagłówki to szeryfowy krój o miękkim, „książkowym” charakterze, brązowy na białym, w hero biały w wersalikach. Logo pisane odręcznie z kłosem.
- **Ton:** bezpośredni, ale mocno „prozdrowotny”, z deklaracjami o składnikach i zdrowiu. Pisze w 1. os. l. mn. („pieczemy”, „używamy”).
- **CTA:** „Sklep” (ikona w nagłówku), obrysowane przyciski „Sprawdź…” na kartach, tekstowe linki „Sprawdź nasze produkty”. W hero brak przycisku.
- **Mocne strony:** paleta najbliższa temu, czego chce nasz użytkownik (brąz, karmel, złoto, juta). Kafle z kłosami dobrze pokazują składniki. Szachownica zdjęcie/tekst przy produktach jest czytelna.
- **Słabe strony:** baner cookies zakrywa pół ekranu na mobile. W hero brak CTA. Na desktopie widać duże puste obszary (treść się nie doczytuje albo znika). Długie akapity pisane dużą czcionką w wąskiej kolumnie. Mnóstwo deklaracji zdrowotnych i słowo „ekologiczne” (nam tego nie wolno). Na pierwszym ekranie nie ma godzin, adresu ani telefonu.

### L2. Putka (sieć, m.in. okolice Warszawy): https://www.putka.pl/
- **Układ sekcji:** nagłówek z okrągłym logo na środku, które „wystaje” poniżej paska. Po lewej menu (Strona główna, Produkty▾, O nas▾, Nasze piekarnie), po prawej (Kariera, Księga Inspiracji) i bordowy przycisk-pigułka „Sklep online” → hero na brzoskwiniowym tle: po lewej duży nagłówek sezonowy, opis i przycisk „Dowiedz się więcej”, po prawej zdjęcie kanapki z mocno zaokrąglonymi rogami → **4 białe kafle szybkich akcji z ikonami** (Zamów online, Skonfiguruj tort, Znajdź swoją piekarnię, Odkryj produkty) → dwie kolumny z sezonowymi promocjami (kawa, drożdżówka), każda ze zdjęciem, tytułem, opisem i przyciskiem → „Dbamy o każdego”: 2 wyróżniki (częste dostawy, niemrożone ciasto) + zdjęcie bułek w kształcie „pigułki” → „Pamiętamy o Waszych potrzebach”: 3 karty (bezglutenowe, niski IG, bez cukru) + „Zobacz wszystko” → „Jesteśmy dla Was…”: 2 kolumny (punkty stacjonarne z przyciskiem „Znajdź swoją piekarnię” oraz zamówienia online z przyciskiem „Przejdź do sklepu”) → „Jesteśmy dla każdego”: 4 zdjęcia ludzi i 4 persony (Tradycjonaliści, Zabiegani, Dbający o zdrowie, Odkrywcy) → „Od tego wszystko się zaczęło”: historia od 1918 r. (tu kończy się zrzut).
- **Kolory / typografia:** kremowo-brzoskwiniowe i jasnobeżowe tła sekcji na przemian z białymi, bordowy (wiśniowy) kolor przycisków i logo, ciemnografitowy tekst. Nagłówki to bardzo gruby, szeroki bezszeryfowy krój. Tekst w cienkim, czytelnym bezszeryfowym kroju. Wszędzie duże zaokrąglenia (zdjęcia, karty, przyciski-pigułki).
- **Ton:** ciepły, marketingowy, zwraca się do klienta na „Ty” i „Wy” („Nie przegap!”, „Przeczytaj więcej!”). Pojawiają się hasła sezonowe.
- **CTA:** „Sklep online” w nagłówku, kafle szybkich akcji, bordowe pigułki w każdej sekcji. Na mobile przycisk ma pełną szerokość ekranu.
- **Mocne strony:** **kafle szybkich akcji tuż pod hero** (od razu wiadomo, co można zrobić). Sezonowość na pierwszym ekranie. Osobna karta dla produktów bezglutenowych. Konsekwentna, ciepła paleta. Mobile jest czytelny: nagłówek, zdjęcie, tekst i przycisk na całą szerokość.
- **Słabe strony:** to sieć, więc skala i ton są „korporacyjne”, a sekcja person jest raczej ozdobna. Strona jest bardzo długa. Zdjęcia oznaczone jako retusz AI obniżają autentyczność. Opis w hero to długi, wyśrodkowany akapit.

### L3. Bracia Kowalscy (Wólka Radzymińska, gm. Nieporęt, nad Zalewem Zegrzyńskim): https://braciakowalscy.pl/
- **Układ sekcji:** biały nagłówek: logo po lewej, menu z kotwicami na środku (start, o nas, oferta, galeria, na sprzedaż, kontakt, ikona Facebooka), po prawej **duża czerwona ikona telefonu, adres i numer dużą czcionką** → hero na całą szerokość (zbliżenie drożdżówek), na środku białe logo, 2 zdania o historii od 1985 r., „zobacz więcej” ze strzałką w dół, w prawym dolnym rogu czerwony kwadrat z odręcznym hasłem → czerwony pas „FIRMA RODZINNA” → układ zygzakowy: tekst „1985 r.” + zdjęcie chlebów, zdjęcie piekarza przy maszynie + tekst „Dziś” z przyciskiem „czytaj więcej” → czerwona sekcja „Co oferujemy?”: 3 ikony (Chleb, Bułki, Słodkie) z krótkimi opisami + „pobierz katalog” (PDF) → (wg HTML) pas zdjęciowy z hasłem, „Znajdziesz nas w:” (logotypy sklepów, na zrzucie puste), galeria 12 zdjęć, „Sprzedajemy” (maszyny), stopka „Zapraszamy do współpracy” (B2B) z adresem, przyciskami „wyznacz trasę” i „mapa google” oraz formularzem kontaktowym rozwijanym jak akordeon.
- **Kolory / typografia:** intensywna czerwień i biel, ciepłe zdjęcia (złote drożdżówki). Nagłówki w cienkim bezszeryfowym kroju, duże. Tekst też bezszeryfowy. Akcent to odręczne hasło w logo.
- **Ton:** rodzinny, anegdotyczny (ojciec założyciel, rodzinna maksyma), pisany w 1. os. l. mn.
- **CTA:** telefon w nagłówku (na mobile zielona ikona słuchawki), „zobacz więcej”, „czytaj więcej”, „pobierz katalog”, „wyznacz trasę”.
- **Mocne strony:** **telefon i adres zawsze widoczne w nagłówku** (najlepiej ze wszystkich stron dla osób starszych). Historia rodzinna opowiedziana osią czasu „wtedy / dziś” (bardzo podobna fabuła do naszej: założyciel w latach 80., kolejne pokolenie). Bliska lokalizacja nad Zalewem Zegrzyńskim.
- **Słabe strony:** oferta tylko w PDF, bez cen i alergenów. Strona wygląda na przestarzałą. Czerwień kojarzy się bardziej z marketem niż z rzemiosłem. Na mobile ogromny czerwony blok z hasłem zajmuje pół ekranu. Brak godzin otwarcia na stronie głównej (w HTML ich nie znalazłem). Duże puste obszary podczas doczytywania.

### L4. Piekarnia Grzybki (Warszawa, wiele sklepów): https://piekarniagrzybki.pl/
- **Układ sekcji:** nagłówek z owalnym logo-pieczątką na środku (napis z rokiem założenia 1927). Menu po lewej (O nas, Produkty, Aktualności, Blog) i po prawej (Nasze sklepy, Kariera, Kontakt) oraz pomarańczowy przycisk „pędzlem” (Akademia Piekarza) → niski slider (napoje kawowe na beżowym tle, strzałki, falista krawędź ze strzałką w dół) → „Dowiedz się czegoś O NAS”: tekst historii po lewej i **kolaż sepiowych zdjęć-polaroidów z archiwum** po prawej, na tle białej cegły, przycisk „Więcej” → „Co nas wyróżnia”: 4 okrągłe zdjęcia z podpisami → „Zapoznaj się z naszymi PRODUKTAMI”: 5 białych kart (wyroby piekarskie, cukiernicze, przekąski, gastronomia, pizza) na ciemnym zdjęciu stołu → „Aktualności czyli co u nas słychać”: 2 wpisy z datą na plakietce → pomarańczowy pas z ikonami Facebooka i Instagrama → „Skontaktuj się z nami”: formularz (imię, nazwisko, telefon, e-mail, temat, wiadomość) + dane kontaktowe → „Znajdź nas”: pełnoszeroka mapa z wieloma pinezkami → stopka.
- **Kolory / typografia:** pomarańcz (logo, nagłówki, akcenty) + czerń + biel, szare tło z cegłą, sepia archiwalnych zdjęć. Nagłówki bezszeryfowe, dwukolorowe (część pomarańczowa, część czarna). Logo szeryfowe w stylu retro.
- **Ton:** informacyjny, trochę oficjalny, mówi w 1. os. l. mn., w aktualnościach zwraca się bezpośrednio do klientów.
- **CTA:** małe obrysowane przyciski „Więcej”/„WIĘCEJ”, „Wyślij” w formularzu, pomarańczowy przycisk w nagłówku. Nie ma wyraźnego przycisku zamówienia.
- **Mocne strony:** **archiwalne zdjęcia jako dowód tradycji** (dobry pomysł dla historii od 1987 r., u nas trzeba je zastąpić zdjęciami zastępczymi). Pełny komplet na jednej stronie: o nas, produkty, aktualności, formularz, mapa. Aktualności z datą.
- **Słabe strony:** hero pokazuje napoje kawowe, a nie pieczywo, więc nie wiadomo od razu, że to piekarnia. Na mobile pierwszy ekran to długi tekst historii. Opisy w kartach są wyjustowane i mają dziury między słowami. Plakietka reCAPTCHA zasłania treść. Małe przyciski „Więcej”.

### GRUPA RZEMIEŚLNICZA (inspiracja ogólnopolska)

### R1. Cała w Mące (Warszawa): https://calawmace.pl/
- **Układ sekcji:** cienki pasek nagłówka z liniami u góry i u dołu: logo (gałązka + nazwa + „PIEKARNIA”) po lewej, menu (Strona Główna, Sklep, O piekarni, Chleby, Słodkości, Praca, Kontakt), ikony Instagrama i Facebooka po prawej → **hero typu „mozaika”**: duże zdjęcie świątecznego stołu (2/3 szerokości) z cienkim napisem w wersalikach i linkiem „oferta świąteczna”, obok beżowe pudełko z krótką historią założycielki i przyciskiem „Zobacz więcej” oraz zdjęcie słodkich wypieków. Dalej (wg HTML, bo na zrzucie pusto): „Nasze chleby” (tekst o zakwasie i powolnym dojrzewaniu + link „Poznaj nasze produkty” + zdjęcie), „Zapisz się na newsletter” (na tle zdjęcia zespołu), „Nasi klienci” (przewijane logotypy partnerów B2B), „Szybki kontakt” (formularz współpracy: imię, e-mail, wiadomość), „Lokalizacje” (4 punkty z adresem, godzinami i linkiem „Poprowadź mnie” + mapa), stopka.
- **Kolory / typografia (tylko z pierwszego ekranu):** dużo bieli, jeden ciepły beż (kolor mąki/skórki) na pudełku tekstowym, czarny tekst. Typografia to cienki, elegancki krój bezszeryfowy, nagłówek hero cienki w wersalikach. Zdjęcia w stylu magazynowym (kwiaty, naturalne światło).
- **Ton:** osobisty, opowieść założycielki, spokojny.
- **CTA:** subtelne: podkreślone linki tekstowe („oferta świąteczna”, „Poznaj nasze produkty”), mały obrysowany „Zobacz więcej”, „Poprowadź mnie” przy lokalizacji.
- **Mocne strony:** najbardziej „rzemieślnicza” estetyka: minimalizm i piękne zdjęcia. Hero-mozaika pokazuje od razu ofertę sezonową i historię. Przy każdej lokalizacji godziny + link do nawigacji. Logotypy partnerów budują zaufanie B2B.
- **Słabe strony:** CTA są słabo widoczne. Treść pojawia się tylko z animacją, więc przy wolnym ładowaniu widać puste miejsca (zrzut to potwierdza). Hero pokazuje nieaktualną ofertę (Wielkanoc 2026 we wrześniu). Na mobile nad logo jest pusty pas. Brak cen na stronie głównej.

### R2. Sztuka Mąki (Grodzisk Mazowiecki, mikropiekarnia): https://www.sztukamaki.pl/
- **Układ sekcji:** nagłówek: małe okrągłe logo, menu z podkreślonymi linkami (Strona główna, O mnie, U mnie znajdziesz, Kontakt, Zamówienia), ikony FB/IG → hero: pytanie-nagłówek „Czym mogę Cię ugościć?”, pod nim duże okrągłe logo i jeden ciemnoszary przycisk „Zamów sobie chleb” → „Mąka. Woda. Sól.”: krótki tekst o zakwasie i długiej fermentacji na szarym pasie + czarno-białe zdjęcie rąk formujących ciasto → „Nazywam się…”: osobista historia piekarza, dwie kolumny → pas 5 krótkich wyróżników (naturalne składniki, długa fermentacja i własny zakwas, małe partie, klasyczne i autorskie receptury, świeże każdego dnia) → „Moje chleby”: 4 nazwy chlebów (zdjęcia się nie doczytały) → „Kontakt”: adres, telefon, e-mail z ikonami.
- **Kolory / typografia:** czerń, biel, szarość, zdjęcia czarno-białe. Nagłówki w grubym geometrycznym kroju bezszeryfowym, tekst w cienkim bezszeryfowym. Brak ciepłych kolorów.
- **Ton:** **bardzo osobisty, na „Ty”**, w 1. os. l. poj. („Czym mogę Cię ugościć?”, „Zamów sobie chleb”, „Daj się skusić!”). Najbliższy tonowi, którego chce nasz użytkownik.
- **CTA:** jeden główny przycisk „Zamów sobie chleb” w hero, „Zamówienia” w menu, pogrubione linki w tekście.
- **Mocne strony:** prosty przekaz o procesie („Mąka. Woda. Sól.” + długa fermentacja), który dobrze pasuje do naszego „18 h fermentacji, bez polepszaczy”. Jedno wyraźne CTA w hero. Pas krótkich wyróżników. Ciepły ton na „Ty”.
- **Słabe strony:** hero bez zdjęcia chleba, tylko logo, więc pierwszy ekran nie budzi apetytu. Monochromia jest chłodna. Duże puste przestrzenie. Tekst wyjustowany w wąskich kolumnach. W sekcji „Moje chleby” nie ma cen.

### R3. Breaking Bread (system zamówień dodla.pl): https://breakingbread.dodla.pl/
- **Układ sekcji:** zdjęcie hero (bochenki z ziarnami) z logo w lewym górnym rogu, strzałka slidera → czarny pas „…zamów i odbierz” z instrukcją zamawiania (dni działania, wybór daty odbioru, koszyk, potwierdzenie mailem) i okrągłą ikoną torby → „Zaloguj się” → panel „Twoje zamówienia”: krok 1 „Wybierz datę” (pole daty), krok 2 „Wybierz produkty”, pusty koszyk. Lista produktów po lewej się nie załadowała (widać tylko wskaźnik ładowania) → stopka „System zamówień: dodla.pl”, Regulamin, Polityka prywatności.
- **Kolory / typografia:** czerń + biel + ciepłe, brązowo-złote zdjęcie. Typografia bezszeryfowa, zaokrąglona, czytelna.
- **Ton:** praktyczny i instrukcyjny, na „Ty/Was”, z żartem o glutenie.
- **CTA:** wybór daty, dodawanie do koszyka, „Zaloguj się”.
- **Mocne strony:** **zamówienie ułożone w kroki (1. data odbioru → 2. produkty)**, co dobrze pasuje do naszej reguły „dzień wcześniej do 14:00 / torty 3 dni wcześniej”. Dni działania podane od razu.
- **Słabe strony:** to narzędzie, a nie wizytówka: brak historii, galerii i opisu piekarni. Długi blok instrukcji w jednym akapicie. Nie widać produktów, dopóki nie załaduje się JS.

### R4. Bardzo Dobry Chleb: https://bardzodobrychleb.pl/
- **Nie przeanalizowano.** Zrzuty desktop, full i mobile pokazują wyłącznie zieloną ikonę i komunikat weryfikacji „Please wait while your request is being verified…”. HTML to tylko strona przejściowa (tytuł „One moment, please...”, skrypt przeładowania po 5 s). Nie ma tu żadnej treści piekarni, więc tej strony nie liczę w statystykach.

---

## Wspólne wzorce w branży
1. **Hero ze zbliżeniem pieczywa lub produktu** (skórka, ziarna, drożdżówki, juta). Na pierwszym ekranie dominuje zdjęcie, a tekstu jest mało.
2. **Historia i rodzina jako główny argument**: rok założenia (1918, 1927, 1985, 2016), założyciel z imienia, kolejne pokolenia, zdjęcia archiwalne lub z pracy przy cieście. Zwykle to druga sekcja strony.
3. **Oferta pokazana kategoriami, bez cen na stronie głównej** (chleb / bułki / słodkie / przekąski). Ceny i alergeny są w sklepie, w PDF albo nigdzie. **Na żadnej z 7 stron nie widziałem cennika z alergenami przy produktach na stronie głównej.**
4. **Wyróżniki w formie krótkich haseł z ikonami lub zdjęciami** (zakwas, długa fermentacja, bez polepszaczy, świeże codziennie).
5. **Sezonowość i aktualności** (Wielkanoc, jesień, majówka, promocje). Często w samym hero.
6. **Zamawianie** to zwykle osobny sklep online lub system zewnętrzny, a w nagłówku stoi przycisk „Sklep/Zamów”.
7. **Lokalizacja z linkiem do nawigacji lub mapą** na dole strony.
8. **Logo na środku nagłówka** z menu rozdzielonym na dwie strony (L1, L2, L4).
9. **Dominujące palety:** ciepłe (brąz, karmel, beż, brzoskwinia, pomarańcz) albo minimalistyczne (biel/czerń + jeden beż). Czerwień w L3 to wyjątek.
10. **Tego nie widziałem nigdzie:** FAQ, trybu ciemnego, „wypieku dnia” dla każdego dnia tygodnia, informacji o terminach zamówień obok formularza (poza R3), statusu „otwarte teraz”.

## Rekomendacje dla designera

### Sekcje obecne u większości konkurencji (N = 7 faktycznie przeanalizowanych stron: L1, L2, L3, L4, R1, R2, R3)
| Sekcja / element | Liczba | Które strony |
|---|---|---|
| Hero z dużym zdjęciem pieczywa lub produktu | **6/7** | L1, L2, L3, L4, R1, R3 (R2 ma w hero tylko logo) |
| O nas / historia na stronie głównej | **6/7** | L1, L2, L3, L4, R1, R2 (brak w R3) |
| Oferta w kategoriach (bez cen) | **6/7** | L1, L2, L3, L4, R1 (wg HTML), R2 (w R3 lista się nie załadowała) |
| Wyraźna ścieżka zamówienia (sklep / „Zamów” / system zamówień) | **5/7** | L1, L2, R1, R2, R3 (brak w L3, L4) |
| Aktualności / blog / oferta sezonowa | **4/7** | L1 (Artykuły w menu), L2 (sezonowe hero), L4 (Aktualności + Blog), R1 (sezonowe hero) |
| Wyróżniki z ikonami / krótkie hasła | **4/7** | L1, L2, L4, R2 |
| Kontakt (dane i/lub formularz) na stronie głównej | **4/7 potwierdzone** | L3 (HTML), L4, R1 (HTML), R2. W L1 i L2 zrzut nie sięga stopki |
| Mapa / lokalizacje / „wyznacz trasę” | **4/7** | L2 (Znajdź piekarnię), L3 (HTML), L4, R1 (HTML) |
| Linki do social media | **4/7 potwierdzone** | L3, L4, R1, R2 |
| Formularz kontaktowy | **3/7** | L3 (HTML), L4, R1 (HTML) |
| Kariera / praca w menu | 3/7 | L2, L4, R1 (nam niepotrzebne) |
| Godziny otwarcia na stronie głównej | **2/7** | R1 (HTML, przy lokalizacjach), R3 (dni działania) |
| Oferta dla firm / B2B | 2/7 | L3, R1 |
| Telefon widoczny w nagłówku | 1/7 | L3 |
| Opinie klientów | 1/7 | L1 (tylko nagłówek na zrzucie) |
| Galeria | 1/7 | L3 (HTML) |
| Informacja o produktach bezglutenowych | 1/7 | L2 |
| Newsletter | 1/7 | R1 |
| Ceny na stronie głównej | **0/7** | brak |
| Alergeny przy produktach | **0/7** | brak |
| FAQ | **0/7** | brak |
| Tryb ciemny | **0/7** zaobserwowane | na zrzutach nie widać, strony wyglądają na jednomotywowe |

**Wniosek:** standard branżowy to hero ze zdjęciem, historia i oferta w kategoriach (6/7), potem zamawianie (5/7). Kontakt, mapa, aktualności i wyróżniki pojawiają się mniej więcej na co drugiej stronie. Cennik, alergeny, FAQ i godziny otwarcia to luki u konkurencji, a nasz intake wymaga ich wszystkich.

### Kierunek wizualny
- **Paleta:** ciepła, „piekarniana”, podobna do L1 i R1, ale spokojniejsza: kremowe tło (kolor mąki/miąższu), brąz skórki chleba jako kolor tekstu i nagłówków, karmel lub złoto na akcenty i przyciski. Bez czerwieni (L3) i bez intensywnego pomarańczu (L4). Nasze przyciski muszą mieć lepszy kontrast niż jasnozłote przyciski L1.
- **Tryb ciemny:** żadna analizowana strona go nie ma. Proponuję „piekarnię nocą”: głęboki brąz lub czekoladowe tło, kremowy tekst, złote akcenty (nie czysta czerń jak R3).
- **Typografia:** szeryfowe, ciepłe nagłówki (domowy charakter, podobnie jak L1) + czytelny bezszeryfowy tekst o dużym rozmiarze (osoby starsze). Nie dawać cienkich krojów jak R1, bo są za słabe dla starszych czytelników.
- **Kształty:** umiarkowanie zaokrąglone karty i przyciski (L2 pokazuje, że działa to ciepło i „miękko”). Można dodać delikatną teksturę (len, juta, papier), ale oszczędnie. W L1 i L4 tekstury trochę przytłaczają.
- **Zdjęcia:** zbliżenia skórki i przekroju chleba żytniego (hero), ręce przy cieście (jak R2, ale w ciepłej kolorystyce, nie czarno-białe), stylizacja „rodzinnego archiwum” dla historii 1987 → dziś (inspiracja L4). Wszystko jako zdjęcia zastępcze, bo użytkownik nie ma własnych.
- **Nagłówek:** nazwa „Piekarynka nad Zegrzem” jako logotyp tekstowy (brak pliku logo). Telefon klikalny i widoczny zawsze (jak L3), a na mobile np. jako przyklejony dolny pasek z „Zadzwoń / Zamów / Napisz”.
- **Ton:** ciepły, na „Ty”, krótkie zdania. Najbliższy wzorzec to R2 („Czym mogę Cię ugościć?”, „Zamów sobie chleb”), ale w liczbie mnogiej, bo piekarnię prowadzi rodzina.
- **Czego unikać (zaobserwowane błędy):** banerów cookies zasłaniających pół ekranu (L1), hero bez produktu (L4 z kawą, R2 z samym logo), treści ładowanych animacją, która zostawia puste miejsca (R1, L1, L3), wyjustowanego tekstu w wąskich kolumnach (L4, R2), nieaktualnej oferty sezonowej w hero (R1), oferty tylko w PDF (L3), małych obrysowanych przycisków „Więcej” (L4). Nie powielać też deklaracji zdrowotnych i słowa „ekologiczne” obecnych w L1.

### Pomysły na wyróżnienie się
1. **„Wypiek dnia” na pierwszym ekranie.** Karta, która sama pokazuje dzisiejszy wypiek wg dnia tygodnia (pon. orkiszowy … niedz. ciasto drożdżowe z kruszonką) z ceną i alergenami, a obok podgląd całego tygodnia. Nikt z konkurencji tego nie ma, a to gotowy powód do codziennych odwiedzin.
2. **Status „Otwarte teraz / Zamykamy o 19:00” + „druga dostawa ok. 12:00”** przy godzinach. Przyda się osobom, które kupują po drodze do pracy. Godziny ma tylko 2/7 stron.
3. **Pełny cennik z alergenami w formie czytelnych plakietek** (gluten, jaja, mleko, orzechy, sezam, gorczyca) + filtr „bez glutenu / bez laktozy” + stały dopisek o śladowych ilościach orzechów i sezamu. U konkurencji 0/7, a dla rodzin i alergików to realna wartość.
4. **Dwa równorzędne CTA „Zamów” i „Napisz do nas”** w hero i na mobile w przyklejonym pasku, plus kafle szybkich akcji pod hero (wzorzec z L2: Zamów, Tort na zamówienie, Dojazd, Cennik).
5. **Formularz zamówienia z terminami wbudowanymi w UI** (wzorzec krokowy z R3): kalendarz blokuje daty niespełniające zasad „dzień wcześniej do 14:00” i „torty min. 3 dni”, a wyboru „odbiór / dostawa” towarzyszy informacja „dostawa gratis od 80 zł, poniżej 10 zł, promień 10 km”.
6. **Oś czasu „1987 → dziś”** (trzy pokolenia: Józef Kowalczyk → syn → wnuczka) w stylu rodzinnego albumu (inspiracja L3 i L4), połączona z wizualizacją „18 godzin fermentacji zakwasu” (np. prosta oś godzin od zaczynu do pieca). Ta druga rzecz to konkret, którego nie pokazuje żadna strona.
7. **FAQ (0/7 u konkurencji):** alergeny i strefa bezglutenowa, terminy zamówień, dostawa, B2B, torty.
8. **Mały blok B2B** („Obsługujemy kawiarnie, restauracje i sklepy, codzienne poranne dostawy”) z CTA „Napisz do nas”. Mają go tylko L3 i R1.
9. **Aktualności sezonowe** (tłusty czwartek, 11 listopada, pierniki, mazurki) jako krótkie karty z datą (wzorzec L4), ale z zasadą, że nieaktualny baner znika z hero (błąd R1).

## Źródła (lista linków)
Analiza opiera się na zrzutach ekranu (desktop 1440×900, cała strona do 5000 px, mobile 390×844) oraz surowym HTML pobranych przez managera **26.09.2026** i zapisanych w `sites/test-piekarnia/docs/research-raw/`. Sam nie odwiedzałem tych stron w przeglądarce ani przez WebFetch.

- L1: https://www.brodziknaturalnie.pl/ (baner cookies zasłania część treści, zrzut obcięty na 5000 px)
- L2: https://www.putka.pl/ (zrzut obcięty na 5000 px)
- L3: https://braciakowalscy.pl/ (dolne sekcje odczytane z HTML)
- L4: https://piekarniagrzybki.pl/
- R1: https://calawmace.pl/ (sekcje poniżej hero odczytane z HTML, bo zrzut jest pusty)
- R2: https://www.sztukamaki.pl/ (zdjęcia sekcji „Moje chleby” się nie załadowały)
- R3: https://breakingbread.dodla.pl/ (lista produktów się nie załadowała)
- R4: https://bardzodobrychleb.pl/ (**nieprzeanalizowana**, widoczny tylko ekran weryfikacji anty-botowej)
