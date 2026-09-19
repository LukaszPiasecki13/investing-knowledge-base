# MSSF vs ustawa o rachunkowości — co się zmienia dla czytającego raport

_Uzupełnienie do [`investing.md`](investing.md), sekcja 2.5. Ostatnia aktualizacja: 2026-09-19._

Tabele bilansu i RZiS w przewodniku opisują układ z **ustawy o rachunkowości (UoR)**. Raporty, które faktycznie otwierasz analizując spółkę z GPW, są w większości sporządzone wg **MSSF**. Ten dokument zbiera różnice, które realnie zmieniają odczyt wskaźników.

---

<details open>
<summary>

## 1. Kto co stosuje

</summary>

| Sprawozdanie | Standard | Podstawa |
| --- | --- | --- |
| **Skonsolidowane** emitenta dopuszczonego do obrotu na rynku regulowanym oraz banku | MSR/MSSF — **obowiązkowo** | art. 55 ust. 5 UoR, w wykonaniu art. 4 rozporządzenia (WE) nr 1606/2002 |
| **Jednostkowe** emitenta | MSSF **albo** UoR — decyzja organu zatwierdzającego | art. 45 ust. 1a-1c UoR |
| Spółka z NewConnect bez grupy kapitałowej | najczęściej UoR | — |
| Spółka nienotowana | UoR | — |

Konsekwencja praktyczna: **w jednym raporcie okresowym potrafią współistnieć dwa układy** — skonsolidowany wg MSSF i jednostkowy wg UoR. Analizuj skonsolidowany; jednostkowy jest istotny głównie przy ocenie zdolności dywidendowej (to z zysku jednostkowego spółki dominującej wypłaca się dywidendę).

Format: raporty roczne emitentów publikowane są w **XHTML z tagowaniem iXBRL (ESEF)**. Plik da się otworzyć w przeglądarce, a otagowane dane finansowe wyciągnąć maszynowo — to najwygodniejsze źródło do własnych arkuszy.

</details>

---

<details open>
<summary>

## 2. Nomenklatura — ta sama treść, inne nazwy

</summary>

| UoR | MSSF | Uwagi |
| --- | --- | --- |
| Bilans | Sprawozdanie z sytuacji finansowej | — |
| Rachunek zysków i strat | Sprawozdanie z zysków lub strat / sprawozdanie z całkowitych dochodów | MSSF wymaga pokazania OCI — osobno albo w jednym sprawozdaniu |
| Rachunek przepływów pieniężnych | Sprawozdanie z przepływów pieniężnych | — |
| Zestawienie zmian w kapitale własnym | Sprawozdanie ze zmian w kapitale własnym | — |
| Wartości niematerialne i prawne | Aktywa niematerialne / wartości niematerialne | — |
| Rzeczowe aktywa trwałe | Rzeczowe aktywa trwałe | Dochodzi osobna pozycja: aktywa z tytułu prawa do użytkowania (MSSF 16) |
| Informacja dodatkowa | Noty objaśniające | — |
| Kapitały (własne) | Kapitał własny; osobno **przypadający akcjonariuszom jednostki dominującej** i **udziały niekontrolujące** | To rozróżnienie jest w MSSF wyeksponowane i konieczne do poprawnego C/WK i C/Z |

</details>

---

<details open>
<summary>

## 3. Różnice, które zmieniają wskaźniki

</summary>

### 3.1. Brak „pozostałej działalności operacyjnej"

UoR ma osobne poziomy „pozostałe przychody/koszty operacyjne" (poziomy 7-8 tabeli RZiS w przewodniku). **MSSF takiej kategorii nie zna** — odpisy, zyski ze sprzedaży aktywów, kary i dotacje są rozrzucone po pozycjach funkcyjnych albo pokazane w osobnej linii według uznania spółki.

Skutek: **nie da się mechanicznie odtworzyć „zysku ze sprzedaży"** z raportu MSSF. Jeśli chcesz oddzielić wynik powtarzalny od jednorazówek, musisz przejść przez noty — spółka zwykle sama wylicza „wynik skorygowany", ale to jej definicja, nie standard.

### 3.2. MSSF 16 — leasing (obowiązuje od 2019)

Najpoważniejsza pułapka w szeregach historycznych. Przed MSSF 16 leasing operacyjny był kosztem operacyjnym; od 2019 wchodzi do bilansu jako aktywo z tytułu prawa do użytkowania i zobowiązanie leasingowe, a w RZiS rozpada się na amortyzację i odsetki.

| Wskaźnik | Efekt wprowadzenia MSSF 16 |
| --- | --- |
| EBITDA | **rośnie** — czynsz zniknął z kosztów operacyjnych |
| EBIT | rośnie nieznacznie |
| Dług netto, D/E, Net Debt/EBITDA | **rosną** — pojawia się zobowiązanie leasingowe |
| Aktywa ogółem | rosną → ROA i rotacja aktywów **spadają** |
| CFO | **rośnie** — spłata leasingu przeniosła się do części finansowej |
| FCF liczony jako CFO − CAPEX | rośnie sztucznie, jeśli nie odejmiesz spłaty leasingu |

**Reguła praktyczna:** porównując lata 2018 i 2019 w spółce leasingującej powierzchnię (handel, gastronomia, logistyka, biura), traktuj to jak zmianę jednostki miary, nie jak zmianę wyników. W FCF odejmuj spłatę zobowiązań leasingowych.

### 3.3. Wartość firmy (goodwill)

