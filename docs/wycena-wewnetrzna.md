# Wycena wewnętrzna i margines bezpieczeństwa

_Samodzielna baza wiedzy o metodach wyceny — uszczegóławia kryterium „upside > 20% do wyceny wewnętrznej" z Etapu 1 i Kroku 2.3 [`investing.md`](investing.md), ale nie wymaga jego znajomości do zrozumienia. Ostatnia aktualizacja: 2026-09-27._

Wycena wewnętrzna (intrinsic value) to szacunek, ile spółka jest warta na podstawie gotówki, którą wygeneruje — niezależnie od tego, ile za nią dziś płaci rynek. Nie jest liczbą, tylko **przedziałem przy jawnie zapisanych założeniach**. Model, który daje jedną liczbę z dokładnością do grosza, zawsze wprowadza w błąd.

---

<details open>
<summary>

## 1. Którą metodę wybrać

</summary>

| Metoda | Kiedy działa | Kiedy zawodzi |
| --- | --- | --- |
| **DCF** (zdyskontowane przepływy) | Spółka dojrzała, przewidywalna, z dodatnim FCF | Spółki cykliczne (prognoza z jednego punktu cyklu), pre-profit, banki |
| **Model Gordona / DDM** | Spółka dywidendowa o stabilnej polityce wypłat | Brak dywidendy albo dywidenda zmienna |
| **Model H / dwuetapowy DDM** | Spółka z wysokim, ale wygasającym tempem wzrostu dywidendy | Wzrost skokowy, nie płynny |
| **EVA / Residual Income** | Ocena, czy i kiedy spółka tworzy wartość ponad koszt kapitału | Spółki z ujemnym lub silnie zmiennym kapitałem własnym |
| **Wycena porównawcza** (mnożniki peerów) | Istnieje wiarygodna grupa porównawcza | Spółka bez odpowiedników; cała branża w bańce |
| **Transakcje porównywalne** (precedent transactions) | Szacowanie premii za przejęcie, sytuacje M&A | Rynek bez podobnych transakcji w rozsądnym horyzoncie czasowym |
| **Suma części (SOTP)** | Konglomeraty, spółki z wyraźnie różnymi segmentami | Silne synergie między segmentami |
| **Wartość likwidacyjna / majątkowa** | Spółki majątkowe, głęboka wartość, sytuacje kryzysowe | Biznes oparty na aktywach niematerialnych |
| **Wzór Grahama** | Szybkie sito, nie wycena | Zawsze, gdy traktuje się go jako wycenę |

**Zasada praktyczna:** licz co najmniej dwiema metodami. Jeśli dają rozbieżne wyniki, rozbieżność sama w sobie jest informacją — zwykle znaczy, że rynek i Twój model inaczej zakładają tempo wzrostu.

</details>

---

<details open>
<summary>

## 2. DCF — zdyskontowane wolne przepływy

</summary>

### 2.1. Szkielet modelu

Wyceniamy **cały biznes** (FCFF — przepływy dla wszystkich dawców kapitału), dyskontując je kosztem kapitału (WACC), a dopiero potem odejmujemy dług.

$$
FCFF = EBIT \cdot (1 - tax\ rate) + D\&A - CAPEX - \Delta working\ capital
$$

$$
EV = \sum_{t=1}^{n} \frac{FCFF_t}{(1 + WACC)^t} + \frac{TV}{(1 + WACC)^n}
$$

$$
TV = \frac{FCFF_n \cdot (1 + g)}{WACC - g}
$$

$$
equity\ value = EV - net\ debt - minority\ interests - preferred\ equity
$$

$$
fair\ value\ per\ share = \frac{equity\ value}{diluted\ shares}
$$

### 2.2. Założenia — i dlaczego to one są całą treścią modelu

