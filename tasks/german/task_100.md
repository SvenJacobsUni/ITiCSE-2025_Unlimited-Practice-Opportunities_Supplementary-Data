# Input
- Programmierkonzept: Rekursion
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Tierzählung

Schreibe eine rekursive Funktion namens `zaehle_tiere(tiere)`, die eine Liste von Tieren als Argument erhält und die Anzahl der Tiere in der Liste zurückgibt. Die Funktion soll dabei rekursiv arbeiten und keine Schleifen verwenden.

Beispielaufruf:
```python
tiere = ["Hund", "Katze", "Vogel", "Fisch"]
print(zaehle_tiere(tiere))  # Ausgabe: 4
```

Hinweis: Die Liste kann auch leer sein.

## Codegerüst
```python
def zaehle_tiere(tiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_tiere(tiere):
    if not tiere:
        return 0
    return 1 + zaehle_tiere(tiere[1:])

tiere = ["Hund", "Katze", "Vogel", "Fisch"]
print(zaehle_tiere(tiere))
```

## Unit Tests
```python
import unittest

from main import zaehle_tiere

class TestZaehleTiere(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(zaehle_tiere([]), 0)

    def test_ein_tier(self):
        self.assertEqual(zaehle_tiere(["Hund"]), 1)

    def test_mehrere_tiere(self):
        self.assertEqual(zaehle_tiere(["Hund", "Katze", "Vogel", "Fisch"]), 4)

    def test_verschiedene_tiere(self):
        self.assertEqual(zaehle_tiere(["Elefant", "Maus", "Tiger", "Löwe", "Giraffe"]), 5)

    def test_wiederholte_tiere(self):
        self.assertEqual(zaehle_tiere(["Hund", "Hund", "Hund"]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 518
