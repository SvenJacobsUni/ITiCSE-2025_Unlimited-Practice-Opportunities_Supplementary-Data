# Input
- Programmierkonzept: If-Else-Anweisungen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Spielerbewertung

Schreibe eine Funktion namens `bewerte_spieler(punkte)`, die die Leistung eines Basketballspielers basierend auf der Anzahl der erzielten Punkte bewertet. Die Funktion soll eine entsprechende Nachricht mit `return` zurückgeben.

- Wenn der Spieler 30 oder mehr Punkte erzielt hat, soll die Nachricht "Hervorragende Leistung!" zurückgegeben werden.
- Wenn der Spieler zwischen 20 und 29 Punkte erzielt hat, soll die Nachricht "Gute Leistung!" zurückgegeben werden.
- Wenn der Spieler zwischen 10 und 19 Punkte erzielt hat, soll die Nachricht "Durchschnittliche Leistung." zurückgegeben werden.
- Wenn der Spieler weniger als 10 Punkte erzielt hat, soll die Nachricht "Verbesserungswürdig." zurückgegeben werden.

Beispielaufrufe:
- `bewerte_spieler(35)` gibt "Hervorragende Leistung!" zurück.
- `bewerte_spieler(25)` gibt "Gute Leistung!" zurück.
- `bewerte_spieler(15)` gibt "Durchschnittliche Leistung." zurück.
- `bewerte_spieler(5)` gibt "Verbesserungswürdig." zurück.

## Codegerüst
```python
def bewerte_spieler(punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_spieler(punkte):
    if punkte >= 30:
        return "Hervorragende Leistung!"
    elif punkte >= 20:
        return "Gute Leistung!"
    elif punkte >= 10:
        return "Durchschnittliche Leistung."
    else:
        return "Verbesserungswürdig."

# Beispielaufrufe
print(bewerte_spieler(35))
print(bewerte_spieler(25))
print(bewerte_spieler(15))
print(bewerte_spieler(5))
```

## Unit Tests
```python
import unittest

from main import bewerte_spieler

class TestBewerteSpieler(unittest.TestCase):
    def test_hervorragende_leistung(self):
        self.assertEqual(bewerte_spieler(35), "Hervorragende Leistung!")
        self.assertEqual(bewerte_spieler(30), "Hervorragende Leistung!")

    def test_gute_leistung(self):
        self.assertEqual(bewerte_spieler(25), "Gute Leistung!")
        self.assertEqual(bewerte_spieler(20), "Gute Leistung!")

    def test_durchschnittliche_leistung(self):
        self.assertEqual(bewerte_spieler(15), "Durchschnittliche Leistung.")
        self.assertEqual(bewerte_spieler(10), "Durchschnittliche Leistung.")

    def test_verbesserungswuerdig(self):
        self.assertEqual(bewerte_spieler(5), "Verbesserungswürdig.")
        self.assertEqual(bewerte_spieler(0), "Verbesserungswürdig.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 425
