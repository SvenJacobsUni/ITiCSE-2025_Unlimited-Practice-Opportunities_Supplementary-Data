# Input
- Programmierkonzept: Float
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Berechnung des durchschnittlichen Stresslevels

Psychische Gesundheit ist ein wichtiges Thema, und das Verständnis von Stressleveln kann dabei helfen, das Wohlbefinden zu verbessern. In dieser Aufgabe sollst du eine Funktion schreiben, die den durchschnittlichen Stresslevel einer Person berechnet.

Schreibe eine Funktion namens `durchschnittlicher_stresslevel(stresswerte)`, die eine Liste von Fließkommazahlen (Floats) als Argument nimmt. Diese Liste repräsentiert die täglichen Stresslevel einer Person über einen bestimmten Zeitraum. Die Funktion soll den durchschnittlichen Stresslevel berechnen und zurückgeben.

Beispielaufruf:
```python
stresswerte = [3.5, 4.0, 2.8, 5.0, 3.9]
print(durchschnittlicher_stresslevel(stresswerte))  # Ausgabe: 3.84
```

Hinweis: Die Ausgabe muss nicht exakt 3.84 sein, da dies nur ein Beispiel ist.

## Codegerüst
```python
def durchschnittlicher_stresslevel(stresswerte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def durchschnittlicher_stresslevel(stresswerte):
    return sum(stresswerte) / len(stresswerte)

stresswerte = [3.5, 4.0, 2.8, 5.0, 3.9]
print(durchschnittlicher_stresslevel(stresswerte))
```

## Unit Tests
```python
import unittest
from main import durchschnittlicher_stresslevel

class TestDurchschnittlicherStresslevel(unittest.TestCase):
    def test_durchschnittlicher_stresslevel_einfach(self):
        self.assertAlmostEqual(durchschnittlicher_stresslevel([3.5, 4.0, 2.8, 5.0, 3.9]), 3.84, places=2)

    def test_durchschnittlicher_stresslevel_leer(self):
        with self.assertRaises(ZeroDivisionError):
            durchschnittlicher_stresslevel([])

    def test_durchschnittlicher_stresslevel_ein_element(self):
        self.assertEqual(durchschnittlicher_stresslevel([4.2]), 4.2)

    def test_durchschnittlicher_stresslevel_negative_werte(self):
        self.assertAlmostEqual(durchschnittlicher_stresslevel([-1.0, -2.0, -3.0]), -2.0, places=2)

    def test_durchschnittlicher_stresslevel_gemischte_werte(self):
        self.assertAlmostEqual(durchschnittlicher_stresslevel([1.0, -1.0, 1.0, -1.0]), 0.0, places=2)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 501
