# Input
- Programmierkonzept: String;Funktionen als Variablen;Listen
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Streaming-Dienste

Schreibe eine Funktion namens `filtere_genres(filme, genre)`, die eine Liste von Filmen und ein Genre als Parameter erhält. Jeder Film ist ein Dictionary mit den Schlüsseln "titel" und "genre". Die Funktion soll eine neue Liste zurückgeben, die nur die Filme enthält, die dem angegebenen Genre entsprechen.

Beispielaufruf:
```python
filme = [
    {"titel": "Film A", "genre": "Action"},
    {"titel": "Film B", "genre": "Drama"},
    {"titel": "Film C", "genre": "Action"},
    {"titel": "Film D", "genre": "Komödie"}
]

ergebnis = filtere_genres(filme, "Action")
# ergebnis sollte [{"titel": "Film A", "genre": "Action"}, {"titel": "Film C", "genre": "Action"}] sein
```

Implementiere die Funktion `filtere_genres(filme, genre)`, sodass sie die oben beschriebene Funktionalität erfüllt.

## Codegerüst
```python
def filtere_genres(filme, genre):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filtere_genres(filme, genre):
    return [film for film in filme if film['genre'] == genre]

filme = [
    {"titel": "Film A", "genre": "Action"},
    {"titel": "Film B", "genre": "Drama"},
    {"titel": "Film C", "genre": "Action"},
    {"titel": "Film D", "genre": "Komödie"}
]

ergebnis = filtere_genres(filme, "Action")
print(ergebnis)
```

## Unit Tests
```python
import unittest
from main import filtere_genres

class TestFiltereGenres(unittest.TestCase):
    def test_action_genre(self):
        filme = [
            {"titel": "Film A", "genre": "Action"},
            {"titel": "Film B", "genre": "Drama"},
            {"titel": "Film C", "genre": "Action"},
            {"titel": "Film D", "genre": "Komödie"}
        ]
        self.assertEqual(filtere_genres(filme, "Action"), [
            {"titel": "Film A", "genre": "Action"},
            {"titel": "Film C", "genre": "Action"}
        ])

    def test_drama_genre(self):
        filme = [
            {"titel": "Film A", "genre": "Action"},
            {"titel": "Film B", "genre": "Drama"},
            {"titel": "Film C", "genre": "Action"},
            {"titel": "Film D", "genre": "Komödie"}
        ]
        self.assertEqual(filtere_genres(filme, "Drama"), [
            {"titel": "Film B", "genre": "Drama"}
        ])

    def test_komoedie_genre(self):
        filme = [
            {"titel": "Film A", "genre": "Action"},
            {"titel": "Film B", "genre": "Drama"},
            {"titel": "Film C", "genre": "Action"},
            {"titel": "Film D", "genre": "Komödie"}
        ]
        self.assertEqual(filtere_genres(filme, "Komödie"), [
            {"titel": "Film D", "genre": "Komödie"}
        ])

    def test_leeres_ergebnis(self):
        filme = [
            {"titel": "Film A", "genre": "Action"},
            {"titel": "Film B", "genre": "Drama"},
            {"titel": "Film C", "genre": "Action"},
            {"titel": "Film D", "genre": "Komödie"}
        ]
        self.assertEqual(filtere_genres(filme, "Horror"), [])

    def test_leere_filmliste(self):
        filme = []
        self.assertEqual(filtere_genres(filme, "Action"), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 609
