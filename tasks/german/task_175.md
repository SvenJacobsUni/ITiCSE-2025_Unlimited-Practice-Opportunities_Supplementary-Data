# Input
- Programmierkonzept: Funktionen als Variablen;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Listen
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustier-Filter

Schreibe eine Funktion namens `filter_haustiere(haustiere, kriterium)`, die eine Liste von Haustieren und ein Kriterium als Parameter erhält. Die Funktion soll eine neue Liste zurückgeben, die nur die Haustiere enthält, die dem Kriterium entsprechen.

Die Haustiere sind als Wörter in einer Liste gegeben, z.B. `["Hund", "Katze", "Hamster", "Vogel", "Fisch"]`.

Das Kriterium ist eine Funktion, die ein Haustier als Argument nimmt und einen Boolean-Wert zurückgibt. Zum Beispiel könnte ein Kriterium eine Funktion sein, die überprüft, ob der Name des Haustiers mit einem bestimmten Buchstaben beginnt.

Beispielaufruf:
```python
haustiere = ["Hund", "Katze", "Hamster", "Vogel", "Fisch"]
kriterium = lambda haustier: haustier.startswith("H")
print(filter_haustiere(haustiere, kriterium))  # Ausgabe: ["Hund", "Hamster"]
```

Implementiere die Funktion `filter_haustiere(haustiere, kriterium)`, sodass sie die oben beschriebene Funktionalität erfüllt.

## Codegerüst
```python
def filter_haustiere(haustiere, kriterium):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_haustiere(haustiere, kriterium):
    return [haustier for haustier in haustiere if kriterium(haustier)]

haustiere = ["Hund", "Katze", "Hamster", "Vogel", "Fisch"]
kriterium = lambda haustier: haustier.startswith("H")
print(filter_haustiere(haustiere, kriterium))  # Ausgabe: ["Hund", "Hamster"]
```

## Unit Tests
```python
import unittest
from main import filter_haustiere

class TestFilterHaustiere(unittest.TestCase):
    def test_haustiere_mit_h(self):
        haustiere = ["Hund", "Katze", "Hamster", "Vogel", "Fisch"]
        kriterium = lambda haustier: haustier.startswith("H")
        self.assertEqual(filter_haustiere(haustiere, kriterium), ["Hund", "Hamster"])

    def test_haustiere_mit_k(self):
        haustiere = ["Hund", "Katze", "Hamster", "Vogel", "Fisch"]
        kriterium = lambda haustier: haustier.startswith("K")
        self.assertEqual(filter_haustiere(haustiere, kriterium), ["Katze"])

    def test_haustiere_mit_v(self):
        haustiere = ["Hund", "Katze", "Hamster", "Vogel", "Fisch"]
        kriterium = lambda haustier: haustier.startswith("V")
        self.assertEqual(filter_haustiere(haustiere, kriterium), ["Vogel"])

    def test_haustiere_mit_f(self):
        haustiere = ["Hund", "Katze", "Hamster", "Vogel", "Fisch"]
        kriterium = lambda haustier: haustier.startswith("F")
        self.assertEqual(filter_haustiere(haustiere, kriterium), ["Fisch"])

    def test_leere_liste(self):
        haustiere = []
        kriterium = lambda haustier: haustier.startswith("H")
        self.assertEqual(filter_haustiere(haustiere, kriterium), [])

    def test_keine_haustiere_erfüllen_kriterium(self):
        haustiere = ["Hund", "Katze", "Hamster", "Vogel", "Fisch"]
        kriterium = lambda haustier: haustier.startswith("Z")
        self.assertEqual(filter_haustiere(haustiere, kriterium), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 607
