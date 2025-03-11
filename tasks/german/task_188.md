# Input
- Programmierkonzept: Integer;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Listen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Statistik

Schreibe eine Funktion namens `bewerte_spieler(punkte_liste)`, die eine Liste von erzielten Punkten eines Basketballspielers in verschiedenen Spielen erhält. Die Funktion soll die Leistung des Spielers bewerten und eine entsprechende Nachricht zurückgeben.

- Wenn der Spieler in einem Spiel mehr als 30 Punkte erzielt hat, soll die Nachricht "Hervorragende Leistung!" zurückgegeben werden.
- Wenn der Spieler in allen Spielen mindestens 10 Punkte erzielt hat, soll die Nachricht "Konstant gute Leistung!" zurückgegeben werden.
- Wenn der Spieler in keinem Spiel mehr als 5 Punkte erzielt hat, soll die Nachricht "Schwache Leistung!" zurückgegeben werden.
- In allen anderen Fällen soll die Nachricht "Durchschnittliche Leistung." zurückgegeben werden.

Beispielaufrufe:
- `bewerte_spieler([12, 15, 8, 22, 30])` gibt "Durchschnittliche Leistung." zurück.
- `bewerte_spieler([35, 28, 40, 22, 31])` gibt "Hervorragende Leistung!" zurück.
- `bewerte_spieler([10, 12, 14, 11, 10])` gibt "Konstant gute Leistung!" zurück.
- `bewerte_spieler([3, 4, 2, 5, 1])` gibt "Schwache Leistung!" zurück.

## Codegerüst
```python
def bewerte_spieler(punkte_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_spieler(punkte_liste):
    if any(p > 30 for p in punkte_liste):
        return "Hervorragende Leistung!"
    elif all(p >= 10 for p in punkte_liste):
        return "Konstant gute Leistung!"
    elif all(p <= 5 for p in punkte_liste):
        return "Schwache Leistung!"
    else:
        return "Durchschnittliche Leistung."

# Beispielaufrufe
print(bewerte_spieler([12, 15, 8, 22, 30]))
print(bewerte_spieler([35, 28, 40, 22, 31]))
print(bewerte_spieler([10, 12, 14, 11, 10]))
print(bewerte_spieler([3, 4, 2, 5, 1]))
```

## Unit Tests
```python
import unittest
from main import bewerte_spieler

class TestBewerteSpieler(unittest.TestCase):
    def test_hervorragende_leistung(self):
        self.assertEqual(bewerte_spieler([35, 28, 40, 22, 31]), "Hervorragende Leistung!")

    def test_konstant_gute_leistung(self):
        self.assertEqual(bewerte_spieler([10, 12, 14, 11, 10]), "Konstant gute Leistung!")

    def test_schwache_leistung(self):
        self.assertEqual(bewerte_spieler([3, 4, 2, 5, 1]), "Schwache Leistung!")

    def test_durchschnittliche_leistung(self):
        self.assertEqual(bewerte_spieler([12, 15, 8, 22, 30]), "Durchschnittliche Leistung.")

    def test_leere_liste(self):
        self.assertEqual(bewerte_spieler([]), "Durchschnittliche Leistung.")

    def test_grenzwert_30_punkte(self):
        self.assertEqual(bewerte_spieler([30, 30, 30]), "Durchschnittliche Leistung.")

    def test_grenzwert_10_punkte(self):
        self.assertEqual(bewerte_spieler([10, 10, 10]), "Konstant gute Leistung.")

    def test_grenzwert_5_punkte(self):
        self.assertEqual(bewerte_spieler([5, 5, 5]), "Schwache Leistung.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 620
