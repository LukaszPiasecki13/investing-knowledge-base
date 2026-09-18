---
name: review-notes
description: Pełny przegląd rozdziału lub pliku z notatkami — równolegle merytoryczny (fact-checker) i strukturalny (walidacja Markdown) — a potem zastosowanie poprawek przez investing-advisor. Użyj po /review-notes [plik lub sekcja].
argument-hint: [plik lub numer sekcji, domyślnie docs/investing.md]
disable-model-invocation: true
---

Przegląd: `$ARGUMENTS` (domyślnie `docs/investing.md`).

1. Uruchom równolegle:
   - subagent `fact-checker` na wskazanym zakresie,
   - `python scripts/check_md.py <plik>` (obrazki, kotwice, `$$`, `<details>`).
2. Zbierz znaleziska. Poziomy `błąd` i `uproszczenie` z pewnością `pewne` oraz wszystkie błędy walidatora przekaż do `investing-advisor` z poleceniem edycji pliku. Pozycje `do weryfikacji` i `brak` (nowe treści) **nie** stosuj automatycznie — wypisz je użytkownikowi do decyzji.
3. Po edycji uruchom ponownie `check_md.py`. Zwróć: liczbę zastosowanych poprawek i listę pozycji czekających na decyzję (jedna linia na pozycję).
