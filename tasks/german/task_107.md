# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);If-Else-Anweisungen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Spielerbewertung

Schreibe eine Funktion namens `bewerte_spieler(punkte, assists, rebounds)`, die die Leistung eines Basketballspielers basierend auf seinen Statistiken bewertet. Die Funktion soll drei Parameter entgegennehmen:

- `punkte`: Anzahl der erzielten Punkte
- `assists`: Anzahl der Assists
- `rebounds`: Anzahl der Rebounds

Die Bewertung erfolgt nach folgenden Kriterien:

- Wenn der Spieler mehr als 20 Punkte erzielt hat und mehr als 5 Assists gegeben hat, soll die Funktion "Hervorragende Leistung!" zurückgeben.
- Wenn der Spieler mehr als 15 Punkte erzielt hat oder mehr als 10 Rebounds gesammelt hat, soll die Funktion "Gute Leistung!" zurückgeben.
- Wenn der Spieler weniger als 5 Punkte erzielt hat und weniger als 3 Assists gegeben hat, soll die Funktion "Schwache Leistung!" zurückgeben.
- In allen anderen Fällen soll die Funktion "Durchschnittliche Leistung" zurückgeben.

Beispielaufrufe:

```python
bewerte_spieler(25, 6, 8)  # gibt "Hervorragende Leistung!" zurück
bewerte_spieler(18, 4, 11)  # gibt "Gute Leistung!" zurück
bewerte_spieler(4, 2, 5)    # gibt "Schwache Leistung!" zurück
bewerte_spieler(10, 4, 7)   # gibt "Durchschnittliche Leistung" zurück
```

## Codegerüst
```python
def bewerte_spieler(punkte, assists, rebounds):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_spieler(punkte, assists, rebounds):
    if punkte > 20 and assists > 5:
        return "Hervorragende Leistung!"
    elif punkte > 15 or rebounds > 10:
        return "Gute Leistung!"
    elif punkte < 5 and assists < 3:
        return "Schwache Leistung!"
    else:
        return "Durchschnittliche Leistung"

# Beispielaufrufe
print(bewerte_spieler(25, 6, 8))  # Hervorragende Leistung!
print(bewerte_spieler(18, 4, 11))  # Gute Leistung!
print(bewerte_spieler(4, 2, 5))    # Schwache Leistung!
print(bewerte_spieler(10, 4, 7))   # Durchschnittliche Leistung
```

## Unit Tests
```python
import unittest

from main import bewerte_spieler

class TestBewerteSpieler(unittest.TestCase):
    def test_hervorragende_leistung(self):
        self.assertEqual(bewerte_spieler(25, 6, 8), "Hervorragende Leistung!")

    def test_gute_leistung_punkte(self):
        self.assertEqual(bewerte_spieler(18, 4, 11), "Gute Leistung!")

    def test_gute_leistung_rebounds(self):
        self.assertEqual(bewerte_spieler(10, 4, 11), "Gute Leistung!")

    def test_schwache_leistung(self):
        self.assertEqual(bewerte_spieler(4, 2, 5), "Schwache Leistung!")

    def test_durchschnittliche_leistung(self):
        self.assertEqual(bewerte_spieler(10, 4, 7), "Durchschnittliche Leistung")

    def test_grenzfall_hervorragende_leistung(self):
        self.assertEqual(bewerte_spieler(21, 6, 8), "Durchschnittliche Leistung")

    def test_grenzfall_gute_leistung(self):
        self.assertEqual(bewerte_spieler(16, 4, 10), "Gute Leistung!")

    def test_grenzfall_schwache_leistung(self):
        self.assertEqual(bewerte_spieler(5, 2, 5), "Durchschnittliche Leistung")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 539
