# Input
- Programmierkonzept: Boolean und None;Operationen mit Zahlen;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungsstatus überprüfen

Schreibe eine Funktion namens `beziehungsstatus(alter, beziehungsdauer)`, die den Beziehungsstatus einer Person basierend auf ihrem Alter und der Dauer ihrer aktuellen Beziehung überprüft. Die Funktion soll eine entsprechende Nachricht mit `return` zurückgeben.

- Wenn die Person jünger als 18 Jahre ist, soll die Funktion "Zu jung für eine ernsthafte Beziehung." zurückgeben.
- Wenn die Person 18 Jahre oder älter ist und die Beziehungsdauer weniger als 1 Jahr beträgt, soll die Funktion "Frisch verliebt!" zurückgeben.
- Wenn die Person 18 Jahre oder älter ist und die Beziehungsdauer zwischen 1 und 5 Jahren liegt, soll die Funktion "In einer stabilen Beziehung." zurückgeben.
- Wenn die Person 18 Jahre oder älter ist und die Beziehungsdauer mehr als 5 Jahre beträgt, soll die Funktion "Langzeitbeziehung." zurückgeben.

Beispielaufrufe:
- `beziehungsstatus(16, 0.5)` gibt "Zu jung für eine ernsthafte Beziehung." zurück.
- `beziehungsstatus(25, 0.8)` gibt "Frisch verliebt!" zurück.
- `beziehungsstatus(30, 3)` gibt "In einer stabilen Beziehung." zurück.
- `beziehungsstatus(40, 6)` gibt "Langzeitbeziehung." zurück.

## Codegerüst
```python
def beziehungsstatus(alter, beziehungsdauer):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beziehungsstatus(alter, beziehungsdauer):
    if alter < 18:
        return "Zu jung für eine ernsthafte Beziehung."
    elif beziehungsdauer < 1:
        return "Frisch verliebt!"
    elif beziehungsdauer <= 5:
        return "In einer stabilen Beziehung."
    else:
        return "Langzeitbeziehung."

# Beispielaufrufe
print(beziehungsstatus(16, 0.5))
print(beziehungsstatus(25, 0.8))
print(beziehungsstatus(30, 3))
print(beziehungsstatus(40, 6))
```

## Unit Tests
```python
import unittest
from main import beziehungsstatus

class TestBeziehungsstatus(unittest.TestCase):
    def test_zu_jung(self):
        self.assertEqual(beziehungsstatus(16, 0.5), "Zu jung für eine ernsthafte Beziehung.")

    def test_frisch_verliebt(self):
        self.assertEqual(beziehungsstatus(25, 0.8), "Frisch verliebt!")

    def test_stabile_beziehung(self):
        self.assertEqual(beziehungsstatus(30, 3), "In einer stabilen Beziehung.")

    def test_langzeitbeziehung(self):
        self.assertEqual(beziehungsstatus(40, 6), "Langzeitbeziehung.")

    def test_grenze_18_jahre(self):
        self.assertEqual(beziehungsstatus(18, 0.5), "Frisch verliebt!")

    def test_grenze_1_jahr(self):
        self.assertEqual(beziehungsstatus(25, 1), "In einer stabilen Beziehung.")

    def test_grenze_5_jahre(self):
        self.assertEqual(beziehungsstatus(30, 5), "In einer stabilen Beziehung.")

    def test_grenze_5_jahre_ueberschritten(self):
        self.assertEqual(beziehungsstatus(30, 5.1), "Langzeitbeziehung.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 587
