# Specyfika sektorowa — gdzie standardowe wskaźniki zawodzą

_Uzupełnienie do [`investing.md`](investing.md), Część III i IV. Ostatnia aktualizacja: 2026-09-19._

Screener z Etapu 1 (CR > 2, P/BV < 1,5, D/A < 35%) jest skalibrowany na spółkę przemysłową lub handlową. Zastosowany bez zmian do banku, dewelopera albo spółki cyklicznej daje wyniki gorsze niż brak analizy — bo wygląda na obiektywny. Ten dokument opisuje, co podstawić w miejsce standardowych wskaźników.

---

<details open>
<summary>

## 1. Banki

</summary>

### 1.1. Dlaczego standardowe wskaźniki nie działają

Dla banku dług nie jest finansowaniem, tylko **surowcem** — depozyty to jednocześnie zobowiązanie i podstawa biznesu. W konsekwencji:

| Wskaźnik | Dlaczego bez sensu dla banku |
| --- | --- |
| Current Ratio, Quick Ratio | Bilans banku nie dzieli się na obrotowy/trwały w tym znaczeniu; płynność regulują normy nadzorcze |
| Debt/Equity, Debt/Assets | Dźwignia rzędu 10-15× jest normą, nie patologią |
| EV, EV/EBIT, EV/EBITDA | EV zakłada, że dług odejmuje się od wartości — w banku to nie ma zastosowania |
| Net Debt / EBITDA | Brak sensownej definicji EBITDA |
| CAPEX, FCF | Nakłady inwestycyjne są marginalne wobec skali bilansu |

### 1.2. Co stosować zamiast

| Wskaźnik | Definicja | O czym mówi |
| --- | --- | --- |
| **NIM** (marża odsetkowa netto) | wynik odsetkowy / średnie aktywa odsetkowe | Podstawowa rentowność biznesu; silnie zależna od poziomu stóp procentowych |
| **C/I** (cost to income) | koszty operacyjne / dochody ogółem | Efektywność. Niższe = lepiej; to główna miara porównawcza między bankami |
| **NPL ratio** | kredyty z utratą wartości (faza 3) / portfel brutto | Jakość portfela |
| **Koszt ryzyka** (cost of risk) | odpisy na ryzyko kredytowe / średni portfel kredytowy, w pb | Bieżące obciążenie wyniku ryzykiem; najbardziej zmienna pozycja w cyklu |
| **CET1** i łączny współczynnik kapitałowy | kapitał podstawowy Tier 1 / aktywa ważone ryzykiem | Bufor wypłacalności i **warunek wypłaty dywidendy** |
| **LCR / NSFR** | normy płynnościowe | Odporność na odpływ depozytów |
| **ROE, P/BV** | jak w przewodniku | W bankach to para podstawowa — zob. niżej |

### 1.3. Relacja ROE — P/BV

Bank o ROE równym kosztowi kapitału powinien być wyceniany w okolicach P/BV = 1. Bank o trwałym ROE wyraźnie wyższym zasługuje na P/BV powyżej 1, i odwrotnie. Dlatego **porównuj P/BV banków wyłącznie razem z ich ROE** — samo „P/BV 0,7, więc tanio" nie znaczy nic, jeśli ROE wynosi 4%.

### 1.4. Co sprawdzić dodatkowo na GPW

- **Wymogi kapitałowe i polityka dywidendowa** — KNF corocznie publikuje kryteria wypłaty dywidendy przez banki; bank poniżej wymaganych progów nie wypłaci nic niezależnie od zysku. **Sprawdź aktualne stanowisko KNF przed założeniem dywidendy w modelu.**
- **Wrażliwość na stopy procentowe** — banki podają w raportach szacunek wpływu zmiany stóp o 100 pb na wynik odsetkowy. To najważniejsza pojedyncza liczba dla tezy makro.
- **Ryzyka prawne portfela** — rezerwy na sprawy sądowe potrafią przez lata dominować nad wynikiem operacyjnym; szukaj ich w notach i w prezentacjach wynikowych, nie w samym RZiS.
- **Struktura depozytów** — udział depozytów bieżących i detalicznych decyduje o koszcie finansowania w cyklu.

### 1.5. Ubezpieczyciele

| Wskaźnik | Definicja | Interpretacja |
| --- | --- | --- |
| **Combined ratio** | (odszkodowania + koszty) / składka zarobiona | **Poniżej 100% = rentowna działalność ubezpieczeniowa**; powyżej — zysk musi pochodzić z portfela inwestycyjnego |
| **Wskaźnik wypłacalności (Solvency II)** | środki własne / kapitałowy wymóg wypłacalności | Bufor regulacyjny; podstawa zdolności dywidendowej |
| Wynik z portfela inwestycyjnego | — | W ubezpieczeniach majątkowych bywa większy od wyniku technicznego — sprawdź, z czego naprawdę jest zysk |

</details>

---

<details open>
<summary>

