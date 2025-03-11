# Input
- Programmierkonzept: Tupel
- Kontext: Gartenarbeit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Gartenarbeit mit Tupeln

Schreibe eine Funktion namens `pflanzen_info(pflanze)`, die Informationen über verschiedene Pflanzen in einem Garten zurückgibt. Die Informationen über die Pflanzen sollen in einem Tupel gespeichert sein. Jedes Tupel soll den Namen der Pflanze, die benötigte Wassermenge (in Litern pro Woche) und die bevorzugte Sonneneinstrahlung (z.B. "Vollsonne", "Halbschatten", "Schatten") enthalten.

Die Funktion soll ein Tupel mit den Informationen der übergebenen Pflanze zurückgeben. Wenn die Pflanze nicht im Garten vorhanden ist, soll die Funktion `None` zurückgeben.

Beispielaufrufe:
```python
pflanzen_info("Tomate")  # könnte z.B. ("Tomate", 5, "Vollsonne") zurückgeben
pflanzen_info("Lavendel")  # könnte z.B. ("Lavendel", 2, "Vollsonne") zurückgeben
pflanzen_info("Unbekannt")  # sollte None zurückgeben
```

## Codegerüst
```python
def pflanzen_info(pflanze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def pflanzen_info(pflanze):
    garten = {
        "Tomate": ("Tomate", 5, "Vollsonne"),
        "Lavendel": ("Lavendel", 2, "Vollsonne"),
        "Basilikum": ("Basilikum", 3, "Halbschatten")
    }
    return garten.get(pflanze)

print(pflanzen_info("Tomate"))
print(pflanzen_info("Lavendel"))
print(pflanzen_info("Unbekannt"))
```

## Unit Tests
```python
import unittest
from main import pflanzen_info

class TestPflanzenInfo(unittest.TestCase):
    def test_tomate(self):
        self.assertEqual(pflanzen_info("Tomate"), ("Tomate", 5, "Vollsonne"))

    def test_lavendel(self):
        self.assertEqual(pflanzen_info("Lavendel"), ("Lavendel", 2, "Vollsonne"))

    def test_basilikum(self):
        self.assertEqual(pflanzen_info("Basilikum"), ("Basilikum", 3, "Halbschatten"))

    def test_unbekannt(self):
        self.assertIsNone(pflanzen_info("Unbekannt"))

    def test_leerer_string(self):
        self.assertIsNone(pflanzen_info(""))

    def test_none(self):
        self.assertIsNone(pflanzen_info(None))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 499
