# Input
- Programmierkonzept: While-Schleifen;Rekursion;Operationen mit Zahlen
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Olympia-Medaillenzähler

Schreibe eine Funktion namens `medaillen_zaehler(anzahl_gold, anzahl_silber, anzahl_bronze)`, die die Gesamtzahl der Medaillen berechnet, die ein Land bei den Olympischen Spielen gewonnen hat. Die Funktion soll die Anzahl der Gold-, Silber- und Bronzemedaillen als Argumente entgegennehmen und die Gesamtzahl der Medaillen zurückgeben.

Zusätzlich soll die Funktion eine weitere Funktion `medaillen_zaehler_rekursiv(anzahl_gold, anzahl_silber, anzahl_bronze)` aufrufen, die die gleiche Berechnung rekursiv durchführt.

Beispielaufruf:
```python
medaillen_zaehler(10, 5, 8)
```
Dieser Aufruf sollte die Gesamtzahl der Medaillen zurückgeben, die das Land gewonnen hat.

## Codegerüst
```python
def medaillen_zaehler(anzahl_gold, anzahl_silber, anzahl_bronze):
    ## Hier Code einfügen

def medaillen_zaehler_rekursiv(anzahl_gold, anzahl_silber, anzahl_bronze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def medaillen_zaehler(anzahl_gold, anzahl_silber, anzahl_bronze):
    return anzahl_gold + anzahl_silber + anzahl_bronze

def medaillen_zaehler_rekursiv(anzahl_gold, anzahl_silber, anzahl_bronze):
    if anzahl_gold == 0 and anzahl_silber == 0 and anzahl_bronze == 0:
        return 0
    return (1 if anzahl_gold > 0 else 0) + (1 if anzahl_silber > 0 else 0) + (1 if anzahl_bronze > 0 else 0) + medaillen_zaehler_rekursiv(max(0, anzahl_gold-1), max(0, anzahl_silber-1), max(0, anzahl_bronze-1))

print(medaillen_zaehler(10, 5, 8))
print(medaillen_zaehler_rekursiv(10, 5, 8))
```

## Unit Tests
```python
import unittest
from main import medaillen_zaehler, medaillen_zaehler_rekursiv

class TestMedaillenZaehler(unittest.TestCase):
    def test_alle_medaillen(self):
        self.assertEqual(medaillen_zaehler(10, 5, 8), 23)
        self.assertEqual(medaillen_zaehler_rekursiv(10, 5, 8), 23)

    def test_keine_medaillen(self):
        self.assertEqual(medaillen_zaehler(0, 0, 0), 0)
        self.assertEqual(medaillen_zaehler_rekursiv(0, 0, 0), 0)

    def test_nur_gold(self):
        self.assertEqual(medaillen_zaehler(5, 0, 0), 5)
        self.assertEqual(medaillen_zaehler_rekursiv(5, 0, 0), 5)

    def test_nur_silber(self):
        self.assertEqual(medaillen_zaehler(0, 7, 0), 7)
        self.assertEqual(medaillen_zaehler_rekursiv(0, 7, 0), 7)

    def test_nur_bronze(self):
        self.assertEqual(medaillen_zaehler(0, 0, 3), 3)
        self.assertEqual(medaillen_zaehler_rekursiv(0, 0, 3), 3)

    def test_randbedingungen(self):
        self.assertEqual(medaillen_zaehler(1, 1, 1), 3)
        self.assertEqual(medaillen_zaehler_rekursiv(1, 1, 1), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 592