## 2. Deweloperzy mieszkaniowi

</summary>

### 2.1. Co jest inne

- **Zapasy to grunty i produkcja w toku**, nie towar handlowy. Wysoki Current Ratio (2-5) nie oznacza płynności — banku ziemi nie sprzedasz w tydzień.
- **Przychód rozpoznawany przy przekazaniu lokalu** (MSSF 15), a nie przy sprzedaży ani przy wpłacie. Stąd skokowe, „grudkowate" przychody: jeden duży projekt oddany w IV kwartale potrafi zrobić połowę roku.
- **Wpłaty klientów** siedzą na rachunkach powierniczych i w zobowiązaniach — nie są jeszcze przychodem, ale są już gotówką w obiegu.
- Z tych powodów **C/Z pojedynczego roku jest w deweloperce niemal bezużyteczne.** Uśredniaj wynik z 3-5 lat.

### 2.2. Wskaźniki właściwe dla branży

| Wskaźnik | O czym mówi |
| --- | --- |
| **Przedsprzedaż (liczba umów rezerwacyjnych/deweloperskich, kwartalnie)** | Najlepszy wskaźnik wyprzedzający — przychody zobaczysz 1,5-2 lata później |
| **Bank ziemi** (liczba PUM do zabudowania) | Ile lat sprzedaży spółka ma zabezpieczone; kurczący się bank ziemi to hamulec wzrostu |
| **Marża brutto na sprzedaży mieszkań** | Główna miara rentowności; wrażliwa na koszty budowy i cenę gruntu sprzed kilku lat |
| **Dług netto / kapitał własny** | Branża jest z natury zadłużona; próg 0,5-0,8 uchodzi za bezpieczny, powyżej 1,0 rośnie ryzyko przy odwróceniu cyklu |
| **Harmonogram przekazań** | Pozwala zrekonstruować przyszłe przychody z już podpisanych umów |

### 2.3. Ryzyko cyklu

Deweloperka jest cykliczna z opóźnieniem: decyzje o zakupie gruntu i rozpoczęciu budowy zapadają 2-3 lata przed przychodem. Najwyższe marże raportowane są więc zwykle wtedy, gdy rynek już się odwrócił — sprzedają się mieszkania budowane na tanich gruntach z poprzedniego cyklu. **Rekordowa marża jest tu sygnałem ostrzegawczym, nie potwierdzeniem tezy.**

</details>

---

<details open>
<summary>

## 3. Spółki cykliczne i surowcowe

</summary>

To jedyna grupa, w której **niskie C/Z jest typowym sygnałem sprzedaży, a wysokie — sygnałem dołka**. Mechanizm:

| Faza cyklu | Zysk | C/Z | Co widzi początkujący | Co jest naprawdę |
| --- | --- | --- | --- | --- |
| Szczyt | rekordowy | bardzo niskie (3-6) | „Tanio!" | Zysk nie do utrzymania; marża wróci do średniej |
| Dołek | bliski zera lub strata | bardzo wysokie lub nieokreślone | „Drogo / nierentowne" | Punkt maksymalnego pesymizmu |

Narzędzia, które to korygują:

- **Zysk znormalizowany** — średnia z pełnego cyklu (7-10 lat) zamiast ostatniego roku. Tę samą logikę realizuje CAPE (sekcja 3.4 przewodnika).
- **C/WK i wartość odtworzeniowa majątku** — stabilniejsze w cyklu niż C/Z.
- **Pozycja na krzywej kosztowej** — w surowcach decyduje o przetrwaniu dołka. Producent z najniższym kosztem gotówkowym wychodzi z bessy z większym udziałem rynku.
- **Struktura kontraktów** — ceny kontraktowe vs spot; zabezpieczenia (hedging) przesuwają wpływ cen o kwartały.
- **Dźwignia** — cykliczna spółka z wysokim długiem to zakład binarny; próg bezpieczeństwa powinien być dużo ostrzejszy niż w przemyśle stabilnym.

</details>

---

<details open>
<summary>

## 4. Spółki technologiczne i software

</summary>

| Problem | Konsekwencja | Co stosować |
| --- | --- | --- |
| Majątek jest w ludziach i kodzie, nie w bilansie | P/BV 8-15 jest normą, nie drożyzną | P/S, EV/Sales, EV/FCF; P/BV pomijaj |
| Duże przychody przyszłych okresów (deferred revenue) w zobowiązaniach | Current Ratio poniżej 1 przy zdrowym biznesie | Sprawdź dynamikę deferred revenue — to wskaźnik wyprzedzający |
| Wynagrodzenie w akcjach (SBC) | CFO i FCF zawyżone; „adjusted" wyniki wyłączają realny koszt | FCF pomniejszony o SBC — zob. [`jakosc-zysku.md`](jakosc-zysku.md) |
| Aktywowane prace rozwojowe | Zysk zawyżony o koszty przeniesione do aktywów | Porównaj dynamikę aktywowanych nakładów z przychodami |
| Koszt pozyskania klienta rozliczany z góry, przychód rozłożony w czasie | Spółka rosnąca wygląda na mniej rentowną, niż jest | Retencja przychodowa, okres zwrotu z pozyskania klienta |

