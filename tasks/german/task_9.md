# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Kontext von Streaming-Diensten

Schreibe eine Funktion `filter_filme(filme, kriterium)`, die eine Liste von Filmen und eine Funktion als Kriterium entgegennimmt. Die Funktion soll eine neue Liste zurückgeben, die nur die Filme enthält, die das Kriterium erfüllen.

Ein Film wird durch ein Dictionary repräsentiert, das mindestens die Schlüssel `titel` und `bewertung` enthält. Die Funktion `kriterium` nimmt ein Filmdictionary als Argument und gibt einen Boolean-Wert zurück.

Beispielaufruf:
```python
filme = [
    {"titel": "Film A", "bewertung": 8.5},
    {"titel": "Film B", "bewertung": 7.0},
    {"titel": "Film C", "bewertung": 9.0}
]

def hohe_bewertung(film):
    return film["bewertung"] > 8.0

gefilterte_filme = filter_filme(filme, hohe_bewertung)
# gefilterte_filme sollte [{"titel": "Film A", "bewertung": 8.5}, {"titel": "Film C", "bewertung": 9.0}] enthalten
```

Implementiere die Funktion `filter_filme(filme, kriterium)`.

## Codegerüst
```python
def filter_filme(filme, kriterium):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_filme(filme, kriterium):
    return [film for film in filme if kriterium(film)]

filme = [
    {"titel": "Film A", "bewertung": 8.5},
    {"titel": "Film B", "bewertung": 7.0},
    {"titel": "Film C", "bewertung": 9.0}
]

def hohe_bewertung(film):
    return film["bewertung"] > 8.0

gefilterte_filme = filter_filme(filme, hohe_bewertung)
print(gefilterte_filme)
```

## Unit Tests
```python
import unittest
from main import filter_filme

class TestFilterFilme(unittest.TestCase):
    def test_hohe_bewertung(self):
        filme = [
            {"titel": "Film A", "bewertung": 8.5},
            {"titel": "Film B", "bewertung": 7.0},
            {"titel": "Film C", "bewertung": 9.0}
        ]
        def hohe_bewertung(film):
            return film["bewertung"] > 8.0
        self.assertEqual(filter_filme(filme, hohe_bewertung), [
            {"titel": "Film A", "bewertung": 8.5},
            {"titel": "Film C", "bewertung": 9.0}
        ])

    def test_niedrige_bewertung(self):
        filme = [
            {"titel": "Film A", "bewertung": 8.5},
            {"titel": "Film B", "bewertung": 7.0},
            {"titel": "Film C", "bewertung": 9.0}
        ]
        def niedrige_bewertung(film):
            return film["bewertung"] < 8.0
        self.assertEqual(filter_filme(filme, niedrige_bewertung), [
            {"titel": "Film B", "bewertung": 7.0}
        ])

    def test_leere_liste(self):
        filme = []
        def hohe_bewertung(film):
            return film["bewertung"] > 8.0
        self.assertEqual(filter_filme(filme, hohe_bewertung), [])

    def test_alle_filme(self):
        filme = [
            {"titel": "Film A", "bewertung": 8.5},
            {"titel": "Film B", "bewertung": 7.0},
            {"titel": "Film C", "bewertung": 9.0}
        ]
        def alle_filme(film):
            return True
        self.assertEqual(filter_filme(filme, alle_filme), filme)

    def test_keine_filme(self):
        filme = [
            {"titel": "Film A", "bewertung": 8.5},
            {"titel": "Film B", "bewertung": 7.0},
            {"titel": "Film C", "bewertung": 9.0}
        ]
        def keine_filme(film):
            return False
        self.assertEqual(filter_filme(filme, keine_filme), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 427
