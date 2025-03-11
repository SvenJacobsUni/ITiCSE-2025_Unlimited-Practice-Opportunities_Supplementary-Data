# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Kontrollstrukturen beim Angeln

Schreibe eine Funktion namens `fisch_fangen(gewicht, laenge)`, die überprüft, ob ein gefangener Fisch die Mindestanforderungen für das Behalten erfüllt. Die Mindestanforderungen sind:

- Das Gewicht des Fisches muss mindestens 1.5 Kilogramm betragen.
- Die Länge des Fisches muss mindestens 30 Zentimeter betragen.

Die Funktion soll `True` zurückgeben, wenn beide Bedingungen erfüllt sind, und `False`, wenn eine oder beide Bedingungen nicht erfüllt sind.

Beispielaufrufe:
- `fisch_fangen(2.0, 35)` gibt `True` zurück.
- `fisch_fangen(1.0, 40)` gibt `False` zurück.
- `fisch_fangen(1.5, 25)` gibt `False` zurück.

## Codegerüst
```python
def fisch_fangen(gewicht, laenge):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fisch_fangen(gewicht, laenge):
    return gewicht >= 1.5 and laenge >= 30

# Beispielaufrufe
print(fisch_fangen(2.0, 35))  # True
print(fisch_fangen(1.0, 40))  # False
print(fisch_fangen(1.5, 25))  # False
```

## Unit Tests
```python
import unittest
from main import fisch_fangen

class TestFischFangen(unittest.TestCase):
    def test_beide_bedingungen_erfuellt(self):
        self.assertTrue(fisch_fangen(2.0, 35))

    def test_gewicht_unter_mindestanforderung(self):
        self.assertFalse(fisch_fangen(1.0, 40))

    def test_laenge_unter_mindestanforderung(self):
        self.assertFalse(fisch_fangen(1.5, 25))

    def test_beide_bedingungen_nicht_erfuellt(self):
        self.assertFalse(fisch_fangen(1.0, 20))

    def test_grenzwert_gewicht(self):
        self.assertTrue(fisch_fangen(1.5, 30))

    def test_grenzwert_laenge(self):
        self.assertTrue(fisch_fangen(2.0, 30))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 445
