# Input
- Programmierkonzept: Funktionen als Variablen;Integer;Rekursion
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Psychische Gesundheit - Rekursive Berechnung des Wohlbefindens

Schreibe eine Funktion namens `berechne_wohlbefinden(tage)`, die das Wohlbefinden einer Person über eine bestimmte Anzahl von Tagen berechnet. Das Wohlbefinden wird durch eine einfache rekursive Formel definiert:

- An einem bestimmten Tag `n` ist das Wohlbefinden die Summe des Wohlbefindens der beiden vorherigen Tage `n-1` und `n-2`.
- Das Wohlbefinden am ersten Tag (`n=1`) beträgt 1.
- Das Wohlbefinden am zweiten Tag (`n=2`) beträgt 1.

Die Funktion soll die Anzahl der Tage `tage` als Argument nehmen und das Wohlbefinden am letzten Tag zurückgeben.

Beispielaufruf: `berechne_wohlbefinden(5)` gibt `5` zurück.

### Kontext

In der Psychologie wird oft untersucht, wie sich das Wohlbefinden einer Person über die Zeit entwickelt. Diese Aufgabe simuliert eine einfache Modellierung des Wohlbefindens, bei der das Wohlbefinden an einem bestimmten Tag von den vorherigen Tagen abhängt.

## Codegerüst
```python
def berechne_wohlbefinden(tage):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_wohlbefinden(tage):
    if tage <= 2:
        return 1
    return berechne_wohlbefinden(tage-1) + berechne_wohlbefinden(tage-2)

print(berechne_wohlbefinden(5))
```

## Unit Tests
```python
import unittest
from main import berechne_wohlbefinden

class TestBerechneWohlbefinden(unittest.TestCase):
    def test_wohlbefinden_tag_1(self):
        self.assertEqual(berechne_wohlbefinden(1), 1)

    def test_wohlbefinden_tag_2(self):
        self.assertEqual(berechne_wohlbefinden(2), 1)

    def test_wohlbefinden_tag_3(self):
        self.assertEqual(berechne_wohlbefinden(3), 2)

    def test_wohlbefinden_tag_5(self):
        self.assertEqual(berechne_wohlbefinden(5), 5)

    def test_wohlbefinden_tag_10(self):
        self.assertEqual(berechne_wohlbefinden(10), 55)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 593
