# Input
- Programmierkonzept: Rekursion
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Fischzählung

Schreibe eine rekursive Funktion namens `zaehle_fische(see)`, die die Anzahl der Fische in einem See zählt. Der See wird als verschachtelte Liste dargestellt, wobei jede Liste entweder eine Zahl (die Anzahl der Fische in diesem Teil des Sees) oder eine weitere Liste (ein tieferer Teil des Sees) enthält.

Beispiel:
```python
see = [2, [3, [1, 4], 5], [6, 7], 8]
```

In diesem Beispiel enthält der See insgesamt 36 Fische.

Implementiere die Funktion `zaehle_fische(see)`, die die Gesamtanzahl der Fische im See zurückgibt.

Beispielaufruf:
```python
print(zaehle_fische(see))  # Ausgabe: 36
```

## Codegerüst
```python
def zaehle_fische(see):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(see):
    if isinstance(see, int):
        return see
    return sum(zaehle_fische(teil) for teil in see)

see = [2, [3, [1, 4], 5], [6, 7], 8]
print(zaehle_fische(see))  # Ausgabe: 36
```

## Unit Tests
```python
import unittest

from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_einfacher_see(self):
        self.assertEqual(zaehle_fische([1, 2, 3]), 6)

    def test_leerer_see(self):
        self.assertEqual(zaehle_fische([]), 0)

    def test_ein_fisch(self):
        self.assertEqual(zaehle_fische([1]), 1)

    def test_verschachtelter_see(self):
        self.assertEqual(zaehle_fische([1, [2, [3, 4]], 5]), 15)

    def test_tief_verschachtelter_see(self):
        self.assertEqual(zaehle_fische([1, [2, [3, [4, [5]]]]]), 15)

    def test_gemischter_see(self):
        self.assertEqual(zaehle_fische([2, [3, [1, 4], 5], [6, 7], 8]), 36)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 447
