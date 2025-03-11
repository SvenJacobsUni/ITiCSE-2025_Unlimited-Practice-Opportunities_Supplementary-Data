# Input
- Programmierkonzept: Tupel
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Statistiken mit Tupeln

Schreibe eine Funktion namens `spieler_statistik(spieler)`, die ein Tupel mit den Statistiken eines Basketballspielers entgegennimmt und eine formatierte Zeichenkette zurückgibt. Das Tupel enthält folgende Informationen in dieser Reihenfolge:

1. Name des Spielers (String)
2. Anzahl der gespielten Spiele (Integer)
3. Durchschnittliche Punkte pro Spiel (Float)
4. Durchschnittliche Rebounds pro Spiel (Float)
5. Durchschnittliche Assists pro Spiel (Float)

Die Funktion soll eine Zeichenkette im folgenden Format zurückgeben:

```
"Spieler: [Name], Spiele: [Anzahl], Punkte/Spiel: [Punkte], Rebounds/Spiel: [Rebounds], Assists/Spiel: [Assists]"
```

Beispielaufruf:
```python
spieler = ("LeBron James", 82, 27.5, 7.4, 7.2)
print(spieler_statistik(spieler))
```

Beispielausgabe:
```
"Spieler: LeBron James, Spiele: 82, Punkte/Spiel: 27.5, Rebounds/Spiel: 7.4, Assists/Spiel: 7.2"
```

## Codegerüst
```python
def spieler_statistik(spieler):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spieler_statistik(spieler):
    return f"Spieler: {spieler[0]}, Spiele: {spieler[1]}, Punkte/Spiel: {spieler[2]}, Rebounds/Spiel: {spieler[3]}, Assists/Spiel: {spieler[4]}"

spieler = ("LeBron James", 82, 27.5, 7.4, 7.2)
print(spieler_statistik(spieler))
```

## Unit Tests
```python
import unittest
from main import spieler_statistik

class TestSpielerStatistik(unittest.TestCase):
    def test_standard_fall(self):
        spieler = ("LeBron James", 82, 27.5, 7.4, 7.2)
        expected = "Spieler: LeBron James, Spiele: 82, Punkte/Spiel: 27.5, Rebounds/Spiel: 7.4, Assists/Spiel: 7.2"
        self.assertEqual(spieler_statistik(spieler), expected)

    def test_anderer_spieler(self):
        spieler = ("Michael Jordan", 82, 30.1, 6.2, 5.3)
        expected = "Spieler: Michael Jordan, Spiele: 82, Punkte/Spiel: 30.1, Rebounds/Spiel: 6.2, Assists/Spiel: 5.3"
        self.assertEqual(spieler_statistik(spieler), expected)

    def test_wenige_spiele(self):
        spieler = ("Kobe Bryant", 10, 25.0, 5.2, 4.5)
        expected = "Spieler: Kobe Bryant, Spiele: 10, Punkte/Spiel: 25.0, Rebounds/Spiel: 5.2, Assists/Spiel: 4.5"
        self.assertEqual(spieler_statistik(spieler), expected)

    def test_rundungswerte(self):
        spieler = ("Stephen Curry", 82, 27.456, 5.678, 6.789)
        expected = "Spieler: Stephen Curry, Spiele: 82, Punkte/Spiel: 27.456, Rebounds/Spiel: 5.678, Assists/Spiel: 6.789"
        self.assertEqual(spieler_statistik(spieler), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 482