| | UoR | MSSF |
| --- | --- | --- |
| Dodatnia wartość firmy | Amortyzowana przez okres ekonomicznej użyteczności; gdy nie da się go wiarygodnie oszacować — maks. 5 lat (art. 44b ust. 10) | **Nieamortyzowana**, testowana corocznie na utratę wartości (MSR 36) |
| Ujemna wartość firmy | Rozliczenia międzyokresowe przychodów w pasywach, odnoszona w wynik w czasie | **Od razu w wynik** jako zysk z okazyjnego nabycia (MSSF 3) |

Dla inwestora: pod MSSF goodwill nie obciąża wyniku systematycznie, tylko **skokowo, gdy przyjdzie odpis** — zwykle w najgorszym możliwym momencie cyklu. Duża pozycja goodwill w bilansie to miara ryzyka, nie wartości. Pod UoR odwrotnie: zysk jest co roku obciążony amortyzacją wartości firmy, co zaniża porównywalność z odpowiednikiem raportującym wg MSSF.

### 3.4. Nieruchomości inwestycyjne (MSR 40)

MSSF pozwala wyceniać nieruchomości inwestycyjne w **wartości godziwej**, a zmianę wyceny odnosić **w wynik**. Skutki:

- zysk netto spółki nieruchomościowej może w większości pochodzić z przeszacowania, a nie z czynszów — to zysk **niegotówkowy**,
- C/Z takiej spółki jest mało użyteczne; sensowniejsze są C/WK i porównanie CFO z zyskiem netto,
- w cyklu spadkowym mechanizm działa w drugą stronę i generuje straty bez żadnego wypływu gotówki.

Pod UoR obowiązuje zasadniczo koszt historyczny, więc ten efekt nie występuje.

### 3.5. Prace rozwojowe i marki (MSR 38)

- Koszty **badań** — zawsze w koszty okresu.
- Koszty **prac rozwojowych** — aktywowane, jeśli spełnione są wszystkie warunki (m.in. techniczna wykonalność, zamiar i możliwość ukończenia, prawdopodobne korzyści).
- **Marki, tytuły prasowe, listy klientów wytworzone we własnym zakresie — nie wolno aktywować.** W bilansie mogą znaleźć się tylko takie, które kupiono.

Praktyczne pytanie kontrolne: rosnąca pozycja „koszty prac rozwojowych" w aktywach przy płaskim CFO oznacza, że część bieżących kosztów nie obciąża wyniku. To legalne i czasem uzasadnione, ale zawyża zysk — porównaj dynamikę aktywowanych nakładów z dynamiką przychodów.

### 3.6. Przychody (MSSF 15)

Przychód rozpoznaje się w momencie **przekazania kontroli** nad dobrem lub usługą, w pięciu krokach (identyfikacja umowy, zobowiązań do wykonania świadczenia, ceny transakcyjnej, alokacji, ujęcia). Konsekwencje branżowe:

- **Deweloper mieszkaniowy** — przychód dopiero przy przekazaniu lokalu, a nie przy sprzedaży czy wpłacie. Stąd skokowe, „grudkowate" przychody i zapasy pełne produkcji w toku.
- **Kontrakty długoterminowe (budownictwo)** — przychód w miarę postępu prac, na podstawie szacunków. Szacunki bywają korygowane; rewizja marży kontraktowej to typowe źródło nagłej straty.
- **Subskrypcje** — część wpłat trafia do przychodów przyszłych okresów w zobowiązaniach. Ich wzrost jest dobrym wskaźnikiem wyprzedzającym.

### 3.7. Instrumenty finansowe (MSSF 9)

Odpisy na należności i kredyty liczy się metodą **oczekiwanych strat kredytowych** — czyli zawczasu, na podstawie modelu, a nie dopiero po stwierdzeniu niewypłacalności. W bankach to główny mechanizm kształtujący koszt ryzyka i główny obszar uznaniowości zarządu.

</details>

---

<details open>
<summary>

## 4. Checklist przy pierwszym otwarciu raportu

</summary>

- [ ] Który to standard — MSSF czy UoR? Czy skonsolidowany, czy jednostkowy?
- [ ] Wariant RZiS: kalkulacyjny (jest marża brutto) czy porównawczy (nie ma)?
- [ ] Czy zysk netto jest rozbity na przypadający jednostce dominującej i udziały niekontrolujące? Do wskaźników bierz pierwszy.
- [ ] Czy w bilansie są aktywa z tytułu prawa do użytkowania i zobowiązania leasingowe (MSSF 16)? Jeśli porównujesz z okresem sprzed 2019 — uwaga na nieporównywalność.
- [ ] Jak duży jest goodwill względem kapitału własnego? Czy w notach jest test na utratę wartości i jakie przyjęto założenia (stopa dyskontowa, wzrost rezydualny)?
- [ ] Czy w wyniku siedzi przeszacowanie nieruchomości albo bargain purchase? Porównaj zysk netto z CFO.
- [ ] Czy spółka publikuje wynik „skorygowany"? Jaką definicję przyjęła i co dokładnie wyłączyła?

</details>

---

## Źródła

| Twierdzenie | Źródło | Zweryfikowano |
| --- | --- | --- |
| Obowiązek MSSF dla skonsolidowanych sprawozdań emitentów i banków | Ustawa o rachunkowości, art. 55 ust. 5; rozporządzenie (WE) nr 1606/2002, art. 4 | 2026-09 |
| Możliwość wyboru MSSF dla sprawozdania jednostkowego | Ustawa o rachunkowości, art. 45 ust. 1a-1c | 2026-09 |
| Amortyzacja wartości firmy wg UoR | Ustawa o rachunkowości, art. 44b ust. 10 | 2026-09 |
| Traktowanie goodwill, ujemnej wartości firmy, leasingu, przychodów, aktywów niematerialnych | MSSF 3, MSSF 15, MSSF 16, MSR 36, MSR 38, MSR 40, MSSF 9 | 2026-09 |
