# Input
- Programmierkonzept: Integer;Listen;String
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Spieler Statistik

Schreibe eine Funktion namens `spieler_statistik(spieler_liste)`, die eine Liste von Spielernamen und deren erzielten Punkte in einem Rugby-Spiel erhält. Die Liste enthält Strings im Format "Name:Punkte", wobei "Name" der Name des Spielers und "Punkte" die erzielten Punkte als Integer sind.

Die Funktion soll die folgenden Aufgaben erfüllen:
1. Die Gesamtpunktzahl aller Spieler berechnen und zurückgeben.
2. Den Namen des Spielers mit den meisten Punkten zurückgeben. Falls mehrere Spieler die gleiche höchste Punktzahl haben, soll der erste in der Liste zurückgegeben werden.

Beispielaufruf:
```python
spieler_liste = ["Max:5", "Anna:3", "Tom:7", "Lisa:7"]
gesamtpunkte, bester_spieler = spieler_statistik(spieler_liste)
print(gesamtpunkte)  # Ausgabe: 22
print(bester_spieler)  # Ausgabe: Tom
```

Implementiere die Funktion `spieler_statistik(spieler_liste)`, um die oben genannten Anforderungen zu erfüllen.

## Codegerüst
```python
def spieler_statistik(spieler_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spieler_statistik(spieler_liste):
    gesamtpunkte = 0
    bester_spieler = ""
    max_punkte = -1
    for eintrag in spieler_liste:
        name, punkte = eintrag.split(":")
        punkte = int(punkte)
        gesamtpunkte += punkte
        if punkte > max_punkte:
            max_punkte = punkte
            bester_spieler = name
    return gesamtpunkte, bester_spieler

spieler_liste = ["Max:5", "Anna:3", "Tom:7", "Lisa:7"]
gesamtpunkte, bester_spieler = spieler_statistik(spieler_liste)
print(gesamtpunkte)  # Ausgabe: 22
print(bester_spieler)  # Ausgabe: Tom
```

## Unit Tests
```python
import unittest

from main import spieler_statistik

class TestSpielerStatistik(unittest.TestCase):
    def test_einfacher_fall(self):
        spieler_liste = ["Max:5", "Anna:3", "Tom:7", "Lisa:7"]
        gesamtpunkte, bester_spieler = spieler_statistik(spieler_liste)
        self.assertEqual(gesamtpunkte, 22)
        self.assertEqual(bester_spieler, "Tom")

    def test_alle_spieler_gleiche_punkte(self):
        spieler_liste = ["Max:5", "Anna:5", "Tom:5", "Lisa:5"]
        gesamtpunkte, bester_spieler = spieler_statistik(spieler_liste)
        self.assertEqual(gesamtpunkte, 20)
        self.assertEqual(bester_spieler, "Max")

    def test_ein_spieler(self):
        spieler_liste = ["Max:10"]
        gesamtpunkte, bester_spieler = spieler_statistik(spieler_liste)
        self.assertEqual(gesamtpunkte, 10)
        self.assertEqual(bester_spieler, "Max")

    def test_leere_liste(self):
        spieler_liste = []
        gesamtpunkte, bester_spieler = spieler_statistik(spieler_liste)
        self.assertEqual(gesamtpunkte, 0)
        self.assertEqual(bester_spieler, "")

    def test_negativ_punkte(self):
        spieler_liste = ["Max:-5", "Anna:3", "Tom:7", "Lisa:7"]
        gesamtpunkte, bester_spieler = spieler_statistik(spieler_liste)
        self.assertEqual(gesamtpunkte, 12)
        self.assertEqual(bester_spieler, "Tom")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 622
