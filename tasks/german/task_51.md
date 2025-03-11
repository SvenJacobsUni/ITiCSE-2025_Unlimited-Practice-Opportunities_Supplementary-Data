# Input
- Programmierkonzept: String
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Modernes Gaming - Spielertag validieren

Schreibe eine Funktion namens `ist_gueltiger_spielertag(spielertag)`, die überprüft, ob ein gegebener Spielertag (String) den folgenden Kriterien entspricht:

1. Der Spielertag muss zwischen 3 und 16 Zeichen lang sein.
2. Der Spielertag darf nur alphanumerische Zeichen (Buchstaben und Zahlen) enthalten.
3. Der Spielertag darf keine Leerzeichen enthalten.

Die Funktion soll `True` zurückgeben, wenn der Spielertag gültig ist, und `False`, wenn er ungültig ist.

Beispielaufrufe:
- `ist_gueltiger_spielertag("Gamer123")` gibt `True` zurück.
- `ist_gueltiger_spielertag("G@mer")` gibt `False` zurück.
- `ist_gueltiger_spielertag("Gamer 123")` gibt `False` zurück.
- `ist_gueltiger_spielertag("G")` gibt `False` zurück.

## Codegerüst
```python
def ist_gueltiger_spielertag(spielertag):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ist_gueltiger_spielertag(spielertag):
    return 3 <= len(spielertag) <= 16 and spielertag.isalnum()

# Beispielaufrufe
print(ist_gueltiger_spielertag("Gamer123"))  # True
print(ist_gueltiger_spielertag("G@mer"))     # False
print(ist_gueltiger_spielertag("Gamer 123")) # False
print(ist_gueltiger_spielertag("G"))         # False
```

## Unit Tests
```python
import unittest
from main import ist_gueltiger_spielertag

class TestIstGueltigerSpielertag(unittest.TestCase):
    def test_gueltiger_spielertag(self):
        self.assertTrue(ist_gueltiger_spielertag("Gamer123"))

    def test_ungueltiger_spielertag_sonderzeichen(self):
        self.assertFalse(ist_gueltiger_spielertag("G@mer"))

    def test_ungueltiger_spielertag_leerzeichen(self):
        self.assertFalse(ist_gueltiger_spielertag("Gamer 123"))

    def test_ungueltiger_spielertag_zu_kurz(self):
        self.assertFalse(ist_gueltiger_spielertag("G"))

    def test_ungueltiger_spielertag_zu_lang(self):
        self.assertFalse(ist_gueltiger_spielertag("Gamer1234567890123"))

    def test_gueltiger_spielertag_minimum_laenge(self):
        self.assertTrue(ist_gueltiger_spielertag("abc"))

    def test_gueltiger_spielertag_maximum_laenge(self):
        self.assertTrue(ist_gueltiger_spielertag("Gamer1234567890"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 469
