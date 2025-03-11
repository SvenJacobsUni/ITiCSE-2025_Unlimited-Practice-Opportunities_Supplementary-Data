# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Rugby-Kontext

Schreibe eine Funktion `filter_spieler(spieler_liste, kriterium_funktion)`, die eine Liste von Rugby-Spielern und eine Funktion als Parameter akzeptiert. Die Funktion soll eine neue Liste zurückgeben, die nur die Spieler enthält, die das Kriterium der übergebenen Funktion erfüllen.

Jeder Spieler wird durch ein Dictionary repräsentiert, das mindestens die Schlüssel `name` und `position` enthält.

Beispiel:

```python
spieler_liste = [
    {"name": "Max", "position": "Stürmer"},
    {"name": "Tom", "position": "Verteidiger"},
    {"name": "Leo", "position": "Stürmer"},
    {"name": "Paul", "position": "Verteidiger"}
]

def ist_stuermer(spieler):
    return spieler["position"] == "Stürmer"

# Aufruf der Funktion
resultat = filter_spieler(spieler_liste, ist_stuermer)
# Erwartetes Ergebnis: [{"name": "Max", "position": "Stürmer"}, {"name": "Leo", "position": "Stürmer"}]
```

Implementiere die Funktion `filter_spieler` und teste sie mit verschiedenen Kriterien.

## Codegerüst
```python
def filter_spieler(spieler_liste, kriterium_funktion):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_spieler(spieler_liste, kriterium_funktion):
    return [spieler for spieler in spieler_liste, if kriterium_funktion(spieler)]

spieler_liste = [
    {"name": "Max", "position": "Stürmer"},
    {"name": "Tom", "position": "Verteidiger"},
    {"name": "Leo", "position": "Stürmer"},
    {"name": "Paul", "position": "Verteidiger"}
]

def ist_stuermer(spieler):
    return spieler["position"] == "Stürmer"

resultat = filter_spieler(spieler_liste, ist_stuermer)
print(resultat)
```

## Unit Tests
```python
import unittest
from main import filter_spieler

class TestFilterSpieler(unittest.TestCase):
    def setUp(self):
        self.spieler_liste = [
            {"name": "Max", "position": "Stürmer"},
            {"name": "Tom", "position": "Verteidiger"},
            {"name": "Leo", "position": "Stürmer"},
            {"name": "Paul", "position": "Verteidiger"}
        ]

    def test_ist_stuermer(self):
        def ist_stuermer(spieler):
            return spieler["position"] == "Stürmer"
        expected = [
            {"name": "Max", "position": "Stürmer"},
            {"name": "Leo", "position": "Stürmer"}
        ]
        self.assertEqual(filter_spieler(self.spieler_liste, ist_stuermer), expected)

    def test_ist_verteidiger(self):
        def ist_verteidiger(spieler):
            return spieler["position"] == "Verteidiger"
        expected = [
            {"name": "Tom", "position": "Verteidiger"},
            {"name": "Paul", "position": "Verteidiger"}
        ]
        self.assertEqual(filter_spieler(self.spieler_liste, ist_verteidiger), expected)

    def test_leere_liste(self):
        def ist_stuermer(spieler):
            return spieler["position"] == "Stürmer"
        self.assertEqual(filter_spieler([], ist_stuermer), [])

    def test_keine_treffer(self):
        def ist_torwart(spieler):
            return spieler["position"] == "Torwart"
        self.assertEqual(filter_spieler(self.spieler_liste, ist_torwart), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 492
