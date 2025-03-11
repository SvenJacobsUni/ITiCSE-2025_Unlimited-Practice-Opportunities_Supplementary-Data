# Input
- Programmierkonzept: Integer
- Kontext: Film

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Filmbewertung

Schreibe eine Funktion namens `bewerte_film(bewertung)`, die eine Bewertung für einen Film entgegennimmt und eine entsprechende Nachricht zurückgibt. Die Bewertung ist ein Integer-Wert zwischen 1 und 10.

- Wenn die Bewertung zwischen 1 und 3 liegt, soll die Nachricht "Der Film war schlecht." zurückgegeben werden.
- Wenn die Bewertung zwischen 4 und 6 liegt, soll die Nachricht "Der Film war durchschnittlich." zurückgegeben werden.
- Wenn die Bewertung zwischen 7 und 10 liegt, soll die Nachricht "Der Film war großartig!" zurückgegeben werden.

Beispielaufrufe:
- `bewerte_film(2)` gibt "Der Film war schlecht." zurück.
- `bewerte_film(5)` gibt "Der Film war durchschnittlich." zurück.
- `bewerte_film(9)` gibt "Der Film war großartig!" zurück.

## Codegerüst
```python
def bewerte_film(bewertung):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_film(bewertung):
    if 1 <= bewertung <= 3:
        return "Der Film war schlecht."
    elif 4 <= bewertung <= 6:
        return "Der Film war durchschnittlich."
    elif 7 <= bewertung <= 10:
        return "Der Film war großartig!"

# Beispielaufrufe
print(bewerte_film(2))
print(bewerte_film(5))
print(bewerte_film(9))
```

## Unit Tests
```python
import unittest
from main import bewerte_film

class TestBewerteFilm(unittest.TestCase):
    def test_schlecht(self):
        self.assertEqual(bewerte_film(2), "Der Film war schlecht.")

    def test_durchschnittlich(self):
        self.assertEqual(bewerte_film(5), "Der Film war durchschnittlich.")

    def test_grossartig(self):
        self.assertEqual(bewerte_film(9), "Der Film war großartig!")

    def test_unterer_randwert(self):
        self.assertEqual(bewerte_film(1), "Der Film war schlecht.")

    def test_oberer_randwert(self):
        self.assertEqual(bewerte_film(10), "Der Film war großartig!")

    def test_grenze_schlecht_durchschnittlich(self):
        self.assertEqual(bewerte_film(3), "Der Film war schlecht.")
        self.assertEqual(bewerte_film(4), "Der Film war durchschnittlich.")

    def test_grenze_durchschnittlich_grossartig(self):
        self.assertEqual(bewerte_film(6), "Der Film war durchschnittlich.")
        self.assertEqual(bewerte_film(7), "Der Film war großartig.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 464
