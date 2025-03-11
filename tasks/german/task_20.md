# Input
- Programmierkonzept: Tupel
- Kontext: Film

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Film-Tupel

Schreibe eine Funktion namens `film_info(film)`, die ein Tupel als Argument erhält. Das Tupel enthält Informationen über einen Film in der folgenden Reihenfolge: Titel (String), Erscheinungsjahr (Integer), Regisseur (String) und Bewertung (Float).

Die Funktion soll eine formatierte Zeichenkette zurückgeben, die die Informationen des Films in einem lesbaren Format darstellt.

Beispielaufruf:
```python
film = ("Inception", 2010, "Christopher Nolan", 8.8)
print(film_info(film))
```

Erwartete Ausgabe:
```
Titel: Inception
Erscheinungsjahr: 2010
Regisseur: Christopher Nolan
Bewertung: 8.8
```

## Codegerüst
```python
def film_info(film):
    ## Hier Code einfügen
```

## Musterlösung
```python
def film_info(film):
    return f"Titel: {film[0]}\nErscheinungsjahr: {film[1]}\nRegisseur: {film[2]}\nBewertung: {film[3]}"

film = ("Inception", 2010, "Christopher Nolan", 8.8)
print(film_info(film))
```

## Unit Tests
```python
import unittest
from main import film_info

class TestFilmInfo(unittest.TestCase):
    def test_standard_film(self):
        film = ("Inception", 2010, "Christopher Nolan", 8.8)
        expected = "Titel: Inception\nErscheinungsjahr: 2010\nRegisseur: Christopher Nolan\nBewertung: 8.8"
        self.assertEqual(film_info(film), expected)

    def test_film_mit_komma_in_titel(self):
        film = ("Spider-Man: No Way Home", 2021, "Jon Watts", 8.4)
        expected = "Titel: Spider-Man: No Way Home\nErscheinungsjahr: 2021\nRegisseur: Jon Watts\nBewertung: 8.4"
        self.assertEqual(film_info(film), expected)

    def test_film_mit_niedriger_bewertung(self):
        film = ("The Room", 2003, "Tommy Wiseau", 3.7)
        expected = "Titel: The Room\nErscheinungsjahr: 2003\nRegisseur: Tommy Wiseau\nBewertung: 3.7"
        self.assertEqual(film_info(film), expected)

    def test_film_mit_hoher_bewertung(self):
        film = ("The Godfather", 1972, "Francis Ford Coppola", 9.2)
        expected = "Titel: The Godfather\nErscheinungsjahr: 1972\nRegisseur: Francis Ford Coppola\nBewertung: 9.2"
        self.assertEqual(film_info(film), expected)

    def test_film_mit_ganzzahliger_bewertung(self):
        film = ("A Beautiful Mind", 2001, "Ron Howard", 8.0)
        expected = "Titel: A Beautiful Mind\nErscheinungsjahr: 2001\nRegisseur: Ron Howard\nBewertung: 8.0"
        self.assertEqual(film_info(film), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 438
