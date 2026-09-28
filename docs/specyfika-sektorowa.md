# Specyfika sektorowa — gdzie standardowe wskaźniki zawodzą

_Samodzielna baza wiedzy o analizie branżowej — uszczegóławia Część III i IV [`investing.md`](investing.md), ale nie wymaga jego znajomości do zrozumienia. Ostatnia aktualizacja: 2026-09-27._

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

## 5. Telekomunikacja

</summary>

### 5.1. Dlaczego to osobna branża analityczna

Telekomy łączą dwie cechy rzadko występujące razem: bardzo dużą kapitałochłonność (sieć trzeba budować i modernizować bez końca) z relatywnie stabilnym, powtarzalnym przychodem abonamentowym. Standardowe C/Z i CR mówią mało — kluczowe są metryki operacyjne na klienta.

### 5.2. Wskaźniki właściwe dla branży

| Wskaźnik | Definicja | O czym mówi |
| --- | --- | --- |
| **ARPU** (Average Revenue Per User) | przychód cykliczny / średnia liczba abonentów | Siła cenowa; spadające ARPU zwykle oznacza wojnę cenową na nasyconym rynku |
| **Churn** (wskaźnik odejść) | liczba klientów utraconych w okresie / średnia liczba klientów | Jakość usługi i lojalność; niski churn pozwala amortyzować wysoki koszt pozyskania klienta (CAC) w dłuższym czasie |
| **CAPEX / przychody** | nakłady inwestycyjne / przychody | Intensywność kapitałowa; jednorazowe zakupy częstotliwości (spektrum) trzeba wyłączyć, licząc „capex utrzymaniowy" do porównań FCF |
| **EV/EBITDA na ARPU** | mnożnik EV/EBITDA skorygowany o poziom ARPU i dywersyfikację usług | Operator zintegrowany (głos + dane + TV + IoT) zasługuje na wyższy mnożnik niż pojedyncza usługa głosowa/szerokopasmowa — orientacyjnie niżej dla samej łączności podstawowej, wyżej dla operatora z pakietami konwergentnymi |

### 5.3. Na co uważać

- **Spektrum (częstotliwości)** — jednorazowe, ogromne wydatki na aukcjach częstotliwości psują porównywalność CAPEX i FCF między latami; wyłączaj je z „capex utrzymaniowego" przy liczeniu powtarzalnego FCF.
- **Dług netto** bywa strukturalnie wysoki (sieć to aktywo długoterminowe, finansowane długiem) — porównuj Net Debt/EBITDA z resztą branży, nie z ogólną normą przemysłową.
- **Konwergencja usług** (bundling głosu, danych, telewizji) redukuje churn, ale wymaga własnej infrastruktury (kabel/światłowód) — operator czysto mobilny bez sieci stacjonarnej jest bardziej narażony na wojnę cenową.
- **Regulacja** (opłaty za roaming, obowiązki dostępowe, ceny za zakańczanie połączeń) — sprawdź otoczenie regulacyjne kraju notowania, bo bezpośrednio kształtuje ARPU.

</details>

---

<details open>
<summary>

## 6. Spółki użyteczności publicznej i energetyka regulowana

</summary>

### 6.1. Dlaczego standardowa wycena zawodzi

Dystrybutor energii, wody czy gazu w modelu regulowanym nie konkuruje o klienta ceną — **regulator ustala, jaki zwrot na majątku wolno mu zarobić**. To zmienia całą logikę analizy: pytanie nie brzmi „czy spółka jest konkurencyjna", tylko „jaki zwrot przyznał regulator i jak stabilna jest ta przyznana stopa".

### 6.2. Mechanizm regulacji (building-block approach)

| Element | Co to jest |
| --- | --- |
| **RAB** (Regulatory Asset Base) | Skumulowane, uznane przez regulatora nakłady inwestycyjne netto po amortyzacji regulacyjnej — baza, od której liczy się dozwolony zwrot |
| **WACC regulacyjny** (allowed return) | Stopa zwrotu z RAB przyznana przez regulatora na dany okres regulacyjny (zwykle kilkuletni) |
| **Przychód dozwolony** | RAB × WACC regulacyjny (zwrot z kapitału) + amortyzacja RAB (zwrot kapitału) + uznane koszty operacyjne + podatek |

