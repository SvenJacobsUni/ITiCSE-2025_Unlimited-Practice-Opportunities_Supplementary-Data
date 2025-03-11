# Input
- Programmierkonzept: Operationen mit Zahlen;Integer
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Modernes Gaming - Spielerlevel Berechnung

In modernen Videospielen ist es üblich, dass Spieler durch das Sammeln von Erfahrungspunkten (XP) im Level aufsteigen. Schreibe eine Funktion namens `berechne_level(xp)`, die das aktuelle Level eines Spielers basierend auf den gesammelten Erfahrungspunkten berechnet und zurückgibt.

Die Level-Berechnung erfolgt nach folgendem Schema:
- Level 1: 0 - 999 XP
- Level 2: 1000 - 1999 XP
- Level 3: 2000 - 2999 XP
- Level 4: 3000 - 3999 XP
- Level 5: 4000 - 4999 XP
- usw.

Jedes weitere Level erfordert 1000 zusätzliche XP.

Beispielaufrufe:
- `berechne_level(1500)` gibt `2` zurück.
- `berechne_level(4500)` gibt `5` zurück.

Implementiere die Funktion `berechne_level(xp)`, die die oben beschriebene Berechnung durchführt.

## Codegerüst
```python
def berechne_level(xp):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_level(xp):
    return xp // 1000 + 1

# Beispielaufrufe
print(berechne_level(1500))  # Ausgabe: 2
print(berechne_level(4500))  # Ausgabe: 5
```

## Unit Tests
```python
import unittest
from main import berechne_level

class TestBerechneLevel(unittest.TestCase):
    def test_level_1(self):
        self.assertEqual(berechne_level(0), 1)
        self.assertEqual(berechne_level(999), 1)

    def test_level_2(self):
        self.assertEqual(berechne_level(1000), 2)
        self.assertEqual(berechne_level(1999), 2)

    def test_level_3(self):
        self.assertEqual(berechne_level(2000), 3)
        self.assertEqual(berechne_level(2999), 3)

    def test_level_4(self):
        self.assertEqual(berechne_level(3000), 4)
        self.assertEqual(berechne_level(3999), 4)

    def test_level_5(self):
        self.assertEqual(berechne_level(4000), 5)
        self.assertEqual(berechne_level(4999), 5)

    def test_high_levels(self):
        self.assertEqual(berechne_level(10000), 11)
        self.assertEqual(berechne_level(12345), 13)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 547
