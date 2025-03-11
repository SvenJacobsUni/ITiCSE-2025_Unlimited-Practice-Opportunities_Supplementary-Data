# Input
- Programmierkonzept: Integer
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tiere zählen

Schreibe eine Funktion namens `zaehle_tiere(tiere)`, die eine Liste von Tieren als Eingabe erhält und die Anzahl der Tiere in der Liste als Integer zurückgibt. 

Beispielaufruf: 
```python
tiere = ["Hund", "Katze", "Vogel", "Hund", "Katze"]
print(zaehle_tiere(tiere))  # Ausgabe: 5
```

Die Funktion soll die Anzahl der Tiere in der Liste korrekt zählen und als Integer zurückgeben.

## Codegerüst
```python
def zaehle_tiere(tiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_tiere(tiere):
    return len(tiere)

tiere = ["Hund", "Katze", "Vogel", "Hund", "Katze"]
print(zaehle_tiere(tiere))  # Ausgabe: 5
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
        self.assertEqual(zaehle_tiere(["Hund", "Katze", "Vogel", "Hund", "Katze"]), 5)

    def test_gleiche_tiere(self):
        self.assertEqual(zaehle_tiere(["Hund", "Hund", "Hund"]), 3)

    def test_verschiedene_tiere(self):
        self.assertEqual(zaehle_tiere(["Hund", "Katze", "Vogel"]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 500
