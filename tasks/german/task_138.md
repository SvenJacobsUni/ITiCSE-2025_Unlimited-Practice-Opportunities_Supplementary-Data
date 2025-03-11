# Input
- Programmierkonzept: Boolean und None;String
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungsstatus überprüfen

Schreibe eine Funktion namens `beziehungsstatus(status)`, die den Beziehungsstatus einer Person überprüft und eine entsprechende Nachricht zurückgibt. Die Funktion soll einen String `status` als Argument nehmen und je nach Eingabe eine passende Nachricht zurückgeben.

- Wenn der `status` "vergeben" ist, soll die Funktion "Herzlichen Glückwunsch zur Beziehung!" zurückgeben.
- Wenn der `status` "single" ist, soll die Funktion "Genieße deine Freiheit!" zurückgeben.
- Wenn der `status` "kompliziert" ist, soll die Funktion "Beziehungen können manchmal schwierig sein." zurückgeben.
- Für alle anderen Eingaben soll die Funktion `None` zurückgeben.

Beispielaufrufe:
- `beziehungsstatus("vergeben")` gibt "Herzlichen Glückwunsch zur Beziehung!" zurück.
- `beziehungsstatus("single")` gibt "Genieße deine Freiheit!" zurück.
- `beziehungsstatus("kompliziert")` gibt "Beziehungen können manchmal schwierig sein." zurück.
- `beziehungsstatus("unbekannt")` gibt `None` zurück.

## Codegerüst
```python
def beziehungsstatus(status):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beziehungsstatus(status):
    if status == "vergeben":
        return "Herzlichen Glückwunsch zur Beziehung!"
    elif status == "single":
        return "Genieße deine Freiheit!"
    elif status == "kompliziert":
        return "Beziehungen können manchmal schwierig sein."
    else:
        return None

# Beispielaufrufe
print(beziehungsstatus("vergeben"))
print(beziehungsstatus("single"))
print(beziehungsstatus("kompliziert"))
print(beziehungsstatus("unbekannt"))
```

## Unit Tests
```python
import unittest

from main import beziehungsstatus

class TestBeziehungsstatus(unittest.TestCase):
    def test_vergeben(self):
        self.assertEqual(beziehungsstatus("vergeben"), "Herzlichen Glückwunsch zur Beziehung!")

    def test_single(self):
        self.assertEqual(beziehungsstatus("single"), "Genieße deine Freiheit!")

    def test_kompliziert(self):
        self.assertEqual(beziehungsstatus("kompliziert"), "Beziehungen können manchmal schwierig sein.")

    def test_unbekannt(self):
        self.assertIsNone(beziehungsstatus("unbekannt"))

    def test_leerer_string(self):
        self.assertIsNone(beziehungsstatus(""))

    def test_none(self):
        self.assertIsNone(beziehungsstatus(None))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 570
