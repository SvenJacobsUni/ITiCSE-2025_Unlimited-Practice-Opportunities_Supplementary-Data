# Input
- Programmierkonzept: Tupel;Integer;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustier-Check

Schreibe eine Funktion namens `haustier_check(haustier)`, die überprüft, ob das übergebene Haustier in einer vordefinierten Liste von erlaubten Haustieren enthalten ist. Die Liste der erlaubten Haustiere ist ein Tupel und enthält die folgenden Tiere: "Hund", "Katze", "Hamster", "Kaninchen", "Papagei".

Die Funktion soll:
1. Überprüfen, ob das übergebene Haustier in der Liste der erlaubten Haustiere enthalten ist.
2. Wenn das Haustier erlaubt ist, soll die Funktion `True` zurückgeben.
3. Wenn das Haustier nicht erlaubt ist, soll die Funktion `False` zurückgeben.

Beispielaufrufe:
- `haustier_check("Hund")` gibt `True` zurück.
- `haustier_check("Schlange")` gibt `False` zurück.

## Codegerüst
```python
def haustier_check(haustier):
    ## Hier Code einfügen
```

## Musterlösung
```python
def haustier_check(haustier):
    return haustier in ("Hund", "Katze", "Hamster", "Kaninchen", "Papagei")

# Beispielaufrufe
print(haustier_check("Hund"))  # True
print(haustier_check("Schlange"))  # False
```

## Unit Tests
```python
import unittest

from main import haustier_check

class TestHaustierCheck(unittest.TestCase):
    def test_erlaubtes_haustier_hund(self):
        self.assertTrue(haustier_check("Hund"))

    def test_erlaubtes_haustier_katze(self):
        self.assertTrue(haustier_check("Katze"))

    def test_nicht_erlaubtes_haustier_schlange(self):
        self.assertFalse(haustier_check("Schlange"))

    def test_nicht_erlaubtes_haustier_pferd(self):
        self.assertFalse(haustier_check("Pferd"))

    def test_erlaubtes_haustier_hamster(self):
        self.assertTrue(haustier_check("Hamster"))

    def test_erlaubtes_haustier_kaninchen(self):
        self.assertTrue(haustier_check("Kaninchen"))

    def test_erlaubtes_haustier_papagei(self):
        self.assertTrue(haustier_check("Papagei"))

    def test_leerer_string(self):
        self.assertFalse(haustier_check(""))

    def test_none(self):
        self.assertFalse(haustier_check(None))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 615
