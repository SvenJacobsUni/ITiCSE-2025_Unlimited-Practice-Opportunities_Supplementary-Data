# Input
- Programmierkonzept: Listen;If-Else-Anweisungen
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Spieler filtern

Schreibe eine Funktion namens `filter_spieler(spieler_liste)`, die eine Liste von Rugby-Spielernamen und deren Positionen als Eingabe erhält. Die Funktion soll eine neue Liste zurückgeben, die nur die Namen der Spieler enthält, die auf der Position "Stürmer" spielen.

Die Eingabeliste hat das Format:
```python
[("Name1", "Position1"), ("Name2", "Position2"), ...]
```

Beispiel:
```python
spieler_liste = [("Max", "Stürmer"), ("Tom", "Verteidiger"), ("Lukas", "Stürmer"), ("Paul", "Flügelspieler")]
```

Aufruf:
```python
filter_spieler(spieler_liste)
```

Erwartete Ausgabe:
```python
["Max", "Lukas"]
```

Implementiere die Funktion `filter_spieler(spieler_liste)`, die die obige Aufgabe erfüllt.

## Codegerüst
```python
def filter_spieler(spieler_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_spieler(spieler_liste):
    return [name for name, position in spieler_liste if position == "Stürmer"]

spieler_liste = [("Max", "Stürmer"), ("Tom", "Verteidiger"), ("Lukas", "Stürmer"), ("Paul", "Flügelspieler")]
print(filter_spieler(spieler_liste))
```

## Unit Tests
```python
import unittest
from main import filter_spieler

class TestFilterSpieler(unittest.TestCase):
    def test_mehrere_stuermer(self):
        self.assertEqual(filter_spieler([("Max", "Stürmer"), ("Tom", "Verteidiger"), ("Lukas", "Stürmer"), ("Paul", "Flügelspieler")]), ["Max", "Lukas"])

    def test_keine_stuermer(self):
        self.assertEqual(filter_spieler([("Tom", "Verteidiger"), ("Paul", "Flügelspieler")]), [])

    def test_alle_stuermer(self):
        self.assertEqual(filter_spieler([("Max", "Stürmer"), ("Lukas", "Stürmer")]), ["Max", "Lukas"])

    def test_leere_liste(self):
        self.assertEqual(filter_spieler([]), [])

    def test_ein_stuermer(self):
        self.assertEqual(filter_spieler([("Max", "Stürmer")]), ["Max"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 553
