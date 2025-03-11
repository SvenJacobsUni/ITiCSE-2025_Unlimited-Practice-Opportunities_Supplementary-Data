# Input
- Programmierkonzept: Funktionen als Variablen;Operationen mit Zahlen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen als Variablen und Operationen mit Zahlen im Kontext "Angeln"

Schreibe eine Funktion namens `fisch_gewicht_berechnen(fisch_gewicht_liste)`, die eine Liste von Gewichten (in Kilogramm) von gefangenen Fischen entgegennimmt und das Gesamtgewicht der Fische berechnet. Die Funktion soll das Gesamtgewicht der Fische zurückgeben.

Zusätzlich soll eine zweite Funktion `durchschnittsgewicht(fisch_gewicht_liste)` implementiert werden, die das Durchschnittsgewicht der Fische berechnet und zurückgibt.

Beispielaufrufe:
```python
fisch_gewicht_liste = [2.5, 3.0, 1.2, 4.8]
gesamtgewicht = fisch_gewicht_berechnen(fisch_gewicht_liste)
print(gesamtgewicht)  # Ausgabe: 11.5

durchschnitt = durchschnittsgewicht(fisch_gewicht_liste)
print(durchschnitt)  # Ausgabe: 2.875
```

Implementiere beide Funktionen so, dass sie korrekt arbeiten und die erwarteten Ergebnisse liefern.

## Codegerüst
```python
def fisch_gewicht_berechnen(fisch_gewicht_liste):
    ## Hier Code einfügen

def durchschnittsgewicht(fisch_gewicht_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fisch_gewicht_berechnen(fisch_gewicht_liste):
    return sum(fisch_gewicht_liste)

def durchschnittsgewicht(fisch_gewicht_liste):
    return sum(fisch_gewicht_liste) / len(fisch_gewicht_liste)

fisch_gewicht_liste = [2.5, 3.0, 1.2, 4.8]
gesamtgewicht = fisch_gewicht_berechnen(fisch_gewicht_liste)
print(gesamtgewicht)  # Ausgabe: 11.5

durchschnitt = durchschnittsgewicht(fisch_gewicht_liste)
print(durchschnitt)  # Ausgabe: 2.875
```

## Unit Tests
```python
import unittest

from main import fisch_gewicht_berechnen, durchschnittsgewicht

class TestFischGewichtBerechnen(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertEqual(fisch_gewicht_berechnen([2.5, 3.0, 1.2, 4.8]), 11.5)

    def test_leere_liste(self):
        self.assertEqual(fisch_gewicht_berechnen([]), 0)

    def test_ein_element(self):
        self.assertEqual(fisch_gewicht_berechnen([5.0]), 5.0)

    def test_negatives_gewicht(self):
        self.assertEqual(fisch_gewicht_berechnen([2.5, -1.0, 3.0]), 4.5)

class TestDurchschnittsgewicht(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertEqual(durchschnittsgewicht([2.5, 3.0, 1.2, 4.8]), 2.875)

    def test_leere_liste(self):
        with self.assertRaises(ZeroDivisionError):
            durchschnittsgewicht([])

    def test_ein_element(self):
        self.assertEqual(durchschnittsgewicht([5.0]), 5.0)

    def test_negatives_gewicht(self):
        self.assertEqual(durchschnittsgewicht([2.5, -1.0, 3.0]), 1.5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 541
