# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Rekursion;For-Schleifen
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beliebteste Serie auf einem Streaming-Dienst

Schreibe eine Funktion `beliebteste_serie(serien_liste)`, die eine Liste von Serien und deren Bewertungen als Eingabe erhält und die Serie mit der höchsten Bewertung zurückgibt. Jede Serie in der Liste ist ein Dictionary mit den Schlüsseln `name` und `bewertung`. Die Funktion soll rekursiv die Serie mit der höchsten Bewertung finden.

Beispielaufruf:
```python
serien = [
    {"name": "Serie A", "bewertung": 8.5},
    {"name": "Serie B", "bewertung": 9.0},
    {"name": "Serie C", "bewertung": 7.8}
]
print(beliebteste_serie(serien))  # Ausgabe: "Serie B"
```

Implementiere die Funktion so, dass sie die höchste Bewertung rekursiv ermittelt und den Namen der Serie mit der höchsten Bewertung zurückgibt.

## Codegerüst
```python
def beliebteste_serie(serien_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beliebteste_serie(serien_liste):
    if len(serien_liste) == 1:
        return serien_liste[0]['name']
    rest_beste = beliebteste_serie(serien_liste[1:])
    return serien_liste[0]['name'] if serien_liste[0]['bewertung'] > next(s['bewertung'] for s in serien_liste if s['name'] == rest_beste) else rest_beste

serien = [
    {"name": "Serie A", "bewertung": 8.5},
    {"name": "Serie B", "bewertung": 9.0},
    {"name": "Serie C", "bewertung": 7.8}
]
print(beliebteste_serie(serien))  # Ausgabe: "Serie B"
```

## Unit Tests
```python
import unittest
from main import beliebteste_serie

class TestBeliebtesteSerie(unittest.TestCase):
    def test_einfacher_fall(self):
        serien = [
            {"name": "Serie A", "bewertung": 8.5},
            {"name": "Serie B", "bewertung": 9.0},
            {"name": "Serie C", "bewertung": 7.8}
        ]
        self.assertEqual(beliebteste_serie(serien), "Serie B")

    def test_alle_gleiche_bewertung(self):
        serien = [
            {"name": "Serie A", "bewertung": 8.0},
            {"name": "Serie B", "bewertung": 8.0},
            {"name": "Serie C", "bewertung": 8.0}
        ]
        self.assertEqual(beliebteste_serie(serien), "Serie A")

    def test_eine_serie(self):
        serien = [
            {"name": "Serie A", "bewertung": 8.5}
        ]
        self.assertEqual(beliebteste_serie(serien), "Serie A")

    def test_leere_liste(self):
        serien = []
        with self.assertRaises(IndexError):
            beliebteste_serie(serien)

    def test_negative_bewertungen(self):
        serien = [
            {"name": "Serie A", "bewertung": -1.0},
            {"name": "Serie B", "bewertung": -2.0},
            {"name": "Serie C", "bewertung": -3.0}
        ]
        self.assertEqual(beliebteste_serie(serien), "Serie A")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 600
