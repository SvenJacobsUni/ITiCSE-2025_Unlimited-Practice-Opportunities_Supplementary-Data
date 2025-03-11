# Input
- Programmierkonzept: For-Schleifen;Rekursion;Operationen mit Zahlen
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Punkteberechnung

Schreibe eine Funktion namens `punkte_berechnung(spieler_punkte)`, die eine Liste von Punkten, die verschiedene Spieler in einem Turnier erzielt haben, als Argument erhält. Die Funktion soll die Gesamtpunktzahl aller Spieler berechnen und zurückgeben. Verwende eine For-Schleife, um die Punkte zu summieren. Implementiere zusätzlich eine rekursive Funktion `max_punkte(punkte_liste)`, die die höchste Punktzahl in der Liste findet und zurückgibt.

Beispielaufruf:
```python
spieler_punkte = [10, 20, 15, 30, 25]
gesamtpunkte = punkte_berechnung(spieler_punkte)
hoechste_punktzahl = max_punkte(spieler_punkte)
print("Gesamtpunkte:", gesamtpunkte)  # Ausgabe: Gesamtpunkte: 100
print("Höchste Punktzahl:", hoechste_punktzahl)  # Ausgabe: Höchste Punktzahl: 30
```

## Codegerüst
```python
def punkte_berechnung(spieler_punkte):
    ## Hier Code einfügen

def max_punkte(punkte_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def punkte_berechnung(spieler_punkte):
    return sum(spieler_punkte)

def max_punkte(punkte_liste):
    if len(punkte_liste) == 1:
        return punkte_liste[0]
    else:
        max_rest = max_punkte(punkte_liste[1:])
        return punkte_liste[0] if punkte_liste[0] > max_rest else max_rest

spieler_punkte = [10, 20, 15, 30, 25]
gesamtpunkte = punkte_berechnung(spieler_punkte)
hoechste_punktzahl = max_punkte(spieler_punkte)
print("Gesamtpunkte:", gesamtpunkte)
print("Höchste Punktzahl:", hoechste_punktzahl)
```

## Unit Tests
```python
import unittest
from main import punkte_berechnung, max_punkte

class TestPunkteBerechnung(unittest.TestCase):
    def test_gesamtpunkte(self):
        self.assertEqual(punkte_berechnung([10, 20, 15, 30, 25]), 100)
        self.assertEqual(punkte_berechnung([0, 0, 0, 0]), 0)
        self.assertEqual(punkte_berechnung([5, 5, 5, 5, 5]), 25)
        self.assertEqual(punkte_berechnung([-10, 20, -15, 30, -25]), 0)
        self.assertEqual(punkte_berechnung([100]), 100)

    def test_max_punkte(self):
        self.assertEqual(max_punkte([10, 20, 15, 30, 25]), 30)
        self.assertEqual(max_punkte([0, 0, 0, 0]), 0)
        self.assertEqual(max_punkte([5, 5, 5, 5, 5]), 5)
        self.assertEqual(max_punkte([-10, 20, -15, 30, -25]), 30)
        self.assertEqual(max_punkte([100]), 100)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 613
