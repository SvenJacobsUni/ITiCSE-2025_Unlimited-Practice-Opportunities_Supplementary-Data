# Input
- Programmierkonzept: String;Integer;For-Schleifen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Fische zählen

Schreibe eine Funktion namens `zaehle_fische(fischarten)`, die eine Liste von Strings als Argument erhält. Jeder String in der Liste repräsentiert eine Fischart, die an einem Tag gefangen wurde. Die Funktion soll die Anzahl der Fische jeder Art zählen und das Ergebnis als Dictionary zurückgeben, wobei die Fischart der Schlüssel und die Anzahl der gefangenen Fische der Wert ist.

Beispielaufruf:
```python
fischarten = ["Hecht", "Karpfen", "Hecht", "Forelle", "Karpfen", "Hecht"]
print(zaehle_fische(fischarten))
```

Erwartete Ausgabe:
```python
{"Hecht": 3, "Karpfen": 2, "Forelle": 1}
```

## Codegerüst
```python
def zaehle_fische(fischarten):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(fischarten):
    zaehlung = {}
    for fisch in fischarten:
        if fisch in zaehlung:
            zaehlung[fisch] += 1
        else:
            zaehlung[fisch] = 1
    return zaehlung

fischarten = ["Hecht", "Karpfen", "Hecht", "Forelle", "Karpfen", "Hecht"]
print(zaehle_fische(fischarten))
```

## Unit Tests
```python
import unittest
from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Hecht", "Forelle", "Karpfen", "Hecht"]), {"Hecht": 3, "Karpfen": 2, "Forelle": 1})

    def test_leere_liste(self):
        self.assertEqual(zaehle_fische([]), {})

    def test_eine_fischart(self):
        self.assertEqual(zaehle_fische(["Hecht", "Hecht", "Hecht"]), {"Hecht": 3})

    def test_verschiedene_fischarten(self):
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Forelle"]), {"Hecht": 1, "Karpfen": 1, "Forelle": 1})

    def test_gemischte_fischarten(self):
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Hecht", "Forelle", "Karpfen", "Hecht", "Forelle", "Forelle"]), {"Hecht": 3, "Karpfen": 2, "Forelle": 3})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 616
