# Źródła danych i słownik skrótów

_Uzupełnienie do [`investing.md`](investing.md). Ostatnia aktualizacja: 2026-09-19._

---

<details open>
<summary>

## 1. Hierarchia źródeł

</summary>

Zasada porządkująca: **im dalej od emitenta, tym większe ryzyko błędu i tym mniej szczegółów.** Serwisy agregujące są świetne do przesiewania i do wykresów historycznych, ale każda liczba, na której oprzesz decyzję, powinna dać się odnaleźć w raporcie spółki.

| Poziom | Źródło | Do czego |
| --- | --- | --- |
| 1 — pierwotne | Raport okresowy spółki (sprawozdanie + noty + opinia audytora) | Wszystko, co wchodzi do tezy |
| 1 — pierwotne | Raporty bieżące ESPI/EBI | Zdarzenia między raportami: zmiany w akcjonariacie, kowenanty, terminy, transakcje insiderów |
| 2 — półpierwotne | Prezentacje wynikowe, transkrypcje konferencji | Narracja zarządu — do skonfrontowania z liczbami, nie do przyjęcia na wiarę |
| 3 — agregatory | Biznesradar, Stooq, serwisy brokerskie | Screening, szeregi historyczne, wskaźniki pochodne |
| 4 — wtórne | Media, fora, analizy | Wyłącznie do generowania hipotez |

</details>

---

<details open>
<summary>

## 2. GPW i NewConnect

</summary>

| Źródło | Co tam jest | Uwagi |
| --- | --- | --- |
| Strona relacji inwestorskich spółki | Raporty okresowe i bieżące, prezentacje, kalendarium | Pierwsze miejsce, do którego idziesz |
| System ESPI/EBI (dostępny m.in. przez serwisy GPW) | Wszystkie raporty bieżące i okresowe emitentów | Raport o terminach publikacji pojawia się zwykle w styczniu |
| Raport roczny w formacie ESEF (XHTML + iXBRL) | Otagowane maszynowo dane finansowe | Najwygodniejsze źródło do własnych arkuszy |
| KNF | Stanowiska nadzorcze, m.in. kryteria dywidendowe dla banków | Niezbędne przy analizie sektora finansowego |
| KDPW | Zasady rozliczeń, cykl rozliczeniowy | Potrzebne przy ustalaniu daty nabycia prawa do dywidendy |

**Czego szukać w raporcie okresowym, w tej kolejności:** sprawozdanie skonsolidowane → noty (zadłużenie, segmenty, transakcje z podmiotami powiązanymi, rezerwy) → opinia biegłego rewidenta (typ opinii, kluczowe sprawy badania) → sprawozdanie zarządu.

</details>

---

<details open>
<summary>

## 3. Rynek amerykański

</summary>

| Źródło | Co tam jest |
| --- | --- |
| **SEC EDGAR** | Wszystkie raporty: 10-K (roczny), 10-Q (kwartalny), 8-K (bieżący), DEF 14A (proxy — wynagrodzenia zarządu, programy motywacyjne, głosowania), 13F/13D/13G (pozycje dużych inwestorów), formularze 3/4/5 (transakcje insiderów) |
| **Full-text search w EDGAR** | Przeszukiwanie treści wszystkich zgłoszeń — najlepsze narzędzie do wyłapywania wzmianek o ryzykach, klientach, kowenantach |
| Strona IR spółki | Prezentacje, transkrypcje, dane uzupełniające (supplemental) |

Sekcje 10-K, od których warto zacząć: **Item 1A Risk Factors** (ryzyka, ale czytaj, które zmieniły się wobec zeszłego roku — to tam jest sygnał), **Item 7 MD&A** (komentarz zarządu), **Item 8** (sprawozdania i noty).

**DEF 14A** jest najczęściej pomijanym dokumentem, a zawiera odpowiedź na pytanie z Kroku 3.3 przewodnika: od czego zależy wynagrodzenie zarządu. Cel oparty wyłącznie na przychodach albo na „adjusted EBITDA" mówi o spółce więcej niż niejedna prezentacja.

</details>

---

<details open>
<summary>

## 4. Higiena pracy z danymi

</summary>

- **Zawsze zapisuj datę i źródło.** „C/Z = 8,4" bez daty jest bezużyteczne po trzech miesiącach.
- **Sprawdź definicję wskaźnika w serwisie**, zanim porównasz go z własnym wyliczeniem — D/E, dług netto, FCF i O-score bywają liczone na kilka sposobów (sekcje 3.3 i 3.8 przewodnika).
- **Dane skorygowane o splity i prawa poboru** — szeregi cen na akcję muszą być skorygowane, inaczej wykres RPS/EPS vs cena nie ma sensu.
- **Sprawdź, czy dane są skonsolidowane, czy jednostkowe.** Mieszanie ich to najczęstsze źródło rozjazdu między własnym wyliczeniem a serwisem.
- **Waluta raportowania** — część spółek z GPW raportuje w EUR lub USD. Porównanie z kursem akcji w złotych wymaga przeliczenia.
- **Rok obrotowy ≠ kalendarzowy** w części spółek; sprawdź przed liczeniem CAGR.

</details>

---

