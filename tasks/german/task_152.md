# Input
- Programmierkonzept: Operationen mit Zahlen;String;Float
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Olympia-Medaillenrechner

Schreibe eine Funktion namens `medaillen_rechner(gold, silber, bronze)`, die die Gesamtpunktzahl eines Landes bei den Olympischen Spielen berechnet. Die Punkteverteilung ist wie folgt:

- Goldmedaille: 3 Punkte
- Silbermedaille: 2 Punkte
- Bronzemedaille: 1 Punkt

Die Funktion soll die Gesamtpunktzahl berechnen und als Fließkommazahl (Float) zurückgeben. 

Beispielaufruf: 
```python
medaillen_rechner(5, 3, 2)
```
Dieser Aufruf sollte die Gesamtpunktzahl für 5 Gold-, 3 Silber- und 2 Bronzemedaillen berechnen und zurückgeben.

## Codegerüst
```python
def medaillen_rechner(gold, silber, bronze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def medaillen_rechner(gold, silber, bronze):
    return float(3 * gold + 2 * silber + 1 * bronze)

print(medaillen_rechner(5, 3, 2))
```

## Unit Tests
```python
import unittest
from main import medaillen_rechner

class TestMedaillenRechner(unittest.TestCase):
    def test_alle_medaillen(self):
        self.assertEqual(medaillen_rechner(5, 3, 2), 5*3 + 3*2 + 2*1)

    def test_keine_medaillen(self):
        self.assertEqual(medaillen_rechner(0, 0, 0), 0.0)

    def test_nur_gold(self):
        self.assertEqual(medaillen_rechner(10, 0, 0), 10*3)

    def test_nur_silber(self):
        self.assertEqual(medaillen_rechner(0, 10, 0), 10*2)

    def test_nur_bronze(self):
        self.assertEqual(medaillen_rechner(0, 0, 10), 10*1)

    def test_mixed_medaillen(self):
        self.assertEqual(medaillen_rechner(1, 1, 1), 3 + 2 + 1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 584
