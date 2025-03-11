# Input
- Programmierkonzept: Listen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Angeln und Listen in Python

Schreibe eine Funktion namens `fange_fische(fische)`, die eine Liste von Fischen als Argument erhält. Die Funktion soll die Anzahl der gefangenen Fische zählen und eine Nachricht zurückgeben, die die Anzahl der Fische angibt.

Beispielaufruf:
```python
fange_fische(["Hecht", "Barsch", "Forelle", "Hecht"])
```

Erwartete Rückgabe:
```
"Du hast 4 Fische gefangen."
```

## Codegerüst
```python
def fange_fische(fische):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fange_fische(fische):
    print(f"Du hast {len(fische)} Fische gefangen.")

fange_fische(["Hecht", "Barsch", "Forelle", "Hecht"])
```

## Unit Tests
```python
import unittest
from main import fange_fische

class TestFangeFische(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(fange_fische([]), "Du hast 0 Fische gefangen.")

    def test_ein_fisch(self):
        self.assertEqual(fange_fische(["Hecht"]), "Du hast 1 Fisch gefangen.")

    def test_mehrere_fische(self):
        self.assertEqual(fange_fische(["Hecht", "Barsch", "Forelle", "Hecht"]), "Du hast 4 Fische gefangen.")

    def test_viele_fische(self):
        self.assertEqual(fange_fische(["Hecht"] * 100), "Du hast 100 Fische gefangen.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 480
