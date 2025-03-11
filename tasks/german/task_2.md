# Input
- Programmierkonzept: While-Schleifen
- Kontext: Film

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Film-Watchlist

Schreibe eine Funktion namens `film_watchlist(filme)`, die eine Liste von Filmen als Argument erhält. Die Funktion soll eine While-Schleife verwenden, um durch die Liste zu iterieren und jeden Film auszugeben. Wenn die Liste leer ist, soll die Funktion "Keine Filme in der Watchlist." ausgeben.

Beispielaufruf:
```python
film_watchlist(["Inception", "The Matrix", "Interstellar"])
```

Erwartete Ausgabe:
```
Inception
The Matrix
Interstellar
```

Beispielaufruf:
```python
film_watchlist([])
```

Erwartete Ausgabe:
```
Keine Filme in der Watchlist.
```

## Codegerüst
```python
def film_watchlist(filme):
    ## Hier Code einfügen
```

## Musterlösung
```python
def film_watchlist(filme):
    if not filme:
        print("Keine Filme in der Watchlist.")
    while filme:
        print(filme.pop(0))

film_watchlist(["Inception", "The Matrix", "Interstellar"])
film_watchlist([])
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import film_watchlist

class TestFilmWatchlist(unittest.TestCase):
    def test_watchlist_with_films(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        film_watchlist(["Inception", "The Matrix", "Interstellar"])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Inception\nThe Matrix\nInterstellar")

    def test_empty_watchlist(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        film_watchlist([])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Keine Filme in der Watchlist.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 420