</details>

---

<details open>
<summary>

## 5. Nieruchomości komercyjne i REIT-y

</summary>

W spółkach nieruchomościowych raportujących wg MSSF znaczna część zysku netto pochodzi z **przeszacowania nieruchomości do wartości godziwej** (MSR 40) — a to zysk niegotówkowy. Dlatego branża używa własnych miar:

$$
FFO = net\ income + real\ estate\ D\&A + impairment\ write\text{-}downs - net\ gains\ on\ sale\ of\ depreciable\ property
$$

**FFO** (Funds From Operations, definicja NAREIT) eliminuje z zysku netto amortyzację związaną z nieruchomościami, odpisy z tytułu utraty wartości oraz zyski/straty ze sprzedaży nieruchomości podlegających amortyzacji — dokłada z powrotem to, co jest niegotówkowe albo jednorazowe, i pokazuje powtarzalny wynik z najmu. **AFFO** dodatkowo odejmuje nakłady odtworzeniowe (capex utrzymaniowy) i inne korekty specyficzne dla spółki. Wskaźnik ceny liczy się jako **P/FFO**, a nie C/Z.

Drugą podstawową miarą jest **NAV** (Net Asset Value) — wartość nieruchomości minus dług; spółki notowane są zwykle z dyskontem lub premią do NAV, i to dyskonto jest właściwym przedmiotem analizy.

Czego sprawdzić: wskaźnik pustostanów, średni pozostały okres najmu (WAULT), strukturę i zapadalność długu, stopę kapitalizacji (yield) przyjętą do wyceny portfela — to ostatnie założenie decyduje o całej wartości księgowej.

**Sytuacja w Polsce:** reżim REIT w kształcie znanym z USA **nie funkcjonuje** — kolejne projekty (FINN, później SINN) nie weszły w życie; stan na wrzesień 2026 to brak ustawy skierowanej do Sejmu. Ekspozycję na polskie nieruchomości komercyjne uzyskuje się więc przez zwykłe spółki giełdowe albo zagraniczne REIT-y (z konsekwencjami podatkowymi — zob. [`podatki-i-konta.md`](podatki-i-konta.md)). **Przed użyciem tej informacji sprawdź aktualny status legislacyjny.**

</details>

---

<details open>
<summary>

## 6. Ściągawka: czym zastąpić standardowe kryteria

</summary>

| Sektor | Zamiast C/Z | Zamiast CR > 2 | Zamiast D/E | Wskaźnik wyprzedzający |
| --- | --- | --- | --- | --- |
| Banki | P/BV razem z ROE | LCR, NSFR | CET1 | Koszt ryzyka, wrażliwość na stopy |
| Ubezpieczyciele | P/BV, C/Z na wyniku technicznym | Solvency II | Solvency II | Combined ratio |
| Deweloperzy | C/Z uśrednione 3-5 lat | Struktura zapasów, rachunki powiernicze | Dług netto / kapitał własny | Przedsprzedaż |
| Cykliczne, surowce | C/Z na zysku znormalizowanym, CAPE | CR standardowy | Ostrzejszy próg niż standard | Ceny surowca, krzywa kosztowa |
| Tech / software | EV/Sales, EV/FCF | Deferred revenue | Net cash | Retencja, deferred revenue |
| Nieruchomości | P/FFO, dyskonto do NAV | Harmonogram zapadalności długu | LTV (dług / wartość portfela) | Pustostany, WAULT |

</details>

---

## Źródła

| Twierdzenie | Źródło | Zweryfikowano |
| --- | --- | --- |
| Rozpoznanie przychodu dewelopera przy przekazaniu lokalu | MSSF 15 | 2026-09 |
| Wycena nieruchomości inwestycyjnych w wartości godziwej | MSR 40 | 2026-09 |
| Odpisy metodą oczekiwanych strat kredytowych | MSSF 9 | 2026-09 |
| Definicja FFO (wynik netto + amortyzacja nieruchomości + odpisy z utraty wartości − zyski/straty ze sprzedaży nieruchomości podlegających amortyzacji) | [Nareit — Funds From Operations (FFO)](https://www.reit.com/glossary/funds-operation-ffo) | 2026-09 |
| Brak obowiązującej ustawy o REIT-ach/SINN w Polsce | [Analiza statusu prac legislacyjnych](https://bank.pl/reit-y-w-polsce-utracona-szansa-czy-swiadoma-ochrona-rynku/) — projekt nieskierowany do Sejmu | 2026-09 |
| Wymogi kapitałowe i kryteria dywidendowe banków | Stanowiska KNF — **publikowane corocznie, sprawdzaj każdorazowo** | do sprawdzenia przy każdym użyciu |
