# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Rugby-Kontext

Schreibe eine Funktion `filter_spieler(spieler_liste, kriterium_funktion)`, die eine Liste von Rugby-Spielern und eine Kriterium-Funktion als Argumente erhält. Die Funktion soll eine neue Liste zurückgeben, die nur die Spieler enthält, die das Kriterium erfüllen.

Jeder Spieler wird durch ein Dictionary repräsentiert, das mindestens die folgenden Schlüssel enthält:
- `name`: Der Name des Spielers (String)
- `position`: Die Position des Spielers (String)
- `punkte`: Die Anzahl der erzielten Punkte (Integer)

Beispiel:
```python
spieler_liste = [
    {"name": "Max", "position": "Stürmer", "punkte": 15},
    {"name": "Tom", "position": "Verteidiger", "punkte": 5},
    {"name": "Leo", "position": "Stürmer", "punkte": 20}
]

def kriterium(spieler):
    return spieler["punkte"] > 10

resultat = filter_spieler(spieler_liste, kriterium)
# resultat sollte [{"name": "Max", "position": "Stürmer", "punkte": 15}, {"name": "Leo", "position": "Stürmer", "punkte": 20}] sein
```

Implementiere die Funktion `filter_spieler(spieler_liste, kriterium_funktion)`.

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
    {"name": "Max", "position": "Stürmer", "punkte": 15},
    {"name": "Tom", "position": "Verteidiger", "punkte": 5},
    {"name": "Leo", "position": "Stürmer", "punkte": 20}
]

def kriterium(spieler):
    return spieler["punkte"] > 10

resultat = filter_spieler(spieler_liste, kriterium)
print(resultat)
```

## Unit Tests
```python
import unittest
from main import filter_spieler

class TestFilterSpieler(unittest.TestCase):
    def test_alle_spieler_erfüllen_kriterium(self):
        spieler_liste = [
            {"name": "Max", "position": "Stürmer", "punkte": 15},
            {"name": "Leo", "position": "Stürmer", "punkte": 20}
        ]
        def kriterium(spieler):
            return spieler["punkte"] > 10
        self.assertEqual(filter_spieler(spieler_liste, kriterium), spieler_liste)

    def test_keiner_erfüllt_kriterium(self):
        spieler_liste = [
            {"name": "Tom", "position": "Verteidiger", "punkte": 5},
            {"name": "Jim", "position": "Verteidiger", "punkte": 3}
        ]
        def kriterium(spieler):
            return spieler["punkte"] > 10
        self.assertEqual(filter_spieler(spieler_liste, kriterium), [])

    def test_einige_erfüllen_kriterium(self):
        spieler_liste = [
            {"name": "Max", "position": "Stürmer", "punkte": 15},
            {"name": "Tom", "position": "Verteidiger", "punkte": 5},
            {"name": "Leo", "position": "Stürmer", "punkte": 20}
        ]
        def kriterium(spieler):
            return spieler["punkte"] > 10
        expected_result = [
            {"name": "Max", "position": "Stürmer", "punkte": 15},
            {"name": "Leo", "position": "Stürmer", "punkte": 20}
        ]
        self.assertEqual(filter_spieler(spieler_liste, kriterium), expected_result)

    def test_leere_liste(self):
        spieler_liste = []
        def kriterium(spieler):
            return spieler["punkte"] > 10
        self.assertEqual(filter_spieler(spieler_liste, kriterium), [])

    def test_kriterium_ist_immer_wahr(self):
        spieler_liste = [
            {"name": "Max", "position": "Stürmer", "punkte": 15},
            {"name": "Tom", "position": "Verteidiger", "punkte": 5},
            {"name": "Leo", "position": "Stürmer", "punkte": 20}
        ]
        def kriterium(spieler):
            return True
        self.assertEqual(filter_spieler(spieler_liste, kriterium), spieler_liste)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 439
