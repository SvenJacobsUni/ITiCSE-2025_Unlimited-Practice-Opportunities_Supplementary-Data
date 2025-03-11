# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Gartenarbeit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung in der Gartenarbeit

Schreibe eine Funktion namens `pflanzen_verwalten(pflanzen_liste, funktion)`, die eine Liste von Pflanzen und eine Funktion als Argumente entgegennimmt. Die Funktion `pflanzen_verwalten` soll die übergebene Funktion auf jede Pflanze in der Liste anwenden und die Ergebnisse in einer neuen Liste zurückgeben.

Beispielaufruf:
```python
def pflanze_beschreiben(pflanze):
    return f"Die Pflanze {pflanze} wächst gut im Garten."

pflanzen = ["Tomate", "Gurke", "Zucchini"]
ergebnisse = pflanzen_verwalten(pflanzen, pflanze_beschreiben)
print(ergebnisse)
```

Erwartete Ausgabe:
```
['Die Pflanze Tomate wächst gut im Garten.', 'Die Pflanze Gurke wächst gut im Garten.', 'Die Pflanze Zucchini wächst gut im Garten.']
```

Implementiere die Funktion `pflanzen_verwalten` so, dass sie die übergebene Funktion auf jede Pflanze in der Liste anwendet und die Ergebnisse in einer neuen Liste zurückgibt.

## Codegerüst
```python
def pflanzen_verwalten(pflanzen_liste, funktion):
    ## Hier Code einfügen
```

## Musterlösung
```python
def pflanzen_verwalten(pflanzen_liste, funktion):
    return [funktion(pflanze) for pflanze in pflanzen_liste]

def pflanze_beschreiben(pflanze):
    return f"Die Pflanze {pflanze} wächst gut im Garten."

pflanzen = ["Tomate", "Gurke", "Zucchini"]
ergebnisse = pflanzen_verwalten(pflanzen, pflanze_beschreiben)
print(ergebnisse)
```

## Unit Tests
```python
import unittest
from main import pflanzen_verwalten

def pflanze_beschreiben(pflanze):
    return f"Die Pflanze {pflanze} wächst gut im Garten."

class TestPflanzenVerwalten(unittest.TestCase):
    def test_einfache_liste(self):
        pflanzen = ["Tomate", "Gurke", "Zucchini"]
        erwartet = [
            "Die Pflanze Tomate wächst gut im Garten.",
            "Die Pflanze Gurke wächst gut im Garten.",
            "Die Pflanze Zucchini wächst gut im Garten."
        ]
        self.assertEqual(pflanzen_verwalten(pflanzen, pflanze_beschreiben), erwartet)

    def test_leere_liste(self):
        pflanzen = []
        erwartet = []
        self.assertEqual(pflanzen_verwalten(pflanzen, pflanze_beschreiben), erwartet)

    def test_eine_pflanze(self):
        pflanzen = ["Tomate"]
        erwartet = ["Die Pflanze Tomate wächst gut im Garten."]
        self.assertEqual(pflanzen_verwalten(pflanzen, pflanze_beschreiben), erwartet)

    def test_verschiedene_pflanzen(self):
        pflanzen = ["Tomate", "Gurke", "Zucchini", "Paprika"]
        erwartet = [
            "Die Pflanze Tomate wächst gut im Garten.",
            "Die Pflanze Gurke wächst gut im Garten.",
            "Die Pflanze Zucchini wächst gut im Garten.",
            "Die Pflanze Paprika wächst gut im Garten."
        ]
        self.assertEqual(pflanzen_verwalten(pflanzen, pflanze_beschreiben), erwartet)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 513
