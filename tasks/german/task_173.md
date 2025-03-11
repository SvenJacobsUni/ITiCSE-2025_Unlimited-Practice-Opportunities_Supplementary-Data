# Input
- Programmierkonzept: Operationen mit Zahlen;Tupel;For-Schleifen
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Leistungen analysieren

Schreibe eine Funktion namens `analyse_leistungen(leistungen)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel enthält den Namen eines Sportlers und seine erzielte Punktzahl in einem Wettkampf. Die Funktion soll die durchschnittliche Punktzahl aller Sportler berechnen und zurückgeben.

Beispielaufruf:
```python
leistungen = [("Anna", 15), ("Ben", 20), ("Clara", 18), ("David", 22)]
durchschnitt = analyse_leistungen(leistungen)
print(durchschnitt)  # Erwartete Ausgabe: 18.75
```

**Hinweis:** Die Funktion soll keine Eingaben über die Standardeingabe erwarten.

## Codegerüst
```python
def analyse_leistungen(leistungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def analyse_leistungen(leistungen):
    return sum(p for _, p in leistungen) / len(leistungen)

leistungen = [("Anna", 15), ("Ben", 20), ("Clara", 18), ("David", 22)]
durchschnitt = analyse_leistungen(leistungen)
print(durchschnitt)  # Erwartete Ausgabe: 18.75
```

## Unit Tests
```python
import unittest

from main import analyse_leistungen

class TestAnalyseLeistungen(unittest.TestCase):
    def test_durchschnitt(self):
        leistungen = [("Anna", 15), ("Ben", 20), ("Clara", 18), ("David", 22)]
        self.assertEqual(analyse_leistungen(leistungen), 18.75)

    def test_leere_liste(self):
        leistungen = []
        with self.assertRaises(ZeroDivisionError):
            analyse_leistungen(leistungen)

    def test_ein_sportler(self):
        leistungen = [("Anna", 15)]
        self.assertEqual(analyse_leistungen(leistungen), 15)

    def test_negative_punkte(self):
        leistungen = [("Anna", -5), ("Ben", 10)]
        self.assertEqual(analyse_leistungen(leistungen), 2.5)

    def test_gemischte_punkte(self):
        leistungen = [("Anna", 0), ("Ben", 10), ("Clara", 20)]
        self.assertEqual(analyse_leistungen(leistungen), 10)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 605
