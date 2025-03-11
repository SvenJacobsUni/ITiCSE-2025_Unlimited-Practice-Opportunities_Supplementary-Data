# Input
- Programmierkonzept: For-Schleifen;While-Schleifen;If-Else-Anweisungen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Fische zählen

Schreibe eine Funktion namens `zaehle_fische(fisch_liste)`, die eine Liste von Fischen als Eingabe erhält. Die Funktion soll die Anzahl der Fische in der Liste zählen und dabei zwischen "Karpfen" und "Hecht" unterscheiden. 

- Wenn der Fisch ein "Karpfen" ist, soll er zur Karpfen-Zählung hinzugefügt werden.
- Wenn der Fisch ein "Hecht" ist, soll er zur Hecht-Zählung hinzugefügt werden.
- Alle anderen Fische sollen ignoriert werden.

Die Funktion soll ein Dictionary zurückgeben, das die Anzahl der Karpfen und Hechte enthält. 

Beispielaufruf:
```python
fische = ["Karpfen", "Hecht", "Karpfen", "Forelle", "Hecht", "Karpfen"]
print(zaehle_fische(fische))
```

Erwartete Ausgabe:
```python
{"Karpfen": 3, "Hecht": 2}
```

## Codegerüst
```python
def zaehle_fische(fisch_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(fisch_liste):
    zaehlung = {"Karpfen": 0, "Hecht": 0}
    for fisch in fisch_liste:
        if fisch in zaehlung:
            zaehlung[fisch] += 1
    return zaehlung

fische = ["Karpfen", "Hecht", "Karpfen", "Forelle", "Hecht", "Karpfen"]
print(zaehle_fische(fische))
```

## Unit Tests
```python
import unittest
from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_gemischte_fische(self):
        self.assertEqual(zaehle_fische(["Karpfen", "Hecht", "Karpfen", "Forelle", "Hecht", "Karpfen"]), {"Karpfen": 3, "Hecht": 2})

    def test_nur_karpfen(self):
        self.assertEqual(zaehle_fische(["Karpfen", "Karpfen", "Karpfen"]), {"Karpfen": 3, "Hecht": 0})

    def test_nur_hechte(self):
        self.assertEqual(zaehle_fische(["Hecht", "Hecht", "Hecht"]), {"Karpfen": 0, "Hecht": 3})

    def test_keine_fische(self):
        self.assertEqual(zaehle_fische([]), {"Karpfen": 0, "Hecht": 0})

    def test_ignorierte_fische(self):
        self.assertEqual(zaehle_fische(["Forelle", "Barsch", "Wels"]), {"Karpfen": 0, "Hecht": 0})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 611
