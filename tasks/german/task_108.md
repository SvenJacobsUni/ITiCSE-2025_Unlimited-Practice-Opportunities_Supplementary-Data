# Input
- Programmierkonzept: Listen;Rekursion
- Kontext: Vergnügungspark

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Vergnügungspark - Attraktionen zählen

Schreibe eine rekursive Funktion namens `zaehle_attraktionen(attraktionen)`, die eine Liste von Attraktionen in einem Vergnügungspark zählt. Die Liste kann sowohl einzelne Attraktionen als auch weitere Listen von Attraktionen enthalten. Die Funktion soll die Gesamtzahl der Attraktionen zurückgeben.

Beispiel:

```python
attraktionen = ["Achterbahn", ["Riesenrad", "Karussell"], "Geisterbahn", ["Wasserrutsche", ["Wildwasserbahn", "Wellenbad"]]]
```

Ein Aufruf von `zaehle_attraktionen(attraktionen)` sollte die Gesamtzahl der Attraktionen in der Liste zurückgeben.

```python
print(zaehle_attraktionen(attraktionen))  # Ausgabe: 7
```

Implementiere die Funktion `zaehle_attraktionen(attraktionen)`, die die Anzahl der Attraktionen in der Liste rekursiv zählt.

## Codegerüst
```python
def zaehle_attraktionen(attraktionen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_attraktionen(attraktionen):
    if not attraktionen:
        return 0
    if isinstance(attraktionen[0], list):
        return zaehle_attraktionen(attraktionen[0]) + zaehle_attraktionen(attraktionen[1:])
    return 1 + zaehle_attraktionen(attraktionen[1:])

attraktionen = ["Achterbahn", ["Riesenrad", "Karussell"], "Geisterbahn", ["Wasserrutsche", ["Wildwasserbahn", "Wellenbad"]]]
print(zaehle_attraktionen(attraktionen))  # Ausgabe: 7
```

## Unit Tests
```python
import unittest

from main import zaehle_attraktionen

class TestZaehleAttraktionen(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertEqual(zaehle_attraktionen(["Achterbahn", "Riesenrad", "Karussell"]), 3)

    def test_verschachtelte_liste(self):
        self.assertEqual(zaehle_attraktionen(["Achterbahn", ["Riesenrad", "Karussell"], "Geisterbahn"]), 4)

    def test_tief_verschachtelte_liste(self):
        self.assertEqual(zaehle_attraktionen(["Achterbahn", ["Riesenrad", ["Karussell", "Geisterbahn"]], "Wasserrutsche"]), 5)

    def test_leere_liste(self):
        self.assertEqual(zaehle_attraktionen([]), 0)

    def test_liste_mit_leeren_unterlisten(self):
        self.assertEqual(zaehle_attraktionen(["Achterbahn", [], "Riesenrad", []]), 2)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 540
