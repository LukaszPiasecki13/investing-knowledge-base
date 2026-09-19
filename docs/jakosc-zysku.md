# Jakość zysku, red flagi księgowe i rozwodnienie

_Uzupełnienie do [`investing.md`](investing.md), Część IV. Ostatnia aktualizacja: 2026-09-19._

Zysk netto jest opinią, gotówka jest faktem. Ten dokument zbiera testy, które pozwalają sprawdzić, ile z raportowanego zysku jest realne — oraz dwa mechanizmy, które najczęściej zjadają zwrot akcjonariusza po cichu: rozwodnienie i wynagrodzenie w akcjach.

---

<details open>
<summary>

## 1. Test podstawowy: zysk kontra gotówka

</summary>

Zaczynaj zawsze od jednej relacji:

$$
cash\ conversion = \frac{CFO}{net\ profit}
$$

W zdrowej spółce relacja jest **trwale powyżej 1,0** — amortyzacja jest kosztem niegotówkowym, więc CFO powinno przewyższać zysk netto. Rozjazd w drugą stronę nazywa się **accrualsami** (korekty memoriałowe):

$$
accruals = \frac{net\ profit - CFO}{average\ total\ assets}
$$

Wysokie dodatnie accruals oznaczają, że zysk powstaje z zapisów księgowych, a nie z wpływów. Sam Piotroski uczynił z tego jeden z dziewięciu testów swojego F-Score (CFO > zysk netto).

**Reguła czytania:** jeden rok rozjazdu wyjaśnia się cyklem inwestycyjnym albo sezonowością. **Trzy lata z rzędu** to systematyczna różnica i trzeba znaleźć jej źródło w kapitale obrotowym (sekcja 3.6 przewodnika: DSO, DIO, DPO) albo w polityce rozpoznawania przychodów.

</details>

---

<details open>
<summary>

## 2. Katalog red flag

</summary>

### 2.1. Przychody

| Sygnał 🚩 | Gdzie sprawdzić | Co może oznaczać |
| --- | --- | --- |
| Przychody rosną szybciej niż należności? Odwrotnie — **należności rosną szybciej niż przychody** | Bilans + sekcja 3.6 przewodnika (DSO) | Sprzedaż wypychana do kanału, wydłużone terminy płatności, rozpoznanie przychodu przed realnym odbiorem |
| Skok przychodów w IV kwartale, korekta w I | Raporty kwartalne vs roczny | Domykanie roku pod cele zarządu |
| Duży udział przychodów z kontraktów długoterminowych wycenianych metodą postępu | Noty o przychodach (MSSF 15) | Przychód oparty na szacunku marży kontraktowej — podatny na rewizję |
| Zmiana polityki rozpoznawania przychodów | Nota o zasadach rachunkowości, porównywalność danych | Jednorazowa poprawa wyniku bez zmiany biznesu |

### 2.2. Koszty i marża

| Sygnał 🚩 | Gdzie sprawdzić | Co może oznaczać |
| --- | --- | --- |
| Rosnące **aktywowane prace rozwojowe** przy płaskim CFO | Bilans (WNiP) + CFI | Bieżące koszty przeniesione do aktywów — zysk zawyżony |
| Wydłużenie okresów amortyzacji albo podniesienie wartości rezydualnych | Nota o zasadach rachunkowości, porównanie amortyzacji do majątku | Obniżenie kosztu okresu bez zmiany rzeczywistości |
| CAPEX trwale poniżej amortyzacji | CFI vs RZiS | Spółka nie odtwarza majątku; dzisiejszy FCF jest pożyczony z przyszłości |
| Rozwiązywanie rezerw poprawiające wynik | Nota o rezerwach | Wynik z księgowości, nie z operacji |
| Spadek marży brutto przy rosnących przychodach | RZiS, wariant kalkulacyjny | Utrata siły cenowej — erozja fosy |

### 2.3. Bilans i finansowanie

| Sygnał 🚩 | Gdzie sprawdzić | Co może oznaczać |
| --- | --- | --- |
| Goodwill duży względem kapitału własnego, bez odpisów mimo słabych wyników segmentu | Noty — test na utratę wartości i jego założenia | Odpis odłożony w czasie; sprawdź przyjętą stopę dyskontową i wzrost rezydualny |
| Skokowo rosnący DPO, faktoring odwrotny, „finansowanie łańcucha dostaw" | Noty o zobowiązaniach | Dług ukryty w zobowiązaniach handlowych — nie widać go w Net Debt/EBITDA |
| Zbliżanie się do progu kowenantu | Nota o zadłużeniu | Ryzyko wymuszonej emisji lub sprzedaży aktywów |
| Rolowanie krótkiego długu na coraz gorszych warunkach | Struktura zapadalności w notach | Problem płynności, nie inwestycji |
| Duża pozycja aktywów z tytułu odroczonego podatku | Nota podatkowa | Aktywo istnieje tylko, jeśli spółka będzie miała z czego rozliczyć straty |

### 2.4. Otoczenie i governance

| Sygnał 🚩 | Gdzie sprawdzić | Co może oznaczać |
| --- | --- | --- |
| Zmiana audytora, zwłaszcza w trakcie roku lub po sporze | Raporty bieżące ESPI | Rozbieżność co do ujęcia istotnej pozycji |
| Opinia z zastrzeżeniem, akapit o kontynuacji działalności, obszerne KAM | Opinia biegłego rewidenta | Audytor sygnalizuje to, czego zarząd nie napisał |
| Transakcje z podmiotami powiązanymi bez biznesowego uzasadnienia | Nota o transakcjach z podmiotami powiązanymi | Transfer wartości poza spółkę |
| Rezygnacja CFO lub członka komitetu audytu bez wyjaśnienia | ESPI | Najczęściej lekceważony sygnał wyprzedzający |
| Rosnący rozjazd między wynikiem raportowanym a „adjusted" | Prezentacje wynikowe vs sprawozdanie | Coroczne „jednorazówki" nie są jednorazowe |

