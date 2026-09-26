# Pipeline tworzenia strony

Agenci są zdefiniowani w `.claude/agents/`. Każdy ma osobny kontekst i nie może wywołać innego agenta. Pracę przekazują sobie przez pliki w `sites/<nazwa>/docs/`, a agentów uruchamia manager (główny agent). Manager przekazuje wiadomości między agentami **słowo w słowo** i nie zmienia ich treści.

```
             informator ── pytania do użytkownika ──► docs/intake.md
                    │                                   │
          ┌─────────┴──────────┐                        │
          ▼                    ▼                        │
     interpreter           researcher                   │
     docs/brief.md         docs/research.md             │
          │    ▲               │                        │
          ▼    │               ▼                        │
   [konflikt brief ↔ research? → pytanie do użytkownika]
          │    │
          ▼    │
      designer → coder → writer ◄─┘  (writer ⇄ interpreter, maks. 3 wymiany)
      design.md  kod +     teksty
      prototype  znaczniki
                               │
                               ▼
                           reviewer → docs/review-N.md
                (kod → coder, teksty → writer; maks. 3 rundy)
                               │
                               ▼
                    wynik dla użytkownika
```

## Kroki

0. **informator**
   - Przebieg 1: pytania do użytkownika (stały zestaw A–F plus pytania branżowe, z propozycjami odpowiedzi).
   - Manager zadaje pytania użytkownikowi.
   - Przebieg 2: `docs/intake.md` ze statusem READY (albo pytania uzupełniające).
1. **Równolegle**, bo gałęzie są od siebie niezależne:
   - **interpreter** czyta intake i tworzy `docs/brief.md`: drzewo sekcji i podsekcji z priorytetami MUST / SHOULD / NICE. Pyta użytkownika **tylko o luki**, których nie pokrył informator (status NEEDS_INPUT → pytania → READY).
   - **researcher** czyta intake i tworzy `docs/research.md`: strony podobnych firm, w tym strony wskazane przez użytkownika jako inspiracja.
2. **Kontrola konfliktu (manager).** Jeśli researcher wskazuje sekcję obecną u większości konkurencji, a w briefie jej nie ma, manager **pyta użytkownika**, czy ją dodać. Odpowiedź trafia do briefu przez interpretera.
3. **designer** czyta intake, brief i research. Tworzy `docs/design.md` (w tym mapę tekstów: id → typ → maks. długość) oraz `docs/prototype.html`. Sekcje MUST i SHOULD są obowiązkowe. Designer nie pisze finalnych tekstów.
4. **coder** czyta design i buduje kod strony w `sites/<nazwa>/`. W miejscu każdego tekstu wstawia znacznik `[[TEXT:id]]` z atrybutem `data-text="id"`. Jest **jedynym autorem kodu** i nie pisze tekstów.
5. **writer** zamienia znaczniki na teksty w `index.html` na podstawie intake i brief. Jest **jedynym autorem tekstów**.
   - Gdy brakuje faktu, pyta interpretera: manager przekazuje pytanie 1:1 i wznawia interpretera z jego pamięcią. Wymiana jest zapisywana w `docs/writer-interpreter.md`.
   - Maksymalnie **3 wymiany na jedną kwestię**. Potem, albo gdy interpreter nie wie, manager pyta użytkownika.
6. **reviewer** czyta kod, teksty i wszystkie dokumenty (tylko odczyt). Manager zapisuje wynik jako `docs/review-N.md`. Każdy punkt ma adresata: `coder` albo `writer`.
7. **Poprawki** (jeśli CHANGES_REQUESTED):
   - coder poprawia punkty dotyczące kodu, a writer punkty dotyczące tekstów,
   - **coder ⇄ reviewer mogą dyskutować samodzielnie.** Coder może odpowiedzieć na punkt „nie zgadzam się” z argumentem, a reviewer w następnej rundzie punkt wycofuje albo podtrzymuje z kontrargumentem. Raporty codera manager zapisuje jako `docs/coder-report-N.md`,
   - writer nie decyduje sam przy sporze z reviewerem. Manager pyta użytkownika,
   - kolejna runda reviewera. **Maksymalnie 3 rundy.**
8. **Wynik.** Po APPROVED albo po 3 rundach manager pokazuje użytkownikowi stronę i otwarte punkty. **Spór coder ⇄ reviewer nierozstrzygnięty po 3 rundach** manager przedstawia użytkownikowi razem ze stanowiskami obu stron, a decyzję podejmuje użytkownik.

## Kto jest autorem czego

| Plik | Autor | Czytają |
|---|---|---|
| `docs/intake.md` | informator | interpreter, researcher, designer, writer, reviewer |
| `docs/brief.md` | interpreter | designer, writer, reviewer |
| `docs/research.md` | researcher | designer |
| `docs/design.md`, `docs/prototype.html` | designer | coder, writer, reviewer |
| kod: struktura HTML, `css/`, `js/`, `assets/` | **coder** | writer, reviewer |
| teksty w `index.html` | **writer** | reviewer |
| `docs/review-N.md`, `docs/coder-report-N.md`, `docs/writer-interpreter.md` | manager (zapisuje wyniki agentów bez zmian) | coder, writer, reviewer |

## Zasady wspólne
- Każda niejasność, konflikt albo kwestia sporna trafia do użytkownika. Wyjątek: dyskusja coder ⇄ reviewer, zgodnie z krokiem 7.
- Agenci nie zmyślają faktów. Czego nie ma w intake, o to trzeba zapytać.
- Manager pyta użytkownika o zgodę przed uruchomieniem pipeline'u.