| Założenie | Jak ustalić | Typowa pułapka |
| --- | --- | --- |
| **Okres prognozy** | 5 lat dla spółki dojrzałej, 10 dla rosnącej | Wydłużanie prognozy, żeby uzasadnić wynik |
| **Tempo wzrostu przychodów** | Historia (CAGR 5- i 10-letni), plany zarządu skorygowane w dół, tempo rynku | Ekstrapolacja najlepszego roku |
| **Marża docelowa** | Historyczna mediana, nie szczyt; dla growth — ścieżka dojścia z uzasadnieniem | Zakładanie marży, jakiej spółka nigdy nie miała |
| **CAPEX** | Relacja do amortyzacji i do przychodów z ostatniej dekady | CAPEX poniżej amortyzacji „na zawsze" |
| **Zmiana kapitału obrotowego** | Z historycznego CCC (sekcja 3.6 przewodnika) | Pominięcie — zawyża FCFF rosnącej spółki |
| **Stopa rezydualna $g$** | **Nie więcej niż długoterminowy wzrost nominalny gospodarki** (inflacja celu + realny wzrost) | $g$ = 5% przy WACC 8% — wartość rezydualna zjada 90% wyceny |
| **WACC** | Zob. 2.3 | Dobranie WACC pod z góry założony wynik |

> **Test uczciwości modelu:** sprawdź, jaki procent wyceny stanowi wartość rezydualna. Powyżej ~75% model nie wycenia biznesu, tylko Twoje założenie o nieskończoności — wtedy skróć okres prognozy albo obniż $g$.

### 2.3. WACC

$$
WACC = \frac{E}{E+D} \cdot r_e + \frac{D}{E+D} \cdot r_d \cdot (1 - tax\ rate)
$$

**Koszt kapitału własnego** liczy się najczęściej z CAPM:

$$
r_e = r_f + \beta \cdot ERP
$$

| Składnik | Skąd wziąć dla spółki z GPW |
| --- | --- |
| $r_f$ — stopa wolna od ryzyka | Rentowność 10-letnich obligacji skarbowych RP (dane bieżące, podaj datę) |
| $\beta$ — wrażliwość na rynek | Z serwisu danych albo z regresji wobec WIG; dla małych spółek odczyt bywa bezużyteczny — użyj bety branżowej odlewarowanej i przelewarowanej strukturą spółki |
| $ERP$ — premia za ryzyko rynkowe | Publikowane co roku szacunki premii dla Polski (m.in. zestawienia A. Damodarana) — **podaj rok i źródło**, bo wartość się zmienia; zob. 2.3.1 |
| $r_d$ — koszt długu | Efektywne oprocentowanie z noty o zadłużeniu, nie stawka rynkowa |

**Waluta i inflacja muszą się zgadzać.** Prognoza w złotych nominalnych wymaga WACC nominalnego opartego na polskiej stopie wolnej od ryzyka. Mieszanie przepływów realnych z nominalną stopą dyskontową to najczęstszy błąd techniczny w DCF.

#### 2.3.1. Premia za ryzyko kraju (Country Risk Premium)

Dla spółki działającej głównie w Polsce (rynek wschodzący wg części klasyfikacji) do premii za ryzyko rynkowe dojrzałego rynku (mature market ERP, czyli USA jako punkt odniesienia) dodaje się premię za ryzyko kraju:

$$
r_e = r_f + \beta \cdot ERP_{mature} + CRP
$$

Metodologia Damodarana szacuje $CRP$ ze spreadu domyślności kraju (default spread, z ratingu suwerennego albo spreadu CDS), skalowanego przez relację zmienności rynku akcji do zmienności rynku obligacji:

$$
CRP = default\ spread \times \frac{\sigma_{equity}}{\sigma_{bonds}}
$$

**Aktualny punkt odniesienia:** w aktualizacji Damodarana z lipca 2026 mature market ERP (rynki rozwinięte) wynosi **4,17%**, a ERP dla samych USA **4,45%**; premia specyficzna dla Polski zmienia się z ratingiem i spreadem CDS — sprawdź aktualną wartość w pełnym zestawieniu (arkusz `ctryprem.xlsx` na stronie Damodarana), nie kopiuj liczby z tego dokumentu bez daty.

