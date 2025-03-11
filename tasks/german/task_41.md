# Input
- Programmierkonzept: Rekursion
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Medaillenzählung

Schreibe eine rekursive Funktion namens `medaillen_zaehlen(medaillen)`, die die Gesamtzahl der Medaillen berechnet, die ein Land bei den Olympischen Spielen gewonnen hat. Die Medaillen werden in einer Liste übergeben, wobei jede Medaille als ein String ("Gold", "Silber" oder "Bronze") repräsentiert wird.

Beispielaufruf:
```python
medaillen = ["Gold", "Silber", "Bronze", "Gold", "Silber"]
print(medaillen_zaehlen(medaillen))  # Ausgabe: 5
```

Implementiere die Funktion so, dass sie rekursiv arbeitet.

## Codegerüst
```python
def medaillen_zaehlen(medaillen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def medaillen_zaehlen(medaillen):
    if not medaillen:
        return 0
    return 1 + medaillen_zaehlen(medaillen[1:])

medaillen = ["Gold", "Silber", "Bronze", "Gold", "Silber"]
print(medaillen_zaehlen(medaillen))  # Ausgabe: 5
```

## Unit Tests
```python
import unittest
from main import medaillen_zaehlen

class TestMedaillenZaehlen(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(medaillen_zaehlen([]), 0)

    def test_eine_medaille(self):
        self.assertEqual(medaillen_zaehlen(["Gold"]), 1)

    def test_mehrere_medaille(self):
        self.assertEqual(medaillen_zaehlen(["Gold", "Silber", "Bronze", "Gold", "Silber"]), 5)

    def test_nur_gold(self):
        self.assertEqual(medaillen_zaehlen(["Gold", "Gold", "Gold"]), 3)

    def test_nur_silber(self):
        self.assertEqual(medaillen_zaehlen(["Silber", "Silber"]), 2)

    def test_nur_bronze(self):
        self.assertEqual(medaillen_zaehlen(["Bronze"]), 1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 459
