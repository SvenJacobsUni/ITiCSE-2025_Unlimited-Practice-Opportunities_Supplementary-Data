# Input
- Programmierkonzept: Listen;Tupel
- Kontext: Gartenarbeit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Gartenarbeit mit Listen und Tupeln

Schreibe eine Funktion namens `pflanzen_info(pflanzen_liste)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel enthält den Namen einer Pflanze und die Anzahl der Pflanzen im Garten. Die Funktion soll eine neue Liste zurückgeben, die nur die Namen der Pflanzen enthält, die mehr als 5 Mal im Garten vorhanden sind.

Beispielaufruf:
```python
pflanzen_liste = [("Tomate", 10), ("Gurke", 3), ("Karotte", 7), ("Salat", 2)]
print(pflanzen_info(pflanzen_liste))
```

Erwartete Ausgabe:
```
['Tomate', 'Karotte']
```

## Codegerüst
```python
def pflanzen_info(pflanzen_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def pflanzen_info(pflanzen_liste):
    return [name for name, anzahl in pflanzen_liste if anzahl > 5]

pflanzen_liste = [("Tomate", 10), ("Gurke", 3), ("Karotte", 7), ("Salat", 2)]
print(pflanzen_info(pflanzen_liste))
```

## Unit Tests
```python
import unittest
from main import pflanzen_info

class TestPflanzenInfo(unittest.TestCase):
    def test_mehr_als_fuenf(self):
        self.assertEqual(pflanzen_info([("Tomate", 10), ("Gurke", 3), ("Karotte", 7), ("Salat", 2)]), ["Tomate", "Karotte"])

    def test_keine_pflanzen(self):
        self.assertEqual(pflanzen_info([]), [])

    def test_alle_weniger_als_fuenf(self):
        self.assertEqual(pflanzen_info([("Tomate", 1), ("Gurke", 2), ("Karotte", 3), ("Salat", 4)]), [])

    def test_alle_mehr_als_fuenf(self):
        self.assertEqual(pflanzen_info([("Tomate", 6), ("Gurke", 7), ("Karotte", 8), ("Salat", 9)]), ["Tomate", "Gurke", "Karotte", "Salat"])

    def test_genau_fuenf(self):
        self.assertEqual(pflanzen_info([("Tomate", 5), ("Gurke", 5), ("Karotte", 5), ("Salat", 5)]), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 578
