# Input
- Programmierkonzept: Tupel
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Angeln mit Tupeln

Schreibe eine Funktion namens `fisch_fangen(fische)`, die ein Tupel von Fischarten als Argument erhält. Die Funktion soll die Anzahl der verschiedenen Fischarten im Tupel zählen und ein neues Tupel zurückgeben, das die Fischarten und ihre jeweiligen Häufigkeiten enthält.

Beispielaufruf:
```python
fische = ("Hecht", "Karpfen", "Hecht", "Forelle", "Karpfen", "Hecht")
print(fisch_fangen(fische))
```

Erwartete Ausgabe:
```python
(("Hecht", 3), ("Karpfen", 2), ("Forelle", 1))
```

## Codegerüst
```python
def fisch_fangen(fische):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fisch_fangen(fische):
    return tuple((fisch, fische.count(fisch)) for fisch in set(fische))

fische = ("Hecht", "Karpfen", "Hecht", "Forelle", "Karpfen", "Hecht")
print(fisch_fangen(fische))
```

## Unit Tests
```python
import unittest
from main import fisch_fangen

class TestFischFangen(unittest.TestCase):
    def test_einfacher_fall(self):
        fische = ("Hecht", "Karpfen", "Hecht", "Forelle", "Karpfen", "Hecht")
        erwartet = (("Hecht", 3), ("Karpfen", 2), ("Forelle", 1))
        self.assertEqual(fisch_fangen(fische), erwartet)

    def test_leeres_tupel(self):
        fische = ()
        erwartet = ()
        self.assertEqual(fisch_fangen(fische), erwartet)

    def test_ein_fisch(self):
        fische = ("Hecht",)
        erwartet = (("Hecht", 1),)
        self.assertEqual(fisch_fangen(fische), erwartet)

    def test_alle_unterschiedlich(self):
        fische = ("Hecht", "Karpfen", "Forelle")
        erwartet = (("Hecht", 1), ("Karpfen", 1), ("Forelle", 1))
        self.assertEqual(fisch_fangen(fische), erwartet)

    def test_gleiche_fische(self):
        fische = ("Hecht", "Hecht", "Hecht")
        erwartet = (("Hecht", 3),)
        self.assertEqual(fisch_fangen(fische), erwartet)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 442
