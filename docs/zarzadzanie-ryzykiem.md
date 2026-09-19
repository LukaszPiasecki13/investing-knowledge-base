# Zarządzanie ryzykiem i portfelem

_Uzupełnienie do [`investing.md`](investing.md) — domyka proces po analizie fundamentalnej: jak wielką pozycję otworzyć, ile pozycji trzymać i jak traktować ryzyko walutowe. Ostatnia aktualizacja: 2026-09-19._

Analiza fundamentalna odpowiada na pytanie „czy warto kupić". Ten dokument odpowiada na drugie, równie ważne pytanie: „ile" i „co jeszcze może pójść nie tak niezależnie od tego, czy analiza była trafna". Nawet bezbłędna teza inwestycyjna, wciśnięta w za dużą pozycję albo bez dywersyfikacji, potrafi zniszczyć portfel.

---

<details open>
<summary>

## 1. Wielkość pozycji

</summary>

### 1.1. Kryterium Kelly'ego — ile teoretycznie zaryzykować

Kryterium Kelly'ego (J.L. Kelly, 1956) wyznacza frakcję kapitału, która maksymalizuje długoterminowe geometryczne tempo wzrostu kapitału — nie zysk z jednego zdarzenia, tylko tempo składane w wielu powtórzeniach.

$$
f^* = \frac{bp - q}{b}
$$

gdzie $f^*$ to frakcja kapitału na pozycję, $b$ — stosunek potencjalnej wygranej do potencjalnej straty, $p$ — subiektywne prawdopodobieństwo, że teza się sprawdzi, a $q = 1-p$.

**Przykład:** oceniasz szansę na sukces tezy na 55%, a potencjalny zysk i strata są symetryczne ($b=1$): $f^* = (1 \times 0{,}55 - 0{,}45)/1 = 0{,}10$, czyli 10% kapitału.

Trzy zastrzeżenia, bez których wzór jest szkodliwy:

