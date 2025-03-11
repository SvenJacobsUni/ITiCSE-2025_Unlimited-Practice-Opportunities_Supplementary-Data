# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Rugby-Kontext

Schreibe eine Funktion `punkte_berechnen(spieler_punkte, berechnungs_funktion)`, die eine Liste von Punkten, die von verschiedenen Rugby-Spielern erzielt wurden, und eine Funktion als Argumente entgegennimmt. Die Funktion `punkte_berechnen` soll die übergebene Berechnungsfunktion auf die Liste der Spielerpunkte anwenden und das Ergebnis zurückgeben.

Beispiel:
- `spieler_punkte` ist eine Liste von Punkten, z.B. `[5, 3, 7, 2]`.
- `berechnungs_funktion` könnte eine Funktion sein, die die Summe der Punkte berechnet.

Beispielaufruf:
```python
def summe_punkte(punkte):
    return sum(punkte)

punkte = [5, 3, 7, 2]
ergebnis = punkte_berechnen(punkte, summe_punkte)
print(ergebnis)  # Ausgabe: 17
```

Implementiere die Funktion `punkte_berechnen` und teste sie mit verschiedenen Berechnungsfunktionen.

## Codegerüst
```python
def punkte_berechnen(spieler_punkte, berechnungs_funktion):
    ## Hier Code einfügen
```

## Musterlösung
```python
def punkte_berechnen(spieler_punkte, berechnungs_funktion):
    return berechnungs_funktion(spieler_punkte)

def summe_punkte(punkte):
    return sum(punkte)

punkte = [5, 3, 7, 2]
ergebnis = punkte_berechnen(punkte, summe_punkte)
print(ergebnis)  # Ausgabe: 17
```

## Unit Tests
```python
import unittest
from main import punkte_berechnen

def summe_punkte(punkte):
    return sum(punkte)

def max_punkte(punkte):
    return max(punkte)

def min_punkte(punkte):
    return min(punkte)

class TestPunkteBerechnen(unittest.TestCase):
    def test_summe_punkte(self):
        self.assertEqual(punkte_berechnen([5, 3, 7, 2], summe_punkte), 17)

    def test_max_punkte(self):
        self.assertEqual(punkte_berechnen([5, 3, 7, 2], max_punkte), 7)

    def test_min_punkte(self):
        self.assertEqual(punkte_berechnen([5, 3, 7, 2], min_punkte), 2)

    def test_leere_liste_summe(self):
        self.assertEqual(punkte_berechnen([], summe_punkte), 0)

    def test_leere_liste_max(self):
        with self.assertRaises(ValueError):
            punkte_berechnen([], max_punkte)

    def test_leere_liste_min(self):
        with self.assertRaises(ValueError):
            punkte_berechnen([], min_punkte)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 431
