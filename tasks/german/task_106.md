# Input
- Programmierkonzept: Float;Tupel
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustiergewicht

Schreibe eine Funktion namens `haustier_gewicht(haustiere)`, die ein Tupel von Haustieren und deren Gewichten (in Kilogramm) als Eingabe erhält. Die Funktion soll das durchschnittliche Gewicht der Haustiere berechnen und zurückgeben.

Beispielaufruf:
```python
haustiere = (("Hund", 20.5), ("Katze", 4.3), ("Hamster", 0.1))
durchschnitt = haustier_gewicht(haustiere)
print(durchschnitt)  # Erwartete Ausgabe: 8.3
```

Implementiere die Funktion so, dass sie das durchschnittliche Gewicht der Haustiere korrekt berechnet und zurückgibt.

## Codegerüst
```python
def haustier_gewicht(haustiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def haustier_gewicht(haustiere):
    return sum(gewicht for _, gewicht in haustiere) / len(haustiere)

haustiere = (("Hund", 20.5), ("Katze", 4.3), ("Hamster", 0.1))
durchschnitt = haustier_gewicht(haustiere)
print(durchschnitt)  # Erwartete Ausgabe: 8.3
```

## Unit Tests
```python
import unittest
from main import haustier_gewicht

class TestHaustierGewicht(unittest.TestCase):
    def test_durchschnittliches_gewicht(self):
        haustiere = (("Hund", 20.5), ("Katze", 4.3), ("Hamster", 0.1))
        self.assertAlmostEqual(haustier_gewicht(haustiere), 8.3, places=1)

    def test_leere_liste(self):
        haustiere = ()
        with self.assertRaises(ZeroDivisionError):
            haustier_gewicht(haustiere)

    def test_ein_haustier(self):
        haustiere = (("Hund", 20.5),)
        self.assertEqual(haustier_gewicht(haustiere), 20.5)

    def test_gemischte_gewichte(self):
        haustiere = (("Hund", 20.5), ("Katze", 4.3), ("Hamster", 0.1), ("Papagei", 1.2))
        self.assertAlmostEqual(haustier_gewicht(haustiere), 6.525, places=3)

    def test_negative_gewichte(self):
        haustiere = (("Hund", -20.5), ("Katze", -4.3), ("Hamster", -0.1))
        self.assertAlmostEqual(haustier_gewicht(haustiere), -8.3, places=1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 538
