# Input
- Programmierkonzept: Listen;Rekursion
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Follower-Zählung in sozialen Medien

In sozialen Medien ist es oft wichtig, die Anzahl der Follower eines Benutzers zu kennen. Schreibe eine rekursive Funktion `zaehle_follower(follower_liste)`, die die Anzahl der Follower in einer verschachtelten Liste zählt. Die Liste kann sowohl einzelne Follower als auch weitere Listen von Followern enthalten.

Beispiel:
```python
follower_liste = ["Anna", ["Ben", "Clara"], "David", ["Eva", ["Frank", "Grace"]]]
```

In diesem Beispiel hat der Benutzer insgesamt 6 Follower.

Implementiere die Funktion `zaehle_follower(follower_liste)`, die die Anzahl der Follower in der verschachtelten Liste zurückgibt.

Beispielaufruf:
```python
print(zaehle_follower(follower_liste))  # Ausgabe: 6
```

## Codegerüst
```python
def zaehle_follower(follower_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_follower(follower_liste):
    if not follower_liste:
        return 0
    if isinstance(follower_liste[0], list):
        return zaehle_follower(follower_liste[0]) + zaehle_follower(follower_liste[1:])
    return 1 + zaehle_follower(follower_liste[1:])

follower_liste = ["Anna", ["Ben", "Clara"], "David", ["Eva", ["Frank", "Grace"]]]
print(zaehle_follower(follower_liste))  # Ausgabe: 6
```

## Unit Tests
```python
import unittest

from main import zaehle_follower

class TestZaehleFollower(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertEqual(zaehle_follower(["Anna", "Ben", "Clara"]), 3)

    def test_verschachtelte_liste(self):
        self.assertEqual(zaehle_follower(["Anna", ["Ben", "Clara"], "David", ["Eva", ["Frank", "Grace"]]]), 6)

    def test_leere_liste(self):
        self.assertEqual(zaehle_follower([]), 0)

    def test_ein_follower(self):
        self.assertEqual(zaehle_follower(["Anna"]), 1)

    def test_tief_verschachtelte_liste(self):
        self.assertEqual(zaehle_follower(["Anna", ["Ben", ["Clara", ["David", ["Eva"]]]]]), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 575
