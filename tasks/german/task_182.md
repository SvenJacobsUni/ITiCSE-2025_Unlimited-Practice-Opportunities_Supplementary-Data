# Input
- Programmierkonzept: String;Listen;Funktionen als Variablen
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Positive Affirmationen

Positive Affirmationen können helfen, das Selbstwertgefühl zu stärken und die psychische Gesundheit zu fördern. In dieser Aufgabe sollst du eine Funktion implementieren, die eine Liste von positiven Affirmationen verarbeitet und eine zufällige Affirmation zurückgibt.

#### Aufgabe

Schreibe eine Funktion `zufaellige_affirmation(affirmationen)`, die eine Liste von positiven Affirmationen als Argument erhält und eine zufällige Affirmation aus dieser Liste zurückgibt. Verwende die Funktion `random.choice` aus dem Modul `random`, um die zufällige Auswahl zu treffen.

#### Beispiel

```python
affirmationen = [
    "Ich bin stark und fähig.",
    "Ich verdiene Liebe und Respekt.",
    "Ich bin genug, so wie ich bin.",
    "Ich kann alles erreichen, was ich mir vornehme."
]

print(zufaellige_affirmation(affirmationen))
```

Die Ausgabe könnte eine der Affirmationen aus der Liste sein, z.B. "Ich bin stark und fähig."

#### Hinweise

- Importiere das Modul `random`, um die Funktion `random.choice` zu verwenden.
- Die Funktion soll eine der Affirmationen aus der Liste zurückgeben.

Viel Erfolg!

## Codegerüst
```python
def zufaellige_affirmation(affirmationen):
    ## Hier Code einfügen
```

## Musterlösung
```python
import random

def zufaellige_affirmation(affirmationen):
    return random.choice(affirmationen)

affirmationen = [
    "Ich bin stark und fähig.",
    "Ich verdiene Liebe und Respekt.",
    "Ich bin genug, so wie ich bin.",
    "Ich kann alles erreichen, was ich mir vornehme."
]

print(zufaellige_affirmation(affirmationen))
```

## Unit Tests
```python
import unittest
from main import zufaellige_affirmation

class TestZufaelligeAffirmation(unittest.TestCase):
    def test_auswahl_aus_liste(self):
        affirmationen = [
            "Ich bin stark und fähig.",
            "Ich verdiene Liebe und Respekt.",
            "Ich bin genug, so wie ich bin.",
            "Ich kann alles erreichen, was ich mir vornehme."
        ]
        ergebnis = zufaellige_affirmation(affirmationen)
        self.assertIn(ergebnis, affirmationen)

    def test_leere_liste(self):
        affirmationen = []
        with self.assertRaises(IndexError):
            zufaellige_affirmation(affirmationen)

    def test_ein_element(self):
        affirmationen = ["Ich bin stark und fähig."]
        self.assertEqual(zufaellige_affirmation(affirmationen), "Ich bin stark und fähig.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 614
