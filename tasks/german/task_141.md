# Input
- Programmierkonzept: String;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Spielerbewertung

Schreibe eine Funktion namens `bewerte_spieler(punkte, assists, rebounds)`, die die Leistung eines Basketballspielers basierend auf seinen Spielstatistiken bewertet. Die Funktion soll drei Parameter entgegennehmen:

- `punkte`: Anzahl der erzielten Punkte (int)
- `assists`: Anzahl der Assists (int)
- `rebounds`: Anzahl der Rebounds (int)

Die Bewertung erfolgt nach folgenden Kriterien:

- Wenn der Spieler mehr als 20 Punkte erzielt hat und mehr als 5 Assists gegeben hat, soll die Funktion "Hervorragende Leistung!" zurückgeben.
- Wenn der Spieler mehr als 15 Punkte erzielt hat und mehr als 10 Rebounds geholt hat, soll die Funktion "Starke Leistung!" zurückgeben.
- Wenn der Spieler mehr als 10 Punkte erzielt hat oder mehr als 5 Assists gegeben hat, soll die Funktion "Gute Leistung!" zurückgeben.
- In allen anderen Fällen soll die Funktion "Durchschnittliche Leistung" zurückgeben.

Beispielaufrufe:

```python
bewerte_spieler(25, 6, 8)  # gibt "Hervorragende Leistung!" zurück
bewerte_spieler(18, 3, 12)  # gibt "Starke Leistung!" zurück
bewerte_spieler(12, 6, 4)  # gibt "Gute Leistung!" zurück
bewerte_spieler(8, 4, 3)  # gibt "Durchschnittliche Leistung" zurück
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
    elif punkte > 15 and rebounds > 10:
        return "Starke Leistung!"
    elif punkte > 10 or assists > 5:
        return "Gute Leistung!"
    else:
        return "Durchschnittliche Leistung"

# Beispielaufrufe
print(bewerte_spieler(25, 6, 8))  # Hervorragende Leistung!
print(bewerte_spieler(18, 3, 12))  # Starke Leistung!
print(bewerte_spieler(12, 6, 4))  # Gute Leistung!
print(bewerte_spieler(8, 4, 3))  # Durchschnittliche Leistung
```

## Unit Tests
```python
import unittest
from main import bewerte_spieler

class TestBewerteSpieler(unittest.TestCase):
    def test_hervorragende_leistung(self):
        self.assertEqual(bewerte_spieler(25, 6, 8), "Hervorragende Leistung!")

    def test_starke_leistung(self):
        self.assertEqual(bewerte_spieler(18, 3, 12), "Starke Leistung!")

    def test_gute_leistung_punkte(self):
        self.assertEqual(bewerte_spieler(12, 4, 4), "Gute Leistung!")

    def test_gute_leistung_assists(self):
        self.assertEqual(bewerte_spieler(8, 6, 3), "Gute Leistung!")

    def test_durchschnittliche_leistung(self):
        self.assertEqual(bewerte_spieler(8, 4, 3), "Durchschnittliche Leistung")

    def test_grenzwert_hervorragende_leistung(self):
        self.assertEqual(bewerte_spieler(21, 6, 5), "Hervorragende Leistung!")

    def test_grenzwert_starke_leistung(self):
        self.assertEqual(bewerte_spieler(16, 4, 11), "Starke Leistung!")

    def test_grenzwert_gute_leistung(self):
        self.assertEqual(bewerte_spieler(11, 6, 4), "Gute Leistung!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 573
