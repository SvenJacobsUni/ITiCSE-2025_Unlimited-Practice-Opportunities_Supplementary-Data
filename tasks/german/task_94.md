# Input
- Programmierkonzept: Float
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Punktestand

Schreibe eine Funktion namens `berechne_punktestand(tries, conversions, penalties)`, die den Punktestand eines Rugby-Spiels berechnet. 

- Ein Try (Versuch) zählt 5 Punkte.
- Eine Conversion (Erhöhung) zählt 2 Punkte.
- Ein Penalty (Straftritt) zählt 3 Punkte.

Die Funktion soll drei Parameter entgegennehmen:
- `tries` (float): Anzahl der erzielten Tries.
- `conversions` (float): Anzahl der erzielten Conversions.
- `penalties` (float): Anzahl der erzielten Penalties.

Die Funktion soll den gesamten Punktestand als float zurückgeben.

Beispielaufruf:
```python
berechne_punktestand(3.0, 2.0, 1.0)
```
Dieser Aufruf sollte den Wert `21.0` zurückgeben.

## Codegerüst
```python
def berechne_punktestand(tries, conversions, penalties):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punktestand(tries, conversions, penalties):
    return tries * 5 + conversions * 2 + penalties * 3

print(berechne_punktestand(3.0, 2.0, 1.0))
```

## Unit Tests
```python
import unittest

from main import berechne_punktestand

class TestBerechnePunktestand(unittest.TestCase):
    def test_alle_arten_von_punkten(self):
        self.assertEqual(berechne_punktestand(3.0, 2.0, 1.0), 21.0)

    def test_nur_tries(self):
        self.assertEqual(berechne_punktestand(4.0, 0.0, 0.0), 20.0)

    def test_nur_conversions(self):
        self.assertEqual(berechne_punktestand(0.0, 3.0, 0.0), 6.0)

    def test_nur_penalties(self):
        self.assertEqual(berechne_punktestand(0.0, 0.0, 5.0), 15.0)

    def test_keine_punkte(self):
        self.assertEqual(berechne_punktestand(0.0, 0.0, 0.0), 0.0)

    def test_gemischte_punkte(self):
        self.assertEqual(berechne_punktestand(2.0, 3.0, 4.0), 25.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 512