<details open>
<summary>

## 5. Słownik skrótów

</summary>

### 5.1. Sprawozdawczość

| Skrót | Rozwinięcie | Polski odpowiednik / znaczenie |
| --- | --- | --- |
| RZiS | — | Rachunek zysków i strat (P&L, income statement) |
| CFO / CFI / CFF | Cash Flow from Operating / Investing / Financing Activities | Przepływy operacyjne / inwestycyjne / finansowe |
| COGS | Cost of Goods Sold | Koszt wytworzenia sprzedanych produktów |
| SG&A | Selling, General & Administrative | Koszty sprzedaży oraz ogólnego zarządu |
| D&A | Depreciation & Amortization | Amortyzacja (środków trwałych i wartości niematerialnych) |
| CAPEX | Capital Expenditures | Nakłady inwestycyjne |
| OCI | Other Comprehensive Income | Pozostałe całkowite dochody |
| MSSF / MSR | Międzynarodowe Standardy Sprawozdawczości Finansowej / Rachunkowości (IFRS / IAS) | — |
| UoR | — | Ustawa o rachunkowości |
| KAM | Key Audit Matters | Kluczowe sprawy badania w opinii audytora |
| ESEF | European Single Electronic Format | Format raportów rocznych emitentów (XHTML + iXBRL) |
| SBC | Stock-Based Compensation | Wynagrodzenie w akcjach |

### 5.2. Rentowność i efektywność

| Skrót | Rozwinięcie | Uwagi |
| --- | --- | --- |
| ROE | Return on Equity | Rentowność kapitału własnego |
| ROA | Return on Assets | Rentowność aktywów |
| ROS | Return on Sales | Rentowność sprzedaży netto |
| ROIC | Return on Invested Capital | Zwrot z kapitału zainwestowanego |
| ROCE | Return on Capital Employed | Zwrot z kapitału zaangażowanego (przed podatkiem) |
| EBIT | Earnings Before Interest and Taxes | Zysk operacyjny |
| EBITDA | EBIT + D&A | **Nie jest pozycją MSSF ani US GAAP** |
| NOPAT | Net Operating Profit After Tax | EBIT po opodatkowaniu |
| WACC | Weighted Average Cost of Capital | Średni ważony koszt kapitału |

### 5.3. Płynność, zadłużenie, sprawność

| Skrót | Rozwinięcie |
| --- | --- |
| CR / QR | Current Ratio / Quick Ratio — płynność bieżąca / szybka |
| DR | Debt Ratio — wskaźnik ogólnego zadłużenia |
| D/E | Debt to Equity — zadłużenie do kapitału własnego |
| ICR | Interest Coverage Ratio — pokrycie odsetek |
| ND/EBITDA | Net Debt / EBITDA — dług netto do EBITDA |
| DSO / DIO / DPO | Days Sales Outstanding / Inventory Outstanding / Payables Outstanding — rotacja należności / zapasów / zobowiązań w dniach |
| CCC | Cash Conversion Cycle — cykl konwersji gotówki |

### 5.4. Wycena

| Skrót | Rozwinięcie | Polski skrót |
| --- | --- | --- |
| P/E | Price to Earnings | C/Z |
| P/BV | Price to Book Value | C/WK |
| P/TBV | Price to Tangible Book Value | — |
| P/S | Price to Sales | C/S |
| P/FCF | Price to Free Cash Flow | — |
| CAPE | Cyclically Adjusted P/E | — |
| PEG | Price/Earnings to Growth | — |
| EV | Enterprise Value | Wartość przedsiębiorstwa |
| FCF / FCFF | Free Cash Flow / Free Cash Flow to the Firm | Wolne przepływy pieniężne |
| DCF | Discounted Cash Flow | Zdyskontowane przepływy pieniężne |
| DDM | Dividend Discount Model | Model zdyskontowanych dywidend |
| NAV | Net Asset Value | Wartość aktywów netto |
| FFO / AFFO | Funds From Operations / Adjusted FFO | Miary dla spółek nieruchomościowych |
| SOTP | Sum of the Parts | Wycena sumą części |

### 5.5. Dywidendy, wzrost, pozostałe

| Skrót | Rozwinięcie |
| --- | --- |
| DPS / EPS / RPS / BVPS | Dividend / Earnings / Revenue / Book Value per Share — na akcję |
| DY | Dividend Yield — stopa dywidendy |
| DPR | Dividend Payout Ratio — stopa wypłaty dywidendy |
| CAGR | Compound Annual Growth Rate — średnioroczne tempo wzrostu składanego |
| YoY / QoQ | Year over Year / Quarter over Quarter — rok do roku / kwartał do kwartału |
| TAM | Total Addressable Market — całkowity rynek docelowy |
| WHT | Withholding Tax — podatek u źródła |
| IKE / IKZE / OIPE / OKI | Indywidualne Konto Emerytalne / Zabezpieczenia Emerytalnego / Ogólnoeuropejski Indywidualny Produkt Emerytalny / Osobiste Konto Inwestycyjne |
| ESPI / EBI | Elektroniczny System Przekazywania Informacji / Elektroniczna Baza Informacji — systemy raportów emitentów |

</details>
