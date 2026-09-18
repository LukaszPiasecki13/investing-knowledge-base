---
name: thesis
description: Tworzy lub aktualizuje tezę inwestycyjną spółki w journal/theses/<TICKER>.md — przed zakupem: dlaczego kupuję, założenia, katalizatory, kryteria wejścia i wyjścia, warunki unieważnienia. Użyj po /thesis TICKER albo gdy użytkownik chce zapisać uzasadnienie decyzji.
argument-hint: TICKER
disable-model-invocation: true
---

Przygotuj tezę inwestycyjną dla `$ARGUMENTS` w `journal/theses/<TICKER>.md` (utwórz katalogi; jeśli plik istnieje, dopisz nową sekcję z datą zamiast nadpisywać).

Jeśli istnieje raport w `analyses/<TICKER>/`, oprzyj się na najnowszym; nie wymyślaj liczb. Brakujące pola zostaw jako `TODO` i wypisz je użytkownikowi — teza musi zawierać jego własne uzasadnienie, nie Twoje.

Szablon:

```markdown
# <TICKER> — teza inwestycyjna

**Data:** YYYY-MM-DD  **Typ:** Value / Growth  **Horyzont:** …  **Cena w dniu decyzji:** …

## Dlaczego kupuję
(2–4 zdania; co rynek źle wycenia lub przeocza)

## Kluczowe założenia (falsyfikowalne)
| # | Założenie | Metryka | Próg unieważnienia |
| --- | --- | --- | --- |

## Katalizatory i daty
## Wycena i margines bezpieczeństwa
Base / Bull / Bear: prawdopodobieństwa, wartość, założenia.

## Powody, by NIE kupować
(min. 3; najsilniejszy kontrargument na górze)

## Wejście / wyjście
- Wejście: cena/warunki, wielkość pozycji (% portfela)
- Wyjście: cel, zmiana fundamentów (co konkretnie), lepsza alternatywa

## Stan emocjonalny i alternatywy rozważane
(FOMO? kotwiczenie? — dane do przyszłego post-mortem)
```