> **Zasada nadrzędna:** „adjusted EBITDA", „wynik znormalizowany", „skorygowany EPS" **nie są pozycjami MSSF ani US GAAP**. Każda spółka definiuje je sama i zmienia definicję, kiedy chce. Zawsze przeliczaj drogę od wyniku raportowanego do skorygowanego pozycja po pozycji — a jeśli te same „jednorazówki" wracają trzeci rok z rzędu, to są normalne koszty prowadzenia biznesu.

</details>

---

<details open>
<summary>

## 3. Rozwodnienie i wynagrodzenie w akcjach (SBC)

</summary>

### 3.1. Dlaczego to jest ważniejsze, niż wygląda

Twój udział w spółce to nie liczba akcji, tylko **ułamek** — liczba Twoich akcji podzielona przez wszystkie akcje. Spółka może zwiększać zysk i jednocześnie zmniejszać Twój zysk na akcję, jeśli szybciej zwiększa liczbę akcji. To najcichszy sposób, w jaki wzrost nie dociera do akcjonariusza.

| EPS | Kiedy używać |
| --- | --- |
| **Podstawowy (basic)** | Zysk / średnia ważona liczba akcji w obrocie |
| **Rozwodniony (diluted)** | Uwzględnia akcje, które powstaną z opcji, warrantów i obligacji zamiennych. **To jest liczba, której używasz do C/Z** |

Różnica basic-diluted większa niż kilka procent to informacja sama w sobie: istnieje duży niewykonany program opcyjny, który zmaterializuje się przy wyższym kursie — czyli dokładnie wtedy, gdy Twoja teza zacznie działać.

### 3.2. Wynagrodzenie w akcjach (Stock-Based Compensation)

SBC jest kosztem ujmowanym w RZiS, ale **niegotówkowym** — więc w rachunku przepływów wraca jako korekta dodatnia do CFO. Stąd dwa efekty:

1. **CFO i FCF są zawyżone** o kwotę SBC w stosunku do sytuacji, w której spółka płaciłaby pracownikom gotówką.
2. Wiele spółek (zwłaszcza amerykańskich technologicznych) wyłącza SBC ze swoich metryk „adjusted" — prezentując jako zysk coś, co w rzeczywistości zapłacili Twoim udziałem w firmie.

**Test:** policz FCF pomniejszony o SBC i porównaj go z FCF raportowanym.

$$
FCF_{skorygowany} = CFO - CAPEX - SBC
$$

Jeśli różnica sięga kilkudziesięciu procent, „rentowność" spółki opiera się na rozwadnianiu akcjonariuszy. Sprawdź też, czy spółka prowadzi skup akcji — i czy skupuje **więcej**, niż emituje w programach motywacyjnych, czy tylko neutralizuje rozwodnienie (drugi przypadek bywa przedstawiany jako „zwrot kapitału akcjonariuszom", choć nim nie jest).

### 3.3. Co śledzić rok do roku

- [ ] Liczba akcji rozwodnionych — trend w ujęciu 5-letnim.
- [ ] SBC jako procent przychodów i jako procent CFO.
- [ ] Emisje: po jakim kursie i na co poszły pieniądze.
- [ ] Skup akcji: czy akcje są umarzane, czy trafiają do programów motywacyjnych.
- [ ] Program motywacyjny: od czego zależy przyznanie — od kursu, od EPS, od przychodów? Cel oparty wyłącznie na przychodach zachęca do wzrostu za wszelką cenę.

</details>

---

<details open>
<summary>

## 4. Szybki przebieg kontrolny

</summary>

Dziesięć minut na spółkę, zanim zainwestujesz w nią więcej czasu:

- [ ] CFO / zysk netto w ujęciu 5-letnim — czy trwale powyżej 1,0?
- [ ] DSO i DIO — czy rosną szybciej niż sprzedaż?
- [ ] CAPEX / amortyzacja — czy majątek jest odtwarzany?
- [ ] Goodwill / kapitał własny — jaka skala ryzyka odpisu?
- [ ] Liczba akcji rozwodnionych — trend.
- [ ] Wynik raportowany vs „adjusted" — co dokładnie wyłączono i czy wraca co roku?
- [ ] Opinia audytora — typ opinii, KAM, kontynuacja działalności.
- [ ] Transakcje z podmiotami powiązanymi — czy występują i czy mają sens.

Każde „nie wiem" przy tych punktach jest argumentem za mniejszą pozycją, nie za dalszym szukaniem uzasadnienia.

</details>

---

## Źródła

| Twierdzenie | Źródło | Zweryfikowano |
| --- | --- | --- |
| Test CFO > zysk netto jako miara jakości zysku | J. Piotroski, *Value Investing: The Use of Historical Financial Statement Information*, 2000 (kryterium nr 4 F-Score) | 2026-09 |
| EBITDA i metryki „adjusted" nie są pozycjami MSSF/US GAAP | MSSF (brak definicji EBITDA w standardach); praktyka non-GAAP measures | 2026-09 |
| Ujęcie SBC jako kosztu niegotówkowego korygującego CFO | MSSF 2 / ASC 718 | 2026-09 |
| Rozpoznanie przychodu i metoda postępu | MSSF 15 | 2026-09 |
