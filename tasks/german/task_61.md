# Input
- Programmierkonzept: Tupel
- Kontext: Gartenarbeit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Gartenarbeit mit Tupeln

Schreibe eine Funktion namens `pflanzen_info(pflanze)`, die Informationen über verschiedene Pflanzen in einem Garten zurückgibt. Die Informationen über die Pflanzen sollen in einem Tupel gespeichert werden. Jedes Tupel soll den Namen der Pflanze, die benötigte Wassermenge (in Litern pro Woche) und die bevorzugte Sonnenmenge (in Stunden pro Tag) enthalten.

Die Funktion soll ein Tupel mit den Informationen der übergebenen Pflanze zurückgeben. Wenn die Pflanze nicht im Garten vorhanden ist, soll die Funktion `None` zurückgeben.

Beispielaufrufe:
- `pflanzen_info("Tomate")` könnte `("Tomate", 5, 8)` zurückgeben.
- `pflanzen_info("Rose")` könnte `("Rose", 3, 6)` zurückgeben.
- `pflanzen_info("Kaktus")` könnte `None` zurückgeben, wenn "Kaktus" nicht im Garten vorhanden ist.

## Codegerüst
```python
def pflanzen_info(pflanze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def pflanzen_info(pflanze):
    garten = {
        "Tomate": ("Tomate", 5, 8),
        "Rose": ("Rose", 3, 6),
        "Basilikum": ("Basilikum", 2, 6)
    }
    return garten.get(pflanze)

# Beispielaufrufe
print(pflanzen_info("Tomate"))
print(pflanzen_info("Rose"))
print(pflanzen_info("Kaktus"))
```

## Unit Tests
```python
import unittest
from main import pflanzen_info

class TestPflanzenInfo(unittest.TestCase):
    def test_tomate(self):
        self.assertEqual(pflanzen_info("Tomate"), ("Tomate", 5, 8))

    def test_rose(self):
        self.assertEqual(pflanzen_info("Rose"), ("Rose", 3, 6))

    def test_basilikum(self):
        self.assertEqual(pflanzen_info("Basilikum"), ("Basilikum", 2, 6))

    def test_kaktus(self):
        self.assertIsNone(pflanzen_info("Kaktus"))

    def test_leerer_string(self):
        self.assertIsNone(pflanzen_info(""))

    def test_none(self):
        self.assertIsNone(pflanzen_info(None))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 479
