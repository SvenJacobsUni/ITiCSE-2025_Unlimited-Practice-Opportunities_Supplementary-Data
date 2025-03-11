# Input
- Programmierkonzept: If-Else-Anweisungen
- Kontext: Musik

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Musikgenre-Empfehlung

Schreibe eine Funktion namens `musik_empfehlung(genre)`, die basierend auf dem übergebenen Musikgenre eine entsprechende Nachricht zurückgibt. Die Funktion soll die folgenden Genres berücksichtigen:

- Bei "Rock" soll die Nachricht "Du magst es laut und energiegeladen!" zurückgegeben werden.
- Bei "Pop" soll die Nachricht "Du liebst eingängige Melodien und Rhythmen!" zurückgegeben werden.
- Bei "Jazz" soll die Nachricht "Du schätzt komplexe Harmonien und Improvisation!" zurückgegeben werden.
- Bei "Klassik" soll die Nachricht "Du genießt zeitlose Meisterwerke und Orchesterklänge!" zurückgegeben werden.

Falls ein anderes Genre übergeben wird, soll die Nachricht "Genre nicht erkannt. Probiere es mit Rock, Pop, Jazz oder Klassik." zurückgegeben werden.

Beispielaufrufe:
- `musik_empfehlung("Rock")` gibt "Du magst es laut und energiegeladen!" zurück.
- `musik_empfehlung("Hip-Hop")` gibt "Genre nicht erkannt. Probiere es mit Rock, Pop, Jazz oder Klassik." zurück.

## Codegerüst
```python
def musik_empfehlung(genre):
    ## Hier Code einfügen
```

## Musterlösung
```python
def musik_empfehlung(genre):
    if genre == "Rock":
        return "Du magst es laut und energiegeladen!"
    elif genre == "Pop":
        return "Du liebst eingängige Melodien und Rhythmen!"
    elif genre == "Jazz":
        return "Du schätzt komplexe Harmonien und Improvisation!"
    elif genre == "Klassik":
        return "Du genießt zeitlose Meisterwerke und Orchesterklänge!"
    else:
        return "Genre nicht erkannt. Probiere es mit Rock, Pop, Jazz oder Klassik."

# Beispielaufrufe
print(musik_empfehlung("Rock"))
print(musik_empfehlung("Hip-Hop"))
```

## Unit Tests
```python
import unittest
from main import musik_empfehlung

class TestMusikEmpfehlung(unittest.TestCase):
    def test_rock(self):
        self.assertEqual(musik_empfehlung("Rock"), "Du magst es laut und energiegeladen!")

    def test_pop(self):
        self.assertEqual(musik_empfehlung("Pop"), "Du liebst eingängige Melodien und Rhythmen!")

    def test_jazz(self):
        self.assertEqual(musik_empfehlung("Jazz"), "Du schätzt komplexe Harmonien und Improvisation!")

    def test_klassik(self):
        self.assertEqual(musik_empfehlung("Klassik"), "Du genießt zeitlose Meisterwerke und Orchesterklänge!")

    def test_unbekanntes_genre(self):
        self.assertEqual(musik_empfehlung("Hip-Hop"), "Genre nicht erkannt. Probiere es mit Rock, Pop, Jazz oder Klassik.")

    def test_leeres_genre(self):
        self.assertEqual(musik_empfehlung(""), "Genre nicht erkannt. Probiere es mit Rock, Pop, Jazz oder Klassik.")

    def test_none_genre(self):
        self.assertEqual(musik_empfehlung(None), "Genre nicht erkannt. Probiere es mit Rock, Pop, Jazz oder Klassik.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 426
