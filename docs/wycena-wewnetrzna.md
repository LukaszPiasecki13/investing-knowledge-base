# Wycena wewnętrzna i margines bezpieczeństwa

_Uzupełnienie do [`investing.md`](investing.md) — rozwinięcie kryterium „upside > 20% do wyceny wewnętrznej" z Etapu 1 i Kroku 2.3. Ostatnia aktualizacja: 2026-09-19._

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
| **Wycena porównawcza** (mnożniki peerów) | Istnieje wiarygodna grupa porównawcza | Spółka bez odpowiedników; cała branża w bańce |
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
equity\ value = EV - net\ debt - minority\ interests
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
| $ERP$ — premia za ryzyko rynkowe | Publikowane co roku szacunki premii dla Polski (m.in. zestawienia A. Damodarana) — **podaj rok i źródło**, bo wartość się zmienia |
| $r_d$ — koszt długu | Efektywne oprocentowanie z noty o zadłużeniu, nie stawka rynkowa |

**Waluta i inflacja muszą się zgadzać.** Prognoza w złotych nominalnych wymaga WACC nominalnego opartego na polskiej stopie wolnej od ryzyka. Mieszanie przepływów realnych z nominalną stopą dyskontową to najczęstszy błąd techniczny w DCF.

### 2.4. Analiza wrażliwości jest obowiązkowa

Nie podawaj jednej liczby. Zrób tabelę wartości na akcję dla siatki WACC × $g$ (np. WACC ±1,5 pp co 0,5 pp, $g$ od 0% do 3%). Dopiero ta tabela pokazuje, czy Twoja teza ma margines, czy stoi na jednym punkcie.

Uzupełniająco policz **DCF odwrotny**: jakiego tempa wzrostu i jakiej marży wymaga **dzisiejsza cena rynkowa**? To najuczciwsze ćwiczenie, jakie można zrobić z modelem — zamiast pytać „ile jest warta", pytasz „w co wierzy rynek i czy to jest realistyczne".

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

</details>

---

<details open>
<summary>

## 4. Wycena porównawcza

</summary>

Najszybsza i najczęściej nadużywana metoda. Trzy zasady, które decydują o jej sensie:

1. **Grupa porównawcza to nie branża z klasyfikacji giełdowej**, tylko spółki o podobnym modelu, rentowności i tempie wzrostu. Trzy dobrze dobrane spółki są warte więcej niż piętnaście z tego samego sektora.
2. **Używaj mediany, nie średniej**, i pokazuj rozrzut. Jeśli mnożniki w grupie rozciągają się od 8 do 35, mediana nic nie znaczy — najpierw wyjaśnij rozrzut.
3. **Dobierz mnożnik do sytuacji** — zob. sekcje 3.4 i 3.7 przewodnika. Przy różnym zadłużeniu w grupie jedynym uczciwym mnożnikiem jest EV/EBIT albo EV/EBITDA.

Wycena porównawcza mówi, ile rynek **dziś płaci** za podobne biznesy. Nie mówi, ile są warte — cała grupa może być droga naraz. Dlatego zestawiaj ją zawsze z metodą dochodową.

</details>

---

<details open>
<summary>

## 5. Wzór Grahama — narzędzie przesiewowe

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

## 6. Margines bezpieczeństwa

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
| Kryteria inwestora defensywnego i margines bezpieczeństwa | B. Graham, *The Intelligent Investor*, rozdz. 14 i 20 | 2026-09 |
| Model Gordona, CAPM, konstrukcja DCF/WACC | Standardowy aparat finansów przedsiębiorstw — treść podręcznikowa, bez pojedynczego źródła | 2026-09 |
| Premia za ryzyko rynkowe dla Polski | Coroczne zestawienia A. Damodarana (NYU Stern) — **wartość zmienna, sprawdź rok** | do sprawdzenia przy każdym użyciu |
| Stopa wolna od ryzyka | Rentowność 10-letnich obligacji skarbowych RP | do sprawdzenia przy każdym użyciu |
