# Input
- Programmierkonzept: Boolean und None;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Float
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungsstatus überprüfen

Schreibe eine Funktion namens `beziehungsstatus(alter, beziehungsdauer, gemeinsame_interessen)`, die den Beziehungsstatus basierend auf dem Alter der Person, der Dauer der Beziehung (in Jahren) und der Anzahl der gemeinsamen Interessen überprüft. Die Funktion soll folgende Regeln anwenden:

1. Wenn das Alter der Person unter 18 ist, soll die Funktion `None` zurückgeben.
2. Wenn die Beziehungsdauer weniger als 1 Jahr beträgt und die Anzahl der gemeinsamen Interessen weniger als 3 ist, soll die Funktion `False` zurückgeben.
3. Wenn die Beziehungsdauer 1 Jahr oder mehr beträgt und die Anzahl der gemeinsamen Interessen 3 oder mehr ist, soll die Funktion `True` zurückgeben.
4. In allen anderen Fällen soll die Funktion `False` zurückgeben.

Beispielaufrufe:
- `beziehungsstatus(17, 2, 5)` gibt `None` zurück.
- `beziehungsstatus(25, 0.5, 2)` gibt `False` zurück.
- `beziehungsstatus(30, 2, 4)` gibt `True` zurück.
- `beziehungsstatus(22, 1, 2)` gibt `False` zurück.

## Codegerüst
```python
def beziehungsstatus(alter, beziehungsdauer, gemeinsame_interessen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beziehungsstatus(alter, beziehungsdauer, gemeinsame_interessen):
    if alter < 18:
        return None
    if beziehungsdauer >= 1 and gemeinsame_interessen >= 3:
        return True
    return False

print(beziehungsstatus(17, 2, 5))  # None
print(beziehungsstatus(25, 0.5, 2))  # False
print(beziehungsstatus(30, 2, 4))  # True
print(beziehungsstatus(22, 1, 2))  # False
```

## Unit Tests
```python
import unittest

from main import beziehungsstatus

class TestBeziehungsstatus(unittest.TestCase):
    def test_unter_18(self):
        self.assertIsNone(beziehungsstatus(17, 2, 5))

    def test_kurze_beziehung_wenige_interessen(self):
        self.assertFalse(beziehungsstatus(25, 0.5, 2))

    def test_lange_beziehung_viele_interessen(self):
        self.assertTrue(beziehungsstatus(30, 2, 4))

    def test_lange_beziehung_wenige_interessen(self):
        self.assertFalse(beziehungsstatus(22, 1, 2))

    def test_kurze_beziehung_viele_interessen(self):
        self.assertFalse(beziehungsstatus(25, 0.5, 3))

    def test_grenzfall_18_jahre(self):
        self.assertFalse(beziehungsstatus(18, 0.5, 2))

    def test_grenzfall_1_jahr(self):
        self.assertTrue(beziehungsstatus(25, 1, 3))

    def test_grenzfall_3_interessen(self):
        self.assertTrue(beziehungsstatus(25, 1, 3))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 597
