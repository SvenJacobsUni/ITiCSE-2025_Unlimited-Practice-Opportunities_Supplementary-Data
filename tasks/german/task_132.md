# Input
- Programmierkonzept: Rekursion;Funktionen als Variablen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Berechnung von Basketballpunkten

Schreibe eine rekursive Funktion namens `berechne_punkte(spieler_punkte)`, die die Gesamtpunktzahl eines Basketballspielers berechnet. Die Funktion soll eine Liste von Punkten als Argument erhalten, wobei jeder Eintrag in der Liste die Punkte eines einzelnen Spiels darstellt. Die Funktion soll die Punkte aller Spiele summieren und das Ergebnis zurückgeben.

Beispielaufruf:
```python
punkte = [10, 15, 20, 5]
gesamtpunkte = berechne_punkte(punkte)
print(gesamtpunkte)  # Ausgabe: 50
```

### Anforderungen:
- Die Funktion `berechne_punkte` soll rekursiv implementiert werden.
- Die Funktion soll die Punkte aller Spiele in der Liste summieren und das Ergebnis zurückgeben.
- Die Funktion soll keine Eingaben über die Standardeingabe erwarten.

### Beispiel:
```python
punkte = [12, 8, 25, 10]
gesamtpunkte = berechne_punkte(punkte)
print(gesamtpunkte)  # Ausgabe: 55
```

Implementiere die Funktion `berechne_punkte(spieler_punkte)` in Python.

## Codegerüst
```python
def berechne_punkte(spieler_punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punkte(spieler_punkte):
    if not spieler_punkte:
        return 0
    return spieler_punkte[0] + berechne_punkte(spieler_punkte[1:])

punkte = [12, 8, 25, 10]
gesamtpunkte = berechne_punkte(punkte)
print(gesamtpunkte)  # Ausgabe: 55
```

## Unit Tests
```python
import unittest
from main import berechne_punkte

class TestBerechnePunkte(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(berechne_punkte([]), 0)

    def test_ein_spiel(self):
        self.assertEqual(berechne_punkte([10]), 10)

    def test_mehrere_spiele(self):
        self.assertEqual(berechne_punkte([10, 15, 20, 5]), 50)

    def test_negativ_punkte(self):
        self.assertEqual(berechne_punkte([10, -5, 20, -10]), 15)

    def test_grosse_zahlen(self):
        self.assertEqual(berechne_punkte([1000, 2000, 3000, 4000]), 10000)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 564
