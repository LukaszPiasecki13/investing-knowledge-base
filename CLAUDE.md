# investing-knowledge-base

Polskojęzyczna baza wiedzy i poradnik inwestycyjny (analiza fundamentalna spółek z GPW i USA). Autor to inwestor indywidualny z ~3-letnim doświadczeniem; dokumenty są jednocześnie notatkami do nauki i materiałem do decyzji inwestycyjnych.

## Struktura

- `docs/investing.md` — główny przewodnik (Części I–IV: podstawy, sprawozdania, wskaźniki, analiza Value/Growth). Obrazki w `docs/image*.png`.
- `analyses/<TICKER>/` — analizy konkretnych spółek (tworzone przez `/analyze`).
- `journal/` — tezy inwestycyjne i post-mortemy (tworzone przez `/thesis` i `/post-mortem`).
- `scripts/` — skrypty pomocnicze (walidacja Markdown, wykresy).
- `.claude/` — agenci, skille, hooki, uprawnienia. Opis: `.claude/README.md`.
- `.github/agents/` — oryginalny agent w formacie Copilota; źródłem prawdy jest teraz `.claude/agents/`.

## Język i styl

- Pisz po polsku. Przy pierwszym użyciu terminu podaj angielski odpowiednik w nawiasie, np. przepływy operacyjne (Cash Flow from Operations, CFO). Skróty jak w istniejących notatkach: C/Z = P/E, C/WK = P/BV.
- Ton profesjonalny, bez infantylizowania; zakładaj znajomość podstaw.
- Podawaj realne liczby (progi, zakresy historyczne, benchmarki branżowe) i zaznaczaj, gdy próg zależy od branży lub cyklu.
- Fakty ponad opinie. Nie wydawaj rekomendacji „kup/sprzedaj" — przedstawiaj tezę, argumenty za i przeciw oraz ryzyka.

## Konwencje Markdown w `docs/investing.md`

- Sekcje to bloki `<details open><summary>` z nagłówkiem w środku; numeracja `1.1`, `2.3.1` itd. i spis treści na górze. Nowy rozdział = wpis w spisie treści.
- Wzory w LaTeX (`$$ ... $$`), nazwy zmiennych po angielsku (`net\ profit`), jak w istniejących wzorach.
- Tabele w stylu istniejących (kolumny „Kryterium / Wartość / Uzasadnienie", 🚩/🟢 dla red/green flag).
- Linki wewnętrzne działają jako kotwice GitHub (`#krok-21-...`). Po zmianie nagłówka sprawdź linki do niego.
- Obrazki: kolejne `image-N.png` w `docs/`, zawsze z sensownym tekstem alternatywnym (nie `alt text`).
- Przy edycji notatek zmieniaj plik bezpośrednio; nie wklejaj „wersji do wklejenia" w czacie i nie pisz podsumowania zmian. Wyjaśnienia „dlaczego" tylko na prośbę.

## Rzetelność merytoryczna

- Liczby o podatkach i limitach (Belka 19%, IKE/IKZE, WHT 15% z USA, terminy raportów GPW) zmieniają się — przed wpisaniem zweryfikuj w źródle pierwotnym i podaj rok.
- Definicje wskaźników sprawdzaj względem MSSF/UoR (GPW) i US GAAP (USA); EBITDA i „adjusted" metryki firm nie są pozycjami GAAP.
- Dane spółek: SEC EDGAR (10-K/10-Q/8-K), ESPI/EBI na emitent.gpw.pl, strony relacji inwestorskich, Biznesradar, Stooq. Zawsze podawaj źródło i datę danych.
- Rozdzielaj fakty (dane) od interpretacji; oznaczaj założenia. Szukaj powodów, by NIE kupować (confirmation bias) — to zasada z notatek.

## Praca z Claude Code

- Wyspecjalizowani agenci w `.claude/agents/`; do przeglądu treści merytorycznej używaj `fact-checker`, do edycji notatek `investing-advisor`, do analizy spółki `company-analyst`, do lektury raportów `filings-reader`.
- Hook po edycji `.md` uruchamia `scripts/check_md.py --hook` (obrazki, kotwice, znaczniki `$$`, `<details>`). `BLAD` napraw przed zakończeniem pracy; `UWAGA` (np. obrazek bez opisu) napraw, jeśli dotyczy Twojej zmiany.
- Wykresy: skrypt Pythona w `scripts/charts/` + dane w CSV obok; gotową grafikę generuj tylko na wyraźną prośbę.
