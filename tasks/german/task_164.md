# Input
- Programmierkonzept: Tupel;Float;Funktionen höherer Ordnung
- Kontext: Gartenarbeit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Gartenarbeit mit Python

Schreibe eine Funktion namens `berechne_flaechen(tupel_liste, funktion)`, die eine Liste von Tupeln und eine Funktion als Argumente entgegennimmt. Jedes Tupel in der Liste repräsentiert die Länge und Breite eines rechteckigen Gartenbeets in Metern. Die Funktion, die als zweites Argument übergeben wird, soll auf jedes Tupel angewendet werden, um die Fläche des jeweiligen Gartenbeets zu berechnen. Die Funktion `berechne_flaechen` soll eine Liste der berechneten Flächen zurückgeben.

Beispielaufruf:
```python
def flaeche(tupel):
    return tupel[0] * tupel[1]

gartenbeete = [(2.5, 3.0), (4.0, 1.5), (3.5, 2.0)]
print(berechne_flaechen(gartenbeete, flaeche))
```

Erwartete Ausgabe:
```
[7.5, 6.0, 7.0]
```

Implementiere die Funktion `berechne_flaechen(tupel_liste, funktion)`.

## Codegerüst
```python
def berechne_flaechen(tupel_liste, funktion):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_flaechen(tupel_liste, funktion):
    return [funktion(t) for t in tupel_liste]

def flaeche(tupel):
    return tupel[0] * tupel[1]

gartenbeete = [(2.5, 3.0), (4.0, 1.5), (3.5, 2.0)]
print(berechne_flaechen(gartenbeete, flaeche))
```

## Unit Tests
```python
import unittest
from main import berechne_flaechen

def flaeche(tupel):
    return tupel[0] * tupel[1]

class TestBerechneFlaechen(unittest.TestCase):
    def test_einfache_flaechen(self):
        gartenbeete = [(2.5, 3.0), (4.0, 1.5), (3.5, 2.0)]
        self.assertEqual(berechne_flaechen(gartenbeete, flaeche), [7.5, 6.0, 7.0])

    def test_leere_liste(self):
        gartenbeete = []
        self.assertEqual(berechne_flaechen(gartenbeete, flaeche), [])

    def test_ein_element(self):
        gartenbeete = [(5.0, 5.0)]
        self.assertEqual(berechne_flaechen(gartenbeete, flaeche), [25.0])

    def test_null_flaeche(self):
        gartenbeete = [(0, 5.0), (5.0, 0)]
        self.assertEqual(berechne_flaechen(gartenbeete, flaeche), [0.0, 0.0])

    def test_negative_werte(self):
        gartenbeete = [(-2.0, 3.0), (4.0, -1.5)]
        self.assertEqual(berechne_flaechen(gartenbeete, flaeche), [-6.0, -6.0])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 596
