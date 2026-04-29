# Tax Calculators

Kalkulator wynagrodzeń dla umów zlecenia w Polsce.

## Funkcje

- **Brutto → Netto** — ile pracownik dostanie na rękę
- **Netto → Brutto** — ile wpisać w umowę przy oczekiwanym netto
- **Koszt firmy** — całkowity koszt pracodawcy ponad brutto

## Obsługiwane przypadki

| Przypadek | Opis |
|---|---|
| Zwykły pracownik | Wszystkie składki + podatek 12% |
| Poniżej 26 lat | Składki ZUS, brak podatku |
| Student | Brak składek i podatku (brutto = netto) |
| Bez chorobowej | Bez dobrowolnej składki 2,45% |

## Stawki (aktualne)

| Składka | Stawka |
|---|---|
| Emerytalna | 9,76% |
| Rentowa | 1,50% |
| Chorobowa | 2,45% |
| Zdrowotna | 9,00% |
| Składki firmy | 20,48% |
| Podatek (I próg) | 12% |
| KUP | 20% |

## Użycie

```js
// Ile dostanę na rękę?
obliczNetto(6000)                        // zwykły pracownik
obliczNetto(6000, false, true)           // poniżej 26 lat
obliczNetto(6000, true)                  // student
obliczNetto(6000, false, false, false)   // bez chorobowej

// Ile wpisać w umowę?
obliczBrutto(5000)                       // chcę 5000 netto

// Ile kosztuje pracodawcę?
obliczKosztFirmy(6000)
```

## Uruchomienie

```bash
node tax_calculator.js
```
