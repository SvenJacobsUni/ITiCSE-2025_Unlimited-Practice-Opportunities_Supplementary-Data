# Input
- Programmierkonzept: Funktionen als Variablen;Boolean und None
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustiere und Funktionen

Schreibe eine Funktion namens `ist_haustier(name)`, die überprüft, ob der übergebene Name zu einer Liste von bekannten Haustieren gehört. Die Liste der bekannten Haustiere ist: `["Hund", "Katze", "Hamster", "Papagei", "Goldfisch"]`. Die Funktion soll `True` zurückgeben, wenn der Name in der Liste enthalten ist, und `False`, wenn nicht.

Zusätzlich soll eine Funktion `ist_haustier_oder_none(name)` implementiert werden, die `ist_haustier(name)` aufruft und `None` zurückgibt, wenn der Name nicht in der Liste der bekannten Haustiere enthalten ist.

Beispielaufrufe:
- `ist_haustier("Hund")` gibt `True` zurück.
- `ist_haustier("Elefant")` gibt `False` zurück.
- `ist_haustier_oder_none("Katze")` gibt `True` zurück.
- `ist_haustier_oder_none("Elefant")` gibt `None` zurück.

## Codegerüst
```python
def ist_haustier(name):
    ## Hier Code einfügen

def ist_haustier_oder_none(name):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ist_haustier(name):
    return name in ["Hund", "Katze", "Hamster", "Papagei", "Goldfisch"]

def ist_haustier_oder_none(name):
    return ist_haustier(name) or None

# Beispielaufrufe
print(ist_haustier("Hund"))  # True
print(ist_haustier("Elefant"))  # False
print(ist_haustier_oder_none("Katze"))  # True
print(ist_haustier_oder_none("Elefant"))  # None
```

## Unit Tests
```python
import unittest
from main import ist_haustier, ist_haustier_oder_none

class TestIstHaustier(unittest.TestCase):
    def test_hund(self):
        self.assertTrue(ist_haustier("Hund"))

    def test_elefant(self):
        self.assertFalse(ist_haustier("Elefant"))

    def test_katze(self):
        self.assertTrue(ist_haustier("Katze"))

    def test_goldfisch(self):
        self.assertTrue(ist_haustier("Goldfisch"))

    def test_leerer_string(self):
        self.assertFalse(ist_haustier(""))

class TestIstHaustierOderNone(unittest.TestCase):
    def test_hund(self):
        self.assertTrue(ist_haustier_oder_none("Hund"))

    def test_elefant(self):
        self.assertIsNone(ist_haustier_oder_none("Elefant"))

    def test_katze(self):
        self.assertTrue(ist_haustier_oder_none("Katze"))

    def test_goldfisch(self):
        self.assertTrue(ist_haustier_oder_none("Goldfisch"))

    def test_leerer_string(self):
        self.assertIsNone(ist_haustier_oder_none(""))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 566