**Uwaga metodologiczna:** premię za ryzyko kraju dodaje się **raz** — albo do ERP w koszcie kapitału własnego (jak powyżej), albo bezpośrednio do stopy wolnej od ryzyka. Dodanie jej w obu miejscach naraz podwójnie liczy to samo ryzyko.

#### 2.3.2. Premia za wielkość (Size Premium)

Małe spółki historycznie osiągały wyższe stopy zwrotu niż wynikałoby to z ich samej bety — obserwacja spopularyzowana przez Ibbotsona, dziś aktualizowana przez Kroll (dawniej Duff & Phelps) w podziale na decyle kapitalizacji.

$$
r_e = r_f + \beta \cdot ERP + CRP + size\ premium
$$

Typowa wartość dla najmniejszych decyli spółek to rzędu **4-5 punktów procentowych**, ale sama koncepcja jest sporna — Damodaran i inni argumentują, że premia za wielkość w dużej mierze zanikła po latach 80. i że jej mechaniczne dodawanie do bety **podwójnie liczy ryzyko** (beta i wielkość są ze sobą skorelowane). Stosuj z ostrożnością: dla małej spółki z GPW lepszym testem bywa podniesienie samej bety (np. przez porównanie z betami zadłużeniowo-korygowanymi mniejszych spółek z branży) niż mechaniczny dodatek punktowy bez uzasadnienia.

### 2.4. Analiza wrażliwości jest obowiązkowa

Nie podawaj jednej liczby. Zrób tabelę wartości na akcję dla siatki WACC × $g$ (np. WACC ±1,5 pp co 0,5 pp, $g$ od 0% do 3%). Dopiero ta tabela pokazuje, czy Twoja teza ma margines, czy stoi na jednym punkcie.

Uzupełniająco policz **DCF odwrotny**: jakiego tempa wzrostu i jakiej marży wymaga **dzisiejsza cena rynkowa**? To najuczciwsze ćwiczenie, jakie można zrobić z modelem — zamiast pytać „ile jest warta", pytasz „w co wierzy rynek i czy to jest realistyczne".

### 2.5. Wartość rezydualna — dwie metody, nie jedna

Wzór z sekcji 2.1 ($TV = FCFF_n(1+g)/(WACC-g)$) to **metoda wieczystej renty (perpetuity growth)**. Istnieje druga, równie standardowa metoda — **mnożnikowa (exit multiple)**:

$$
TV = EBITDA_n \times mnożnik\ wyjścia
$$

gdzie mnożnik wyjścia to EV/EBITDA (albo EV/EBIT) zaobserwowany dziś w porównywalnych transakcjach lub u porównywalnych spółek.

| | Perpetuity growth | Exit multiple |
| --- | --- | --- |
| Zaleta | Ma podstawy teoretyczne (wieczysta renta rosnąca); nie zależy od dzisiejszych nastrojów rynku | Założenie łatwe do obrony: „10× EBITDA, bo tyle płaci rynek za podobne spółki" |
| Wada | Ekstremalnie czuła na różnicę $WACC - g$; łatwo o iluzję precyzji | Przemyca wycenę rynkową (relatywną) do modelu, który miał być od niej niezależny; jeśli cała branża jest przewartościowana, TV też będzie |
| Typowy wynik | Wyższa wartość rezydualna niż exit multiple przy tych samych założeniach | Niższa, bardziej „ostrożna" wartość |

**Dobra praktyka: policz obie i porównaj.** Rozbieżność jest sygnałem — jeśli exit multiple implikuje $g$ dużo wyższe albo niższe niż to, co jawnie założyłeś w metodzie renty wieczystej, jedno z dwóch założeń jest niespójne z drugim. Odwróć wzór na TV, żeby sprawdzić jaki $g$ jest **implikowany** przez Twój mnożnik wyjścia:

