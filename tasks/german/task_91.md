# Input
- Programmierkonzept: While-Schleifen
- Kontext: Aquarium

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Aquarium - Fische zählen

Schreibe eine Funktion namens `zaehle_fische(fische)`, die eine Liste von Fischen als Argument erhält. Die Funktion soll eine While-Schleife verwenden, um die Anzahl der Fische in der Liste zu zählen und diese Anzahl zurückzugeben.

Beispielaufruf:
```python
fische = ["Goldfisch", "Guppy", "Neonsalmler", "Platy"]
print(zaehle_fische(fische))  # Ausgabe: 4
```

Implementiere die Funktion `zaehle_fische(fische)`, die die Anzahl der Fische in der Liste zählt und zurückgibt.

## Codegerüst
```python
def zaehle_fische(fische):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(fische):
    count = 0
    i = 0
    while i < len(fische):
        count += 1
        i += 1
    return count

fische = ["Goldfisch", "Guppy", "Neonsalmler", "Platy"]
print(zaehle_fische(fische))
```

## Unit Tests
```python
import unittest
from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(zaehle_fische([]), 0)

    def test_ein_fisch(self):
        self.assertEqual(zaehle_fische(["Goldfisch"]), 1)

    def test_mehrere_fische(self):
        self.assertEqual(zaehle_fische(["Goldfisch", "Guppy", "Neonsalmler", "Platy"]), 4)

    def test_gleiche_fische(self):
        self.assertEqual(zaehle_fische(["Guppy", "Guppy", "Guppy"]), 3)

    def test_gemischte_fische(self):
        self.assertEqual(zaehle_fische(["Goldfisch", "Guppy", "Guppy", "Neonsalmler", "Platy", "Platy"]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 509