### 6.3. Wskaźniki właściwe dla branży

| Wskaźnik | O czym mówi |
| --- | --- |
| **EV/RAB** | Analogia do P/BV dla spółek regulowanych; mnożnik w okolicach 1,0-1,5× jest typowy — znacząco wyższy sygnalizuje, że rynek oczekuje zwrotu ponad regulacyjny (np. dzięki działalności nieregulowanej) |
| **Spread: rzeczywisty ROE vs WACC regulacyjny** | Czy spółka wykonuje lepiej czy gorzej niż zakładał regulator (efektywność kosztowa, dyscyplina inwestycyjna) |
| **Udział przychodów nieregulowanych** | Segmenty poza regulacją (np. sprzedaż detaliczna energii, usługi dodatkowe) mają inny profil ryzyka i inny właściwy mnożnik — traktuj jak SOTP ([`wycena-wewnetrzna.md`](wycena-wewnetrzna.md#6-suma-części-i-wartość-likwidacyjna)) |

### 6.4. Na co uważać

- **Ryzyko regulacyjne jest ryzykiem politycznym** — zmiana metody wyznaczania WACC regulacyjnego albo tempa wzrostu RAB między okresami regulacyjnymi to główne ryzyko tezy, nie konkurencja rynkowa.
- **Inflacja i WACC regulacyjny nie mogą być liczone podwójnie** — RAB indeksowana inflacją wymaga WACC realnego; RAB w wartości nominalnej wymaga WACC nominalnego. Sprawdź, którą metodę stosuje regulator.
- **CAPEX jest w tym modelu paliwem wzrostu, nie kosztem** — większy uznany RAB to większa baza przyszłych przychodów, więc spółka regulowana ma odwrotną motywację do inwestowania niż spółka rynkowa (bodziec do maksymalizacji uznanych nakładów, nie do ich minimalizacji).

</details>

---

<details open>
<summary>

## 7. Handel detaliczny i dobra konsumpcyjne

</summary>

### 7.1. Wskaźniki właściwe dla branży

| Wskaźnik | Definicja | O czym mówi |
| --- | --- | --- |
| **Sprzedaż porównywalna** (LFL / same-store sales) | dynamika przychodów tych samych, działających od ponad roku placówek | Wzrost organiczny bez efektu nowych otwarć — najważniejsza pojedyncza metryka branży; typowy zdrowy zakres to **2-5% rocznie**, powyżej sygnalizuje albo bardzo dobrą koniunkturę, albo niską bazę |
| **Rotacja zapasów** (inventory turnover) | COGS / średnie zapasy (w skali roku) | Efektywność kapitału obrotowego; typowy zakres w handlu detalicznym to **4-8×** rocznie — poniżej oznacza zaleganie towaru (ryzyko przecen), znacząco powyżej może sygnalizować braki towarowe |
| **GMROI** (Gross Margin Return on Investment) | marża brutto % × rotacja zapasów | Łączy rentowność z efektywnością kapitału obrotowego w jedną miarę — użyteczne do porównań między formatami sklepów |
| **Sprzedaż na m² powierzchni** | przychód / powierzchnia handlowa | Produktywność sieci; spadająca przy stałej liczbie sklepów to sygnał kanibalizacji lub utraty ruchu |

### 7.2. Marża brutto zależy od segmentu — nie porównuj między nimi

Poziomy referencyjne różnią się drastycznie w zależności od formatu: dyskont/handel towarami podstawowymi **20-25%**, spożywczy/FMCG **25-30%**, handel ogólny **30-40%**, specjalistyczny **40-55%**, dobra luksusowe **55-70%**. Porównanie marży dyskontu z marżą sieci specjalistycznej jako sygnału „lepszego/gorszego zarządzania" jest bezwartościowe — to inne modele biznesowe z definicji.

### 7.3. Na co uważać

- **E-commerce vs sklepy stacjonarne** — inna struktura kosztów (logistyka i zwroty vs czynsze i personel); udział kanału online w przychodach i jego rentowność brzegowa (marginal profitability) to coraz częściej kluczowa metryka wyprzedzająca.
- **Sezonowość** — handel detaliczny (zwłaszcza modowy i z zabawkami/elektroniką) ma silnie skoncentrowany IV kwartał; porównania r/r muszą uwzględniać kalendarz świąt.
- **Leasing powierzchni handlowej** — po MSSF 16 zobowiązania z czynszów wchodzą do bilansu (zob. sekcja 2.5 przewodnika); sieci z dużą liczbą wynajmowanych lokali mają wyższy dług raportowany niż przed 2019 r., bez zmiany realnego ryzyka.
- **Private label (marki własne)** — wyższa marża brutto niż marki producenckie, ale wymaga własnych nakładów na rozwój produktu i kontrolę jakości.

</details>

---

<details open>
<summary>

## 8. Farmacja i biotechnologia

</summary>

### 8.1. Dlaczego to najbardziej wyspecjalizowana branża do analizy

Wartość spółki biotechnologicznej pre-commercial w całości siedzi w **przyszłości niepewnej z natury** — w lekach, które jeszcze nie przeszły badań klinicznych. Standardowe wskaźniki (C/Z, ROE) nie mają zastosowania, bo spółka zwykle nie ma jeszcze przychodu.

### 8.2. Fazy badań klinicznych i prawdopodobieństwo sukcesu

| Faza | Cel | Orientacyjne prawdopodobieństwo przejścia do kolejnej fazy |
| --- | --- | --- |
| Faza I | Bezpieczeństwo, na małej grupie zdrowych/chorych ochotników | — |
| Faza II | Wstępna skuteczność i dawkowanie | **~30-35%** przechodzi do Fazy III — to największa bariera w całym procesie |
| Faza III | Skuteczność i bezpieczeństwo na dużej populacji | — |
| Rejestracja (np. FDA) | Formalna zgoda na dopuszczenie do obrotu | — |

Całościowe prawdopodobieństwo dojścia od Fazy I do rejestracji wynosi orientacyjnie **10-14%**, ale różni się drastycznie między obszarami terapeutycznymi: onkologia ma jedne z najniższych wskaźników sukcesu (**~3-7%**), choroby rzadkie i hematologia — jedne z najwyższych (**~25%**). Programy z biomarkerem selekcjonującym pacjentów mają istotnie wyższą szansę sukcesu niż programy bez selekcji.

### 8.3. Metoda wyceny: rNPV (risk-adjusted NPV)

Standardowy DCF (sekcja 2 [`wycena-wewnetrzna.md`](wycena-wewnetrzna.md)) trzeba zmodyfikować, ważąc przepływy z każdego programu prawdopodobieństwem sukcesu na każdym etapie:

$$
rNPV = \sum_{i} PoS_i \times \frac{CF_i}{(1+r)^{t_i}}
$$

gdzie $PoS_i$ to skumulowane prawdopodobieństwo dotrwania do momentu przepływu $CF_i$ (produkt prawdopodobieństw przejścia przez wszystkie wcześniejsze fazy).

**To założenie decyduje o całej wycenie** — błąd w oszacowaniu prawdopodobieństwa sukcesu o 10 punktów procentowych może zmienić wartość pojedynczego programu o 50-100%. Sprawdzaj, czy analityk/spółka używa prawdopodobieństw specyficznych dla obszaru terapeutycznego, czy uniwersalnego uśrednienia.

### 8.4. Patent cliff — ryzyko dla spółek już komercyjnych

Dla dojrzałych spółek farmaceutycznych kluczowe ryzyko jest odwrotne: utrata wyłączności patentowej na istniejące leki i wejście generyków/biopodobnych, które potrafią zabrać większość przychodu z danego produktu w ciągu 1-2 lat od wygaśnięcia patentu. Sprawdź **harmonogram wygasania patentów** na główne produkty spółki wobec harmonogramu jej pipeline'u — spółka z bliskim patent cliff i słabym pipeline'em ma strukturalny problem niezależnie od bieżących wyników.

### 8.5. Wskaźniki dla spółek komercyjnych

| Wskaźnik | Typowy zakres | Uwaga |
| --- | --- | --- |
| **EV/EBITDA** | **10-16×** dla spółek na etapie komercyjnym | Spółki z bliskim patent cliff notowane z dyskontem do średniej sektorowej |
| **R&D / przychody** | Silnie zależne od modelu (generyczny vs innowacyjny) | Spadający udział R&D przy rosnących przychodach bywa sygnałem „żniw" portfela bez odbudowy pipeline'u |

</details>

---

<details open>
<summary>

## 9. Nieruchomości komercyjne i REIT-y

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

## 10. Ściągawka: czym zastąpić standardowe kryteria

</summary>

| Sektor | Zamiast C/Z | Zamiast CR > 2 | Zamiast D/E | Wskaźnik wyprzedzający |
| --- | --- | --- | --- | --- |
| Banki | P/BV razem z ROE | LCR, NSFR | CET1 | Koszt ryzyka, wrażliwość na stopy |
| Ubezpieczyciele | P/BV, C/Z na wyniku technicznym | Solvency II | Solvency II | Combined ratio |
| Deweloperzy | C/Z uśrednione 3-5 lat | Struktura zapasów, rachunki powiernicze | Dług netto / kapitał własny | Przedsprzedaż |
| Cykliczne, surowce | C/Z na zysku znormalizowanym, CAPE | CR standardowy | Ostrzejszy próg niż standard | Ceny surowca, krzywa kosztowa |
| Tech / software | EV/Sales, EV/FCF | Deferred revenue | Net cash | Retencja, deferred revenue |
| Telekomunikacja | EV/EBITDA wobec ARPU | Nie stosuje się bezpośrednio | ND/EBITDA branżowy, wyższy niż przemysł | ARPU, churn |
| Utilities regulowane | EV/RAB | Nie stosuje się (biznes regulowany) | Dźwignia akceptowana wyżej — stabilny przepływ | Decyzje regulatora, spread ROE-WACC regulacyjny |
| Retail / FMCG | C/Z z korektą na format sklepu | Rotacja zapasów, GMROI | Zobowiązania handlowe wobec DPO | LFL (sprzedaż porównywalna) |
| Farmacja / biotech | rNPV zamiast C/Z (pre-commercial); EV/EBITDA (komercyjne) | Nie stosuje się do pre-profit | Runway gotówki | Wyniki faz badań klinicznych, patent cliff |
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
| Definicje ARPU, churn, capex/sales i mnożniki EV/EBITDA wobec ARPU dla telekomów | [Visible Alpha — Integrated Telecom KPIs](https://visiblealpha.com/telecommunications/integrated-telecom-companies/telecom-kpis/); [ibinterviewquestions.com — Telecom Valuation](https://ibinterviewquestions.com/guides/tmt-investment-banking/telecom-valuation-ev-ebitda-ev-subscriber) | 2026-09 |
| Mechanizm regulacji RAB/WACC regulacyjny (building-block approach), mnożniki EV/RAB ok. 1,0-1,5× | [RSM — Regulated Asset Value and Regulatory Asset Base](https://www.rsm.global/australia/insights/regulated-asset-value-ravregulatory-asset-base-rab-key-principles); [ibinterviewquestions.com — Infrastructure and Utilities Valuation](https://ibinterviewquestions.com/guides/valuation-investment-banking/infrastructure-utilities-valuation-rab-allowed-returns) | 2026-09 |
| Benchmarki marży brutto i rotacji zapasów w handlu detalicznym; wzrost LFL 2-5%/rok jako typowy zdrowy zakres | Zbiorcze zestawienia branżowe (Shopify, FocusCFO, aislestock.com) — **reguły kciuka, bez jednego pierwotnego źródła** | 2026-09 |
| Prawdopodobieństwo sukcesu badań klinicznych wg fazy i obszaru terapeutycznego (10-14% ogółem, ~30-35% Faza II→III, onkologia 3-7%, choroby rzadkie ~25%) | [ibinterviewquestions.com — Probability of Success by Phase](https://ibinterviewquestions.com/guides/healthcare-investment-banking/probability-of-success-by-phase) | 2026-09 |
| Metoda wyceny rNPV (risk-adjusted NPV) dla programów badawczych | [BiopharmaVantage — Pharma & Biotech Valuation Guide](https://www.biopharmavantage.com/pharma-biotech-valuation-best-practices) | 2026-09 |
| EV/EBITDA sektora farmaceutycznego 10-16× dla spółek komercyjnych | [DrugPatentWatch — Valuation of Pharmaceutical Companies](https://www.drugpatentwatch.com/blog/valuation-of-pharma-companies-5-key-considerations-2/) | 2026-09 |