$$
g_{implikowane} = \frac{WACC \times TV_{exit} - FCFF_n}{TV_{exit} + FCFF_n}
$$

### 2.6. Przykład liczbowy (szkic)

Wyłącznie do zilustrowania mechaniki, nie jako wzorzec dla realnej spółki. Spółka dojrzała: $FCFF_0 = 100$ mln zł, wzrost 4%/rok przez 5 lat, $WACC = 9\%$, $g$ rezydualne $= 2{,}5\%$. Wartości poniżej przeliczone precyzyjnie, a w tabeli zaokrąglone do jednej cyfry po przecinku.

| Rok | 1 | 2 | 3 | 4 | 5 |
| --- | --- | --- | --- | --- | --- |
| FCFF (mln zł) | 104,0 | 108,2 | 112,5 | 117,0 | 121,7 |
| Współczynnik dyskonta (1,09)^-t | 0,917 | 0,842 | 0,772 | 0,708 | 0,650 |
| Wartość bieżąca | 95,4 | 91,0 | 86,9 | 82,9 | 79,1 |

Suma wartości bieżących z lat 1-5: **435,3 mln zł**.

$$
TV = \frac{121{,}7 \times 1{,}025}{0{,}09 - 0{,}025} = \frac{124{,}7}{0{,}065} \approx 1918{,}6\ mln\ zł
$$

Zdyskontowana wartość rezydualna: $1918{,}6 \times 0{,}650 \approx 1246{,}9$ mln zł.

$$
EV \approx 435{,}3 + 1246{,}9 = 1682{,}2\ mln\ zł
$$

**Obserwacja, która powinna niepokoić:** wartość rezydualna stanowi tu $1246{,}9 / 1682{,}2 \approx 74\%$ całej wyceny — blisko granicy 75% z sekcji 2.2. Przy $g = 3{,}5\%$ (WACC-g = 5,5%) TV wzrosłoby do ok. 2289,5 mln zł, a EV do ok. 1923,3 mln zł — wzrost o **ok. 14%**. To pokazuje w praktyce, dlaczego analiza wrażliwości (sekcja 2.4) jest obowiązkowa, a nie opcjonalna: przesunięcie $g$ o jeden punkt procentowy, przy WACC bliskim $g$, przesuwa wycenę o kilkanaście procent — a przy mniejszej różnicy $WACC-g$ efekt jest jeszcze silniejszy.

</details>

---

<details open>
<summary>

## 3. Model Gordona (DDM) — dla spółek dywidendowych

</summary>

$$
P_0 = \frac{D_1}{r - g}
$$

gdzie $D_1$ to dywidenda oczekiwana za rok, $r$ — wymagana stopa zwrotu, $g$ — długoterminowe tempo wzrostu dywidendy.

Warunek stosowalności: $g < r$ oraz realnie stabilna polityka wypłat. Model jest bardzo wrażliwy na mianownik — przy $r = 9\%$ zmiana $g$ z 3% na 4% podnosi wycenę o 20%. Dlatego traktuj go jak test spójności, nie jak wycenę.

Przydatne przekształcenie — **tempo wzrostu możliwe do sfinansowania z zysków zatrzymanych**:

$$
g = ROE \cdot (1 - payout\ ratio)
$$

Spółka wypłacająca 80% zysku przy ROE 12% może rosnąć organicznie o ok. 2,4% rocznie. Jeśli zarząd obiecuje 8% wzrostu przy takiej wypłacie, różnicę musi sfinansować długiem albo emisją — i o to warto zapytać.

### 3.1. Model H — kiedy wzrost gaśnie płynnie, nie skokowo

