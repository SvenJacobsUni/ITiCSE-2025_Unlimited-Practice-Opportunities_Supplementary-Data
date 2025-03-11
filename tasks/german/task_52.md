# Input
- Programmierkonzept: Operationen mit Zahlen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Punktestand berechnen

Schreibe eine Funktion namens `berechne_punktestand(zweier, dreier)`, die den Punktestand eines Basketballspiels basierend auf der Anzahl der erzielten Zweipunkte- und Dreipunktewürfe berechnet. Die Funktion soll zwei Argumente entgegennehmen:

- `zweier`: Die Anzahl der erzielten Zweipunktewürfe.
- `dreier`: Die Anzahl der erzielten Dreipunktewürfe.

Die Funktion soll den gesamten Punktestand berechnen und zurückgeben.

Beispielaufruf:
```python
punktestand = berechne_punktestand(10, 5)
print(punktestand)  # Ausgabe: 35
```

In diesem Beispiel wurden 10 Zweipunktewürfe (10 * 2 = 20 Punkte) und 5 Dreipunktewürfe (5 * 3 = 15 Punkte) erzielt, was insgesamt 35 Punkte ergibt.

## Codegerüst
```python
def berechne_punktestand(zweier, dreier):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punktestand(zweier, dreier):
    return zweier * 2 + dreier * 3

print(berechne_punktestand(10, 5))  # Ausgabe: 35
```

## Unit Tests
```python
import unittest
from main import berechne_punktestand

class TestBerechnePunktestand(unittest.TestCase):
    def test_kein_punkt(self):
        self.assertEqual(berechne_punktestand(0, 0), 0)

    def test_nur_zweier(self):
        self.assertEqual(berechne_punktestand(10, 0), 20)

    def test_nur_dreier(self):
        self.assertEqual(berechne_punktestand(0, 5), 15)

    def test_gemischt(self):
        self.assertEqual(berechne_punktestand(10, 5), 35)

    def test_grosse_zahlen(self):
        self.assertEqual(berechne_punktestand(1000, 500), 3500)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 470
