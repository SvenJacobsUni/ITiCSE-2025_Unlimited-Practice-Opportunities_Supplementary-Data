# Input
- Programmierkonzept: Float
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tiergewicht in Kilogramm

Schreibe eine Funktion namens `gewicht_in_kg(gewicht_pfund)`, die das Gewicht eines Tieres in Pfund (float) als Argument entgegennimmt und das Gewicht in Kilogramm (float) zurückgibt. Beachte, dass 1 Pfund ungefähr 0.453592 Kilogramm entspricht.

Beispielaufruf:
```python
gewicht_in_kg(10.0)
```
sollte ungefähr `4.53592` zurückgeben.

## Codegerüst
```python
def gewicht_in_kg(gewicht_pfund):
    ## Hier Code einfügen
```

## Musterlösung
```python
def gewicht_in_kg(gewicht_pfund):
    return gewicht_pfund * 0.453592

print(gewicht_in_kg(10.0))
```

## Unit Tests
```python
import unittest

from main import gewicht_in_kg

class TestGewichtInKg(unittest.TestCase):
    def test_zehn_pfund(self):
        self.assertAlmostEqual(gewicht_in_kg(10.0), 4.53592, places=5)

    def test_null_pfund(self):
        self.assertEqual(gewicht_in_kg(0.0), 0.0)

    def test_ein_pfund(self):
        self.assertAlmostEqual(gewicht_in_kg(1.0), 0.453592, places=5)

    def test_negatives_gewicht(self):
        self.assertAlmostEqual(gewicht_in_kg(-5.0), -2.26796, places=5)

    def test_grosses_gewicht(self):
        self.assertAlmostEqual(gewicht_in_kg(1000.0), 453.592, places=3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 468
