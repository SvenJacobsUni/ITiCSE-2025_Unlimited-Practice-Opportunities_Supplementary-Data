# Input
- Programmierkonzept: Rekursion;Float;Integer
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Berechnung der Medaillenpunkte

In den Olympischen Spielen werden Medaillen in Gold, Silber und Bronze vergeben. Jede Medaille hat einen bestimmten Punktwert:

- Gold: 3 Punkte
- Silber: 2 Punkte
- Bronze: 1 Punkt

Schreibe eine rekursive Funktion `berechne_medaillenpunkte(gold, silber, bronze)`, die die Gesamtpunktzahl für eine Nation basierend auf der Anzahl der gewonnenen Medaillen berechnet. Die Parameter `gold`, `silber` und `bronze` sind Ganzzahlen (Integer), die die Anzahl der jeweiligen Medaillen angeben. Die Funktion soll die Gesamtpunktzahl als Fließkommazahl (Float) zurückgeben.

Beispielaufruf:
```python
punkte = berechne_medaillenpunkte(5, 3, 2)
print(punkte)  # Ausgabe: 21.0
```

Implementiere die Funktion so, dass sie rekursiv arbeitet.

## Codegerüst
```python
def berechne_medaillenpunkte(gold, silber, bronze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_medaillenpunkte(gold, silber, bronze):
    if gold == 0 and silber == 0 and bronze == 0:
        return 0.0
    if gold > 0:
        return 3.0 + berechne_medaillenpunkte(gold - 1, silber, bronze)
    if silber > 0:
        return 2.0 + berechne_medaillenpunkte(gold, silber - 1, bronze)
    return 1.0 + berechne_medaillenpunkte(gold, silber, bronze - 1)

punkte = berechne_medaillenpunkte(5, 3, 2)
print(punkte)  # Ausgabe: 21.0
```

## Unit Tests
```python
import unittest
from main import berechne_medaillenpunkte

class TestBerechneMedaillenpunkte(unittest.TestCase):
    def test_keine_medaillen(self):
        self.assertEqual(berechne_medaillenpunkte(0, 0, 0), 0.0)

    def test_nur_gold(self):
        self.assertEqual(berechne_medaillenpunkte(5, 0, 0), 15.0)

    def test_nur_silber(self):
        self.assertEqual(berechne_medaillenpunkte(0, 3, 0), 6.0)

    def test_nur_bronze(self):
        self.assertEqual(berechne_medaillenpunkte(0, 0, 2), 2.0)

    def test_gemischte_medaillen(self):
        self.assertEqual(berechne_medaillenpunkte(5, 3, 2), 21.0)

    def test_randbedingung(self):
        self.assertEqual(berechne_medaillenpunkte(1, 1, 1), 6.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 617