Model Gordona i klasyczny model dwuetapowy zakładają **skokową** zmianę tempa wzrostu (np. z 15% na 3% z dnia na dzień na granicy dwóch etapów) — nierealistyczne dla większości spółek. **Model H** (Fuller-Hsia, 1984) zakłada, że tempo wzrostu **spada liniowo** od wysokiego $g_S$ do docelowego $g_L$ w ciągu okresu o „półokresie" $H$:

$$
P_0 = \frac{D_0 (1+g_L)}{r - g_L} + \frac{D_0 \cdot H \cdot (g_S - g_L)}{r - g_L}
$$

gdzie $D_0$ to bieżąca dywidenda, $g_S$ — tempo wzrostu na starcie, $g_L$ — tempo docelowe (rezydualne), $H$ — połowa liczby lat, w ciągu których wzrost spada z $g_S$ do $g_L$ (np. przy 10-letnim okresie wygasania wzrostu, $H = 5$), a $r$ — wymagana stopa zwrotu.

Pierwszy człon to standardowa wycena Gordona przy stałym $g_L$; drugi dodaje wartość „premii" za nadwyżkowy wzrost w okresie przejściowym. Model H jest wygodny obliczeniowo (nie trzeba osobno prognozować dywidendy w każdym roku okresu przejściowego), ale wciąż zależy od arbitralnego wyboru $H$ — to nie zwalnia z testu wrażliwości znanego z DCF (sekcja 2.4).

</details>

---

<details open>
<summary>

## 4. EVA / Residual Income — czy spółka zarabia więcej niż kosztuje ją kapitał

</summary>

Ekonomiczna wartość dodana (Economic Value Added, EVA — koncepcja spopularyzowana przez Stern Stewart & Co.) i pokrewny model dochodu rezydualnego (Residual Income) pytają nie „ile spółka zarobiła", tylko „ile zarobiła **ponad** to, co kosztował kapitał użyty do tego zarobku".

$$
EVA = NOPAT - (invested\ capital \times WACC) = (ROIC - WACC) \times invested\ capital
$$

gdzie $NOPAT$ i $invested\ capital$ są zdefiniowane jak w sekcji 3.1.3 przewodnika ($ROIC = NOPAT / invested\ capital$).

**Interpretacja jest natychmiastowa:** EVA dodatnie = spółka tworzy wartość ponad koszt kapitału (co jest właśnie treścią reguły ROIC > WACC z przewodnika); EVA ujemne = spółka niszczy wartość, niezależnie od tego, czy księgowy zysk netto jest dodatni. Duża, rosnąca, ale nierentowna względem kosztu kapitału spółka ma **rosnący zysk netto i coraz bardziej ujemne EVA** naraz — to częsta pułapka przy analizie „wzrostu" bez odniesienia do kosztu kapitału.

**Wycena metodą dochodu rezydualnego** sumuje zdyskontowane przyszłe EVA i dodaje do bieżącego kapitału zainwestowanego:

$$
EV = invested\ capital_0 + \sum_{t=1}^{n} \frac{EVA_t}{(1+WACC)^t} + \frac{EVA_n \cdot (1+g)/(WACC-g)}{(1+WACC)^n}
$$

Matematycznie ta metoda przy tych samych założeniach daje **tę samą wycenę co DCF** — to inny sposób zapisania tego samego modelu, nie konkurencyjna teoria. Jej wartość jest diagnostyczna: EVA rozbija wycenę na „kapitał już zainwestowany" i „wartość dodana w przyszłości", co ułatwia rozmowę o tym, ile z ceny akcji płaci się za rzeczy, które spółka **już ma**, a ile za obietnicę tego, czego jeszcze nie zrobiła.

</details>

---

<details open>
<summary>

## 5. Wycena porównawcza i transakcje porównywalne

</summary>

### 5.1. Wycena porównawcza (trading comparables)

Najszybsza i najczęściej nadużywana metoda. Trzy zasady, które decydują o jej sensie:

