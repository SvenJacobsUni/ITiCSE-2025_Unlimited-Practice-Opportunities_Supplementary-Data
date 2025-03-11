# Input
- Programmierkonzept: While-Schleifen
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Follower-Zähler

Schreibe eine Funktion namens `follower_zaehler(start_follower, ziel_follower)`, die die Anzahl der Tage berechnet, die benötigt werden, um eine bestimmte Anzahl von Followern auf einer Social-Media-Plattform zu erreichen. 

- `start_follower` ist die Anzahl der Follower, die du zu Beginn hast.
- `ziel_follower` ist die Anzahl der Follower, die du erreichen möchtest.

Jeden Tag gewinnst du 10 neue Follower. Die Funktion soll die Anzahl der Tage zurückgeben, die benötigt werden, um die `ziel_follower` zu erreichen oder zu überschreiten.

Beispielaufruf: `follower_zaehler(100, 150)` gibt `5` zurück.

## Codegerüst
```python
def follower_zaehler(start_follower, ziel_follower):
    ## Hier Code einfügen
```

## Musterlösung
```python
def follower_zaehler(start_follower, ziel_follower):
    return (ziel_follower - start_follower + 9) // 10

print(follower_zaehler(100, 150))
```

## Unit Tests
```python
import unittest
from main import follower_zaehler

class TestFollowerZaehler(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertEqual(follower_zaehler(100, 150), 5)

    def test_keine_zunahme_noetig(self):
        self.assertEqual(follower_zaehler(100, 100), 0)

    def test_ein_tag_noetig(self):
        self.assertEqual(follower_zaehler(100, 109), 1)

    def test_mehrere_tage_noetig(self):
        self.assertEqual(follower_zaehler(100, 200), 10)

    def test_grosse_zunahme(self):
        self.assertEqual(follower_zaehler(100, 1000), 90)

    def test_start_und_ziel_gleich(self):
        self.assertEqual(follower_zaehler(0, 0), 0)

    def test_start_groesser_als_ziel(self):
        self.assertEqual(follower_zaehler(150, 100), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 446
