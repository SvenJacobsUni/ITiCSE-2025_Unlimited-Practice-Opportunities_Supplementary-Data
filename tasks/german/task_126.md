# Input
- Programmierkonzept: Float;Listen
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Durchschnittliches Gewicht von Tieren

Schreibe eine Funktion namens `durchschnittliches_gewicht(tiere)`, die eine Liste von Floats als Argument nimmt. Diese Liste repräsentiert die Gewichte verschiedener Tiere in Kilogramm. Die Funktion soll das durchschnittliche Gewicht der Tiere berechnen und zurückgeben.

Beispielaufruf:
```python
gewichte = [4.5, 7.2, 3.8, 5.0, 6.1]
print(durchschnittliches_gewicht(gewichte))  # Ausgabe: 5.32
```

Hinweis: Die Ausgabe kann leicht variieren aufgrund von Rundungsdifferenzen.

## Codegerüst
```python
def durchschnittliches_gewicht(tiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def durchschnittliches_gewicht(tiere):
    return sum(tiere) / len(tiere)

gewichte = [4.5, 7.2, 3.8, 5.0, 6.1]
print(durchschnittliches_gewicht(gewichte))
```

## Unit Tests
```python
import unittest
from main import durchschnittliches_gewicht

class TestDurchschnittlichesGewicht(unittest.TestCase):
    def test_durchschnitt(self):
        self.assertAlmostEqual(durchschnittliches_gewicht([4.5, 7.2, 3.8, 5.0, 6.1]), 5.32, places=2)

    def test_leere_liste(self):
        with self.assertRaises(ZeroDivisionError):
            durchschnittliches_gewicht([])

    def test_ein_element(self):
        self.assertEqual(durchschnittliches_gewicht([5.0]), 5.0)

    def test_ganze_zahlen(self):
        self.assertEqual(durchschnittliches_gewicht([1, 2, 3, 4, 5]), 3.0)

    def test_gemischte_zahlen(self):
        self.assertAlmostEqual(durchschnittliches_gewicht([1.5, 2.5, 3.5, 4.5, 5.5]), 3.5, places=2)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 558
