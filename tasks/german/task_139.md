# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);While-Schleifen
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungsstatus überprüfen

Schreibe eine Funktion namens `beziehungsstatus(pruefungen)`, die eine Liste von Prüfungen (als Tupel) erhält. Jedes Tupel enthält zwei Elemente: den Namen einer Person und deren Beziehungsstatus (als String). Die Funktion soll die Anzahl der Personen in jeder der folgenden Kategorien zählen: "Single", "In einer Beziehung", "Verheiratet" und "Es ist kompliziert". Die Funktion soll ein Dictionary zurückgeben, das die Anzahl der Personen in jeder Kategorie enthält.

Beispielaufruf:
```python
pruefungen = [("Anna", "Single"), ("Ben", "In einer Beziehung"), ("Clara", "Verheiratet"), ("David", "Es ist kompliziert"), ("Eva", "Single")]
print(beziehungsstatus(pruefungen))
```

Erwartete Ausgabe:
```python
{
    "Single": 2,
    "In einer Beziehung": 1,
    "Verheiratet": 1,
    "Es ist kompliziert": 1
}
```

## Codegerüst
```python
def beziehungsstatus(pruefungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beziehungsstatus(pruefungen):
    status_dict = {"Single": 0, "In einer Beziehung": 0, "Verheiratet": 0, "Es ist kompliziert": 0}
    for _, status in pruefungen:
        if status in status_dict:
            status_dict[status] += 1
    return status_dict

pruefungen = [("Anna", "Single"), ("Ben", "In einer Beziehung"), ("Clara", "Verheiratet"), ("David", "Es ist kompliziert"), ("Eva", "Single")]
print(beziehungsstatus(pruefungen))
```

## Unit Tests
```python
import unittest
from main import beziehungsstatus

class TestBeziehungsstatus(unittest.TestCase):
    def test_alle_kategorien(self):
        pruefungen = [("Anna", "Single"), ("Ben", "In einer Beziehung"), ("Clara", "Verheiratet"), ("David", "Es ist kompliziert"), ("Eva", "Single")]
        expected = {"Single": 2, "In einer Beziehung": 1, "Verheiratet": 1, "Es ist kompliziert": 1}
        self.assertEqual(beziehungsstatus(pruefungen), expected)

    def test_nur_single(self):
        pruefungen = [("Anna", "Single"), ("Ben", "Single"), ("Clara", "Single")]
        expected = {"Single": 3, "In einer Beziehung": 0, "Verheiratet": 0, "Es ist kompliziert": 0}
        self.assertEqual(beziehungsstatus(pruefungen), expected)

    def test_leere_liste(self):
        pruefungen = []
        expected = {"Single": 0, "In einer Beziehung": 0, "Verheiratet": 0, "Es ist kompliziert": 0}
        self.assertEqual(beziehungsstatus(pruefungen), expected)

    def test_alle_verheiratet(self):
        pruefungen = [("Anna", "Verheiratet"), ("Ben", "Verheiratet"), ("Clara", "Verheiratet")]
        expected = {"Single": 0, "In einer Beziehung": 0, "Verheiratet": 3, "Es ist kompliziert": 0}
        self.assertEqual(beziehungsstatus(pruefungen), expected)

    def test_alle_kompliziert(self):
        pruefungen = [("Anna", "Es ist kompliziert"), ("Ben", "Es ist kompliziert"), ("Clara", "Es ist kompliziert")]
        expected = {"Single": 0, "In einer Beziehung": 0, "Verheiratet": 0, "Es ist kompliziert": 3}
        self.assertEqual(beziehungsstatus(pruefungen), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 571
