# Input
- Programmierkonzept: String;Listen
- Kontext: Film

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Film-Genres

Schreibe eine Funktion namens `film_genres(filme)`, die eine Liste von Filmtiteln als Eingabe erhält. Jeder Filmtitel ist ein String, der den Titel des Films und das Genre in Klammern enthält, z.B. "Inception (Sci-Fi)". Die Funktion soll eine Liste der Genres zurückgeben, die in der Eingabeliste vorkommen. Die Genres sollen in der Ausgabe-Liste nur einmal vorkommen, auch wenn sie in der Eingabeliste mehrfach vorhanden sind.

Beispielaufruf:
```python
filme = ["Inception (Sci-Fi)", "Titanic (Romance)", "The Matrix (Sci-Fi)", "The Notebook (Romance)"]
print(film_genres(filme))
```

Erwartete Ausgabe:
```
['Sci-Fi', 'Romance']
```

## Codegerüst
```python
def film_genres(filme):
    ## Hier Code einfügen
```

## Musterlösung
```python
def film_genres(filme):
    return list({film.split('(')[-1].strip(')') for film in filme})

filme = ["Inception (Sci-Fi)", "Titanic (Romance)", "The Matrix (Sci-Fi)", "The Notebook (Romance)"]
print(film_genres(filme))
```

## Unit Tests
```python
import unittest
from main import film_genres

class TestFilmGenres(unittest.TestCase):
    def test_einfacher_fall(self):
        filme = ["Inception (Sci-Fi)", "Titanic (Romance)", "The Matrix (Sci-Fi)", "The Notebook (Romance)"]
        self.assertEqual(set(film_genres(filme)), {"Sci-Fi", "Romance"})

    def test_leere_liste(self):
        filme = []
        self.assertEqual(film_genres(filme), [])

    def test_ein_genre(self):
        filme = ["Inception (Sci-Fi)"]
        self.assertEqual(film_genres(filme), ["Sci-Fi"])

    def test_mehrere_genres(self):
        filme = ["Inception (Sci-Fi)", "Titanic (Romance)", "Avatar (Action)", "The Notebook (Romance)"]
        self.assertEqual(set(film_genres(filme)), {"Sci-Fi", "Romance", "Action"})

    def test_verschiedene_schreibweisen(self):
        filme = ["Inception (Sci-Fi)", "Titanic (romance)", "Avatar (Action)", "The Notebook (Romance)"]
        self.assertEqual(set(film_genres(filme)), {"Sci-Fi", "romance", "Action", "Romance"})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 552
