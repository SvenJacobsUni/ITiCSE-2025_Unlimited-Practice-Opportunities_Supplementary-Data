# Input
- Programmierkonzept: Rekursion
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Zählung von Haustieren

Schreibe eine rekursive Funktion namens `zaehle_haustiere(haustiere)`, die die Anzahl der Haustiere in einer verschachtelten Liste zählt. Die Liste kann sowohl einzelne Haustiere als auch weitere Listen von Haustieren enthalten.

Beispiel:
```python
haustiere = ["Hund", ["Katze", "Vogel"], ["Fisch", ["Hamster", "Kaninchen"]]]
```

Ein Aufruf von `zaehle_haustiere(haustiere)` sollte die Gesamtzahl der Haustiere in der Liste zurückgeben.

```python
zaehle_haustiere(haustiere)  # sollte 6 zurückgeben
```

Implementiere die Funktion `zaehle_haustiere(haustiere)`, die die Anzahl der Haustiere in der verschachtelten Liste korrekt zählt.

## Codegerüst
```python
def zaehle_haustiere(haustiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_haustiere(haustiere):
    if not haustiere:
        return 0
    if isinstance(haustiere[0], list):
        return zaehle_haustiere(haustiere[0]) + zaehle_haustiere(haustiere[1:])
    return 1 + zaehle_haustiere(haustiere[1:])

haustiere = ["Hund", ["Katze", "Vogel"], ["Fisch", ["Hamster", "Kaninchen"]]]
print(zaehle_haustiere(haustiere))  # sollte 6 zurückgeben
```

## Unit Tests
```python
import unittest
from main import zaehle_haustiere

class TestZaehleHaustiere(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertEqual(zaehle_haustiere(["Hund", "Katze", "Vogel"]), 3)

    def test_verschachtelte_liste(self):
        self.assertEqual(zaehle_haustiere(["Hund", ["Katze", "Vogel"], ["Fisch", ["Hamster", "Kaninchen"]]]), 6)

    def test_leere_liste(self):
        self.assertEqual(zaehle_haustiere([]), 0)

    def test_ein_haustier(self):
        self.assertEqual(zaehle_haustiere(["Hund"]), 1)

    def test_tief_verschachtelte_liste(self):
        self.assertEqual(zaehle_haustiere(["Hund", ["Katze", ["Vogel", ["Fisch", ["Hamster", "Kaninchen"]]]]]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 498
