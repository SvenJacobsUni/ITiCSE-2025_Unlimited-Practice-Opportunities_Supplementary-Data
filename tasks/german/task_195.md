# Input
- Programmierkonzept: If-Else-Anweisungen;Boolean und None;Funktionen als Variablen
- Kontext: Restaurant

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Restaurant-Bestellung

Schreibe eine Funktion namens `bestellung_aufnehmen(bestellung)`, die eine Bestellung in einem Restaurant entgegennimmt und eine entsprechende Nachricht zurückgibt. Die Funktion soll folgende Bedingungen prüfen:

1. Wenn die Bestellung "Pizza" ist, soll die Nachricht "Ihre Pizza wird zubereitet." zurückgegeben werden.
2. Wenn die Bestellung "Pasta" ist, soll die Nachricht "Ihre Pasta wird zubereitet." zurückgegeben werden.
3. Wenn die Bestellung "Salat" ist, soll die Nachricht "Ihr Salat wird zubereitet." zurückgegeben werden.
4. Für alle anderen Bestellungen soll die Nachricht "Diese Bestellung ist leider nicht verfügbar." zurückgegeben werden.

Beispielaufrufe:
- `bestellung_aufnehmen("Pizza")` gibt "Ihre Pizza wird zubereitet." zurück.
- `bestellung_aufnehmen("Burger")` gibt "Diese Bestellung ist leider nicht verfügbar." zurück.

## Codegerüst
```python
def bestellung_aufnehmen(bestellung):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bestellung_aufnehmen(bestellung):
    if bestellung == "Pizza":
        return "Ihre Pizza wird zubereitet."
    elif bestellung == "Pasta":
        return "Ihre Pasta wird zubereitet."
    elif bestellung == "Salat":
        return "Ihr Salat wird zubereitet."
    else:
        return "Diese Bestellung ist leider nicht verfügbar."

# Beispielaufrufe
print(bestellung_aufnehmen("Pizza"))
print(bestellung_aufnehmen("Burger"))
```

## Unit Tests
```python
import unittest
from main import bestellung_aufnehmen

class TestBestellungAufnehmen(unittest.TestCase):
    def test_pizza_bestellung(self):
        self.assertEqual(bestellung_aufnehmen("Pizza"), "Ihre Pizza wird zubereitet.")

    def test_pasta_bestellung(self):
        self.assertEqual(bestellung_aufnehmen("Pasta"), "Ihre Pasta wird zubereitet.")

    def test_salat_bestellung(self):
        self.assertEqual(bestellung_aufnehmen("Salat"), "Ihr Salat wird zubereitet.")

    def test_unverfuegbare_bestellung(self):
        self.assertEqual(bestellung_aufnehmen("Burger"), "Diese Bestellung ist leider nicht verfügbar.")

    def test_leere_bestellung(self):
        self.assertEqual(bestellung_aufnehmen(""), "Diese Bestellung ist leider nicht verfügbar.")

    def test_null_bestellung(self):
        self.assertEqual(bestellung_aufnehmen(None), "Diese Bestellung ist leider nicht verfügbar.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 627
