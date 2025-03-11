# Input
- Programmierkonzept: Rekursion
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Berechnung der Rugby-Punktzahl

In einem Rugby-Spiel erhält ein Team Punkte durch verschiedene Aktionen:

- Ein Versuch (Try) bringt 5 Punkte.
- Eine Erhöhung (Conversion) bringt 2 Punkte.
- Ein Straftritt (Penalty) oder ein Dropgoal bringt jeweils 3 Punkte.

Schreibe eine rekursive Funktion `berechne_punkte(aktionen)`, die eine Liste von Aktionen als Eingabe erhält und die Gesamtpunktzahl des Teams berechnet. Jede Aktion in der Liste ist ein String, der entweder "Try", "Conversion", "Penalty" oder "Dropgoal" lautet.

Beispielaufruf:
```python
aktionen = ["Try", "Conversion", "Penalty", "Try", "Dropgoal"]
print(berechne_punkte(aktionen))  # Ausgabe: 18
```

Implementiere die Funktion `berechne_punkte(aktionen)`, die die Gesamtpunktzahl des Teams berechnet und zurückgibt.

## Codegerüst
```python
def berechne_punkte(aktionen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punkte(aktionen):
    if not aktionen:
        return 0
    punkte = {"Try": 5, "Conversion": 2, "Penalty": 3, "Dropgoal": 3}
    return punkte[aktionen[0]] + berechne_punkte(aktionen[1:])

aktionen = ["Try", "Conversion", "Penalty", "Try", "Dropgoal"]
print(berechne_punkte(aktionen))
```

## Unit Tests
```python
import unittest
from main import berechne_punkte

class TestBerechnePunkte(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(berechne_punkte([]), 0)

    def test_nur_try(self):
        self.assertEqual(berechne_punkte(["Try"]), 5)

    def test_nur_conversion(self):
        self.assertEqual(berechne_punkte(["Conversion"]), 2)

    def test_nur_penalty(self):
        self.assertEqual(berechne_punkte(["Penalty"]), 3)

    def test_nur_dropgoal(self):
        self.assertEqual(berechne_punkte(["Dropgoal"]), 3)

    def test_gemischte_aktionen(self):
        self.assertEqual(berechne_punkte(["Try", "Conversion", "Penalty", "Try", "Dropgoal"]), 18)

    def test_mehrere_tries(self):
        self.assertEqual(berechne_punkte(["Try", "Try", "Try"]), 15)

    def test_mehrere_conversions(self):
        self.assertEqual(berechne_punkte(["Conversion", "Conversion", "Conversion"]), 6)

    def test_mehrere_penalties(self):
        self.assertEqual(berechne_punkte(["Penalty", "Penalty", "Penalty"]), 9)

    def test_mehrere_dropgoals(self):
        self.assertEqual(berechne_punkte(["Dropgoal", "Dropgoal", "Dropgoal"]), 9)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 483
