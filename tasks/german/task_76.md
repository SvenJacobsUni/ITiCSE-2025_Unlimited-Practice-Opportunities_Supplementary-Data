# Input
- Programmierkonzept: For-Schleifen
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Punktestand

Schreibe eine Funktion namens `berechne_punktestand(punkte_liste)`, die eine Liste von erzielten Punkten in einem Basketballspiel als Argument erhält. Die Funktion soll die Gesamtpunktzahl berechnen und zurückgeben. Verwende eine For-Schleife, um die Punkte zu summieren.

Beispielaufruf:
```python
punkte = [2, 3, 2, 1, 3, 2]
gesamtpunktzahl = berechne_punktestand(punkte)
print(gesamtpunktzahl)  # Ausgabe: 13
```

Implementiere die Funktion `berechne_punktestand(punkte_liste)`, sodass sie die Gesamtpunktzahl korrekt berechnet und zurückgibt.

## Codegerüst
```python
def berechne_punktestand(punkte_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punktestand(punkte_liste):
    return sum(punkte_liste)

punkte = [2, 3, 2, 1, 3, 2]
gesamtpunktzahl = berechne_punktestand(punkte)
print(gesamtpunktzahl)  # Ausgabe: 13
```

## Unit Tests
```python
import unittest
from main import berechne_punktestand

class TestBerechnePunktestand(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(berechne_punktestand([]), 0)

    def test_ein_punkt(self):
        self.assertEqual(berechne_punktestand([2]), 2)

    def test_mehrere_punkte(self):
        self.assertEqual(berechne_punktestand([2, 3, 2, 1, 3, 2]), 13)

    def test_negativer_punkt(self):
        self.assertEqual(berechne_punktestand([2, -1, 3]), 4)

    def test_gemischte_punkte(self):
        self.assertEqual(berechne_punktestand([2, 3, 0, 1, 3, 2]), 11)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 494
