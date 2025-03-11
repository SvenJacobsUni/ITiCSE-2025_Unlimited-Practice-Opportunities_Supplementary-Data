# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Kontext "Kochen"

Schreibe eine Funktion `koch_assistent(rezept, zubereitung)`, die zwei Argumente akzeptiert: eine Liste von Zutaten (`rezept`) und eine Funktion (`zubereitung`), die die Zubereitungsschritte beschreibt. Die Funktion `koch_assistent` soll die Zubereitungsschritte auf jede Zutat anwenden und eine Liste der Ergebnisse zurückgeben.

Beispielaufruf:
```python
def schneide(ingredient):
    return f"Schneide {ingredient}"

zutaten = ["Tomaten", "Zwiebeln", "Paprika"]
resultat = koch_assistent(zutaten, schneide)
print(resultat)  # Ausgabe: ["Schneide Tomaten", "Schneide Zwiebeln", "Schneide Paprika"]
```

Implementiere die Funktion `koch_assistent` so, dass sie die Zubereitungsschritte auf jede Zutat in der Liste anwendet und die Ergebnisse in einer neuen Liste zurückgibt.

## Codegerüst
```python
def koch_assistent(rezept, zubereitung):
    ## Hier Code einfügen
```

## Musterlösung
```python
def koch_assistent(rezept, zubereitung):
    return [zubereitung(zutat) for zutat in rezept]

def schneide(ingredient):
    return f"Schneide {ingredient}"

zutaten = ["Tomaten", "Zwiebeln", "Paprika"]
resultat = koch_assistent(zutaten, schneide)
print(resultat)
```

## Unit Tests
```python
import unittest
from main import koch_assistent

def schneide(ingredient):
    return f"Schneide {ingredient}"

def koche(ingredient):
    return f"Koche {ingredient}"

class TestKochAssistent(unittest.TestCase):
    def test_schneide(self):
        zutaten = ["Tomaten", "Zwiebeln", "Paprika"]
        expected = ["Schneide Tomaten", "Schneide Zwiebeln", "Schneide Paprika"]
        self.assertEqual(koch_assistent(zutaten, schneide), expected)

    def test_koche(self):
        zutaten = ["Kartoffeln", "Karotten"]
        expected = ["Koche Kartoffeln", "Koche Karotten"]
        self.assertEqual(koch_assistent(zutaten, koche), expected)

    def test_leere_liste(self):
        zutaten = []
        expected = []
        self.assertEqual(koch_assistent(zutaten, schneide), expected)

    def test_eine_zutat(self):
        zutaten = ["Gurke"]
        expected = ["Schneide Gurke"]
        self.assertEqual(koch_assistent(zutaten, schneide), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 463
