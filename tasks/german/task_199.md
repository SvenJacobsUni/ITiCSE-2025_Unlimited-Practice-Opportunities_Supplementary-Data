# Input
- Programmierkonzept: While-Schleifen;String;Tupel
- Kontext: Film

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Filmzitate zählen

Schreibe eine Funktion namens `zaehle_zitate(filmzitate)`, die eine Liste von Filmzitaten als Tupel erhält. Jedes Tupel enthält den Namen des Films und das Zitat. Die Funktion soll die Anzahl der Zitate für jeden Film zählen und das Ergebnis als Dictionary zurückgeben. Verwende eine While-Schleife, um durch die Liste der Filmzitate zu iterieren.

#### Beispiel:
```python
filmzitate = [
    ("Der Pate", "Ich werde ihm ein Angebot machen, das er nicht ablehnen kann."),
    ("Star Wars", "Möge die Macht mit dir sein."),
    ("Der Pate", "Lass die Waffe. Nimm die Cannoli."),
    ("Star Wars", "Ich bin dein Vater."),
    ("Der Pate", "Es war Barzini die ganze Zeit."),
]

ergebnis = zaehle_zitate(filmzitate)
print(ergebnis)  # Ausgabe: {'Der Pate': 3, 'Star Wars': 2}
```

Implementiere die Funktion `zaehle_zitate(filmzitate)`, die das oben beschriebene Verhalten aufweist.

## Codegerüst
```python
def zaehle_zitate(filmzitate):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_zitate(filmzitate):
    ergebnis = {}
    i = 0
    while i < len(filmzitate):
        film, _ = filmzitate[i]
        if film in ergebnis:
            ergebnis[film] += 1
        else:
            ergebnis[film] = 1
        i += 1
    return ergebnis

filmzitate = [
    ("Der Pate", "Ich werde ihm ein Angebot machen, das er nicht ablehnen kann."),
    ("Star Wars", "Möge die Macht mit dir sein."),
    ("Der Pate", "Lass die Waffe. Nimm die Cannoli."),
    ("Star Wars", "Ich bin dein Vater."),
    ("Der Pate", "Es war Barzini die ganze Zeit."),
]

ergebnis = zaehle_zitate(filmzitate)
print(ergebnis)  # Ausgabe: {'Der Pate': 3, 'Star Wars': 2}
```

## Unit Tests
```python
import unittest

from main import zaehle_zitate

class TestZaehleZitate(unittest.TestCase):
    def test_mehrere_filme(self):
        filmzitate = [
            ("Der Pate", "Ich werde ihm ein Angebot machen, das er nicht ablehnen kann."),
            ("Star Wars", "Möge die Macht mit dir sein."),
            ("Der Pate", "Lass die Waffe. Nimm die Cannoli."),
            ("Star Wars", "Ich bin dein Vater."),
            ("Der Pate", "Es war Barzini die ganze Zeit."),
        ]
        self.assertEqual(zaehle_zitate(filmzitate), {'Der Pate': 3, 'Star Wars': 2})

    def test_ein_film(self):
        filmzitate = [
            ("Inception", "Du musst tiefer gehen."),
            ("Inception", "Ein Gedanke ist wie ein Virus."),
        ]
        self.assertEqual(zaehle_zitate(filmzitate), {'Inception': 2})

    def test_keine_zitate(self):
        filmzitate = []
        self.assertEqual(zaehle_zitate(filmzitate), {})

    def test_ein_zitat(self):
        filmzitate = [("Matrix", "Es gibt keinen Löffel.")]
        self.assertEqual(zaehle_zitate(filmzitate), {'Matrix': 1})

    def test_verschiedene_filme(self):
        filmzitate = [
            ("Matrix", "Es gibt keinen Löffel."),
            ("Inception", "Du musst tiefer gehen."),
            ("Star Wars", "Möge die Macht mit dir sein."),
        ]
        self.assertEqual(zaehle_zitate(filmzitate), {'Matrix': 1, 'Inception': 1, 'Star Wars': 1})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 631
