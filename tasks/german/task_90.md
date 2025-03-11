# Input
- Programmierkonzept: For-Schleifen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Fische zählen

Schreibe eine Funktion namens `zaehle_fische(fische_liste)`, die eine Liste von Fischen als Eingabe erhält und die Anzahl der Fische in der Liste zählt. Die Funktion soll die Anzahl der Fische mit `return` zurückgeben.

Beispielaufruf:
```python
fische = ["Hecht", "Karpfen", "Forelle", "Hecht", "Barsch"]
anzahl = zaehle_fische(fische)
print(anzahl)  # Ausgabe: 5
```

Verwende eine For-Schleife, um die Anzahl der Fische in der Liste zu ermitteln.

## Codegerüst
```python
def zaehle_fische(fische_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(fische_liste):
    return len(fische_liste)

fische = ["Hecht", "Karpfen", "Forelle", "Hecht", "Barsch"]
anzahl = zaehle_fische(fische)
print(anzahl)  # Ausgabe: 5
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
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Forelle", "Hecht", "Barsch"]), 5)

    def test_alle_gleichen_fische(self):
        self.assertEqual(zaehle_fische(["Hecht", "Hecht", "Hecht"]), 3)

    def test_verschiedene_fische(self):
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Forelle", "Barsch", "Zander"]), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 508
