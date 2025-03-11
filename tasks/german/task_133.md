# Input
- Programmierkonzept: Rekursion;For-Schleifen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Punktestand

Schreibe eine Funktion namens `berechne_punktestand(spieler_punkte)`, die eine Liste von Punkten, die von verschiedenen Basketballspielern in einem Spiel erzielt wurden, als Argument erhält. Die Funktion soll rekursiv die Summe aller Punkte berechnen und zurückgeben. Verwende zusätzlich eine For-Schleife, um die Punkte der einzelnen Spieler auszugeben.

Beispiel:
```python
spieler_punkte = [12, 15, 10, 8, 20]
```

Aufruf:
```python
berechne_punktestand(spieler_punkte)
```

Erwartete Ausgabe:
```
Spieler 1 hat 12 Punkte erzielt.
Spieler 2 hat 15 Punkte erzielt.
Spieler 3 hat 10 Punkte erzielt.
Spieler 4 hat 8 Punkte erzielt.
Spieler 5 hat 20 Punkte erzielt.
```

Rückgabewert:
```
65
```

## Codegerüst
```python
def berechne_punktestand(spieler_punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punktestand(spieler_punkte):
    def summe(punkte):
        if not punkte:
            return 0
        return punkte[0] + summe(punkte[1:])
    
    for i, punkte in enumerate(spieler_punkte, 1):
        print(f"Spieler {i} hat {punkte} Punkte erzielt.")
    
    return summe(spieler_punkte)

spieler_punkte = [12, 15, 10, 8, 20]
print(berechne_punktestand(spieler_punkte))
```

## Unit Tests
```python
import unittest
from main import berechne_punktestand

class TestBerechnePunktestand(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertEqual(berechne_punktestand([12, 15, 10, 8, 20]), 65)

    def test_leere_liste(self):
        self.assertEqual(berechne_punktestand([]), 0)

    def test_ein_element(self):
        self.assertEqual(berechne_punktestand([25]), 25)

    def test_negativ_und_positiv(self):
        self.assertEqual(berechne_punktestand([-5, 10, -3, 8]), 10)

    def test_grosse_zahlen(self):
        self.assertEqual(berechne_punktestand([1000, 2000, 3000, 4000]), 10000)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 565
