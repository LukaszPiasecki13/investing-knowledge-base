---
name: chart
description: Tworzy wykres z danymi finansowymi do poradnika (np. przychód, zysk i cena akcji na akcję w czasie) jako odtwarzalny skrypt Pythona + plik CSV, a gotową grafikę PNG generuje na wyraźną prośbę. Użyj, gdy użytkownik prosi o wykres lub grafikę opartą na danych.
argument-hint: opis wykresu, np. "DOMDEV przychód/zysk/cena 2011-2020"
---

Wykres: `$ARGUMENTS`.

1. **Dane**: zapisz w `scripts/charts/data/<nazwa>.csv` z nagłówkami i jednostkami. Jeśli danych brakuje — pobierz je ze źródła (EDGAR, ESPI, Biznesradar, Stooq) i dopisz kolumnę/plik `source` z URL i datą pobrania. Nie wymyślaj wartości; brak danych zgłoś użytkownikowi.
2. **Skrypt**: `scripts/charts/<nazwa>.py` (matplotlib + pandas), czytający CSV i zapisujący PNG do `docs/`. Zmienne na górze pliku; polskie opisy osi, tytuł z zakresem lat i jednostką (np. „Kwota (PLN)"), etykiety wartości na słupkach, czytelne w jasnym motywie GitHuba.
3. **Grafika**: uruchom skrypt (`python scripts/charts/<nazwa>.py`) **tylko** gdy użytkownik wprost prosi o gotowy obraz lub gdy wykres ma trafić do dokumentu. Nazwij plik kolejnym `image-N.png` (sprawdź istniejące w `docs/`).
4. Przy wstawianiu do Markdown użyj sensownego tekstu alternatywnego, nie `alt text`.

Skill `dataviz` z pluginów, jeśli jest zainstalowany, ma pierwszeństwo w kwestii stylu i palety.
