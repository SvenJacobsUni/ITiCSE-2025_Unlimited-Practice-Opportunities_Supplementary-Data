# Input
- Programmierkonzept: Float
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Zutatenmengen berechnen

Schreibe eine Funktion namens `berechne_zutatenmenge(anzahl_personen)`, die die benötigte Menge einer Zutat für ein Rezept berechnet. Das Rezept ist für 4 Personen ausgelegt und benötigt 250.0 Gramm Mehl. Die Funktion soll die benötigte Menge Mehl für die angegebene Anzahl von Personen berechnen und zurückgeben.

Beispielaufruf: `berechne_zutatenmenge(2)` gibt `125.0` zurück.

## Codegerüst
```python
def berechne_zutatenmenge(anzahl_personen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_zutatenmenge(anzahl_personen):
    return 250.0 * anzahl_personen / 4

print(berechne_zutatenmenge(2))
```

## Unit Tests
```python
import unittest
from main import berechne_zutatenmenge

class TestBerechneZutatenmenge(unittest.TestCase):
    def test_zwei_personen(self):
        self.assertEqual(berechne_zutatenmenge(2), 125.0)

    def test_vier_personen(self):
        self.assertEqual(berechne_zutatenmenge(4), 250.0)

    def test_acht_personen(self):
        self.assertEqual(berechne_zutatenmenge(8), 500.0)

    def test_null_personen(self):
        self.assertEqual(berechne_zutatenmenge(0), 0.0)

    def test_halbe_person(self):
        self.assertEqual(berechne_zutatenmenge(0.5), 31.25)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 516
