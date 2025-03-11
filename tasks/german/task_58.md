# Input
- Programmierkonzept: Integer
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Soziale Medien - Follower-Zähler

Schreibe eine Funktion namens `follower_zaehler(follower_liste)`, die eine Liste von Integern als Argument erhält. Jeder Integer in der Liste repräsentiert die Anzahl der Follower eines Benutzers in einem sozialen Netzwerk. Die Funktion soll die Gesamtanzahl der Follower berechnen und zurückgeben.

Beispielaufruf:
```python
follower_zaehler([150, 200, 350, 400])
```
soll `1100` zurückgeben.

## Codegerüst
```python
def follower_zaehler(follower_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def follower_zaehler(follower_liste):
    return sum(follower_liste)

print(follower_zaehler([150, 200, 350, 400]))
```

## Unit Tests
```python
import unittest

from main import follower_zaehler

class TestFollowerZaehler(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertEqual(follower_zaehler([150, 200, 350, 400]), 1100)

    def test_leere_liste(self):
        self.assertEqual(follower_zaehler([]), 0)

    def test_ein_element(self):
        self.assertEqual(follower_zaehler([500]), 500)

    def test_negativer_wert(self):
        self.assertEqual(follower_zaehler([100, -50, 200]), 250)

    def test_gemischte_werte(self):
        self.assertEqual(follower_zaehler([100, 200, 300, 400, 500]), 1500)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 476
