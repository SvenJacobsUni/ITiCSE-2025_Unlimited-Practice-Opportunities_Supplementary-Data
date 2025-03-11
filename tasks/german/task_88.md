# Input
- Programmierkonzept: Integer
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Punktzahlberechnung

Schreibe eine Funktion namens `berechne_punkte(tore, assists)`, die die Gesamtpunktzahl eines Spielers in einem Fußballspiel berechnet. Dabei erhält der Spieler 3 Punkte für jedes erzielte Tor und 1 Punkt für jede Vorlage (Assist). Die Funktion soll die Gesamtpunktzahl als Integer zurückgeben.

Beispielaufruf:
```python
berechne_punkte(2, 3)
```
Dieser Aufruf sollte 9 zurückgeben, da der Spieler 2 Tore (2 * 3 = 6 Punkte) und 3 Assists (3 * 1 = 3 Punkte) erzielt hat, was insgesamt 9 Punkte ergibt.

## Codegerüst
```python
def berechne_punkte(tore, assists):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punkte(tore, assists):
    return tore * 3 + assists

# Beispielaufruf
print(berechne_punkte(2, 3))
```

## Unit Tests
```python
import unittest

from main import berechne_punkte

class TestBerechnePunkte(unittest.TestCase):
    def test_keine_tore_und_assists(self):
        self.assertEqual(berechne_punkte(0, 0), 0)

    def test_nur_tore(self):
        self.assertEqual(berechne_punkte(3, 0), 9)

    def test_nur_assists(self):
        self.assertEqual(berechne_punkte(0, 4), 4)

    def test_tore_und_assists(self):
        self.assertEqual(berechne_punkte(2, 3), 9)

    def test_grosse_zahlen(self):
        self.assertEqual(berechne_punkte(100, 200), 500)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 506
