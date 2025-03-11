# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Tupel;For-Schleifen
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Psychische Gesundheit und Aktivitätslevel

Schreibe eine Funktion namens `bewerte_aktivitaet(tage)`, die ein Tupel von 7 Ganzzahlen (jeweils zwischen 0 und 24) als Eingabe erhält. Jede Zahl im Tupel repräsentiert die Anzahl der Stunden, die eine Person an einem bestimmten Tag der Woche aktiv war. Die Funktion soll die Aktivitätslevel der Person bewerten und eine entsprechende Nachricht zurückgeben.

- Wenn die Person an mindestens 5 Tagen der Woche mehr als 1 Stunde aktiv war, soll die Nachricht "Gut gemacht! Du bist sehr aktiv." zurückgegeben werden.
- Wenn die Person an mindestens 3 Tagen der Woche mehr als 1 Stunde aktiv war, soll die Nachricht "Nicht schlecht, aber es gibt Raum für Verbesserung." zurückgegeben werden.
- Andernfalls soll die Nachricht "Versuche, aktiver zu sein, um deine psychische Gesundheit zu verbessern." zurückgegeben werden.

Beispielaufruf:
```python
bewerte_aktivitaet((1, 2, 0, 3, 4, 0, 1))
```

Erwartete Ausgabe:
```
Nicht schlecht, aber es gibt Raum für Verbesserung.
```

## Codegerüst
```python
def bewerte_aktivitaet(tage):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_aktivitaet(tage):
    aktiv = sum(1 for stunden in tage wenn stunden > 1)
    wenn aktiv >= 5:
        print("Gut gemacht! Du bist sehr aktiv.")
    elif aktiv >= 3:
        print("Nicht schlecht, aber es gibt Raum für Verbesserung.")
    sonst:
        print("Versuche, aktiver zu sein, um deine psychische Gesundheit zu verbessern.")

bewerte_aktivitaet((1, 2, 0, 3, 4, 0, 1))
```

## Unit Tests
```python
import unittest
from main import bewerte_aktivitaet

class TestBewerteAktivitaet(unittest.TestCase):
    def test_sehr_aktiv(self):
        self.assertEqual(bewerte_aktivitaet((2, 3, 4, 5, 6, 1, 0)), "Gut gemacht! Du bist sehr aktiv.")

    def test_mittelmaessig_aktiv(self):
        self.assertEqual(bewerte_aktivitaet((1, 2, 0, 3, 4, 0, 1)), "Nicht schlecht, aber es gibt Raum für Verbesserung.")

    def test_wenig_aktiv(self):
        self.assertEqual(bewerte_aktivitaet((0, 1, 0, 1, 0, 0, 0)), "Versuche, aktiver zu sein, um deine psychische Gesundheit zu verbessern.")

    def test_grenze_aktiv(self):
        self.assertEqual(bewerte_aktivitaet((1, 2, 1, 2, 1, 2, 1)), "Nicht schlecht, aber es gibt Raum für Verbesserung.")

    def test_grenze_sehr_aktiv(self):
        self.assertEqual(bewerte_aktivitaet((2, 2, 2, 2, 2, 0, 0)), "Gut gemacht! Du bist sehr aktiv.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 630
