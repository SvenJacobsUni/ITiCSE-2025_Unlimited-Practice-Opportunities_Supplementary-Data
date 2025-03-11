# Input
- Programmierkonzept: String;Integer;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Fangquote beim Angeln

Schreibe eine Funktion namens `fangquote(fischart, gewicht)`, die überprüft, ob ein gefangener Fisch den Mindestanforderungen entspricht. Die Funktion soll zwei Parameter entgegennehmen: `fischart` (String) und `gewicht` (Integer). 

Die Mindestanforderungen sind wie folgt:
- Für "Hecht" muss das Gewicht mindestens 5 kg betragen.
- Für "Zander" muss das Gewicht mindestens 3 kg betragen.
- Für "Barsch" muss das Gewicht mindestens 1 kg betragen.

Die Funktion soll `True` zurückgeben, wenn der Fisch den Mindestanforderungen entspricht, und `False`, wenn nicht.

Beispielaufrufe:
- `fangquote("Hecht", 6)` gibt `True` zurück.
- `fangquote("Zander", 2)` gibt `False` zurück.

## Codegerüst
```python
def fangquote(fischart, gewicht):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fangquote(fischart, gewicht):
    mindestgewicht = {"Hecht": 5, "Zander": 3, "Barsch": 1}
    return gewicht >= mindestgewicht.get(fischart, float('inf'))

# Beispielaufrufe
print(fangquote("Hecht", 6))  # True
print(fangquote("Zander", 2))  # False
```

## Unit Tests
```python
import unittest
from main import fangquote

class TestFangquote(unittest.TestCase):
    def test_hecht_ueber_mindestgewicht(self):
        self.assertTrue(fangquote("Hecht", 6))

    def test_hecht_unter_mindestgewicht(self):
        self.assertFalse(fangquote("Hecht", 4))

    def test_zander_ueber_mindestgewicht(self):
        self.assertTrue(fangquote("Zander", 4))

    def test_zander_unter_mindestgewicht(self):
        self.assertFalse(fangquote("Zander", 2))

    def test_barsch_ueber_mindestgewicht(self):
        self.assertTrue(fangquote("Barsch", 2))

    def test_barsch_unter_mindestgewicht(self):
        self.assertFalse(fangquote("Barsch", 0.5))

    def test_unbekannte_fischart(self):
        self.assertFalse(fangquote("Karpfen", 10))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 583
