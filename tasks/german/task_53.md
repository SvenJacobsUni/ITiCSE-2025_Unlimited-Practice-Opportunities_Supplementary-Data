# Input
- Programmierkonzept: While-Schleifen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Training

Schreibe eine Funktion namens `basketball_training(ziel_punkte)`, die eine While-Schleife verwendet, um die Anzahl der benötigten Würfe zu berechnen, bis ein Spieler eine bestimmte Anzahl von Punkten erreicht hat. Jeder erfolgreiche Wurf zählt 2 Punkte. Die Funktion soll die Anzahl der Würfe zurückgeben.

Beispielaufruf: `basketball_training(10)` gibt `5` zurück, da 5 erfolgreiche Würfe benötigt werden, um 10 Punkte zu erreichen.

## Codegerüst
```python
def basketball_training(ziel_punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def basketball_training(ziel_punkte):
    punkte, würfe = 0, 0
    while punkte < ziel_punkte:
        punkte += 2
        würfe += 1
    print(würfe)

basketball_training(10)
```

## Unit Tests
```python
import unittest
from main import basketball_training

class TestBasketballTraining(unittest.TestCase):
    def test_zehn_punkte(self):
        self.assertEqual(basketball_training(10), 5)

    def test_null_punkte(self):
        self.assertEqual(basketball_training(0), 0)

    def test_ungerade_punkte(self):
        self.assertEqual(basketball_training(7), 4)

    def test_grosse_punktezahl(self):
        self.assertEqual(basketball_training(100), 50)

    def test_negative_punkte(self):
        self.assertEqual(basketball_training(-5), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 471
