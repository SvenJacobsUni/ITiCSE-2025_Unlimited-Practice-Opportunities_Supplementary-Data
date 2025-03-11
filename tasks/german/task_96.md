# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Sport

Schreibe eine Funktion namens `filter_sportler(sportler_liste, kriterium_funktion)`, die eine Liste von Sportlern und eine Funktion als Parameter entgegennimmt. Die Funktion soll eine neue Liste zurückgeben, die nur die Sportler enthält, die das Kriterium der übergebenen Funktion erfüllen.

Ein Sportler wird durch ein Dictionary repräsentiert, das mindestens die Schlüssel `name` und `sportart` enthält.

Beispiel:

```python
sportler_liste = [
    {"name": "Anna", "sportart": "Tennis"},
    {"name": "Ben", "sportart": "Fußball"},
    {"name": "Clara", "sportart": "Schwimmen"},
    {"name": "David", "sportart": "Tennis"}
]

def ist_tennisspieler(sportler):
    return sportler["sportart"] == "Tennis"

# Aufruf der Funktion
gefilterte_sportler = filter_sportler(sportler_liste, ist_tennisspieler)
# Erwartete Ausgabe: [{"name": "Anna", "sportart": "Tennis"}, {"name": "David", "sportart": "Tennis"}]
```

Implementiere die Funktion `filter_sportler` so, dass sie die Liste der Sportler basierend auf der übergebenen Kriterium-Funktion filtert und die gefilterte Liste zurückgibt.

## Codegerüst
```python
def filter_sportler(sportler_liste, kriterium_funktion):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_sportler(sportler_liste, kriterium_funktion):
    return [sportler for sportler in sportler_liste wenn kriterium_funktion(sportler)]

sportler_liste = [
    {"name": "Anna", "sportart": "Tennis"},
    {"name": "Ben", "sportart": "Fußball"},
    {"name": "Clara", "sportart": "Schwimmen"},
    {"name": "David", "sportart": "Tennis"}
]

def ist_tennisspieler(sportler):
    return sportler["sportart"] == "Tennis"

gefilterte_sportler = filter_sportler(sportler_liste, ist_tennisspieler)
print(gefilterte_sportler)
```

## Unit Tests
```python
import unittest
from main import filter_sportler

class TestFilterSportler(unittest.TestCase):
    def test_tennisspieler(self):
        sportler_liste = [
            {"name": "Anna", "sportart": "Tennis"},
            {"name": "Ben", "sportart": "Fußball"},
            {"name": "Clara", "sportart": "Schwimmen"},
            {"name": "David", "sportart": "Tennis"}
        ]
        def ist_tennisspieler(sportler):
            return sportler["sportart"] == "Tennis"
        self.assertEqual(filter_sportler(sportler_liste, ist_tennisspieler), [
            {"name": "Anna", "sportart": "Tennis"},
            {"name": "David", "sportart": "Tennis"}
        ])

    def test_fussballspieler(self):
        sportler_liste = [
            {"name": "Anna", "sportart": "Tennis"},
            {"name": "Ben", "sportart": "Fußball"},
            {"name": "Clara", "sportart": "Schwimmen"},
            {"name": "David", "sportart": "Tennis"}
        ]
        def ist_fussballspieler(sportler):
            return sportler["sportart"] == "Fußball"
        self.assertEqual(filter_sportler(sportler_liste, ist_fussballspieler), [
            {"name": "Ben", "sportart": "Fußball"}
        ])

    def test_keine_sportler(self):
        sportler_liste = []
        def ist_tennisspieler(sportler):
            return sportler["sportart"] == "Tennis"
        self.assertEqual(filter_sportler(sportler_liste, ist_tennisspieler), [])

    def test_alle_sportler(self):
        sportler_liste = [
            {"name": "Anna", "sportart": "Tennis"},
            {"name": "Ben", "sportart": "Fußball"},
            {"name": "Clara", "sportart": "Schwimmen"},
            {"name": "David", "sportart": "Tennis"}
        ]
        def alle_sportler(sportler):
            return True
        self.assertEqual(filter_sportler(sportler_liste, alle_sportler), sportler_liste)

    def test_keine_tennisspieler(self):
        sportler_liste = [
            {"name": "Ben", "sportart": "Fußball"},
            {"name": "Clara", "sportart": "Schwimmen"}
        ]
        def ist_tennisspieler(sportler):
            return sportler["sportart"] == "Tennis"
        self.assertEqual(filter_sportler(sportler_liste, ist_tennisspieler), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 514
