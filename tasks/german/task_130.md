# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);String
- Kontext: Vergnügungspark

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Eintrittskontrolle im Vergnügungspark

Schreibe eine Funktion namens `eintritt_erlaubt(alter, groesse)`, die überprüft, ob eine Person in eine bestimmte Attraktion im Vergnügungspark darf. Die Funktion soll zwei Parameter entgegennehmen: `alter` (ein Integer) und `groesse` (ein Float, der die Größe in Metern angibt).

Die Bedingungen für den Eintritt sind:
- Die Person muss mindestens 12 Jahre alt sein.
- Die Person muss mindestens 1.40 Meter groß sein.

Die Funktion soll `True` zurückgeben, wenn beide Bedingungen erfüllt sind, und `False`, wenn eine oder beide Bedingungen nicht erfüllt sind.

Beispielaufrufe:
- `eintritt_erlaubt(14, 1.50)` gibt `True` zurück.
- `eintritt_erlaubt(10, 1.50)` gibt `False` zurück.
- `eintritt_erlaubt(14, 1.35)` gibt `False` zurück.

## Codegerüst
```python
def eintritt_erlaubt(alter, groesse):
    ## Hier Code einfügen
```

## Musterlösung
```python
def eintritt_erlaubt(alter, groesse):
    return alter >= 12 and groesse >= 1.4

print(eintritt_erlaubt(14, 1.50))  # True
print(eintritt_erlaubt(10, 1.50))  # False
print(eintritt_erlaubt(14, 1.35))  # False
```

## Unit Tests
```python
import unittest
from main import eintritt_erlaubt

class TestEintrittErlaubt(unittest.TestCase):
    def test_erlaubt(self):
        self.assertTrue(eintritt_erlaubt(14, 1.50))

    def test_zu_jung(self):
        self.assertFalse(eintritt_erlaubt(10, 1.50))

    def test_zu_klein(self):
        self.assertFalse(eintritt_erlaubt(14, 1.35))

    def test_grenze_alter(self):
        self.assertTrue(eintritt_erlaubt(12, 1.50))

    def test_grenze_groesse(self):
        self.assertTrue(eintritt_erlaubt(14, 1.40))

    def test_grenze_beide(self):
        self.assertTrue(eintritt_erlaubt(12, 1.40))

    def test_unter_grenze_alter(self):
        self.assertFalse(eintritt_erlaubt(11, 1.40))

    def test_unter_grenze_groesse(self):
        self.assertFalse(eintritt_erlaubt(12, 1.39))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 562
