# Input
- Programmierkonzept: Boolean und None;Rekursion
- Kontext: Film

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Filmempfehlung basierend auf Bewertungen

Schreibe eine rekursive Funktion `empfehle_film(filme, bewertung)`, die eine Liste von Filmen und eine Bewertung als Parameter erhält. Jeder Film in der Liste ist ein Dictionary mit den Schlüsseln `titel` und `bewertung`. Die Funktion soll den ersten Film zurückgeben, dessen Bewertung größer oder gleich der übergebenen Bewertung ist. Wenn kein solcher Film gefunden wird, soll die Funktion `None` zurückgeben.

Beispielaufruf:
```python
filme = [
    {"titel": "Film A", "bewertung": 7.5},
    {"titel": "Film B", "bewertung": 8.0},
    {"titel": "Film C", "bewertung": 6.0}
]
print(empfehle_film(filme, 7.0))  # Gibt {"titel": "Film A", "bewertung": 7.5} zurück
print(empfehle_film(filme, 8.5))  # Gibt None zurück
```

Implementiere die Funktion `empfehle_film(filme, bewertung)`.

## Codegerüst
```python
def empfehle_film(filme, bewertung):
    ## Hier Code einfügen
```

## Musterlösung
```python
def empfehle_film(filme, bewertung):
    if not filme:
        return None
    if filme[0]['bewertung'] >= bewertung:
        return filme[0]
    return empfehle_film(filme[1:], bewertung)

filme = [
    {"titel": "Film A", "bewertung": 7.5},
    {"titel": "Film B", "bewertung": 8.0},
    {"titel": "Film C", "bewertung": 6.0}
]
print(empfehle_film(filme, 7.0))  # Gibt {"titel": "Film A", "bewertung": 7.5} zurück
print(empfehle_film(filme, 8.5))  # Gibt None zurück
```

## Unit Tests
```python
import unittest

from main import empfehle_film

class TestEmpfehleFilm(unittest.TestCase):
    def test_film_gefunden(self):
        filme = [
            {"titel": "Film A", "bewertung": 7.5},
            {"titel": "Film B", "bewertung": 8.0},
            {"titel": "Film C", "bewertung": 6.0}
        ]
        self.assertEqual(empfehle_film(filme, 7.0), {"titel": "Film A", "bewertung": 7.5})

    def test_keine_film_gefunden(self):
        filme = [
            {"titel": "Film A", "bewertung": 7.5},
            {"titel": "Film B", "bewertung": 8.0},
            {"titel": "Film C", "bewertung": 6.0}
        ]
        self.assertIsNone(empfehle_film(filme, 8.5))

    def test_leere_liste(self):
        filme = []
        self.assertIsNone(empfehle_film(filme, 7.0))

    def test_alle_filme_unter_bewertung(self):
        filme = [
            {"titel": "Film A", "bewertung": 5.5},
            {"titel": "Film B", "bewertung": 6.0},
            {"titel": "Film C", "bewertung": 4.0}
        ]
        self.assertIsNone(empfehle_film(filme, 7.0))

    def test_erste_film_gefunden(self):
        filme = [
            {"titel": "Film A", "bewertung": 7.0},
            {"titel": "Film B", "bewertung": 8.0},
            {"titel": "Film C", "bewertung": 6.0}
        ]
        self.assertEqual(empfehle_film(filme, 7.0), {"titel": "Film A", "bewertung": 7.0})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 582
