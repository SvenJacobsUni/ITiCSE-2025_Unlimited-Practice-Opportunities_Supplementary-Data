# Input
- Programmierkonzept: Funktionen als Variablen;Rekursion;Tupel
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rezeptverwaltung mit Rekursion und Tupeln

Schreibe eine Funktion `kochrezept(rezept)`, die ein Rezept als Eingabe erhält und die Zutaten und Zubereitungsschritte rekursiv durchläuft. Das Rezept wird als verschachteltes Tupel übergeben, wobei jedes Element entweder eine Zutat (als String) oder ein weiterer Zubereitungsschritt (als Tupel) ist. Die Funktion soll die Zutaten und Schritte in der richtigen Reihenfolge ausgeben.

Beispiel:

```python
rezept = (
    "Zutaten vorbereiten",
    (
        "Tomaten schneiden",
        "Zwiebeln hacken",
        (
            "Knoblauch schälen",
            "Knoblauch hacken"
        )
    ),
    "Alles in die Pfanne geben",
    "Mit Salz und Pfeffer würzen"
)

kochrezept(rezept)
```

Erwartete Ausgabe:

```
Zutaten vorbereiten
Tomaten schneiden
Zwiebeln hacken
Knoblauch schälen
Knoblauch hacken
Alles in die Pfanne geben
Mit Salz und Pfeffer würzen
```

Implementiere die Funktion `kochrezept(rezept)`, die das Rezept rekursiv durchläuft und die Schritte in der richtigen Reihenfolge ausgibt.

## Codegerüst
```python
def kochrezept(rezept):
    ## Hier Code einfügen
```

## Musterlösung
```python
def kochrezept(rezept):
    for schritt in rezept:
        if isinstance(schritt, tuple):
            kochrezept(schritt)
        else:
            print(schritt)

rezept = (
    "Zutaten vorbereiten",
    (
        "Tomaten schneiden",
        "Zwiebeln hacken",
        (
            "Knoblauch schälen",
            "Knoblauch hacken"
        )
    ),
    "Alles in die Pfanne geben",
    "Mit Salz und Pfeffer würzen"
)

kochrezept(rezept)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import kochrezept

class TestKochrezept(unittest.TestCase):
    def setUp(self):
        self.rezept = (
            "Zutaten vorbereiten",
            (
                "Tomaten schneiden",
                "Zwiebeln hacken",
                (
                    "Knoblauch schälen",
                    "Knoblauch hacken"
                )
            ),
            "Alles in die Pfanne geben",
            "Mit Salz und Pfeffer würzen"
        )

    def test_kochrezept(self):
        expected_output = (
            "Zutaten vorbereiten\n"
            "Tomaten schneiden\n"
            "Zwiebeln hacken\n"
            "Knoblauch schälen\n"
            "Knoblauch hacken\n"
            "Alles in die Pfanne geben\n"
            "Mit Salz und Pfeffer würzen\n"
        )
        captured_output = StringIO()
        sys.stdout = captured_output
        kochrezept(self.rezept)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 599
