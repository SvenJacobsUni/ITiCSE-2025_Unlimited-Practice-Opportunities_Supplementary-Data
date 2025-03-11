# Input
- Programmierkonzept: Boolean und None;For-Schleifen
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tiere zählen

Schreibe eine Funktion namens `zaehle_tiere(tier_liste)`, die eine Liste von Tieren als Argument erhält. Die Funktion soll die Anzahl der Tiere in der Liste zählen und zurückgeben. Wenn die Liste leer ist, soll die Funktion `None` zurückgeben. 

Beispielaufrufe:

- `zaehle_tiere(["Hund", "Katze", "Vogel"])` gibt `3` zurück.
- `zaehle_tiere([])` gibt `None` zurück.

Verwende eine `for`-Schleife, um die Tiere in der Liste zu zählen.

## Codegerüst
```python
def zaehle_tiere(tier_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_tiere(tier_liste):
    if not tier_liste:
        return None
    return len(tier_liste)

print(zaehle_tiere(["Hund", "Katze", "Vogel"]))  # Ausgabe: 3
print(zaehle_tiere([]))  # Ausgabe: None
```

## Unit Tests
```python
import unittest

from main import zaehle_tiere

class TestZaehleTiere(unittest.TestCase):
    def test_mehrere_tiere(self):
        self.assertEqual(zaehle_tiere(["Hund", "Katze", "Vogel"]), 3)

    def test_leere_liste(self):
        self.assertEqual(zaehle_tiere([]), None)

    def test_ein_tier(self):
        self.assertEqual(zaehle_tiere(["Hund"]), 1)

    def test_zwei_tiere(self):
        self.assertEqual(zaehle_tiere(["Hund", "Katze"]), 2)

    def test_viele_tiere(self):
        self.assertEqual(zaehle_tiere(["Hund", "Katze", "Vogel", "Fisch", "Maus"]), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 561
