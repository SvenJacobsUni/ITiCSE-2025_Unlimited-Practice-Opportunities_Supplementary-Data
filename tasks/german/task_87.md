# Input
- Programmierkonzept: Rekursion
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Fischzählung

Schreibe eine rekursive Funktion namens `zaehle_fische(teich)`, die die Anzahl der Fische in einem Teich zählt. Der Teich wird als Liste von Listen dargestellt, wobei jede innere Liste entweder leer ist oder weitere Listen enthält. Ein leerer Teich (leere Liste) enthält keine Fische.

Beispielaufrufe:

```python
# Ein Teich ohne Fische
teich1 = []

# Ein Teich mit einem Fisch
teich2 = [[], []]

# Ein Teich mit drei Fischen
teich3 = [[], [[], []], [[], [[], []]]]

print(zaehle_fische(teich1))  # Ausgabe: 0
print(zaehle_fische(teich2))  # Ausgabe: 2
print(zaehle_fische(teich3))  # Ausgabe: 6
```

Implementiere die Funktion `zaehle_fische(teich)`, die die Anzahl der Fische im Teich rekursiv zählt und zurückgibt.

## Codegerüst
```python
def zaehle_fische(teich):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(teich):
    return 1 + sum(zaehle_fische(t) for t in teich) if teich else 0

# Beispielaufrufe
teich1 = []
teich2 = [[], []]
teich3 = [[], [[], []], [[], [[], []]]]

print(zaehle_fische(teich1))  # Ausgabe: 0
print(zaehle_fische(teich2))  # Ausgabe: 2
print(zaehle_fische(teich3))  # Ausgabe: 6
```

## Unit Tests
```python
import unittest
from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_leerer_teich(self):
        self.assertEqual(zaehle_fische([]), 0)

    def test_ein_fisch(self):
        self.assertEqual(zaehle_fische([[], []]), 2)

    def test_mehrere_fische(self):
        self.assertEqual(zaehle_fische([[], [[], []], [[], [[], []]]]), 6)

    def test_verschachtelter_teich(self):
        self.assertEqual(zaehle_fische([[], [[], [[], []]], [[], []]]), 5)

    def test_tief_verschachtelter_teich(self):
        self.assertEqual(zaehle_fische([[], [[], [[], [[], []]]], [[], []]]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 505