1. **Grupa porównawcza to nie branża z klasyfikacji giełdowej**, tylko spółki o podobnym modelu, rentowności i tempie wzrostu. Trzy dobrze dobrane spółki są warte więcej niż piętnaście z tego samego sektora.
2. **Używaj mediany, nie średniej**, i pokazuj rozrzut. Jeśli mnożniki w grupie rozciągają się od 8 do 35, mediana nic nie znaczy — najpierw wyjaśnij rozrzut.
3. **Dobierz mnożnik do sytuacji** — zob. sekcje 3.4 i 3.7 przewodnika oraz [`specyfika-sektorowa.md`](specyfika-sektorowa.md) dla mnożników branżowych. Przy różnym zadłużeniu w grupie jedynym uczciwym mnożnikiem jest EV/EBIT albo EV/EBITDA.

Wycena porównawcza mówi, ile rynek **dziś płaci** za podobne biznesy. Nie mówi, ile są warte — cała grupa może być droga naraz. Dlatego zestawiaj ją zawsze z metodą dochodową.

### 5.2. Transakcje porównywalne (precedent transactions)

Wariant wyceny porównawczej oparty nie na dzisiejszych cenach giełdowych, a na **cenach faktycznie zapłaconych przy przejęciach** podobnych spółek w przeszłości.

| | Wycena porównawcza (trading comps) | Transakcje porównywalne (precedent transactions) |
| --- | --- | --- |
| Co mierzy | Cena za mniejszościowy pakiet na giełdzie | Cena za **kontrolę** nad całą spółką |
| Zawiera premię za kontrolę? | Nie | **Tak** — zwykle 20-40% powyżej kursu giełdowego sprzed ogłoszenia transakcji |
| Aktualność | Bardzo aktualna (ceny z dziś) | Tak aktualna, jak najnowsza transakcja w branży — może być nieaktualna o lata |
| Zastosowanie | Wycena akcji na giełdzie | Szacowanie, za ile spółka mogłaby zostać przejęta |

**Zastosowanie praktyczne:** jeśli teza inwestycyjna zawiera element „ta spółka jest kandydatem do przejęcia" (np. z powodu niskiej wyceny wobec majątku albo strategicznego aktywa), transakcje porównywalne dają punkt odniesienia dla potencjalnej premii — trading comps tego nie pokażą, bo z definicji nie zawierają premii za kontrolę. Odwrotnie: **nie stosuj mnożników z transakcji porównywalnych do wyceny akcji na giełdzie** — systematycznie zawyżysz wynik o wielkość premii za kontrolę.

</details>

---

<details open>
<summary>

## 6. Suma części i wartość likwidacyjna

</summary>

### 6.1. Suma części (Sum of the Parts, SOTP)

Stosowana, gdy spółka ma kilka wyraźnie różnych segmentów, które rynek wyceniłby inaczej jako samodzielne biznesy — np. spółka energetyczna z segmentem wydobycia (cykliczny, wysoki mnożnik EV/EBITDA) i segmentem regulowanej dystrybucji (stabilny, niski koszt kapitału, inny mnożnik właściwy — zob. [`specyfika-sektorowa.md`](specyfika-sektorowa.md)).

**Procedura:**

1. Wyceń każdy segment osobno — najlepiej metodą właściwą dla jego branży (DCF dla stabilnego, mnożnik EV/EBITDA branżowy dla cyklicznego, EV/RAB dla regulowanego).
2. Zsumuj wartości segmentów, dodaj gotówkę korporacyjną, odejmij dług korporacyjny i koszty centrali nieprzypisane do segmentów.
3. Porównaj wynik z kapitalizacją giełdową całej spółki — różnica to **dyskonto konglomeratowe** (conglomerate discount) albo **premia**.

