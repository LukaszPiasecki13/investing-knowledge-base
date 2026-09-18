---
name: post-mortem
description: Przegląd decyzji inwestycyjnej po czasie (kwartalny/roczny albo po zamknięciu pozycji) — porównuje tezę z faktami i klasyfikuje błąd (analiza, timing, emocje, dyscyplina) lub sukces. Użyj po /post-mortem TICKER.
argument-hint: TICKER
disable-model-invocation: true
---

Zrób post-mortem dla `$ARGUMENTS`.

1. Wczytaj `journal/theses/<TICKER>.md` i najnowszy raport z `analyses/<TICKER>/`. Brak tezy → powiedz o tym wprost i poproś o odtworzenie jej z pamięci użytkownika; nie zgaduj, co zakładał.
2. Pobierz aktualne dane (nowe raporty, cena) — `filings-reader` dla raportów. Podaj źródło i datę.
3. Zapisz `journal/post-mortems/<TICKER>-YYYY-MM-DD.md`:
   - **Założenia tezy vs rzeczywistość** (tabela: założenie / próg / stan dziś / status: trzyma się – osłabione – obalone).
   - **Wynik** (stopa zwrotu vs benchmark, dywidendy, podatek) — tylko jeśli użytkownik podał ceny transakcji.
   - **Klasyfikacja**: błąd analizy / timing (dobra spółka, zły moment) / emocje / brak dyscypliny (nie zadziałał exit) / pech (zdarzenie spoza tezy) / sukces powtarzalny.
   - **Czego się nauczyłem** — jedna reguła do dopisania w checkliście lub w `docs/investing.md`.
4. Zwróć wnioski w 3–5 zdaniach. Rozróżnij jakość decyzji od jakości wyniku (dobra decyzja może dać stratę i odwrotnie).
