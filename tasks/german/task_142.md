# Input
- Programmierkonzept: While-Schleifen;If-Else-Anweisungen
- Kontext: Film

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Filmempfehlung basierend auf Bewertungen

Schreibe eine Funktion namens `film_empfehlung(bewertungen)`, die eine Liste von Bewertungen (Zahlen von 1 bis 5) als Argument erhält. Die Funktion soll die durchschnittliche Bewertung berechnen und basierend auf dieser Bewertung eine Empfehlung ausgeben.

- Wenn die durchschnittliche Bewertung 4 oder höher ist, soll die Funktion "Sehr empfehlenswert!" zurückgeben.
- Wenn die durchschnittliche Bewertung zwischen 3 und 4 liegt, soll die Funktion "Empfehlenswert" zurückgeben.
- Wenn die durchschnittliche Bewertung zwischen 2 und 3 liegt, soll die Funktion "Durchschnittlich" zurückgeben.
- Wenn die durchschnittliche Bewertung unter 2 liegt, soll die Funktion "Nicht empfehlenswert" zurückgeben.

Beispielaufruf:
```python
print(film_empfehlung([5, 4, 3, 4, 5]))  # Ausgabe: "Sehr empfehlenswert!"
```

## Codegerüst
```python
def film_empfehlung(bewertungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def film_empfehlung(bewertungen):
    avg = sum(bewertungen) / len(bewertungen)
    if avg >= 4:
        return "Sehr empfehlenswert!"
    elif avg >= 3:
        return "Empfehlenswert"
    elif avg >= 2:
        return "Durchschnittlich"
    else:
        return "Nicht empfehlenswert"

print(film_empfehlung([5, 4, 3, 4, 5]))
```

## Unit Tests
```python
import unittest
from main import film_empfehlung

class TestFilmEmpfehlung(unittest.TestCase):
    def test_sehr_empfehlenswert(self):
        self.assertEqual(film_empfehlung([5, 4, 4, 5, 5]), "Sehr empfehlenswert!")

    def test_empfehlenswert(self):
        self.assertEqual(film_empfehlung([3, 3, 4, 3, 3]), "Empfehlenswert")

    def test_durchschnittlich(self):
        self.assertEqual(film_empfehlung([2, 2, 3, 2, 2]), "Durchschnittlich")

    def test_nicht_empfehlenswert(self):
        self.assertEqual(film_empfehlung([1, 1, 2, 1, 1]), "Nicht empfehlenswert")

    def test_leere_liste(self):
        with self.assertRaises(ZeroDivisionError):
            film_empfehlung([])

    def test_ein_element(self):
        self.assertEqual(film_empfehlung([5]), "Sehr empfehlenswert!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 574