**Dyskonto konglomeratowe jest normą, nie anomalią** — rynek systematycznie wycenia sumę segmentów niżej niż ich hipotetyczna wartość osobno, bo: brak czystej ekspozycji dla inwestorów chcących postawić tylko na jeden segment, ryzyko subsydiowania słabszego segmentu przez mocniejszy, złożoność analizy. Dyskonto 10-20% do sumy wycen segmentów jest typowe; wyższe każe szukać przyczyny (np. brak katalizatora do wydzielenia — spin-off).

### 6.2. Wartość likwidacyjna / majątkowa

Odpowiada na pytanie: „ile dostaliby akcjonariusze, gdyby spółkę zamknięto i spieniężono jej majątek dziś" — dolna granica wartości, użyteczna przy spółkach głęboko niedowartościowanych albo w kłopotach.

| Poziom | Metoda | Kiedy stosować |
| --- | --- | --- |
| **Wartość księgowa netto** | Aktywa − zobowiązania, bez korekt | Zbyt optymistyczna — zapasy i należności rzadko spienięża się po wartości księgowej |
| **Wartość likwidacyjna skorygowana** (NCAV, Graham) | Aktywa obrotowe skorygowane o dyskonto (np. 100% gotówki, 80% należności, 50-67% zapasów) minus **wszystkie** zobowiązania | Klasyczne sito Grahama na „net-nets" — spółki notowane poniżej NCAV |
| **Wartość odtworzeniowa** (replacement value) | Ile kosztowałoby odtworzenie majątku produkcyjnego od zera, po cenach dzisiejszych | Branże kapitałochłonne, cykliczne (sekcja 3 [`specyfika-sektorowa.md`](specyfika-sektorowa.md)) |

$$
NCAV = current\ assets \times discount\ factors - total\ liabilities
$$

Test Grahama „net-net": spółka notowana **poniżej 2/3 NCAV** na akcję uznawana była za statystycznie atrakcyjną — ale to sito, nie wycena: część takich spółek jest tania właśnie dlatego, że biznes operacyjny traci pieniądze i zjada ten majątek. Sprawdź trend CFO i marż, zanim uznasz niską cenę do NCAV za okazję.

</details>

---

<details open>
<summary>

## 7. Wzór Grahama — narzędzie przesiewowe

</summary>

$$
V = EPS \cdot (8{,}5 + 2g)
$$

gdzie $EPS$ to znormalizowany zysk na akcję, $8,5$ to mnożnik przyjęty dla spółki bez wzrostu, a $g$ — oczekiwane tempo wzrostu w procentach na najbliższe 7-10 lat. Wersja zrewidowana (1974) koryguje wynik o poziom stóp procentowych:

$$
V = \frac{EPS \cdot (8{,}5 + 2g) \cdot 4{,}4}{Y}
$$

gdzie 4,4 to średnia rentowność amerykańskich obligacji korporacyjnych klasy AAA w 1962 r. (rok skonstruowania oryginalnego wzoru), a $Y$ — **bieżąca** rentowność 20-letnich obligacji korporacyjnych AAA. Dzielenie przez $Y$ przelicza statyczny mnożnik z 1962 r. na dzisiejsze otoczenie stóp procentowych.

**Ograniczenia, których nie da się obejść:** wzór jest liniowy wobec $g$, więc przy wysokim zakładanym wzroście daje absurdalne wyniki; „8,5" to mnożnik spółki niewzrostowej z rynku amerykańskiego lat 60., nieprzenoszalny wprost na GPW; a sam Graham traktował go jako ilustrację, nie jako metodę wyceny, i przestrzegał przed formułami dającymi złudzenie precyzji.

Używaj go wyłącznie jako **szybkiego sita** przy przeglądaniu wielu spółek — nigdy jako uzasadnienia pozycji.

</details>

---

<details open>
<summary>

## 8. Margines bezpieczeństwa

</summary>

Margines bezpieczeństwa to różnica między wartością a ceną — bufor na to, że model jest błędny. Nie na to, że rynek się myli; na to, że **Ty się mylisz**.

