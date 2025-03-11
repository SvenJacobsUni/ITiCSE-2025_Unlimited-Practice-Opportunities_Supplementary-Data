# Input
- Programmierkonzept: Rekursion;If-Else-Anweisungen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Fischzählung

Schreibe eine rekursive Funktion namens `zaehle_fische(fische)`, die die Anzahl der Fische in einem See zählt. Die Funktion soll eine Liste von Fischen als Argument erhalten, wobei jeder Fisch durch einen String repräsentiert wird. Wenn die Liste leer ist, soll die Funktion 0 zurückgeben. Andernfalls soll die Funktion die Anzahl der Fische in der Liste zurückgeben.

Beispielaufrufe:
- `zaehle_fische([])` gibt `0` zurück.
- `zaehle_fische(["Hecht", "Karpfen", "Forelle"])` gibt `3` zurück.

## Codegerüst
```python
def zaehle_fische(fische):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(fische):
    if not fische:
        return 0
    return 1 + zaehle_fische(fische[1:])

print(zaehle_fische([]))
print(zaehle_fische(["Hecht", "Karpfen", "Forelle"]))
```

## Unit Tests
```python
import unittest
from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(zaehle_fische([]), 0)

    def test_ein_fisch(self):
        self.assertEqual(zaehle_fische(["Hecht"]), 1)

    def test_mehrere_fische(self):
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Forelle"]), 3)

    def test_viele_fische(self):
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Forelle", "Barsch", "Wels", "Zander"]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 533
