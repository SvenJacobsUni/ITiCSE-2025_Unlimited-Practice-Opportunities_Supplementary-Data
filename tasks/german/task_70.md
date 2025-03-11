# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Kontrollstrukturen beim Angeln

Schreibe eine Funktion namens `fisch_fangen(gewicht, laenge)`, die überprüft, ob ein gefangener Fisch die Mindestanforderungen für das Behalten erfüllt. Ein Fisch darf nur behalten werden, wenn er mindestens 2 kg wiegt und mindestens 30 cm lang ist. Die Funktion soll `True` zurückgeben, wenn der Fisch behalten werden darf, und `False`, wenn nicht.

Beispielaufrufe:
- `fisch_fangen(2.5, 35)` gibt `True` zurück.
- `fisch_fangen(1.8, 32)` gibt `False` zurück.
- `fisch_fangen(2.0, 29)` gibt `False` zurück.

## Codegerüst
```python
def fisch_fangen(gewicht, laenge):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fisch_fangen(gewicht, laenge):
    return gewicht >= 2 and laenge >= 30

# Beispielaufrufe
print(fisch_fangen(2.5, 35))  # True
print(fisch_fangen(1.8, 32))  # False
print(fisch_fangen(2.0, 29))  # False
```

## Unit Tests
```python
import unittest
from main import fisch_fangen

class TestFischFangen(unittest.TestCase):
    def test_fisch_behalten(self):
        self.assertTrue(fisch_fangen(2.5, 35))

    def test_fisch_zu_leicht(self):
        self.assertFalse(fisch_fangen(1.8, 32))

    def test_fisch_zu_kurz(self):
        self.assertFalse(fisch_fangen(2.0, 29))

    def test_fisch_genau_grenze(self):
        self.assertTrue(fisch_fangen(2.0, 30))

    def test_fisch_unter_grenze(self):
        self.assertFalse(fisch_fangen(1.9, 29))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 488