$$
margin\ of\ safety = \frac{intrinsic\ value - price}{intrinsic\ value}\cdot 100\%
$$

Wymagany margines nie jest stały — skaluje się z niepewnością:

| Profil spółki | Sugerowany margines | Dlaczego |
| --- | --- | --- |
| Dojrzała, stabilne przepływy, niski dług, długa historia | 20-25% | Prognoza obarczona najmniejszym błędem |
| Cykliczna albo surowcowa | 40-50% | Punkt cyklu potrafi przesunąć zysk o rząd wielkości |
| Wysoki dług lub bliskie kowenanty | 40%+ | Błąd w prognozie uderza w kapitał własny z dźwignią |
| Koncentracja klientów lub jeden produkt | 40%+ | Wariancja pojedynczego zdarzenia |
| Growth wyceniany przyszłością | Margines liczony **na mnożniku wyjścia**, nie na cenie | Główne ryzyko to kompresja mnożnika, nie spadek zysku |

**Zapisz przed kupnem:** wartość wewnętrzną z przedziałem, kluczowe założenie, przy którym teza się sypie, i cenę, powyżej której przestajesz kupować. Model bez tych trzech zapisów po pierwszym spadku kursu zamieni się w uzasadnienie tego, co i tak chciałeś zrobić.

</details>

---

## Źródła

| Twierdzenie | Źródło | Zweryfikowano |
| --- | --- | --- |
| Wzór Grahama, wersja podstawowa (1962) | B. Graham, *The Intelligent Investor*, rozdz. 11 | 2026-09 |
| Wzór Grahama, wersja zrewidowana (4,4 / Y) | Rewizja ogłoszona na seminarium ICFA/FARF, wrzesień 1974, włączona do wyd. *The Intelligent Investor* z 1974 r. | 2026-09 |
| Kryteria inwestora defensywnego, margines bezpieczeństwa, NCAV / net-nets | B. Graham, *The Intelligent Investor*, rozdz. 14, 15 i 20 | 2026-09 |
| Model Gordona, CAPM, konstrukcja DCF/WACC, SOTP, precedent transactions | Standardowy aparat finansów przedsiębiorstw i bankowości inwestycyjnej — treść podręcznikowa, bez pojedynczego źródła | 2026-09 |
| Model H (dwuetapowy z liniowo wygasającym wzrostem) | R.J. Fuller, C.-C. Hsia, *A Simplified Common Stock Valuation Model*, Financial Analysts Journal, 1984 | 2026-09 |
| EVA / Economic Value Added | Koncepcja Stern Stewart & Co. (G.B. Stewart, *The Quest for Value*, 1991) | 2026-09 |
| Metoda mnożnikowa (exit multiple) terminal value jako alternatywa dla perpetuity growth | Standardowa praktyka bankowości inwestycyjnej — obie metody powszechnie stosowane, bez jednego pierwotnego źródła | 2026-09 |
| Premia za ryzyko kraju — metodologia (default spread × relacja zmienności) | A. Damodaran (NYU Stern), *Country Risk: Determinants, Measures and Implications* | 2026-09 |
| Mature market ERP 4,17%, ERP USA 4,45% | A. Damodaran, *Equity Risk Premiums, by country* — aktualizacja lipiec 2026 | 2026-09 |
| Premia za wielkość (size premium), rząd wielkości 4-5 pp dla najmniejszych decyli | R. Ibbotson; Kroll (dawniej Duff & Phelps), decylowe zestawienia premii za wielkość | 2026-09 |
| Stopa wolna od ryzyka | Rentowność 10-letnich obligacji skarbowych RP | do sprawdzenia przy każdym użyciu |
| Premia za ryzyko rynkowe/kraju dla Polski — konkretna liczba | Coroczne zestawienia A. Damodarana (NYU Stern) — **wartość zmienna, sprawdź rok** | do sprawdzenia przy każdym użyciu |
