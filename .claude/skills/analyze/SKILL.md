---
name: analyze
description: Uruchamia analizę spółki według frameworku Value lub Growth z docs/investing.md i zapisuje raport w analyses/<TICKER>/. Użyj po wpisaniu /analyze TICKER [value|growth].
argument-hint: TICKER [value|growth]
disable-model-invocation: true
---

Przeprowadź analizę spółki `$ARGUMENTS`.

1. Sparsuj argumenty: ticker (i rynek: GPW lub USA) oraz typ `value` / `growth`. Brak typu → zapytaj użytkownika jednym krótkim pytaniem, jeśli profil spółki nie rozstrzyga.
2. Uruchom subagenta `company-analyst` z tymi parametrami. Do wczytania raportów źródłowych (10-K, raport roczny, ESPI) zleć mu użycie `filings-reader`.
3. Po zakończeniu uruchom `fact-checker` na wygenerowanym raporcie, ograniczając zakres do liczb i wzorów użytych w analizie.
4. Zwróć użytkownikowi: ścieżkę raportu, wynik screenera (spełnione/niespełnione kryteria), główne ryzyka i uwagi z `fact-checker`. Bez rekomendacji kup/sprzedaj.
