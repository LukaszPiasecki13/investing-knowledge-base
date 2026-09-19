# Analiza fundamentalna spółek giełdowych - przewodnik praktyczny

_Wersja robocza - usystematyzowane notatki_

_Ostatnia aktualizacja: 2026-09-19. Progi liczbowe pochodzące z przepisów opatrzone są rokiem i podstawą prawną — przed użyciem sprawdź, czy nadal obowiązują (sekcja [Źródła](#źródła))._

**Dokumenty powiązane:**

| Dokument | Zakres |
| --- | --- |
| [`mssf-vs-uor.md`](mssf-vs-uor.md) | Różnice MSSF vs ustawa o rachunkowości — dlaczego raport z GPW wygląda inaczej niż podręcznikowy bilans |
| [`jakosc-zysku.md`](jakosc-zysku.md) | Jakość zysku, red flagi księgowe, rozwodnienie i wynagrodzenie w akcjach (SBC) |
| [`wycena-wewnetrzna.md`](wycena-wewnetrzna.md) | DCF, model Gordona, wycena porównawcza, wzór Grahama, margines bezpieczeństwa |
| [`specyfika-sektorowa.md`](specyfika-sektorowa.md) | Banki, deweloperzy, spółki cykliczne, REIT-y — gdzie standardowe wskaźniki zawodzą |
| [`podatki-i-konta.md`](podatki-i-konta.md) | Belka, OKI, IKE/IKZE, W-8BEN i dywidendy z USA (stan na 2026) |
| [`zrodla-i-slownik.md`](zrodla-i-slownik.md) | Skąd brać dane + słownik skrótów PL/EN |

---

<details open>
<summary>

## 📑 Spis treści

</summary>

### 1. CZĘŚĆ I: Podstawy analizy fundamentalnej
- [1.1. Wprowadzenie](#11-wprowadzenie)

### 2. CZĘŚĆ II: Sprawozdania finansowe - jak je czytać
- [2.1. Wprowadzenie do sprawozdań finansowych](#21-wprowadzenie-do-sprawozdań-finansowych)
- [2.2. Rachunek zysków i strat (RZiS)](#22-rachunek-zysków-i-strat-rzis)
- [2.3. Bilans](#23-bilans)
- [2.4. Rachunek przepływów pieniężnych (Cash Flow)](#24-rachunek-przepływów-pieniężnych-cash-flow)
- [2.5. MSSF czy ustawa o rachunkowości — który układ czytasz](#25-mssf-czy-ustawa-o-rachunkowości--który-układ-czytasz)

### 3. CZĘŚĆ III: Wskaźniki finansowe
- [3.1. Wskaźniki rentowności](#31-wskaźniki-rentowności)
- [3.2. Wskaźniki płynności finansowej](#32-wskaźniki-płynności-finansowej)
- [3.3. Wskaźniki zadłużenia i wypłacalności](#33-wskaźniki-zadłużenia-i-wypłacalności)
- [3.4. Wskaźniki cenowe/giełdowe](#34-wskaźniki-cenowegiełdowe)
- [3.5. Wskaźniki dywidendowe](#35-wskaźniki-dywidendowe)
- [3.6. Wskaźniki sprawności i cykl konwersji gotówki](#36-wskaźniki-sprawności-i-cykl-konwersji-gotówki)
- [3.7. Wartość przedsiębiorstwa (EV) i mnożniki oparte o EV](#37-wartość-przedsiębiorstwa-ev-i-mnożniki-oparte-o-ev)
- [3.8. Modele scoringowe ryzyka i jakości](#38-modele-scoringowe-ryzyka-i-jakości)
- [3.9. Miary tempa wzrostu](#39-miary-tempa-wzrostu)

### 4. CZĘŚĆ IV: Analiza Fundamentalna
- [4.1. Analiza firm typu Value](#41-analiza-firm-typu-value)
- [4.2. Analiza firm typu Growth](#42-analiza-firm-typu-growth)

### [Źródła](#źródła)

</details>

---

<details open>
<summary>

# 1. CZĘŚĆ I: Podstawy analizy fundamentalnej

</summary>

## 1.1. Wprowadzenie

Celem dokumentu jest uporządkowanie kroków analizy spółki giełdowej i zrozumienie podstawowych elementów sprawozdań finansowych.

**Analiza wstępna (biznes i branża)**

Sprawdź:

- czym zajmuje się spółka (model biznesowy, źródła przychodów),
- w jakiej działa branży,
- czy branża się rozwija i ma perspektywy wzrostu.

**Szybki checklist**

- Przychody i zysk: rosną czy falują?
- Marża operacyjna: stabilna czy spada?
- CFO: dodatni i zbliżony do zysku netto?
- Dług netto: rośnie szybciej niż biznes?
- Należności / zapasy: rosną szybciej niż sprzedaż?
- Dywidenda: z gotówki czy na kredyt?

</details>

---

<details open>
<summary>

# 2. CZĘŚĆ II: Sprawozdania finansowe - jak je czytać

</summary>

<details open>
<summary>

## 2.1. Wprowadzenie do sprawozdań finansowych

</summary>

**Elementy sprawozdania i sens dla inwestora**

Poniższa tabela pokazuje, co zawiera każda część sprawozdania i na co patrzeć jako inwestor.

| Część sprawozdania | Co w niej znajdziesz (w skrócie) | Po co to inwestorowi / na co patrzeć |
| --- | --- | --- |
| Bilans (Sytuacja finansowa) | Aktywa (majątek: gotówka, należności, zapasy, środki trwałe) oraz pasywa (kapitał własny + zobowiązania) - stan na dzień | Bezpieczeństwo i stabilność: zadłużenie, płynność, jakość aktywów (np. czy rosną należności/zapasy), struktura finansowania |
| Rachunek zysków i strat (RZiS) | Przychody, koszty, wynik operacyjny, finansowy, podatek, zysk netto - za okres | Rentowność i wzrost: marże, tempo wzrostu, czy zysk jest powtarzalny, udział kosztów stałych/zmiennych |
| Rachunek przepływów pieniężnych (Cash Flow) | Przepływy: operacyjne (CFO), inwestycyjne (CFI), finansowe (CFF) - za okres | Prawdziwa gotówka vs papierowy zysk: czy zysk zamienia się w CFO, CAPEX vs amortyzacja, dywidendy i spłaty długu z realnej gotówki |
| Zmiany w kapitale własnym | Jak zmienił się kapitał: zysk zatrzymany, dywidendy, emisje/wykupy akcji, inne korekty | Polityka dla akcjonariuszy: czy firma buduje kapitał, czy rozwadnia, czy dywidenda jest zdrowa |
| Noty objaśniające (Informacja dodatkowa) | Szczegóły pozycji z bilansu/RZiS/CF, zasady rachunkowości, segmenty, zadłużenie (terminy, oprocentowanie), rezerwy, spory, transakcje powiązane | Największe mięso: tu wychodzą jednorazówki, ryzyka, kowenanty, manipulacje rachunkowe i to, co naprawdę siedzi w liczbach |
| Opinia biegłego rewidenta (audyt) | Typ opinii (bez zastrzeżeń / z zastrzeżeniem / odmowa / negatywna), kluczowe sprawy badania (KAM) | Czerwona lampka lub zielone światło: zastrzeżenia, problemy z kontynuacją działalności, obszary ryzyka wskazane przez audytora |
| Sprawozdanie z działalności / raport zarządu (często razem) | Opis biznesu, ryzyk, otoczenia, perspektyw, komentarz do wyników, inwestycje | Kontekst i narracja: weryfikujesz, czy opowieść zarządu pasuje do liczb; szukasz konkretów zamiast marketingu |

**Zalecana kolejność czytania raportu**

1. RZiS - czy rośnie biznes i marże?
2. Cash Flow - czy zysk zamienia się w gotówkę?
3. Bilans - czy nie rośnie dług / zapasy / należności podejrzanie?
4. Noty - zadłużenie, jednorazowe zdarzenia, segmenty, ryzyka.
5. Kapitał własny + raport zarządu - kontekst i jakość zarządzania.

**Terminy publikacji raportów (rynek regulowany GPW, stan na 2026)**

Podstawa: Rozporządzenie Ministra Finansów z 6 czerwca 2025 r. w sprawie informacji bieżących i okresowych (Dz.U. 2025 poz. 755, obowiązuje od 24.06.2025; zastąpiło rozporządzenie z 29 marca 2018 r.). To są **terminy graniczne**, nie daty publikacji.

| Raport | Termin ustawowy | Data graniczna przy roku kalendarzowym |
| --- | --- | --- |
| Roczny | 4 miesiące od końca roku obrotowego | 30 kwietnia |
| Za I kwartał | 60 dni od końca kwartału | 30 maja |
| Półroczny | 3 miesiące od końca półrocza | 30 września |
| Za III kwartał | 60 dni od końca kwartału | 29 listopada |

Trzy rzeczy, o których warto pamiętać:

- **Nie ma raportów za II i IV kwartał** — ich rolę pełnią raport półroczny i roczny. Dane za IV kwartał trzeba wyliczyć samodzielnie jako różnicę rok minus trzy kwartały (albo poczekać na raport roczny).
- Spółka publikuje **własny kalendarz** raportem bieżącym w styczniu i zwykle raportuje wcześniej niż termin graniczny (GPW SA za 2026: I kwartał 27 maja, III kwartał 16 listopada). Zmiana terminu wymaga osobnego raportu bieżącego — nagłe przesunięcie publikacji „w tył" bywa sygnałem ostrzegawczym.
- **NewConnect (ASO) ma własne, luźniejsze terminy** z Regulaminu ASO, a zakres raportu kwartalnego jest tam znacznie uboższy. Nie zakładaj, że mała spółka z NC raportuje tak samo jak spółka z rynku głównego.

</details>

---

<details open>
<summary>

## 2.2. Rachunek zysków i strat (RZiS)

</summary>

Poniżej **wariant kalkulacyjny** RZiS (koszty grupowane według funkcji), w kolejności z załącznika nr 1 do ustawy o rachunkowości. Ustawa dopuszcza też **wariant porównawczy** (koszty według rodzaju: amortyzacja, materiały i energia, usługi obce, wynagrodzenia, podatki i opłaty, pozostałe, plus pozycja „zmiana stanu produktów"). Obydwa doprowadzają do tego samego zysku ze sprzedaży — różnią się tylko sposobem pokazania kosztów. Sprawdź na początku, który wariant stosuje spółka, bo wariant porównawczy nie pokazuje marży brutto ze sprzedaży.

| Poziom | Pozycja RZiS | Wpływ na wynik | Znaczenie dla inwestora |
| --- | --- | --- | --- |
| 1 | Przychody ze sprzedaży netto | + | Sprzedaż usług, wyrobów i towarów po potrąceniu VAT. Punkt startowy do oceny skali biznesu. |
| 2 | Koszty wytworzenia sprzedanych wyrobów (COGS) | - | Koszty bezpośrednio związane z produkcją/świadczeniem usług (materiały, energia, wynagrodzenia produkcyjne, usługi obce, amortyzacja). |
| 3 | **Zysk/strata brutto ze sprzedaży** | = | Pierwszy kluczowy poziom rentowności podstawowej działalności. Baza marży brutto — miary siły cenowej. |
| 4 | Koszty sprzedaży | - | Koszty związane z pozyskaniem i obsługą sprzedaży. |
| 5 | Koszty ogólnego zarządu | - | Koszty utrzymania organizacji. |
| 6 | **Zysk/strata ze sprzedaży** | = | Faktyczny wynik na kluczowej działalności operacyjnej, przed pozostałą działalnością operacyjną. To jest „czysta" miara biznesu. |
| 7 | Pozostałe przychody operacyjne | + | Dodatkowe przychody operacyjne (np. dotacje, sprzedaż aktywów, rozwiązanie rezerw). |
| 8 | Pozostałe koszty operacyjne | - | Dodatkowe koszty operacyjne (np. kary, odszkodowania, odpisy aktualizujące). |
| 9 | **Zysk/strata na działalności operacyjnej (EBIT)** | = | Wynik operacyjny przed finansowaniem i podatkiem. |
| 10 | Przychody finansowe | + | Dywidendy, odsetki, zyski ze zbycia aktywów finansowych, dodatnie różnice kursowe. |
| 11 | Koszty finansowe | - | Koszt odsetek i innych operacji finansowych. |
| 12 | Udział w wynikach jednostek stowarzyszonych | +/- | Tylko w sprawozdaniu skonsolidowanym: wynik spółek konsolidowanych metodą praw własności. Bywa istotną częścią zysku, a nie generuje gotówki w spółce matce. |
| 13 | **Zysk/strata brutto** | = | Wynik przed opodatkowaniem. |
| 14 | Podatek dochodowy | - | Obciążenie okresu (część bieżąca + odroczona). Efektywna stawka daleka od 19% zawsze wymaga zajrzenia do noty. |
| 15 | Wynik na działalności zaniechanej | +/- | Wynik segmentów przeznaczonych do sprzedaży lub zamknięcia. Nie ekstrapoluj go na przyszłość. |
| 16 | **Zysk/strata netto** | = | Wynik końcowy po podatku. |
| 17 | — w tym przypadający akcjonariuszom jednostki dominującej | | **To jest licznik EPS i mianownik C/Z.** |
| 18 | — w tym przypadający udziałom niekontrolującym | | Część wyniku należna mniejszościowym współwłaścicielom spółek zależnych — nie jest Twoja. |
| 19 | Całkowite dochody (OCI) | = | Zysk netto + pozycje odnoszone bezpośrednio na kapitał (różnice kursowe z przeliczenia, wycena instrumentów zabezpieczających, przeszacowania). Tłumaczy, dlaczego kapitał własny zmienia się inaczej niż zysk netto. |

**Gdzie na tej drabinie siedzą jednorazówki.** Im niżej pozycja, tym mniej mówi o powtarzalności biznesu. Skokowy wzrost zysku netto przy płaskim zysku ze sprzedaży (poziom 6) to prawie zawsze pozostała działalność operacyjna (poziom 7), finansowa (10) albo podatek (14) — sprawdź w nocie, zanim uznasz to za poprawę.

</details>

---

<details open>
<summary>

## 2.3. Bilans

</summary>

### 2.3.1. Aktywa - słownik pojęć

Najważniejsze pozycje po stronie aktywów i ich znaczenie:

| Pozycja | Wyjaśnienie |
| --- | --- |
| Aktywa | Zasoby majątkowe jednostki finansowane pasywami. |
| **Aktywa trwałe** | Aktywa o ekonomicznej przydatności dłuższej niż 1 rok. |
| Wartości niematerialne i prawne | Prawa majątkowe (licencje, patenty, oprogramowanie), koszty zakończonych prac rozwojowych oraz **wartość firmy (goodwill)**. Goodwill to **nie** „wartość marki": powstaje wyłącznie przy przejęciu innej spółki jako nadwyżka ceny nabycia nad wartością godziwą możliwych do zidentyfikowania aktywów netto. Marki wytworzonej we własnym zakresie nie wolno aktywować (MSR 38). |
| ⚠️ Goodwill — amortyzacja czy test | Wg **MSSF** goodwill nie jest amortyzowany, tylko corocznie testowany na utratę wartości (MSR 36) — stąd nagłe, wielkie odpisy psujące ROE w jednym kwartale. Wg **UoR** (art. 44b ust. 10) jest amortyzowany przez okres ekonomicznej użyteczności, a gdy nie da się go wiarygodnie oszacować — nie dłużej niż 5 lat. Duży goodwill w bilansie = ryzyko odpisu, nie wartość. |
| Rzeczowe aktywa trwałe | Aktywa trwałe posiadające materialną formę: grunty, budynki, urządzenia, środki transportu. |
| Należności długoterminowe | Należności, których termin wymagalności jest dłuższy niż 1 rok (nie wliczając należności z tytułu dostaw i usług). |
| Inwestycje długoterminowe | Nieruchomości, akcje, obligacje i pożyczki, które nabyte zostały w celu osiągnięcia korzyści ekonomicznej w okresie dłuższym niż 1 rok. |
| Długoterminowe rozliczenia okresowe | Np. aktywa z tytułu odroczonego podatku dochodowego. |
| **Aktywa obrotowe** | Aktywa o ekonomicznej przydatności krótszej niż 1 rok. |
| Zapasy | Materiały, produkty w toku, produkty gotowe i towary, czyli składniki używane do produkcji, jak i te na handel. |
| Należności krótkoterminowe | Wszystkie należności z tytułu dostaw i usług oraz inne, których termin wymagalności jest krótszy niż 1 rok. |
| Inwestycje krótkoterminowe | Gotówka i inne inwestycje krótkoterminowe (lokaty, pożyczki i obligacje do 1 roku itp.). |
| Krótkoterminowe rozliczenia międzyokresowe | Wartość opłaconych z góry środków pieniężnych na koszty podlegające kolejnemu okresowi sprawozdawczemu. |

### 2.3.2. Pasywa - słownik pojęć

Najważniejsze pozycje po stronie pasywów i ich znaczenie:

| Pozycja | Wyjaśnienie |
| --- | --- |
| **Pasywa** | Prawa majątkowe właścicieli i innych podmiotów do aktywów jednostki. **Ludzkim językiem:** sposób finansowania aktywów. |
| **Kapitał własny** | Równowartość aktywów sfinansowana ze środków właścicieli. |
| - Kapitał podstawowy | Pierwotny wkład właścicieli przy założeniu spółki gospodarczej + kapitał z emisji nowych akcji, ale do ich wartości nominalnej. |
| - Kapitał zapasowy | Należy go zwiększać, dopóki nie osiągnie przynajmniej 1/3 kapitału zakładowego (założycielskiego). Zwiększa go nadwyżka wartości wyemitowanych udziałów nad ich wartością nominalną. |
| - Kapitał z aktualizacji wyceny | Zmiana wartości środków trwałych, inwestycji finansowych oraz efekt sprzedanych lub zlikwidowanych środków trwałych. |
| - Pozostałe kapitały rezerwowe | Np. przeznaczenie kapitału na przyszłe dywidendy. |
| - Wynik finansowy z lat ubiegłych | Zysk/straty z poprzedniego okresu, co do których właściciele nie podjęli decyzji o ich rozdysponowaniu. |
| - Wynik finansowy z bieżącego roku | Wartość wyniku zgodnie z rachunkiem zysków i strat. |
| **Zobowiązania** | Równowartość aktywów sfinansowana ze środków zewnętrznych. |
| - Rezerwy na zobowiązania | Np. odroczony podatek dochodowy czy zobowiązania emerytalne. |
| - Zobowiązania długoterminowe | Kredyty i pożyczki, obligacje i inne zobowiązania powyżej 1 roku. |
| - Zobowiązania krótkoterminowe | Kredyty i pożyczki, obligacje i inne zobowiązania poniżej 1 roku. |
| - Rozliczenia międzyokresowe | Przychody rozliczane w czasie (np. dotacje, przedpłaty klientów) oraz — **wg UoR** — ujemna wartość firmy, gdy firma kupuje inną poniżej wartości godziwej jej aktywów netto. Uwaga: **wg MSSF 3** ujemna wartość firmy (bargain purchase) trafia od razu do rachunku wyników jako zysk, a nie do bilansu — potrafi jednorazowo napompować zysk netto przejmującego. |

</details>

---

<details open>
<summary>

## 2.4. Rachunek przepływów pieniężnych (Cash Flow)

</summary>

### 2.4.1. Pozycje i znaczenie

Najważniejsze sekcje rachunku przepływów pieniężnych i ich interpretacja:

| Pozycja | Wyjaśnienie |
| --- | --- |
| **Przepływy pieniężne z działalności operacyjnej** | Ile gotówki spółka zyskała/straciła na swojej głównej działalności w danym okresie sprawozdawczym. |
| Zakres działalności operacyjnej | Podstawowy rodzaj działalności jednostki oraz inne rodzaje działalności niezaliczone do inwestycyjnej lub finansowej. |
| **Przepływy pieniężne z działalności inwestycyjnej** | Ile gotówki spółka zainwestowała (-) lub uzyskała ze zbycia inwestycji (+). |
| Zakres działalności inwestycyjnej | Nabywanie i zbywanie składników aktywów trwałych i krótkoterminowych aktywów finansowych oraz związane z nimi koszty i korzyści. |
| **Przepływy pieniężne z działalności finansowej** | Ile gotówki spółka pozyskała z emisji akcji, obligacji lub zaciągnięcia długu (+), albo ile długu spłaciła (-). |
| Zakres działalności finansowej | Pozyskiwanie lub utrata źródeł finansowania oraz związane z nimi pieniężne koszty i korzyści. |

### 2.4.2. Ocena matrycy przepływów (znaki)

Najpierw patrz na znak przepływów operacyjnych (CFO), a potem oceniaj układ razem z CFI i CFF. Układ `+ - -` bywa zdrowy, natomiast `- + +` często sygnalizuje problemy z podstawową działalnością.

| Nr | Sytuacja | CFO (operacyjna) | CFI (inwestycyjna) | CFF (finansowa) |
| --- | --- | --- | --- | --- |
| 1 | Firma gromadzi środki pieniężne na koncie, aby przeznaczyć je na przyszłe inwestycje. | + | + | + |
| 2 | Idealna sytuacja - firma zarabia, inwestuje i spłaca zobowiązania. | + | - | - |
| 3 | Firma zarabia, inwestuje, ale pozyskuje dodatkowe finansowanie zewnętrzne. | + | - | + |
| 4 | Firma zarabia, ale sprzedaje aktywa (dezinwestuje) i reguluje zobowiązania. | + | + | - |
| 5 | Ujemne przepływy operacyjne, ale firma sprzedaje aktywa i pozyskuje środki z finansowania. Może świadczyć o przejściowych trudnościach. | - | + | + |
| 6 | Niedobory gotówkowe przedsiębiorstwa są pokrywane ze sprzedaży aktywów, co może oznaczać przyszłe bankructwo. | - | + | - |
| 7 | Sytuacja typowa dla młodych, rozwijających się firm, które jeszcze nie osiągnęły rentowności i dużo inwestują. | - | - | + |
| 8 | Przedsiębiorstwo inwestuje mimo notowania strat i konieczności regulowania wcześniejszych zobowiązań. | - | - | - |

**Sam znak to za mało — zestaw CFI z amortyzacją.** Układ `+ - -` wygląda wzorowo, ale jeśli CAPEX jest **trwale niższy od amortyzacji**, spółka nie inwestuje, tylko zjada własny majątek: dziś pokazuje wysoką gotówkę i dywidendę, za kilka lat będzie musiała nadrobić zaległe nakłady. Porównuj CAPEX do amortyzacji w cyklu 5-10 lat (w biznesie stabilnym zdrowa relacja to okolice 1,0; poniżej 0,7 przez kilka lat to sygnał ostrzegawczy, chyba że spółka świadomie wychodzi z kapitałochłonnego segmentu).

### 2.4.3. Wolne przepływy pieniężne (Free Cash Flow, FCF)

FCF to gotówka, która zostaje po utrzymaniu i rozwoju majątku — jedyne realne źródło dywidend, skupów akcji i spłaty długu bez nowego finansowania.

$$
FCF = CFO - CAPEX
$$

- **CAPEX** to wydatki na rzeczowe aktywa trwałe i wartości niematerialne z sekcji inwestycyjnej — nie cała CFI (CFI zawiera też zakupy i sprzedaż papierów wartościowych oraz przejęcia).
- Wariant konserwatywny odejmuje dodatkowo spłatę zobowiązań leasingowych z sekcji finansowej — po MSSF 16 leasing wypadł z CFO i „poprawił" ją czysto technicznie.
- FCF bywa ujemny w latach dużych inwestycji i to nie jest wada; wadą jest **trwale** ujemny FCF przy jednoczesnej wypłacie dywidendy.

</details>

---

<details open>
<summary>

## 2.5. MSSF czy ustawa o rachunkowości — który układ czytasz

</summary>

Sekcje 2.2 i 2.3 opisują układ z **ustawy o rachunkowości (UoR)**. Tymczasem sprawozdania, które faktycznie czytasz analizując spółkę z GPW, są w większości sporządzone wg **MSSF**:

- **Skonsolidowane** sprawozdania emitentów dopuszczonych do obrotu na rynku regulowanym oraz banków sporządza się obowiązkowo wg MSR/MSSF — art. 55 ust. 5 UoR, w wykonaniu art. 4 rozporządzenia (WE) nr 1606/2002.
- **Jednostkowe** sprawozdanie emitenta może być wg MSSF albo wg UoR — decyduje organ zatwierdzający (art. 45 ust. 1a-1c UoR). Stąd w jednym raporcie potrafią współistnieć dwa różne układy.

Praktyczna konsekwencja: nazwy pozycji, układ RZiS i część zasad wyceny będą inne, niż sugerują tabele powyżej. Najważniejsze różnice — nomenklatura, brak kategorii „pozostała działalność operacyjna", leasing wg MSSF 16, nieruchomości inwestycyjne w wartości godziwej, goodwill, ujemna wartość firmy — zebrane są w [`mssf-vs-uor.md`](mssf-vs-uor.md).

</details>

</details>

---

<details open>
<summary>

# 3. CZĘŚĆ III: Wskaźniki finansowe

</summary>

<details open>
<summary>

## 3.1. Wskaźniki rentowności

</summary>

### 3.1.1. Marże — rentowność na kolejnych poziomach RZiS

Marże czyta się razem, jako jeden profil. Każda odpowiada na inne pytanie i każda odnosi się do tego samego mianownika — przychodów ze sprzedaży.

| Marża | Wzór | O czym mówi | Na co uważać |
| --- | --- | --- | --- |
| **Brutto** (gross margin) | (przychody − COGS) / przychody | Siła cenowa i przewaga produktowa. Najbardziej stabilna w czasie w spółkach z fosą. | Widoczna tylko w wariancie kalkulacyjnym RZiS. Spółki różnie kwalifikują koszty do COGS — porównuj w obrębie jednej spółki i jednej branży. |
| **Operacyjna** (EBIT margin) | EBIT / przychody | Efektywność całej operacji po kosztach sprzedaży i zarządu. Główna miara skalowania biznesu. | Zawiera pozostałą działalność operacyjną, czyli także jednorazówki. Dla czystszego obrazu policz też marżę na zysku ze sprzedaży (poziom 6 RZiS). |
| **EBITDA** | EBITDA / przychody | Przybliżenie gotówkowej rentowności operacyjnej; używana do porównań spółek o różnej amortyzacji. | **EBITDA nie jest pozycją MSSF ani US GAAP** — każdy liczy ją po swojemu, a „adjusted EBITDA" tym bardziej. Po MSSF 16 (od 2019) leasing wypadł z kosztów operacyjnych do amortyzacji i odsetek, więc EBITDA skokowo urosła — szeregi obejmujące 2018 i 2019 są nieporównywalne. |
| **Netto** (ROS) | zysk netto / przychody | Ile z każdej złotówki sprzedaży zostaje po wszystkim. | Wrażliwa na podatek odroczony, różnice kursowe i wynik na działalności finansowej. |

$$
EBITDA = EBIT + depreciation + amortization
$$

### 3.1.2. Zwrot z kapitału

**ROE** (Return on Equity) - stopa zwrotu z kapitału własnego lub rentowność kapitału własnego - w przedsiębiorczości, wskaźnik rentowności oznaczający jak wiele zysku udało się wygospodarować spółce z wniesionych kapitałów własnych. Im wartość tego wskaźnika jest wyższa, tym korzystniejsza jest sytuacja firmy. Wyższa efektywność kapitału własnego wiąże się z możliwością uzyskania wyższej nadwyżki finansowej, a co za tym idzie wyższych dywidend.


$$
ROE = \frac{net\ profit}{average\ equity}\cdot 100\%
$$

**Licz od stanu średniego.** Licznik jest strumieniem za cały okres, mianownik — stanem na jeden dzień. Przy szybko rosnącym (albo skokowo zmienionym emisją) kapitale stan końcowy zaniża ROE, a początkowy zawyża. Standard to średnia z początku i końca okresu.

**Rozkład DuPont — skąd naprawdę bierze się ROE:**

$$
ROE = \frac{net\ profit}{sales} \cdot \frac{sales}{assets} \cdot \frac{assets}{equity}
$$

czyli **marża netto × rotacja aktywów × dźwignia finansowa**. To najważniejsze pytanie kontrolne przy każdym wysokim ROE: czy spółka zarabia dzięki marży (przewaga produktowa), dzięki obrotowi (efektywność, typowe dla handlu) czy dzięki dźwigni (pożyczony kapitał). Trzeci przypadek to ROE kupione za ryzyko — i pierwsze, co wyparuje w recesji.

Kiedy ROE kłamie:
- po dużym **skupie akcji** — kapitał własny spada, ROE rośnie bez żadnej poprawy biznesu,
- przy **ujemnym kapitale własnym** — wskaźnik traci sens (matematycznie wychodzi ujemny albo absurdalnie wysoki),
- w spółce z dużym **goodwill** — odpis jednorazowo zawala licznik i mianownik naraz,
- w **banku** — ROE jest tam podstawową miarą, ale progi są zupełnie inne niż w przemyśle (zob. [`specyfika-sektorowa.md`](specyfika-sektorowa.md)).


**ROA** (Return on Assets) - wskaźnik rentowności aktywów. ROA to stosunek zysku netto spółki do wartości jej aktywów. Może być też obliczany jako iloczyn rentowności sprzedaży oraz wskaźnika obrotu aktywów. Informuje o zdolności spółki do wypracowywania zysków i efektywności % gospodarowania jej majątkiem. Im wyższy jest wskaźnik ROA, tym lepsza jest kondycja finansowa spółki. Wskaźnik istotny m.in. dla instytucji finansowych rozważających udzielenie kredytu i badających możliwości jego spłaty.


$$
ROA = \frac{net\ profit}{average\ total\ assets}\cdot 100\%
$$


**ROS** (Return on Sales) - wskaźnik rentowności sprzedaży, rentowność netto - wskaźnik rentowności oznaczający, jak wiele zysku netto pozostaje w przedsiębiorstwie ze sprzedaży. Wskaźnik rentowności sprzedaży to stosunek zysku netto do przychodów netto ze sprzedaży. Informuje o tym ile procent sprzedaży stanowi marża zysku po odliczeniu wszystkich kosztów i zapłaceniu podatków. Wyższy poziom tego wskaźnika wskazuje na korzystniejszą kondycję finansową przedsiębiorstwa. Pogorszenie wskaźnika oznacza, że przedsiębiorstwo musi zrealizować większe rozmiary sprzedaży, aby osiągnąć ten sam zysk.

$$
ROS = \frac{net\ profit}{net\ sales}\cdot 100\%
$$

### 3.1.3. ROIC i ROCE — czy wzrost w ogóle tworzy wartość

ROE i ROA są liczone od zysku netto, więc mieszają wynik operacyjny ze strukturą finansowania i podatkami. **ROIC** (Return on Invested Capital) odcina ten szum: pyta, ile spółka zarabia na kapitale faktycznie zaangażowanym w biznes, niezależnie od tego, czyj to kapitał.

$$
ROIC = \frac{NOPAT}{invested\ capital} = \frac{EBIT \cdot (1 - tax\ rate)}{equity + net\ debt}
$$

**ROCE** (Return on Capital Employed) to bliski kuzyn liczony przed podatkiem: EBIT / (aktywa ogółem − zobowiązania krótkoterminowe). Wygodniejszy, gdy efektywna stopa podatkowa skacze.

**Reguła, wokół której kręci się cała ocena wzrostu:**

| Relacja | Co się dzieje | Wniosek |
| --- | --- | --- |
| ROIC > WACC | Każda złotówka reinwestowana zwiększa wartość spółki | Wzrost jest wart płacenia za niego |
| ROIC ≈ WACC | Wzrost jest neutralny | Spółka biegnie, żeby stać w miejscu |
| ROIC < WACC | Reinwestycja **niszczy** wartość | Rosnące przychody są pułapką; lepiej, żeby spółka wypłaciła gotówkę |

**WACC** (Weighted Average Cost of Capital) to średni ważony koszt kapitału — koszt długu po tarczy podatkowej i koszt kapitału własnego, ważone ich udziałem w finansowaniu. Sposób szacowania i typowe wartości: [`wycena-wewnetrzna.md`](wycena-wewnetrzna.md).

Praktyczne progi (reguła kciuka, silnie zależna od branży): ROIC trwale **> 15%** to sygnał realnej przewagi konkurencyjnej; ROIC poniżej ~8% w spółce niefinansowej oznacza, że biznes prawdopodobnie nie pokrywa kosztu kapitału. Kapitałochłonne branże regulowane (energetyka, wodociągi) z natury mają ROIC niższy i niższy WACC — porównuj tylko wewnątrz branży.

</details>

---

<details open>
<summary>

## 3.2. Wskaźniki płynności finansowej

</summary>

**Cash Ratio** - wskaźnik płynności gotówkowej. Określa, ile razy środki pieniężne będące w dyspozycji przedsiębiorstwa (w kasie lub na rachunku bankowym) pokrywają jego bieżące zobowiązania wobec osób trzecich. Optymalna wysokość tego wskaźnika wynosi 0,2. Wskaźnik ten nie odgrywa istotnej roli przy ustalaniu płynności przedsiębiorstwa, ponieważ w myśl reguł zarządzania finansami, środki pieniężne powinny być ograniczone do minimum, gdyż tylko aktywa zaangażowane w obrocie generują wynik finansowy.


$$
Cash\ Ratio = \frac{cash}{current\ liabilities}
$$


**QR** (Quick Ratio) - wskaźnik płynności szybkiej. Określa, ile razy aktywa bieżące o wysokim stopniu płynności, będące w dyspozycji przedsiębiorstwa, pokrywają jego bieżące zobowiązania wobec osób trzecich. Wskaźnik ten jest wobec wskaźnika CR skorygowany o najmniej płynne aktywa obrotowe, tj. zapasy i rozliczenia międzyokresowe czynne. Optymalna wysokość tego wskaźnika powinna wynosić 1,0, tj. pasywa bieżące powinny być w całości pokryte aktywami bieżącymi o wysokim stopniu płynności. W przypadku przedsiębiorstw charakteryzujących się szybką rotacją aktywów (np. handlowych) norma ta jest obniżona do poziomu 0,7. Niska wartość tego wskaźnika może świadczyć o problemach w zakresie płynności, wysoka zaś o nieproduktywnym nagromadzeniu środków pieniężnych i/lub występowaniu wysokiego stanu należności, co może mieć niekorzystny wpływ na wyniki przedsiębiorstwa.


$$
QR = \frac{current\ assets - inventory - prepayments}{current\ liabilities}
$$


**CR** (Current Ratio) - wskaźnik płynności bieżącej. Informuje o zdolności firmy do wywiązywania się z bieżących zobowiązań, gdyż wskazuje na to, w jakim stopniu majątek obrotowy może pokryć bieżące zobowiązania. Wskaźnik powinien przyjmować wartość w granicach 1,3 - 2. Za optymalną wielkość banki często przyjmują wskaźnik na poziomie równym 2.

$$
CR = \frac{current\ assets}{current\ liabilities}
$$

### 3.2.1. Progi płynności są regułami kciuka, nie prawem

Wartości 0,2 / 1,0 / 1,3-2,0 pochodzą z polskich podręczników finansów przedsiębiorstw i były kalibrowane na produkcji i handlu hurtowym. Zanim odrzucisz spółkę za niski CR, sprawdź model biznesowy:

| Model | Typowy CR | Dlaczego |
| --- | --- | --- |
| Sieć handlowa detaliczna | poniżej 1,0 | Ujemny kapitał obrotowy: klient płaci od razu, dostawcy czekają 60-90 dni. To zaleta, nie wada — dostawcy finansują biznes. |
| Software / SaaS | często < 1,0 | Duże przychody przyszłych okresów (deferred revenue) siedzą w zobowiązaniach krótkoterminowych, choć są już opłaconą gotówką. |
| Deweloper mieszkaniowy | wysoki, 2-5 | Grunty i produkcja w toku księgowane w zapasach. Wysoki CR nie oznacza tu płynności — zapasu nie da się sprzedać w tydzień. |
| Bank / ubezpieczyciel | nie stosuje się | Bilans ma zupełnie inną strukturę; używa się miar adekwatności kapitałowej i płynności regulacyjnej. |

Wniosek dla screenerów: kryterium **CR > 2 z automatu wycina cały sektor finansowy i sporą część spółek technologicznych**, a przepuszcza deweloperów z zamrożonym kapitałem. Zob. [`specyfika-sektorowa.md`](specyfika-sektorowa.md).

Uwaga terminologiczna: „rozliczenia międzyokresowe czynne" ze wzoru na QR to kategoria z UoR. W sprawozdaniu wg MSSF odpowiadają im głównie „przedpłaty" i „pozostałe aktywa obrotowe".

</details>

---

<details open>
<summary>

## 3.3. Wskaźniki zadłużenia i wypłacalności

</summary>

**DR** (Debt Ratio) - wskaźnik ogólnego zadłużenia. Wskaźnik finansowy stanowiący stosunek kapitałów obcych (zobowiązań) do aktywów. Wskaźnik ogólnego zadłużenia jest najbardziej ogólnym obrazem struktury finansowania aktywów przedsiębiorstwa. Im większa jest wartość tego wskaźnika tym wyższe ryzyko ponosi kredytodawca. Stąd często przyjmuje się, że jego wartość powyżej 0,67 wskazuje na nadmierne ryzyko kredytowe. Niski poziom wskaźnika świadczy o samodzielności finansowej przedsiębiorstwa. Przyjęty punkt odniesienia (norma) nie oznacza optymalnej struktury finansowania. Ta zależna jest m.in. od kosztu pozyskania kapitału, a także od generowanej stopy zwrotu (rentowności ekonomicznej, wskaźnika rentowności aktywów) przez przedsiębiorstwo.


$$
DR = \frac{total\ liabilities}{total\ assets}
$$


**D/E** (Debt to Equity Ratio) - wskaźnik informujący o poziomie zadłużenia kapitałów własnych przedsiębiorstwa i zarazem relację kapitałów obcych do kapitałów własnych jako źródeł finansowania przedsiębiorstwa. Przyjmuje się, że wielkość tego wskaźnika nie powinna być wyższa niż 1,0 dla przedsiębiorstw dużych i średnich oraz 3,0 dla przedsiębiorstw małych.

$$
Debt\ to\ Equity = \frac{total\ liabilities}{equity}
$$

⚠️ **Dwie różne rzeczy o tej samej nazwie.** Serwisy finansowe liczą D/E na dwa sposoby i różnica potrafi sięgnąć kilkudziesięciu procent:

- **Zobowiązania ogółem / kapitał własny** — wersja powyżej, szeroka; wlicza zobowiązania handlowe, rezerwy i rozliczenia międzyokresowe.
- **Dług oprocentowany / kapitał własny** — wersja wąska; tylko kredyty, pożyczki, obligacje i zobowiązania leasingowe. To ona odpowiada na pytanie „ile spółka płaci odsetek".

Przy porównywaniu spółek zawsze sprawdź, którą wersję podaje Twoje źródło. Do oceny ryzyka niewypłacalności użyteczniejsza jest wąska.


**ICR** (Interest Coverage Ratio) - wskaźnik pokrycia odsetek. Określa, ile razy zysk operacyjny (EBIT) spółki pokrywa koszty z tytułu odsetek od zadłużenia. Im wyższa wartość wskaźnika, tym łatwiej spółce regulować zobowiązania odsetkowe bez zagrożenia dla płynności. Wartość powyżej 3 zazwyczaj wskazuje na bezpieczny poziom, natomiast spadek poniżej 1,5 to wyraźny sygnał ostrzegawczy i rosnące ryzyko niewypłacalności.

$$
ICR = \frac{EBIT}{interest\ expense}
$$

Ograniczenia ICR: traci sens przy **pozycji gotówkowej netto** (spółka bez długu ma wskaźnik nieskończony lub ujemny bez powodu do niepokoju); część odsetek bywa **kapitalizowana** w wartości środków trwałych i nie pojawia się w kosztach finansowych — sprawdź notę o kosztach finansowania zewnętrznego; w spółce z dużą amortyzacją bywa uzupełniany wariantem EBITDA / odsetki.

### 3.3.1. Dług netto i Net Debt / EBITDA

Dług brutto sam w sobie mówi mało — spółka z 500 mln długu i 600 mln gotówki jest w innej sytuacji niż spółka z 500 mln długu i pustą kasą.

$$
net\ debt = interest\ bearing\ debt - cash\ and\ equivalents
$$

$$
Net\ Debt / EBITDA = \frac{net\ debt}{EBITDA}
$$

Wskaźnik odpowiada na pytanie: **ile lat pełnej EBITDA potrzeba na spłatę zadłużenia netto.** To najczęściej używana miara w kowenantach bankowych, więc warto znać próg zapisany w umowach kredytowych spółki (jest w nocie o zadłużeniu).

| Poziom | Interpretacja (spółka niefinansowa, poza szczytem cyklu) |
| --- | --- |
| < 0 (net cash) | Gotówka przewyższa dług — komfort i opcja na przejęcia lub skup akcji |
| 0-2,0 | Bezpiecznie |
| 2,0-3,0 | Akceptowalnie przy stabilnych przepływach; typowy poziom kowenantu to 3,0-3,5 |
| > 3,5-4,0 | Ryzyko — spółka traci elastyczność, a przy spadku EBITDA wskaźnik rośnie podwójnie szybko |

Trzy pułapki: wskaźnik jest **bezużyteczny przy ujemnej EBITDA**; **rośnie sam z siebie w recesji** (mianownik spada), więc kowenanty pękają dokładnie wtedy, gdy najtrudniej o refinansowanie; po **MSSF 16** zobowiązania leasingowe weszły do długu, więc dla spółek leasingujących powierzchnię odczyty sprzed i po 2019 nie są porównywalne.

</details>

---

<details open>
<summary>

## 3.4. Wskaźniki cenowe/giełdowe

</summary>

**P/E** (Price/Earnings Ratio) - wskaźnik cena/zysk. Jest stosunkiem rynkowej ceny akcji do zysku netto spółki. Niski poziom wskaźnika może sugerować, że inwestycja jest korzystna, ponieważ firma osiąga spore zyski przy relatywnie niskiej wycenie rynkowej. W praktyce zbyt duża wartość C/Z może świadczyć o dużym entuzjazmie inwestorów lub o spekulacji dużych inwestorów. Wskaźnik C/Z powinien być porównywany ze wskaźnikiem branżowym i wyznaczonym dla innych spółek, lub do wskaźnika tej samej spółki w przeszłości. Porównując C/Z firm z tej samej branży, można spodziewać się, że akcje spółki o wysokim poziomie C/Z są przewartościowane i ich kurs może w najbliższym czasie spaść.


$$
P/E = \frac{share\ price}{earnings\ per\ share\ (EPS)}
$$

🚩 **Bardzo niskie C/Z to zwykle ostrzeżenie, nie okazja.** Rynek rzadko wycenia spółkę na 4× zysk „przez nieuwagę". Zanim uznasz to za niedowartościowanie, wyklucz cztery najczęstsze przyczyny:

| Przyczyna | Jak sprawdzić |
| --- | --- |
| **Szczyt cyklu** — spółka cykliczna zarabia rekordowo i rynek wie, że to się nie utrzyma | Porównaj marżę i zysk do średniej z 7-10 lat; niskie C/Z przy rekordowej marży = peak earnings |
| **Zysk jednorazowy** — sprzedaż aktywów, przeszacowanie nieruchomości, bargain purchase | Zysk ze sprzedaży (poziom 6 RZiS) vs zysk netto; nota o pozostałej działalności operacyjnej |
| **Rynek dyskontuje spadek zysków** — utrata kontraktu, wygaśnięcie patentu, regulacja | Prognozy analityków, raport zarządu, komunikaty ESPI |
| **Ryzyko bilansowe lub właścicielskie** — wysoki dług, kowenanty, transfer zysków do głównego akcjonariusza | Net Debt/EBITDA, noty o zadłużeniu, transakcje z podmiotami powiązanymi |

Pozostałe zastrzeżenia do C/Z:
- **Nieokreślone przy stracie** — ujemnego C/Z nie interpretuje się, tylko pomija.
- **Zależy od struktury kapitału** — spółka zalewarowana ma niższe C/Z przy tym samym biznesie. Do porównań między spółkami użyj EV/EBIT (sekcja 3.7).
- **Trailing vs forward** — trailing liczy zysk z 4 ostatnich kwartałów (fakt), forward z prognozy (opinia analityków, systematycznie zbyt optymistyczna). Podawaj, którego używasz.
- **Który EPS** — do wskaźnika bierz zysk **rozwodniony** i **przypadający akcjonariuszom jednostki dominującej** (poziom 17 tabeli RZiS), nie cały zysk netto grupy.


**CAPE** (Cyclically Adjusted P/E) - cyklicznie dostosowany wskaźnik cena/zysk, spopularyzowany przez Roberta Shillera i Johna Campbella. Wariant C/Z, w którym zamiast zysku z ostatnich 4 kwartałów bierzemy **średni zysk z 10 lat urealniony inflacją** — dla indeksu lub spółki. Zyskał popularność jako miara „bardziej obiektywna" i mniej podatna na chwilowe skoki lub dołki zysku. Jest fatalny dla spółek wzrostowych. Stosować do spółek Value i stabilnych.

$$
CAPE = \frac{share\ price}{average\ real\ EPS\ over\ 10\ years}
$$

Dwa warunki poprawnego użycia, o których łatwo zapomnieć:
- **Urealnienie inflacją jest obowiązkowe.** Zysk sprzed 10 lat w nominalnych złotych jest nieporównywalny z dzisiejszym; bez deflacji wskaźnikiem CPI CAPE systematycznie zaniża wycenę.
- Dla **pojedynczej spółki** CAPE ma sens tylko przy stabilnej liczbie akcji. Po dużej emisji albo skupie historyczne EPS-y nie opisują tej samej jednostki — wtedy uśredniaj zysk całkowity i dziel przez bieżącą liczbę akcji.

Wskaźnik pochodny: **wzór Grahama na maksymalną cenę** używa tej samej idei, ale na średniej z 3 lat — zob. sekcja [4.1](#41-analiza-firm-typu-value) i [`wycena-wewnetrzna.md`](wycena-wewnetrzna.md).

**P/BV** (Price to Book Value) - wskaźnik cena do wartości księgowej. Pokazuje relację kapitalizacji giełdowej (ceny rynkowej) do wartości księgowej spółki. Wartość poniżej 1 może sugerować niedowartościowanie.

$$
P/BV = \frac{market\ capitalization}{equity\ attributable\ to\ owners\ of\ the\ parent}
$$

**Licznik i mianownik muszą opisywać to samo.** Kapitalizacja to wartość akcji spółki dominującej, więc w mianowniku musi stać kapitał własny **przypadający akcjonariuszom jednostki dominującej** — bez udziałów niekontrolujących. W grupach z dużymi mniejszościami różnica jest znacząca.

Wariant ostrożniejszy — **P/TBV** (Price to Tangible Book Value), z kapitału własnego odjęte goodwill i wartości niematerialne:

$$
P/TBV = \frac{market\ capitalization}{equity - goodwill - intangibles}
$$

To właśnie do wartości rzeczowej odnosił się próg 1,5 u Grahama. Różnica P/BV vs P/TBV pokazuje, jak dużą część „wartości księgowej" stanowią pozycje, których nie da się spieniężyć.

Kiedy P/BV wprowadza w błąd: w spółkach usługowych i software'owych majątek jest w ludziach i kodzie, a nie w bilansie (P/BV = 8 nie oznacza tam drożyzny); po latach skupów akcji kapitał własny bywa sztucznie niski lub ujemny; grunty i nieruchomości kupione dekady temu figurują w koszcie historycznym, więc realna wartość majątku bywa znacznie wyższa niż księgowa.

**P/S** (Price to Sales) — kapitalizacja / przychody. Jedyny mnożnik działający dla spółek bez zysku. Odporny na kreatywną księgowość kosztów, ale całkowicie ignoruje rentowność — spółka z marżą 2% i marżą 40% mogą mieć to samo P/S. Sensowny wyłącznie wewnątrz jednej branży.

$$
P/S = \frac{market\ capitalization}{revenue}
$$

**P/FCF** (Price to Free Cash Flow) — kapitalizacja / FCF. Odpowiednik C/Z liczony na gotówce zamiast na zysku księgowym; trudniejszy do zmanipulowania. Zmienny rok do roku (cykle inwestycyjne), więc porównuj do mediany z 3-5 lat, a nie do pojedynczego odczytu.

$$
P/FCF = \frac{market\ capitalization}{free\ cash\ flow}
$$

**PEG** (Price/Earnings to Growth) — C/Z podzielone przez tempo wzrostu EPS wyrażone w punktach procentowych. Narzędzie growth: pozwala porównać drogą spółkę szybko rosnącą z tanią spółką stojącą w miejscu.

$$
PEG = \frac{P/E}{EPS\ growth\ rate\ (\%)}
$$

Wartość < 1 uchodzi za atrakcyjną, > 2 za drogą. Największa słabość: mianownik to prognoza. PEG liczony na podstawie wzrostu z ostatniego roku ekstrapoluje jednorazowy skok i potrafi pokazać 0,3 dla spółki po odbiciu z dołka. Używaj wzrostu oczekiwanego na 3-5 lat i traktuj jako sito, nie jako wycenę.

</details>

---

<details open>
<summary>

## 3.5. Wskaźniki dywidendowe

</summary>


**DPR** (Dividend Payout Ratio) - stopa wypłaty dywidendy. Wskaźnik, który liczymy, dzieląc kwotę wypłacanej dywidendy przez zysk netto z poprzedniego okresu sprawozdawczego (zwykle poprzedniego roku, bo głównie z niego wypłaca się dywidendy). Im wyższy, tym bardziej „serio" firma podchodzi do wypłacania dywidend lub tym mniej pomysłu ma na pożytkowanie zarobionej gotówki w przedsiębiorstwie.


$$
DPR = \frac{total\ dividend}{net\ profit}\cdot 100\%
$$


**DY** (Dividend Yield) - stopa dywidendy. Wskaźnik, który uzyskujemy dzieląc kwotę wypłacanej dywidendy na akcję przez cenę akcji. Zwykle w granicach 2-6%; mówi, ile dywidendy „wycisnęlibyśmy" kupując akcje spółki po obecnej cenie.


$$
DY = \frac{dividend\ per\ share}{share\ price}\cdot 100\%
$$

🚩 **Wysoka stopa dywidendy nie jest sama w sobie zaletą.** Licznik zmienia się raz w roku, mianownik codziennie — więc DY najczęściej rośnie dlatego, że **spadła cena**, a rynek dyskontuje cięcie wypłaty. Odczyt powyżej ~8-10% na GPW to prawie zawsze jedna z trzech sytuacji:

- dywidenda **jednorazowa** (sprzedaż aktywów, wypłata z kapitału zapasowego po latach akumulacji) — nie powtórzy się,
- **spółka w kłopotach**, której kurs spadł szybciej niż zarząd zdążył obciąć dywidendę,
- **spółka w schyłkowej branży**, wypłacająca całość zysku, bo nie ma w co inwestować (to bywa racjonalne, ale zysk z takiej pozycji sprowadza się do samej dywidendy).

### 3.5.1. Czy dywidenda jest z czego wypłacana

DPR liczone od zysku netto nie odpowiada na pytanie o bezpieczeństwo wypłaty — zysk to zapis księgowy. Policz oba:

$$
FCF\ payout = \frac{total\ dividend}{free\ cash\ flow}\cdot 100\%
$$

$$
dividend\ cover = \frac{EPS}{DPS}
$$

- **DPR > 100% przez rok** nie musi oznaczać patologii: KSH pozwala wypłacać także z zysków lat ubiegłych i z kapitału zapasowego utworzonego z zysku. Przez kilka lat z rzędu — oznacza.
- **DPR umiarkowane, ale FCF payout > 100%** to najczęstszy ukryty problem: zysk jest, gotówki nie ma, dywidenda idzie z kredytu.
- Kapitał zapasowy w spółce akcyjnej ma część nienaruszalną: art. 396 § 1 KSH nakazuje przelewać co najmniej 8% zysku rocznego, dopóki kapitał nie osiągnie 1/3 kapitału zakładowego, a ta część może służyć wyłącznie pokryciu straty.

### 3.5.2. Kalendarz dywidendy

| Data | Co oznacza |
| --- | --- |
| Uchwała walnego zgromadzenia | Ustala kwotę oraz dwie poniższe daty. Do tego momentu wszystko jest rekomendacją zarządu, nie zobowiązaniem. |
| **Dzień dywidendy** (dzień ustalenia prawa) | Trzeba mieć akcje **zapisane na rachunku** na koniec tego dnia. Ze względu na rozliczenie transakcji w cyklu D+2 akcje trzeba kupić odpowiednio wcześniej — sprawdź aktualny cykl rozliczeniowy KDPW. |
| Dzień wypłaty | Kiedy pieniądze trafiają na rachunek; bywa kilka miesięcy po dniu dywidendy. |

W pierwszej sesji po dniu ustalenia prawa kurs odniesienia jest **obniżany o kwotę dywidendy**. Nie ma darmowego obiadu: kupno „pod dywidendę" tuż przed odcięciem daje gotówkę i o tyle samo niższy kurs — a do tego podatek. Szczegóły opodatkowania: [`podatki-i-konta.md`](podatki-i-konta.md).

Spółka może też wypłacać **zaliczkę na poczet dywidendy** w trakcie roku — wtedy roczne DPR liczy się z sumy wypłat.

</details>

---

<details open>
<summary>

## 3.6. Wskaźniki sprawności i cykl konwersji gotówki

</summary>

Ta grupa odpowiada na pytanie z checklisty ze [wstępu](#11-wprowadzenie): *czy należności i zapasy rosną szybciej niż sprzedaż?* Same kwoty z bilansu tego nie pokażą — potrzebna jest relacja do obrotu, wyrażona w dniach.

| Wskaźnik | Wzór | Co mierzy |
| --- | --- | --- |
| **DSO** — rotacja należności w dniach | (średnie należności / przychody) × 365 | Ile dni trwa ściągnięcie pieniędzy od klienta |
| **DIO** — rotacja zapasów w dniach | (średnie zapasy / COGS) × 365 | Ile dni towar leży w magazynie |
| **DPO** — rotacja zobowiązań w dniach | (średnie zobowiązania handlowe / COGS) × 365 | Ile dni spółka zwleka z zapłatą dostawcom |

$$
CCC = DSO + DIO - DPO
$$

**Cykl konwersji gotówki (Cash Conversion Cycle)** to liczba dni, przez które gotówka spółki jest zamrożona w kapitale obrotowym. Im krótszy, tym mniej kapitału potrzeba do sfinansowania tej samej sprzedaży.

Jak to czytać:

- **CCC ujemny to bardzo mocna pozycja** — klient płaci przed dostawcą. Typowe dla dużych sieci handlowych i części modeli subskrypcyjnych. Taka spółka finansuje wzrost cudzymi pieniędzmi.
- **Rosnący DSO przy płaskiej sprzedaży** to klasyczny sygnał, że przychód został rozpoznany, ale gotówki nie ma: albo spółka wydłuża terminy, żeby wcisnąć sprzedaż, albo klienci przestali płacić. Zestaw to z odpisami na należności w notach.
- **Rosnący DIO** oznacza zapas, który się nie sprzedaje — a to zapowiedź odpisu i uderzenia w marżę. W handlu modą i elektroniką to najważniejszy wskaźnik wyprzedzający.
- **Skokowo rosnący DPO** bywa przedstawiany jako „poprawa zarządzania kapitałem obrotowym", ale często jest po prostu opóźnianiem płatności przy braku gotówki. Sprawdź, czy w tym samym czasie nie rosną zobowiązania przeterminowane (nota) albo koszty faktoringu odwrotnego.

Uzupełniająco: **rotacja aktywów** (przychody / średnie aktywa ogółem) — środkowy człon rozkładu DuPont; jej spadek przy rosnących przychodach oznacza, że spółka kupuje wzrost coraz większym majątkiem.

</details>

---

<details open>
<summary>

## 3.7. Wartość przedsiębiorstwa (EV) i mnożniki oparte o EV

</summary>

C/Z i C/WK patrzą wyłącznie na kapitał akcjonariuszy, więc **nie nadają się do porównywania spółek o różnym zadłużeniu**. Spółka bez długu i spółka z długiem równym połowie kapitalizacji mogą prowadzić identyczny biznes i mieć zupełnie inne C/Z. EV rozwiązuje ten problem: wycenia cały biznes, niezależnie od tego, kto go finansuje.

$$
EV = market\ capitalization + net\ debt + minority\ interests + preferred\ equity
$$

Czyli: ile kosztowałoby przejęcie całej spółki — trzeba zapłacić akcjonariuszom i przejąć jej dług, ale gotówka z bilansu wraca do kieszeni kupującego. W praktyce do zwykłej analizy wystarcza **kapitalizacja + dług netto**; udziały niekontrolujące dodaje się, gdy są istotne.

| Mnożnik | Wzór | Kiedy stosować |
| --- | --- | --- |
| **EV/EBIT** | EV / EBIT | Domyślny mnożnik porównawczy. Odporny zarówno na strukturę kapitału, jak i na różnice w stawkach podatkowych. |
| **EV/EBITDA** | EV / EBITDA | Gdy porównywane spółki mają bardzo różną amortyzację (np. po przejęciach). Uwaga: ignoruje CAPEX, więc faworyzuje biznesy kapitałochłonne — tam, gdzie majątek trzeba odtwarzać, EBITDA jest fikcją. |
| **EV/Sales** | EV / przychody | Dla spółek bez zysku; lepsze od P/S, bo uwzględnia dług. |
| **EV/FCF** | EV / FCF | Najbliżej realnej stopy zwrotu z całego biznesu. |

**Odwrotność EV/EBIT to earnings yield Greenblatta** (EBIT / EV) — wygodne, bo porównywalne wprost z rentownością obligacji: mówi, ile procent rocznie „zarabia" cały biznes w stosunku do ceny jego przejęcia.

Pułapki: dług netto liczy się **na dzień bilansowy**, a kapitalizacja na dziś — przy dużych zmianach zadłużenia mnożnik się rozjeżdża; EV spółki z ogromną gotówką (typowe dla części spółek technologicznych) bywa dużo niższe od kapitalizacji i sprawia wrażenie okazji, choć ta gotówka może być przeznaczona na już ogłoszone przejęcie; w spółkach finansowych EV nie ma sensu, bo dług jest tam surowcem, a nie finansowaniem.

</details>

---

<details open>
<summary>

## 3.8. Modele scoringowe ryzyka i jakości

</summary>

Modele scoringowe sprowadzają kilka wskaźników do jednej liczby. Nie zastępują analizy — służą do **szybkiej eliminacji** na etapie screeningu i do wyłapania spółek, które „wyglądają tanio", bo są w kłopotach.

### 3.8.1. Altman Z''-score (wersja dla rynków wschodzących)

Oryginalny Z-score Altmana (1968) był kalibrowany na amerykańskich spółkach produkcyjnych i zawierał człon z kapitalizacją giełdową. Do GPW i spółek nieprodukcyjnych stosuje się wariant **Z''** dla rynków wschodzących, oparty wyłącznie na danych bilansowych:

$$
Z'' = 3{,}25 + 6{,}56 \cdot X_1 + 3{,}26 \cdot X_2 + 6{,}72 \cdot X_3 + 1{,}05 \cdot X_4
$$

gdzie:

| Zmienna | Definicja |
| --- | --- |
| $X_1$ | kapitał obrotowy netto / aktywa ogółem |
| $X_2$ | zyski zatrzymane / aktywa ogółem |
| $X_3$ | EBIT / aktywa ogółem |
| $X_4$ | wartość księgowa kapitału własnego / zobowiązania ogółem |

| Z'' | Strefa |
| --- | --- |
| > 2,6 | bezpieczna |
| 1,1 - 2,6 | szara (podwyższone ryzyko) |
| < 1,1 | zagrożenia |

### 3.8.2. Ohlson O-score

Model logitowy Ohlsona (1980) zwraca **logarytm szansy**, a nie prawdopodobieństwo. Prawdopodobieństwo upadłości liczy się dopiero jako:

$$
P = \frac{e^{O}}{1 + e^{O}}
$$

Stąd częste nieporozumienie: „O-score < 0,5" znaczy coś zupełnie innego niż „prawdopodobieństwo < 0,5" (temu drugiemu odpowiada O = 0, a Ohlson w oryginalnej pracy stosował punkt odcięcia 0,038 prawdopodobieństwa). **Zanim użyjesz progu z jakiegokolwiek serwisu, sprawdź w jego dokumentacji, czy podaje surowy score, czy prawdopodobieństwo** — inaczej kryterium jest niewykonalne.

### 3.8.3. Piotroski F-Score

Dziewięć binarnych testów (każdy spełniony = 1 punkt), zaprojektowanych właśnie po to, by wśród tanich spółek (niskie C/WK) odróżnić zdrowe od pułapek wartości. Wszystkie dane pochodzą wprost ze sprawozdania, więc da się je policzyć ręcznie.

| Obszar | Test |
| --- | --- |
| Rentowność | 1. ROA dodatni |
| | 2. CFO dodatni |
| | 3. ROA wyższy niż rok temu |
| | 4. CFO > zysk netto (jakość zysku — brak nadmiaru memoriałowych korekt) |
| Struktura finansowania | 5. Dźwignia długoterminowa niższa niż rok temu |
| | 6. Current Ratio wyższy niż rok temu |
| | 7. Brak emisji nowych akcji w ostatnim roku |
| Efektywność operacyjna | 8. Marża brutto wyższa niż rok temu |
| | 9. Rotacja aktywów wyższa niż rok temu |

Interpretacja: **8-9 punktów** — spółka mocna, **0-2** — do odrzucenia. Test nr 4 jest tu najcenniejszy pojedynczo: to najprostszy dostępny filtr jakości zysku.

</details>

---

<details open>
<summary>

## 3.9. Miary tempa wzrostu

</summary>

**Dynamika r/r (YoY)** — porównanie okresu do tego samego okresu rok wcześniej. Dla spółek sezonowych to jedyne uczciwe porównanie kwartałów (q/q myli sezonowość ze zmianą trendu).

**CAGR** (Compound Annual Growth Rate) — średnioroczna stopa wzrostu składanego, czyli tempo, które doprowadziłoby od wartości początkowej do końcowej po równo w każdym roku:

$$
CAGR = \left( \frac{end\ value}{begin\ value} \right)^{\frac{1}{n}} - 1
$$

gdzie $n$ to liczba **lat**, nie liczba obserwacji (dla danych 2015-2020 mamy $n = 5$, nie 6).

Trzy zastrzeżenia, które decydują o wiarygodności całej analizy historycznej:

- **CAGR jest wrażliwy wyłącznie na punkty skrajne.** Rok startowy w dołku cyklu wygeneruje imponujące tempo, które nie opisuje niczego poza odbiciem. Dlatego Graham porównywał **średnie trzyletnie** z początku i końca dekady zamiast pojedynczych lat — to warto przejąć.
- **Nie działa przy zmianie znaku.** Dla przejścia ze straty w zysk CAGR jest matematycznie bez sensu; opisuj taki przypadek słownie albo przez wartości bezwzględne.
- **Licz zawsze kilka okien naraz** (3, 5 i 10 lat). Rozjazd między nimi jest informacją: CAGR 3-letni wyraźnie niższy od 10-letniego oznacza wygasanie wzrostu, wyższy — akcelerację.

**Akceleracja** — zmiana samej dynamiki r/r w kolejnych kwartałach. Trzy kwartały z rzędu rosnącej dynamiki to sygnał wejścia w nową fazę; trzy kwartały spowalniania w spółce wycenionej jak growth to najczęstszy początek przeceny mnożnika.

</details>

</details>

---

<details open>
<summary>

# 4. CZĘŚĆ IV: Analiza Fundamentalna

</summary>

<details open>
<summary>

## 4.1. Analiza firm typu Value

</summary>

Poniżej siedem kryteriów Grahama dla „inwestora defensywnego" (*The Intelligent Investor*, wyd. 1973, rozdz. 14) w wersji oryginalnej i w adaptacji na realia GPW.

| KRYTERIUM | GRAHAM (oryginał, liczby z 1972) | Adaptacja na GPW |
| --- | --- | --- |
| Wielkość | Min. **100 mln USD rocznej sprzedaży** dla spółki przemysłowej **albo** 50 mln USD aktywów dla spółki użyteczności publicznej. Po uwzględnieniu inflacji odpowiada to dziś kwocie rzędu kilkuset mln USD. | Obniżamy wymaganie do 300 mln zł kapitału własnego (ze względu na specyfikę i wielkość GPW). |
| Kondycja finansowa | Wskaźnik płynności bieżącej (CR) > 2 **oraz dług długoterminowy ≤ kapitał obrotowy netto** (aktywa obrotowe − zobowiązania krótkoterminowe) dla spółek przemysłowych. | CR > 2. Kryterium długu wobec kapitału obrotowego zachowujemy — na GPW odsiewa skutecznie. |
| Stabilność zysków | Dodatni zysk w **każdym** z 10 ostatnich lat. | Obecne ROE > 5% i brak strat w ostatnich 5 latach. |
| Rejestr dywidend | Nieprzerwane wypłaty dywidendy przez 20 lat. | Brak twardego kryterium (na GPW prawie nikt go nie spełnia), ale doceniany jest powtarzalny proces wypłaty z FCF. |
| Wzrost dochodów | Wzrost zysku na akcję o min. **33% w ciągu dekady, liczony na średnich trzyletnich** z początku i końca okresu (a nie z pojedynczych lat). | Opcjonalnie w pierwszej fazie — u Grahama dynamika nie jest kluczowa. |
| Umiarkowana cena wobec wyników | C/Z ≤ 15 wobec **średniego zysku z 3 ostatnich lat** (nie wobec 10-letniego CAPE). | C/Z < 10 (bieżące). |
| Umiarkowana cena wobec wartości | C/WK ≤ 1,5 wobec **rzeczowej** wartości księgowej (P/TBV) **lub** reguła łączna: C/Z × C/WK ≤ 22,5. | C/WK < 1,5 jako sito bazowe; do 3,0 dopuszczalne, gdy spełniona jest reguła łączna C/Z × C/WK ≤ 22,5 i ROE > 15%. |

> **Reguła 22,5** jest wygodniejsza niż dwa osobne progi, bo pozwala na wymianę: można zapłacić więcej wobec zysku, jeśli płaci się mniej wobec majątku, i odwrotnie. Przykład: C/Z 18 i C/WK 1,2 daje 21,6 — przechodzi; C/Z 12 i C/WK 2,5 daje 30 — nie przechodzi.


**Plan analizy value investing (3 etapy):**

1. **Etap 1: Skan i wstępna selekcja spółek** — automatyczny screening.
2. **Etap 2: Wstępna analiza historyczna** — weryfikacja trendów z 5-10 lat: zyskowność, fundamenty, wycena.
3. **Etap 3: Analiza jakościowa** — głęboka ocena biznesu, zarządu, fosy (moat), ryzyk i katalizatorów wzrostu.

---

### Etap 1: Skan i wstępna selekcja spółek

#### Parametry screenera

| Kryterium | Wartość graniczna | Uzasadnienie |
| --- | --- | --- |
| **Kapitał własny** | > 300 mln PLN | Wielkość — firma stabilna, płynność akcji, dostępność raportów. |
| **Current Ratio (CR)** | > 2,0 | Kondycja finansowa — płynność bieżąca. Firma z łatwością pokrywa zobowiązania krótkoterminowe. |
| **Cena/Wartość księgowa (P/BV)** | < 1,5 | Nie przepłacamy za majątek netto. Tolerancja do 3,0 wyłącznie przy spełnionej regule Grahama C/Z × C/WK ≤ 22,5. |
| **Cena/Zysk (P/E)** | < 10 | Niska wycena względem bieżących zysków. |
| **ROE** | > 5% | Stabilność zysków — omijamy pułapki wartości (value traps), spółka musi efektywnie zarabiać na własnym kapitale. |

**Dlaczego progi w screenerze są luźniejsze niż w Etapie 2.** Screener ma być **szerokim sitem**: jego zadaniem jest zejść z kilkuset spółek do kilkunastu, nie wybrać zwycięzcy. Stąd ROE > 5% tutaj i ROE > 10-15% w Etapie 2 — to nie sprzeczność, tylko dwa kolejne zacieśnienia. Ustawienie ostrych progów już na screenerze wycina spółki, które mają jeden słaby rok w dziesięcioletniej historii, a to często właśnie te, które są tanie.

⚠️ **Czego ten screener nie znajdzie.** Kryterium CR > 2 z automatu wyklucza banki, ubezpieczycieli i większość spółek technologicznych, a przepuszcza deweloperów z kapitałem zamrożonym w gruntach. Jeśli chcesz analizować sektor finansowy, potrzebujesz osobnego zestawu kryteriów — zob. [`specyfika-sektorowa.md`](specyfika-sektorowa.md).

---

### Etap 2: Wstępna analiza historyczna (eliminacja)

Celem tego etapu jest szybkie odrzucenie spółek niespełniających kluczowych kryteriów przed przejściem do czasochłonnej analizy jakościowej. Zgodnie z planem analizy dokonujemy weryfikacji w trzech głównych filarach.

#### 1. Zyskowność
*Czy firma rośnie i generuje realną gotówkę?*
- [ ] **Rosnące przychody historyczne:** *Revenue, Revenue Growth YoY, Revenue Estimates for n-next years*
- [ ] **Rosnące prognozy przychodów:** *Revenue Estimated Growth* + rewizje prognoz w górę
- [ ] **Rosnące zyski historyczne:** *EPS, EPS Growth YoY, EPS Estimates for n-next years*
- [ ] **Rosnące prognozy zysków:** *EPS Estimated Growth* + rewizje prognoz w górę
- [ ] **Pozytywny Cash-Flow:** *CFO*, *Net Income*, *Operating Margin*

#### 2. Fundamenty
*Czy firma jest bezpieczna finansowo i efektywnie zarządza kapitałem?*
- [ ] **Current/Quick Ratio:** > 1 i rośnie (bezpieczna płynność bieżąca, zdolność do spłaty długów w krótkim terminie).
- [ ] **Debt to Assets:** < 35% — kryterium ostrzejsze od ogólnej normy kredytowej (DR < 0,67 z sekcji 3.3) świadomie, bo w Value płacimy za bezpieczeństwo, nie za dźwignię.
- [ ] **Debt to Equity:** < 1,0 (bezpieczna dźwignia finansowa). Sprawdź, czy Twoje źródło liczy D/E od zobowiązań ogółem czy od długu oprocentowanego — sekcja 3.3.
- [ ] **Net Debt / EBITDA:** < 2,5 i poniżej progu kowenantów z noty o zadłużeniu.
- [ ] **Interest Coverage:** > 3,0 i rośnie (zyski operacyjne bezpiecznie pokrywają koszty odsetek).
- [ ] **Rentowność:** ROE > 10-15%, ROA > 5% (na stabilnym lub rosnącym poziomie); ROIC > WACC.
- [ ] **Bezpieczeństwo bazowe:** Altman Z'' > 2,6 (strefa bezpieczna) **lub** Piotroski F-Score ≥ 7. Jeśli używasz O-score Ohlsona, sprawdź najpierw w dokumentacji serwisu, czy podaje surowy score, czy prawdopodobieństwo — progi są nieporównywalne (sekcja 3.8).
- [ ] **Cykl konwersji gotówki:** stabilny lub malejący; rosnący DSO przy płaskiej sprzedaży = stop (sekcja 3.6).

#### 3. Wycena
*Czy nie przepłacamy względem historycznych mnożników i czy mamy margines bezpieczeństwa?*
- [ ] **P/E:** < mediana 3y.
- [ ] **P/S:** < mediana 5y.
- [ ] **P/FCF:** < mediana 3y.
- [ ] **P/BV:** < mediana 3y.
- [ ] **Upside:** > 20% do wyceny wewnętrznej < mediana.

---

#### Krok 2.1: Zyskowność — zarabianie pieniędzy, dynamika, rozwój
**Pytanie kluczowe:** Czy biznes rośnie w przeliczeniu na jedną akcję i czy ten wzrost zamienia się w gotówkę?

**A. Metryki na akcję (per-share)**

Wszystko liczymy **na akcję**, nie w wartościach bezwzględnych. Powód jest prosty: spółka może podwoić przychody, emitując przy tym trzy razy więcej akcji — i wtedy Twój udział w biznesie realnie się skurczył. Wzrost widoczny w milionach złotych, a niewidoczny na akcję, nie jest wzrostem dla akcjonariusza.

| Metryka | Czego szukamy w Value | Sygnał ostrzegawczy 🚩 |
| --- | --- | --- |
| **RPS** (przychód na akcję) | Stabilny, powtarzalny wzrost — w Value wystarczy tempo zbliżone do nominalnego wzrostu gospodarki | Płaski RPS przy rosnących przychodach ogółem = wzrost kupiony emisją akcji |
| **EPS** (zysk na akcję) | Rośnie co najmniej tak szybko jak RPS; brak lat ze stratą | EPS skacze bez zmiany przychodów — sprawdź jednorazówki (poziomy 7-15 tabeli RZiS) |
| **BVPS** (wartość księgowa na akcję) | Systematyczny wzrost 3-5%/rok z zysków zatrzymanych | Spadek BVPS mimo zysków = rozwodnienie albo wypłata ponad zysk |
| **Liczba akcji** | Stała lub malejąca (skupy) | Trwały wzrost liczby akcji — każdy rok rozwadnia Twój udział |

**Jak czytać wykres:** nanieś RPS i EPS na słupki, a cenę akcji jako linię na tej samej osi czasu. W dobrej spółce Value linia ceny podąża w długim terminie za słupkami. Rozjazd jest informacją: cena rosnąca bez wzrostu RPS/EPS to ekspansja mnożnika (płacisz coraz drożej za to samo), cena stojąca przy rosnących słupkach to potencjalna okazja — i wtedy pytanie brzmi, czego rynek widzi, a Ty nie.

**Przykład dobrej spółki — przychód i zysk na akcję wobec ceny akcji:**

![Wykres słupkowy: przychód na akcję (RPS) i zysk netto na akcję (EPS) spółki DOMDEV wobec linii ceny akcji, lata 2011-2020](image.png)

Słupki RPS i EPS rosną systematycznie przez cały okres, a linia ceny — po okresie stagnacji — nadrabia dystans. To wzorcowy układ: wzrost wartości wyprzedza wzrost kursu, więc wycena po drodze **taniała**.

**B. Rentowność i jej trwałość**

| Wskaźnik | Czego szukamy | Dlaczego |
| --- | --- | --- |
| **ROE** | Stabilne, powyżej 10-15%, bez trendu spadkowego | W Value ważniejsza od poziomu jest **powtarzalność** — jednorazowe 30% mówi mniej niż dziesięć lat po 14% |
| **ROA** | > 5% i stabilne | Kontrola nad ROE: jeśli ROE rośnie, a ROA stoi, cały przyrost pochodzi z dźwigni |
| **Marża operacyjna** | Stabilna — w Value nie wymagamy ekspansji | Spadająca marża przy rosnących przychodach = utrata siły cenowej, czyli erozja fosy |
| **Rozkład DuPont** | Sprawdź, który człon napędza ROE | Zob. sekcja 3.1.2 |

**Przykład dobrej spółki — ROE i ROA:**

![Wykres słupkowy: ROE i ROA spółki DOMDEV wraz ze średnim ROE od 2011 roku, lata 2011-2020](image-1.png)

Linia średniego ROE pokazuje to, o co chodzi w Value: rozrzut wokół średniej jest wąski, a słupki nie schodzą poniżej progu w żadnym roku — także w latach słabszej koniunktury.

**C. Zamiana zysku na gotówkę**

Najważniejszy pojedynczy test na tym etapie:

$$
cash\ conversion = \frac{CFO}{net\ profit}
$$

Relacja trwale **powyżej 1,0** oznacza, że zysk księgowy jest z nawiązką pokryty gotówką (amortyzacja jest kosztem niegotówkowym, więc w zdrowej spółce CFO powinno przewyższać zysk netto). Relacja utrzymująca się **poniżej 0,8** przez kilka lat to sygnał, że zysk powstaje w memoriale, a nie w kasie — wtedy wracasz do sekcji 3.6 i sprawdzasz DSO oraz DIO.

---

#### Krok 2.2: Fundamenty — bezpieczeństwo finansowe (płynność, dług, przepływy)
**Pytanie kluczowe:** Czy firma jest stabilna finansowo i potrafi spłacać długi z operacyjnej gotówki?

| Wskaźnik | Co sprawdzamy | Interpretacja | Sygnał pozytywny |
| --- | --- | --- | --- |
| **Zobowiązania na akcję (Liabilities/Share)** | Trend zadłużania per akcja | Pozwala błyskawicznie wychwycić, w jakim stopniu działalność spółki jest napędzana rosnącym cudzym kapitałem. W przypadku "Value" silnie pożądana jest powolna ewolucja bez nakręcania luki kredytowej. | Stabilne lub malejące zobowiązania p/s |
| **Relacja BVPS do Zobowiązań p/s** | Budowa majątku względem długu | Zestawienie Wartości księgowej na akcję (BVPS) i Zobowiązań. | BVPS konsekwentnie rośnie szybciej niż linia zobowiązań |
| **Struktura Przepływów (Cash Flow)** | Jak gotówka rzeźbi biznes | Zysk giełdowy (EPS) to zapis księgowy oparty o marże, ale to gotówka (Cash) pozwala przetrwać zimę. Patrzysz, czy rosnący biznes nie "spala gotówki". | Układ operacyjnej, dojrzałej Value: `+ - -` (Zarabia, Reinwestuje, Oddaje dług/dywidendę). |



**Przykład neutralnej spółki — majątek wobec zobowiązań:**

![Wykres słupkowy: wartość księgowa na akcję (BVPS), zobowiązania na akcję i cena akcji spółki KERNEL, lata 2011-2020](image-2.png)

Układ neutralny, a nie zły: BVPS rośnie, ale zobowiązania na akcję rosną w podobnym tempie. Majątek przyrasta więc w dużej mierze za cudze pieniądze — w Value oczekiwalibyśmy, że odstęp między liniami się **powiększa**, a nie utrzymuje.

**Przykład neutralnej spółki — struktura przepływów:**

![Wykres skumulowany: przepływy operacyjne, inwestycyjne i finansowe na akcję spółki FAMUR, lata 2011-2020](image-3.png)

Tu patrzymy wyłącznie na znaki i ich trwałość. Lata z układem `+ - -` to okresy zdrowe; lata, w których finansowanie robi się dodatnie przy słabej operacyjnej, są dokładnie tymi, które trzeba wyjaśnić w Etapie 3 (Krok 3.2).

---

#### Krok 2.3: Wycena — czy spółka jest historycznie tania?
**Pytanie kluczowe:** Czy płacimy mniej, niż rynek płacił za tę samą spółkę w przeszłości — i czy jest z czego zrobić margines bezpieczeństwa?

W Value punktem odniesienia jest **własna historia spółki**, a nie średnia rynkowa. Spółka o trwale słabszym biznesie „zasługuje" na niższy mnożnik i porównywanie jej do indeksu tylko wprowadza w błąd.

**A. Mnożniki wobec własnej mediany**

| Wskaźnik | Próg | Uwagi |
| --- | --- | --- |
| **C/Z** | < mediana 3-letnia | Odrzuć lata z zyskiem jednorazowym, zanim policzysz medianę |
| **C/S** | < mediana 5-letnia | Najbardziej odporny na księgowość — dobry test kontrolny dla C/Z |
| **C/FCF** | < mediana 3-letnia | Najważniejszy, jeśli spółka wypłaca dywidendę |
| **C/WK** | < mediana 3-letnia | Dla spółek majątkowych; porównaj też z C/WK rzeczowym (P/TBV) |
| **EV/EBIT** | < mediana 3-letnia | Konieczny, jeśli zadłużenie spółki istotnie zmieniło się w analizowanym okresie |

Używaj **mediany, nie średniej** — jeden rok bańki albo paniki potrafi przesunąć średnią o kilkadziesiąt procent.

**B. Dlaczego jest tanio — trzy scenariusze**

Niska wycena wobec własnej historii ma zawsze jakąś przyczynę. Rozstrzygnięcie, która to, jest właściwą treścią tego kroku:

| Scenariusz | Objaw | Co robić |
| --- | --- | --- |
| **Wycena wróciła do normy** — wcześniej było drogo | Mnożnik spadł, fundamenty bez zmian | Sprawdź, czy dzisiejszy poziom to faktycznie okazja, czy tylko koniec przewartościowania |
| **Pogorszenie przejściowe** — jednorazowe zdarzenie, cykl, kurs walutowy | Mnożnik spadł razem z zyskiem, ale bilans i pozycja rynkowa bez zmian | To właściwy przypadek dla Value; przejdź do Etapu 3 |
| **Pułapka wartości** — biznes trwale traci | Mnożnik spada od lat, marża i udział rynkowy razem z nim | Odrzuć; tanio będzie dalej taniało |

**C. Margines bezpieczeństwa**

Dopiero po ustaleniu przyczyny ma sens porównanie ceny z wyceną wewnętrzną. Kryterium ze screenera (**upside > 20%**) jest minimum dla spółki stabilnej; dla spółki cyklicznej albo z jednym dominującym klientem żądaj więcej. Metody liczenia wartości wewnętrznej — DCF, model Gordona, wycena porównawcza i wzór Grahama — są w [`wycena-wewnetrzna.md`](wycena-wewnetrzna.md).

---

### Etap 3: Analiza jakościowa (Due Diligence)

**Cel:** Odsianie pozornie tanich spółek (value traps), zrozumienie anomalii z Etapu 2 i ocena redukcji ryzyka. Szukamy odpowiedzi na pytanie: *Dlaczego rynek wycenia tę spółkę tak tanio?*

#### Krok 3.1: Biznes i Fosa (Moat)
**Pytanie kluczowe:** Na czym spółka zarabia i czy ktoś może jej to łatwo odebrać?

| Element | Co sprawdzamy w raportach | Alarm (Red Flag) 🚩 | Pozytyw (Green Flag) 🟢 |
| --- | --- | --- | --- |
| **Struktura przychodów** | Z jakich segmentów / produktów pochodzi większość marży? | Uzależnienie od 1-2 klientów (>30% przychodów). | Zdywersyfikowany portfel klientów i przychodów. |
| **Cykliczność / Sezonowość** | Wrażliwość na cykle makro (np. deweloperka, surowce, rolnictwo). | Górka cyklu koniunkturalnego (wyniki historycznie u szczytu). | Biznes odporny na recesję, stały powtarzalny popyt. |
| **Przewaga (Moat)** | Bariery wejścia, siła marki, patenty, efekt skali. | Łatwość skopiowania produktu, walka o klienta wyłącznie ceną. | Wysokie koszty zmiany dostawcy (switching costs). |

#### Krok 3.2: Śledztwo księgowe (Wyjaśnianie anomalii)
**Pytanie kluczowe:** Co kryje się za dziwnymi skokami/spadkami historycznych układów finansowych spółki?

| Anomalia ze skanera (Etap 2) | Gdzie szukać odpowiedzi | Interpretacja (na co uważać) |
| --- | --- | --- |
| **Nagły spadek ROE/ROA** | Sprawozdanie zarządu -> czynniki jednorazowe | Odpisy aktualizujące majątek, jednorazowe kary, utrata kluczowego kontraktu, błędy operacyjne. |
| **Spadek Wartości Księgowej na akcję (BVPS)** | Noty -> Kapitał własny, zmiany liczby akcji | Drastyczny spadek z zyskami często oznacza **rozwodnienie kapitału** (ogromna emisja nowych akcji). |
| **Mocno ujemny Cash Flow r/r przy zyskach Netto** | Rachunek Cash Flow -> Zmiany kapitału obrotowego | Spółka wykazuje „papierowy zysk”, ale nie potrafi ściągnąć należności od klientów rezygnując z płynności. |
| **Błędy/zaskoczenia w przepływach Finansowych** | Noty -> Struktura i rolowanie długu | Zaciąganie drogiego długu na ratowanie płynności zamiast na produktywne inwestycje/akwizycje. |

#### Krok 3.3: Zarząd i Akcjonariat (Governance)
**Pytanie kluczowe:** Czy zarząd traktuje kapitał drobnych akcjonariuszy z szacunkiem i realizuje cele spółki?

| Kryterium | Co analizujemy | Sygnał ostrzegawczy 🚩 | Sygnał pozytywny 🟢 |
| --- | --- | --- | --- |
| **Skin in the game** | Akcje posiadane przez zarząd/założycieli | Brak udziałów własnych, częste „sypanie” (sprzedawanie) akcjami przez insiderów przy górkach. | Dokupywanie akcji na dołkach bezpośrednio przez zarząd. |
| **Struktura właścicielska** | Kto ostatecznie sprawuje władzę po walnym | Silny dominujący holding transferujący zyski bokiem (transakcje powiązane bez biznesowego sensu). | Zrównoważony akcjonariat i założyciel z długoterminową i realną wizją. |
| **Polityka dywidendowa** | Metoda wypłaty gotówki | Brak zasady, dywidendy powzięte w wyniku kredytu pod zastaw, wypłaty z jednorazowego zastrzyku gotówki. | Ustalony, znany % stabilnie pozyskiwany wyłącznie w strefie FCF (wolnych gotówkowych przepływów). |

#### Krok 3.4: Katalizatory i warunki unieważnienia tezy
**Pytanie kluczowe:** Co konkretnie ma sprawić, że rynek zmieni zdanie — i po czym poznam, że się myliłem?

Tani i dobry biznes może być tani i dobry przez pięć lat. Teza Value bez katalizatora to zakład o cierpliwość; teza bez warunków unieważnienia to zaproszenie do trzymania spadającej spółki w nieskończoność.

| Element | Co zapisać przed kupnem |
| --- | --- |
| **Katalizator** | Konkretne zdarzenie, które ma odblokować wycenę: wyjście ze stratnego segmentu, koniec cyklu inwestycyjnego (CAPEX wraca do amortyzacji), spłata długu poniżej progu kowenantu, rozpoczęcie skupu akcji, zmiana w akcjonariacie, powrót dywidendy. „Rynek w końcu zauważy" nie jest katalizatorem. |
| **Horyzont** | W jakim czasie katalizator ma zadziałać i co zrobisz, jeśli nie zadziała. |
| **Warunki unieważnienia** | 2-4 **obserwowalne** zdarzenia, po których teza jest martwa niezależnie od kursu: marża brutto spada poniżej X przez dwa kwartały, Net Debt/EBITDA przekracza kowenant, odejście kluczowego klienta, emisja rozwadniająca, rezygnacja audytora, zmiana polityki dywidendowej. |
| **Czego nie wiem** | Lista otwartych pytań i założeń, których nie udało się zweryfikować. To ona decyduje o wielkości pozycji. |
| **Argumenty strony przeciwnej** | Najlepszy powód, żeby **nie** kupować, sformułowany uczciwie. Jeśli nie potrafisz go napisać, nie rozumiesz jeszcze tej spółki. |

Całość zapisz **przed** zakupem — po fakcie pamięć dopasowuje uzasadnienie do wyniku. To jest treść dokumentu w `journal/`, a przy zamknięciu pozycji podstawa post-mortemu.

> **Złota reguła inwestora:** Decyzje oprzyj na twardych liczbach, rachunku CF (gotówka nie kłamie) i uwagach audytora, a nie medialnym „story”. Weryfikuj tezę poszukując powodów dlaczego masz spółki **NIE KUPOWAĆ** (ogranicz *confirmation bias*).

</details>

---

<details open>
<summary>

## 4.2. Analiza firm typu Growth

</summary>

**Filozofia growth investing** koncentruje się na spółkach o wysokim potencjale wzrostu przychodów i ekspansji rynkowej. W przeciwieństwie do value investing, akceptujemy wyższe mnożniki wyceny (P/E, P/S), jeśli wzrost jest trwały i ma fundamentalne podstawy. Kluczowe są: TAM (Total Addressable Market), przewaga konkurencyjna, reinwestycja FCF w rozwój oraz quality of growth (rentowność marż wraz ze skalą).

**Dwa podejścia do growth:**

1. **Mocne fundamenty (Quality Growth)** — spółki z udowodnionym wzrostem przychodów, poprawą rentowności, dodatnim lub rosnącym CFO; inwestycja średnio/długoterminowa.
2. **Wczesna faza / pre-profit (Emerging Growth)** — spółki jeszcze nierentowne, których teza opiera się na wielkości rynku (TAM), tempie wzrostu przychodów i widocznej ścieżce do rentowności; inwestycja obarczona ryzykiem finansowania, wymagająca mniejszej pozycji.

| | Quality Growth | Emerging Growth |
| --- | --- | --- |
| **Wzrost przychodów** | 15-30% rocznie, powtarzalny | > 30%, ale zmienny |
| **Rentowność** | Dodatnia, marże rosną ze skalą | Ujemna, strata maleje r/r |
| **CFO** | Dodatni i rosnący | Ujemny — kluczowy jest **runway** (ile kwartałów gotówki zostało) |
| **Główne ryzyko** | Przepłacenie — kompresja mnożnika przy pierwszym spowolnieniu | Wyczerpanie gotówki i emisja rozwadniająca po niskim kursie |
| **Mnożnik** | P/E, forward P/E, PEG | EV/Sales; P/E nie ma zastosowania |
| **Test przetrwania** | Net Debt/EBITDA, ICR | Runway > 2 lata **bez** nowego finansowania |

Dalsza część rozdziału opisuje ścieżkę Quality Growth; różnice dla pre-profit zaznaczone są osobno.

**Plan analizy growth investing (3 etapy):**

1. **Etap 1: Skan i wstępna selekcja spółek** — automatyczny screening na dynamikę wzrostu.
2. **Etap 2: Wstępna analiza historyczna** — weryfikacja trwałości wzrostu, rentowności i przepływów z 3-5 lat.
3. **Etap 3: Analiza jakościowa** — ocena TAM, moat, reinwestycji kapitału, ryzyk i katalizatorów wzrostu.

---

### Etap 1 (Growth): Skan i wstępna selekcja spółek

**Cel:** Znaleźć spółki o udowodnionym wzroście przychodów i zysków, które nie są jeszcze „gigantami" (mają przestrzeń do dalszej ekspansji).

#### Parametry screenera (Growth)

| Kryterium | Wartość graniczna | Uzasadnienie |
| --- | --- | --- |
| **Kapitalizacja** | < 1 mld PLN (GPW) / < 5 mld USD (USA) | Średnie przedsiębiorstwa — dynamika wzrostu łatwiejsza do utrzymania niż u gigantów. |
| **Przychody dynamika 4Q r/r** | > 15% | Bieżące tempo wzrostu — wzrost musi być aktualny, nie tylko historyczny. |
| **Przychody CAGR 3 lata** | > 13% | Średnioterminowa konsekwencja wzrostu — unikamy jednorazowych skoków. |
| **Przychody CAGR 5 lat** | > 10% | Długoterminowa konsekwencja wzrostu — weryfikacja trwałości trendu. |
| **Zysk ze sprzedaży dynamika 4Q r/r** | > 12% | Wzrost zysku operacyjnego (nie tylko top-line) — weryfikacja, że biznes skaluje się rentownie. |
| **Zysk ze sprzedaży CAGR 3 lata** | > 13% | Poprawa rentowności wraz ze wzrostem — sygnał korzyści skali. |
| **Zysk ze sprzedaży CAGR 5 lat** | > 8% | Długoterminowa poprawa marż operacyjnych. |
| **CFO** | Opcjonalnie: już dodatnie lub rosnące | Dla dojrzalszych growth — gotówka operacyjna powinna w końcu być dodatnia. |

**Uwaga:** Dla spółek **pre-profit** (jeszcze nierentownych) akceptujemy ujemny zysk netto, jeśli:
- Strata rok do roku maleje (ścieżka do rentowności widoczna),
- Przychody rosną szybciej niż koszty (operating leverage),
- Spółka ma dość gotówki na utrzymanie działalności (runway > 2 lata).

---

### Etap 2 (Growth): Wstępna analiza historyczna (eliminacja)

Po przejściu screenera analizujemy **trendy historyczne** w trzech wymiarach, z naciskiem na wzrost i skalowanie biznesu:

1. **Zyskowność i wzrost** — tempo przychodów, ekspansja marż, efektywność kapitału.
2. **Fundamenty** — płynność, zadłużenie, przepływy gotówki (czy wzrost jest zrównoważony).
3. **Wycena** — relatywna ocena mnożników w kontekście wzrostu (PEG ratio, P/S).

---

#### Krok 2.1 (Growth): Zyskowność i wzrost — tempo, skala, ekspansja marż
**Pytanie kluczowe:** Czy przychody rosną stabilnie, czy marże się poprawiają wraz ze skalą, czy kapitał jest efektywnie reinwestowany?

**A. Metryki wzrostu na akcję (per-share)**

Analogicznie jak w [Value (4.1 Krok 2.1A)](#krok-21-zyskowność--zarabianie-pieniędzy-dynamika-rozwój), ale z wyższymi wymaganiami:
- **RPS:** CAGR > 15% przez 3+ lata (vs stabilny wzrost w Value)
- **EPS:** Akceptujemy ujemny EPS jeśli strata maleje r/r; dla rentownych EPS rośnie szybciej niż RPS
- **BVPS:** Wzrost min. 10%/rok (vs 3-5% w Value)

**Przykład dobrej spółki growth:**

![Wykres słupkowy: przychód na akcję (RPS) i zysk netto na akcję (EPS) spółki MPLVERBUM wobec linii ceny akcji, lata 2012-Q2 2021](image-4.png)

**B. Rentowność i ekspansja marż (operating leverage)**

**Koncepcja jak w [Value](#krok-21-zyskowność--zarabianie-pieniędzy-dynamika-rozwój),** ale dla growth kluczowa jest **ekspansja marż** (biznes powinien skalować się — marże rosną wraz z przychodami):

| Wskaźnik | Czego szukamy w growth | Sygnał pozytywny |
| --- | --- | --- |
| **Marża brutto** | Rosnąca = pricing power, przewaga produktowa | ↑ Wzrost lub stabilność >40% |
| **Marża operacyjna (EBIT)** | **Kluczowe:** poprawa marży przy wzroście przychodów = korzyści skali | ↑ Wzrost marży wraz z przychodami |
| **Marża netto** | Nawet jeśli ujemna, powinna rosnąć w czasie | ↑ Poprawa lub już dodatnia i rosnąca |
| **ROE / ROIC** | Wysoki ROIC (>15%) = kapitał produktywnie użyty | ↑ ROIC > WACC; ROE rośnie |

**C. Tempo wzrostu i akceleracja**
| Metryka | Co analizujemy | Interpretacja | Sygnał pozytywny |
| --- | --- | --- | --- |
| **CAGR przychodów vs CAGR zysków** | Porównanie 3-5 lat | Zyski rosnące szybciej = korzyści skali, poprawa marż. | ↑ CAGR zysków ≥ CAGR przychodów |
| **Kwartalna akceleracja (q/q i r/r)** | Ostatnie 4-6 kwartałów | Przyspieszenie wzrostu = momentum, spółka wchodzi w nową fazę. Beat & raise w guidance. | ↑ Przyspieszające tempo r/r |
| **Revenue surprise / EPS surprise** | Porównanie raportów z konsensusem | Regularnie bije oczekiwania = silny execution. | ↑ Pozytywne zaskoczenia >50% kwartałów |

---

#### Krok 2.2 (Growth): Fundamenty — bezpieczeństwo finansowe
**Pytanie kluczowe:** Czy firma ma dość zasobów na finansowanie wzrostu? Czy wzrost jest organiczny czy napędzany długiem?

**A. Zadłużenie i płynność**

Logika analizy podobna jak w [Value (4.1 Krok 2.2)](#krok-22-fundamenty--bezpieczeństwo-finansowe-płynność-dług-przepływy), ale z różnymi akceptowalnymi progami:

| Wskaźnik | Różnice vs Value | Sygnał pozytywny Growth |
| --- | --- | --- |
| **Zobowiązania na akcję** | Akceptujemy rosnący dług, jeśli służy produktywnym inwestycjom (CAPEX, R&D, M&A), nie ratowaniu płynności. | Rosnące wolniej niż BVPS |
| **Net Debt / EBITDA** | Tylko dla rentownych growth: <3 OK, >4 ryzyko. Dla pre-profit nie stosujemy. | <2 LUB net cash |
| **Current Ratio (CR)** | Mniej krytyczne niż w value, ale CR <1 = alarm. | >1,5 |

**B. Struktura przepływów (Cash Flow)**

Logika jak w [Value (4.1 Krok 2.2 Cash Flow)](#krok-22-fundamenty--bezpieczeństwo-finansowe-płynność-dług-przepływy), ale **różne akceptowalne wzorce** dla growth:

| Wskaźnik | Różnice vs Value | Sygnał pozytywny Growth |
| --- | --- | --- |
| **CFO** | Dla early-stage: **ujemny CFO OK**, jeśli poprawia się r/r. Dla dojrzałych: dodatni i rosnący. | CFO dodatnie i rosnące LUB ujemne z poprawą r/r |
| **Cash Flow Pattern** | Dojrzały growth: `+ - -` / Early growth: `- - +` (spala gotówkę, inwestuje, funding) | Early: `- - +` z poprawą CFO |

---

#### Krok 2.3 (Growth): Wycena — relatywna i w kontekście wzrostu
**Pytanie kluczowe:** Czy płacimy rozsądną cenę za wzrost? Czy mnożniki są uzasadnione tempem ekspansji?

**A. Mnożniki rynkowe**

**Różnica kluczowa vs Value:** Dla growth akceptujemy **wyższe mnożniki**, jeśli wzrost jest szybki i trwały. Używamy innych wskaźników (PEG, P/S, EV/Sales).

| Wskaźnik | Kiedy stosować | Benchmark Growth |
| --- | --- | --- |
| **P/E (C/Z)** | Dla rentownych growth | <30 przy wzroście EPS >20%/rok |
| **Forward P/E** | Lepsze niż trailing P/E (odzwierciedla przyszły wzrost) | <25 przy silnym guidance |
| **PEG Ratio** | P/E / wzrost EPS (%) — **kluczowy dla growth** | <1,5 (idealnie <1) |
| **P/S** | Dla pre-profit growth | <10 przy wzroście przychodów >25% |
| **EV/Sales** | Lepsze niż P/S (uwzględnia dług/gotówkę) | <8 przy wzroście >20% |

**B. Wycena vs historia**

Podobnie jak w [Value (4.1 Krok 2.3)](#krok-23-wycena--czy-spółka-jest-historycznie-tania), ale dla growth:
- Cena akcji — szukamy korekty po rajdzie (dolny 50-percentyl historii)
- P/E może być wyższy niż średnia branży (maks. 1,5× przy silnym wzroście)
- **Momentum cenowe:** dla momentum growth RSI 50-70 (unikaj >80)

---

### Etap 3 (Growth): Analiza jakościowa (Due Diligence)

**Cel:** Ustalić, czy wzrost z Etapu 2 ma źródło, które przetrwa kolejne 3-5 lat. W Value pytamy „dlaczego jest tanio"; w Growth pytanie brzmi: **„dlaczego ten wzrost ma trwać i dlaczego konkurencja go nie zabierze"**.

#### Krok 3.1 (Growth): Rynek i źródło wzrostu
**Pytanie kluczowe:** Skąd biorą się nowe przychody i czy jest jeszcze gdzie rosnąć?

| Element | Co sprawdzamy | Alarm 🚩 | Pozytyw 🟢 |
| --- | --- | --- | --- |
| **TAM** (Total Addressable Market) | Wielkość rynku i dotychczasowa penetracja | TAM liczony „z prezentacji" metodą top-down (1% ogromnego rynku); spółka ma już większość swojego rynku | TAM policzony bottom-up (liczba klientów × realny przychód na klienta); penetracja wciąż jednocyfrowa |
| **Dekompozycja wzrostu** | Ile wzrostu pochodzi z nowych klientów, ile z podwyżek cen, ile z przejęć | Wzrost głównie z akwizycji — to nie ten sam biznes co rok temu, a goodwill rośnie | Przewaga wzrostu organicznego; przejęcia jako dodatek |
| **Wzrost geograficzny** | Czy model przenosi się na nowe rynki | Ekspansja zagraniczna z marżą niższą niż w kraju i bez skali | Powtarzalny schemat wejścia, rentowny po znanym czasie |
| **Koncentracja** | Udział największych klientów i kanałów | Jeden klient lub jedna platforma > 30% przychodów | Rozproszona baza, długie umowy |

#### Krok 3.2 (Growth): Unit economics i jakość wzrostu
**Pytanie kluczowe:** Czy pojedynczy klient jest rentowny — i czy robi się bardziej rentowny ze skalą?

Wzrost przychodów kupiony poniżej kosztu pozyskania to nie wzrost, tylko dotowanie klientów.

| Miara | Co mówi | Punkt odniesienia |
| --- | --- | --- |
| **Marża brutto** | Ile zostaje na pokrycie kosztów pozyskania klienta i rozwoju | Trend ważniejszy od poziomu; spadająca marża brutto przy rosnących przychodach to najgorszy możliwy układ w growth |
| **Retencja / churn** (modele subskrypcyjne) | Czy klient zostaje | Retencja przychodowa powyżej 100% oznacza, że stara baza sama rośnie — wtedy nowa sprzedaż jest czystym dodatkiem |
| **Koszt pozyskania vs wartość klienta** | Czy sprzedaż się zwraca | Szacuj okres zwrotu w miesiącach; im dłuższy, tym bardziej spółka zależy od finansowania |
| **Dźwignia operacyjna** | Czy koszty stałe rosną wolniej niż przychody | Udział kosztów sprzedaży i zarządu w przychodach powinien **maleć** rok do roku |
| **ROIC na nowym kapitale** | Czy reinwestycja tworzy wartość | ROIC > WACC (sekcja 3.1.3). Bez tego szybki wzrost niszczy wartość tym szybciej, im szybciej rośnie |

#### Krok 3.3 (Growth): Fosa, konkurencja i ryzyko finansowania
**Pytanie kluczowe:** Co powstrzymuje konkurenta z większym kapitałem — i co się stanie, gdy zamknie się okno finansowania?

| Element | Alarm 🚩 | Pozytyw 🟢 |
| --- | --- | --- |
| **Bariera wejścia** | Przewaga oparta wyłącznie na tempie i kapitale; produkt do skopiowania w rok | Efekty sieciowe, koszty zmiany dostawcy, dane lub regulacja po stronie spółki |
| **Reakcja konkurencji** | Wejście dużego gracza z darmową wersją tego samego | Spółka podnosi ceny i nie traci klientów — dowód na siłę cenową |
| **Rozwodnienie** | Liczba akcji rośnie o kilka procent rocznie; duża część wynagrodzeń w akcjach (SBC) maskowana w „adjusted" wynikach | Stabilna liczba akcji; SBC ujmowane wprost i mieszczące się w marży |
| **Runway** (pre-profit) | Gotówka na mniej niż 4 kwartały przy obecnym tempie spalania | Runway > 2 lata bez nowego finansowania, albo dostęp do niewykorzystanych linii |
| **Zarząd** | Guidance regularnie rewidowany w dół; założyciel sprzedaje akcje przy szczytach | Powtarzalne „beat & raise"; założyciel dokupuje |

Mechanika rozwodnienia i wynagrodzeń w akcjach — istotna zwłaszcza dla spółek z USA — jest rozwinięta w [`jakosc-zysku.md`](jakosc-zysku.md).

#### Krok 3.4 (Growth): Warunki unieważnienia tezy

Jak w [Value (Krok 3.4)](#krok-34-katalizatory-i-warunki-unieważnienia-tezy), ale wyzwalacze są inne. W growth teza umiera nie wtedy, gdy kurs spada, lecz gdy **przestaje działać mechanizm wzrostu**:

- dynamika przychodów r/r spada poniżej progu tezy w dwóch kolejnych kwartałach,
- marża brutto spada mimo rosnących przychodów (brak dźwigni operacyjnej),
- retencja schodzi poniżej progu — baza przestaje się sama bronić,
- liczba akcji rośnie szybciej, niż zakładałeś, albo pojawia się emisja po kursie niższym niż Twój,
- zarząd obniża guidance drugi raz z rzędu.

Osobno zapisz, **jakiego mnożnika użyjesz do wyjścia**. Największa część strat w growth nie bierze się ze spadku zysków, tylko z kompresji mnożnika: te same wyniki wyceniane C/Z 40 zamiast 60 to −33% bez żadnej zmiany w biznesie.

---

**Złota reguła growth investora:** Płacimy za przyszły wzrost, nie za przeszłość. Weryfikuj, czy **źródło wzrostu jest trwałe** (TAM, moat, unit economics), czy **zarząd umie wykonywać** (beat & raise, ROIC), i czy **wycena jest uzasadniona tempem** (PEG <2). Unikaj pułapki *hype bez fundamentów* — narracja musi być poparta liczbami (przychody, marże, CFO).

</details>

</details>

---

<details open>
<summary>

## Źródła

</summary>

Progi i liczby pochodzące z przepisów lub z konkretnych publikacji — z datą weryfikacji. Reguły kciuka z podręczników finansów przedsiębiorstw (progi CR, QR, Cash Ratio, DR, ICR) oznaczone są w tekście jako takie i nie mają pojedynczego źródła.

| Miejsce w tekście | Źródło | Zweryfikowano |
| --- | --- | --- |
| Terminy raportów okresowych (2.1) | Rozporządzenie Ministra Finansów z 6.06.2025 r. w sprawie informacji bieżących i okresowych (Dz.U. 2025 poz. 755); [SEG — raporty okresowe](https://seg.org.pl/regulacje/kategorie/pl-raporty-okresowe) | 2026-09 |
| Amortyzacja wartości firmy wg UoR (2.3.1) | Ustawa o rachunkowości, art. 44b ust. 10 | 2026-09 |
| Obowiązek MSSF dla emitentów (2.5) | Ustawa o rachunkowości, art. 55 ust. 5 oraz art. 45 ust. 1a-1c; rozporządzenie (WE) nr 1606/2002, art. 4 | 2026-09 |
| Kapitał zapasowy — 8% zysku, 1/3 kapitału zakładowego (3.5.1) | Kodeks spółek handlowych, art. 396 § 1 | 2026-09 |
| Altman Z'' dla rynków wschodzących — współczynniki i progi (3.8.1) | E. Altman, model Z''; [opis modelu](https://en.wikipedia.org/wiki/Altman_Z-score) | 2026-09 |
| Ohlson O-score — postać logitowa i punkt odcięcia (3.8.2) | J. Ohlson, *Financial Ratios and the Probabilistic Prediction of Bankruptcy*, Journal of Accounting Research, 1980 | 2026-09 |
| Piotroski F-Score — 9 kryteriów (3.8.3) | J. Piotroski, *Value Investing: The Use of Historical Financial Statement Information*, 2000; [zestawienie kryteriów](https://en.wikipedia.org/wiki/Piotroski_F-score) | 2026-09 |
| Kryteria Grahama dla inwestora defensywnego (4.1) | B. Graham, *The Intelligent Investor*, wyd. 1973, rozdz. 14; [omówienie z liczbami](https://blog.portfolio123.com/a-stock-pickers-guide-to-benjamin-grahams-screening-rules/) | 2026-09 |

</details>
