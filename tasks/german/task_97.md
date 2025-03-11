# Input
- Programmierkonzept: Boolean und None
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustiere und Boolean

Schreibe eine Funktion namens `ist_haustier(name)`, die überprüft, ob der übergebene Name zu einem bekannten Haustier gehört. Die Funktion soll `True` zurückgeben, wenn der Name in der Liste der bekannten Haustiere enthalten ist, und `False`, wenn nicht. Wenn der Name `None` ist, soll die Funktion ebenfalls `False` zurückgeben.

Bekannte Haustiere sind:
- "Hund"
- "Katze"
- "Hamster"
- "Kaninchen"
- "Papagei"

Beispielaufrufe:
- `ist_haustier("Hund")` gibt `True` zurück.
- `ist_haustier("Elefant")` gibt `False` zurück.
- `ist_haustier(None)` gibt `False` zurück.

## Codegerüst
```python
def ist_haustier(name):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ist_haustier(name):
    return name in ["Hund", "Katze", "Hamster", "Kaninchen", "Papagei"]

# Testfälle
print(ist_haustier("Hund"))      # True
print(ist_haustier("Elefant"))   # False
print(ist_haustier(None))        # False
```

## Unit Tests
```python
import unittest
from main import ist_haustier

class TestIstHaustier(unittest.TestCase):
    def test_hund(self):
        self.assertTrue(ist_haustier("Hund"))

    def test_katze(self):
        self.assertTrue(ist_haustier("Katze"))

    def test_hamster(self):
        self.assertTrue(ist_haustier("Hamster"))

    def test_kaninchen(self):
        self.assertTrue(ist_haustier("Kaninchen"))

    def test_papagei(self):
        self.assertTrue(ist_haustier("Papagei"))

    def test_elefant(self):
        self.assertFalse(ist_haustier("Elefant"))

    def test_none(self):
        self.assertFalse(ist_haustier(None))

    def test_leerer_string(self):
        self.assertFalse(ist_haustier(""))

    def test_unbekanntes_tier(self):
        self.assertFalse(ist_haustier("Tiger"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 515