- **$p$ i $b$ to szacunki, nie dane.** W inwestowaniu w akcje (w przeciwieństwie do zakładu z jasno zdefiniowanymi kursami) nie znasz ich naprawdę — szacujesz je z analizy, z błędem. Wzór podany na złych wejściach da złą odpowiedź z tą samą precyzją co na dobrych.
- **Pełny Kelly jest brutalny dla psychiki i dla portfela.** Maksymalizuje tempo wzrostu, ale po drodze generuje głębokie obsunięcia — teoretyczne maksymalne obsunięcie przy pełnym Kelly zbliża się do 100% kapitału zaangażowanego w tę strategię.
- **W praktyce stosuje się Kelly frakcyjny** — połowę ($f^*/2$, „half-Kelly") albo jedną czwartą wyniku. Łapie większość korzyści ze wzrostu przy dużo mniejszej zmienności i mniejszym ryzyku błędu w oszacowaniu $p$.

### 1.2. Reguły praktyczne (rules of thumb)

Kelly jest ramą myślową, nie kalkulatorem do codziennego użytku. W praktyce inwestorzy indywidualni posługują się prostszymi regułami:

| Reguła | Typowy zakres | Uzasadnienie |
| --- | --- | --- |
| Maksymalna pozycja na jedną spółkę | 5-10% portfela | Błąd w tezie jednej spółki (bankructwo, oszustwo księgowe, jednorazowe zdarzenie) nie niszczy portfela |
| Maksymalna pozycja o wysokim przekonaniu i niskim ryzyku | do 15-20% | Rzadkie wyjątki — spółka bardzo dobrze poznana, płynna, niecykliczna |
| Maksymalna ekspozycja na jeden sektor | 20-30% | Ryzyko sektorowe (regulacja, cykl, szok surowcowy) bije w wiele pozycji naraz |
| Maksymalna ekspozycja na jedną walutę spoza PLN | zależnie od tolerancji na ryzyko walutowe (sekcja 3) | Ryzyko kursowe dokłada się do ryzyka spółki, nie zastępuje go |

Wielkość pozycji powinna też **odpowiadać marginesowi bezpieczeństwa** z [`wycena-wewnetrzna.md`](wycena-wewnetrzna.md#6-margines-bezpieczeństwa): teza z małym marginesem lub dużą niepewnością (branża regulowana, koncentracja klientów, słaba historia) zasługuje na mniejszą pozycję niż teza o tym samym oczekiwanym zysku, ale z większym marginesem. To jest praktyczne przełożenie „**Czego nie wiem**" z Kroku 3.4 przewodnika — im dłuższa ta lista, tym mniejsza pozycja.

</details>

---

<details open>
<summary>

## 2. Dywersyfikacja

</summary>

### 2.1. Ile pozycji

Klasyczne badanie Evansa i Archera (1968) wykazało, że losowo wybrany portfel 15 akcji redukuje ryzyko swoiste (specyficzne dla spółki) do poziomu bliskiego rynkowi; późniejsze prace (m.in. Statman, 1987) przesunęły ten szacunek do 20-30 akcji, zależnie od metodologii i okresu badania. Konsensus: **większość korzyści z dywersyfikacji jest zrealizowana przy 20-30 pozycjach** z różnych branż — powyżej tego dodawanie kolejnych spółek daje coraz mniej.

Trzy zastrzeżenia:

- To musi być **20-30 pozycji naprawdę niezależnych**, nie 20 spółek z tej samej branży i tego samego kraju — takie „dwadzieścia" wciąż jest skoncentrowanym zakładem na jeden cykl.
- Ryzyko systematyczne (rynkowe, walutowe, makro) **nie znika przy żadnej liczbie pozycji** — dywersyfikacja usuwa tylko ryzyko swoiste dla spółki.
- Dla inwestora indywidualnego z ograniczonym czasem na analizę **więcej pozycji, niż da się realnie śledzić, jest złudną dywersyfikacją** — 30 spółek, których raportów nikt nie czyta, to gorsza sytuacja niż 10 dobrze poznanych.

### 2.2. Korelacja, nie tylko liczba

Dwie spółki z różnych branż mogą być skorelowane przez wspólny czynnik: obie zależą od kursu EUR/PLN, obie mają jednego dominującego akcjonariusza, obie są wrażliwe na tę samą stopę procentową. Przed uznaniem portfela za zdywersyfikowany, sprawdź wspólne czynniki ryzyka, a nie tylko klasyfikację sektorową.

### 2.3. Rebalancing

Portfel bez rebalancingu z czasem koncentruje się w tym, co najbardziej wzrosło — czyli w pozycjach o najwyższej wycenie względem fundamentów. Dwa podejścia:

- **Kalendarzowy** — przegląd wag co kwartał/pół roku, niezależnie od ruchów cen.
- **Progowy** — rebalancing, gdy pozycja przekroczy zdefiniowany wcześniej limit (np. z 8% do 15% portfela).

Rebalancing polegający na **przycinaniu** przerośniętej pozycji (a nie na jej całkowitym zamknięciu) pozwala pogodzić dyscyplinę wielkości pozycji z niechęcią do sprzedawania dobrze działającej tezy.

</details>

---

<details open>
<summary>

## 3. Ryzyko walutowe (PLN wobec USD/EUR)

</summary>

### 3.1. Mechanizm

Inwestując w spółkę notowaną w USD, masz **dwa** źródła zmienności zamiast jednego: cenę akcji w USD i kurs USD/PLN. Nawet trafna teza inwestycyjna może dać słaby wynik w PLN, jeśli waluta się w tym czasie osłabiła — i odwrotnie, słaba spółka może „zarobić" na walucie.

### 3.2. Hedgować czy nie

| Instrument / decyzja | Kiedy sensowne |
| --- | --- |
| **Nie hedgować** (akceptować ryzyko walutowe) | Akcje na długi horyzont — historycznie ryzyko walutowe akcji częściowo się kompensuje z ryzykiem rynkowym (dolar bywa silny akurat wtedy, gdy globalne akcje słabną), a koszt hedgingu long-term bywa nieopłacalny |
| **ETF z zabezpieczeniem walutowym (hedged)** | Gdy chcesz czystej ekspozycji na indeks/rynek bez komponentu walutowego — kosztem rolowania zabezpieczenia |
| **Naturalny hedge przez margin/pożyczkę w walucie obcej** | Zaawansowane, wymaga zrozumienia ryzyka dźwigni |
| **Hedging na rynku obligacji/instrumentów dłużnych** | Częściej uzasadniony niż na akcjach — zmienność kursu walutowego bywa duża względem niskiej zmienności instrumentu dłużnego, więc bez zabezpieczenia ryzyko walutowe dominuje nad ryzykiem instrumentu |

### 3.3. Koszt hedgingu — parytet stóp procentowych

Zabezpieczenie kursu walutowego (np. kontraktem forward) nie jest darmowe — jego koszt wynika w przybliżeniu z **różnicy stóp procentowych** między Polską a USA (kryty parytet stóp procentowych). Im wyższa stopa w Polsce względem USA, tym korzystniejszy (lub tym mniej kosztowny) jest hedging z perspektywy inwestora w PLN — i odwrotnie.

**Stan na wrzesień 2026** (do zweryfikowania przy użyciu — te liczby są z natury krótkotrwałe): stopa referencyjna NBP wynosi 3,75%, a stopa funduszy federalnych Fed (Federal Funds Rate) po decyzji z 16 września 2026 r. wynosi 3,75-4,00% — różnica jest obecnie bliska zeru, w przeciwieństwie do okresów, gdy różnica sięgała kilku punktów procentowych (np. przy stopie NBP ok. 6,5% i Fed ok. 1,5-1,75%, hedging dawał inwestorowi w PLN dodatkowe ~5 pp rocznie). **Nie ekstrapoluj tej różnicy w przyszłość — sprawdź aktualne stopy NBP i Fed przed decyzją o hedgingu.**

### 3.4. Praktyczna reguła

Dla portfela akcyjnego z horyzontem wieloletnim ryzyko walutowe jest zwykle **akceptowane, nie zabezpieczane** — koszt i złożoność hedgingu rzadko są tego warte dla przeciętnego inwestora indywidualnego. Zabezpieczenie warto rozważyć punktowo: przy dużej, skoncentrowanej pozycji walutowej, przy krótszym horyzoncie (np. znana potrzeba wypłaty w PLN za 1-2 lata) albo na części portfela dłużnej.

</details>

---

<details open>
<summary>

## 4. Checklist przed otwarciem nowej pozycji

</summary>

- [ ] Jaki procent portfela zajmie ta pozycja — i czy to w granicach reguł z sekcji 1.2?
- [ ] Czy portfel po dodaniu tej pozycji ma nadal 20+ realnie niezależnych pozycji, czy koncentruje się w jednym czynniku ryzyka (sekcja 2.2)?
- [ ] Czy wielkość pozycji jest odwrotnie proporcjonalna do listy „czego nie wiem" z tezy (Krok 3.4 przewodnika)?
- [ ] Jaka jest ekspozycja walutowa portfela po tej pozycji i czy wymaga to reakcji (sekcja 3)?
- [ ] Czy zapisany jest poziom, przy którym pozycja zostanie przycięta w ramach rebalancingu?

</details>

---

## Źródła

| Twierdzenie | Źródło | Zweryfikowano |
| --- | --- | --- |
| Kryterium Kelly'ego, wzór $f^*=(bp-q)/b$ | J.L. Kelly Jr., *A New Interpretation of Information Rate*, Bell System Technical Journal, 1956 | 2026-09 |
| Kelly frakcyjny (half-/quarter-Kelly) jako praktyka standardowa | Powszechna praktyka zarządzania ryzykiem — bez pojedynczego źródła akademickiego | 2026-09 |
| 15 akcji redukuje ryzyko swoiste do poziomu bliskiego rynkowi | J.L. Evans, S.H. Archer, *Diversification and the Reduction of Dispersion*, Journal of Finance, 1968 | 2026-09 |
| Rewizja szacunku do 20-30 akcji | M. Statman, *How Many Stocks Make a Diversified Portfolio?*, Journal of Financial and Quantitative Analysis, 1987 | 2026-09 |
| Stopa referencyjna NBP: 3,75% (wrzesień 2026) | [Bankier — RPP wrzesień 2026](https://www.bankier.pl/wiadomosc/Stopy-w-NBP-bez-zmian-we-wrzesiu-2026-Rada-nie-zmienia-stop-ale-czy-zmienila-kurs-9194318.html) | 2026-09 |
| Stopa funduszy federalnych Fed: 3,75-4,00% po decyzji z 16.09.2026 | [CNBC — Fed rate decision September 2026](https://www.cnbc.com/2026/09/16/fed-rate-decision-september-2026.html) | 2026-09 |
| Mechanizm kosztu hedgingu walutowego (parytet stóp procentowych) | Standardowa teoria finansów międzynarodowych — bez pojedynczego źródła | 2026-09 |
