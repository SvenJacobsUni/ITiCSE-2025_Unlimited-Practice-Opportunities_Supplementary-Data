# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);For-Schleifen;Tupel
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Spieler-Statistiken

Schreibe eine Funktion `spieler_statistiken(spieler_liste)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel repräsentiert einen Rugby-Spieler und enthält folgende Informationen in dieser Reihenfolge: Name (String), Alter (Integer), Anzahl der Versuche (Integer).

Die Funktion soll die folgenden Aufgaben erfüllen:
1. Alle Spieler, die älter als 30 Jahre sind und mehr als 5 Versuche erzielt haben, in einer neuen Liste speichern.
2. Die Anzahl der Spieler, die diese Kriterien erfüllen, zurückgeben.
3. Die Namen dieser Spieler in der Konsole ausgeben.

Beispielaufruf:
```python
spieler_liste = [("Max", 32, 6), ("Tom", 28, 4), ("John", 35, 7), ("Alex", 22, 3)]
anzahl_spieler = spieler_statistiken(spieler_liste)
print(anzahl_spieler)  # Ausgabe: 2
```

In diesem Beispiel sind "Max" und "John" die Spieler, die älter als 30 Jahre sind und mehr als 5 Versuche erzielt haben.

## Codegerüst
```python
def spieler_statistiken(spieler_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spieler_statistiken(spieler_liste):
    result = [spieler[0] for spieler in spieler_liste if spieler[1] > 30 and spieler[2] > 5]
    for name in result:
        print(name)
    return len(result)

spieler_liste = [("Max", 32, 6), ("Tom", 28, 4), ("John", 35, 7), ("Alex", 22, 3)]
anzahl_spieler = spieler_statistiken(spieler_liste)
print(anzahl_spieler)
```

## Unit Tests
```python
import unittest
from main import spieler_statistiken

class TestSpielerStatistiken(unittest.TestCase):
    def test_mehrere_spieler(self):
        spieler_liste = [("Max", 32, 6), ("Tom", 28, 4), ("John", 35, 7), ("Alex", 22, 3)]
        self.assertEqual(spieler_statistiken(spieler_liste), 2)

    def test_keine_spieler(self):
        spieler_liste = [("Tom", 28, 4), ("Alex", 22, 3)]
        self.assertEqual(spieler_statistiken(spieler_liste), 0)

    def test_alle_spieler(self):
        spieler_liste = [("Max", 32, 6), ("John", 35, 7)]
        self.assertEqual(spieler_statistiken(spieler_liste), 2)

    def test_grenzwert_spieler(self):
        spieler_liste = [("Max", 30, 6), ("John", 31, 5)]
        self.assertEqual(spieler_statistiken(spieler_liste), 0)

    def test_leere_liste(self):
        spieler_liste = []
        self.assertEqual(spieler_statistiken(spieler_liste), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 624
