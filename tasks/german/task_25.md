# Input
- Programmierkonzept: While-Schleifen
- Kontext: Gartenarbeit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Gartenarbeit mit While-Schleifen

Schreibe eine Funktion namens `pflanze_giessen(pflanzen)`, die eine Liste von Pflanzen als Argument erhält. Jede Pflanze in der Liste hat einen Wasserstand, der durch eine Zahl dargestellt wird. Die Funktion soll jede Pflanze so lange gießen, bis ihr Wasserstand mindestens 5 erreicht. Der Wasserstand jeder Pflanze erhöht sich bei jedem Gießen um 1. Die Funktion soll die Anzahl der Gießvorgänge für jede Pflanze zurückgeben.

Beispielaufruf:
```python
pflanzen = [2, 4, 1]
print(pflanze_giessen(pflanzen))  # Ausgabe: [3, 1, 4]
```

In diesem Beispiel benötigt die erste Pflanze 3 Gießvorgänge, die zweite Pflanze 1 Gießvorgang und die dritte Pflanze 4 Gießvorgänge, um den Wasserstand von mindestens 5 zu erreichen.

## Codegerüst
```python
def pflanze_giessen(pflanzen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def pflanze_giessen(pflanzen):
    return [max(0, 5 - p) for p in pflanzen]

pflanzen = [2, 4, 1]
print(pflanze_giessen(pflanzen))
```

## Unit Tests
```python
import unittest
from main import pflanze_giessen

class TestPflanzeGiessen(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertEqual(pflanze_giessen([2, 4, 1]), [3, 1, 4])

    def test_alle_pflanzen_bereits_ausreichend_gegossen(self):
        self.assertEqual(pflanze_giessen([5, 6, 7]), [0, 0, 0])

    def test_alle_pflanzen_müssen_gegossen_werden(self):
        self.assertEqual(pflanze_giessen([0, 0, 0]), [5, 5, 5])

    def test_leere_liste(self):
        self.assertEqual(pflanze_giessen([]), [])

    def test_randbedingungen(self):
        self.assertEqual(pflanze_giessen([4, 5, 6]), [1, 0, 0])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 443
