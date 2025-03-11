# Input
- Programmierkonzept: Funktionen als Variablen;If-Else-Anweisungen
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungsstatus überprüfen

Schreibe eine Funktion namens `beziehungsstatus(status)`, die den aktuellen Beziehungsstatus einer Person überprüft und eine entsprechende Nachricht zurückgibt. Die Funktion soll eine der folgenden Nachrichten zurückgeben, basierend auf dem übergebenen Status:

- Wenn der Status "vergeben" ist, soll die Nachricht "Herzlichen Glückwunsch zur Beziehung!" zurückgegeben werden.
- Wenn der Status "single" ist, soll die Nachricht "Genieße deine Freiheit!" zurückgegeben werden.
- Wenn der Status "kompliziert" ist, soll die Nachricht "Beziehungen können manchmal schwierig sein." zurückgegeben werden.
- Für alle anderen Status soll die Nachricht "Unbekannter Beziehungsstatus." zurückgegeben werden.

Beispielaufrufe:
- `beziehungsstatus("vergeben")` gibt "Herzlichen Glückwunsch zur Beziehung!" zurück.
- `beziehungsstatus("single")` gibt "Genieße deine Freiheit!" zurück.
- `beziehungsstatus("kompliziert")` gibt "Beziehungen können manchmal schwierig sein." zurück.
- `beziehungsstatus("verwitwet")` gibt "Unbekannter Beziehungsstatus." zurück.

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
        return "Unbekannter Beziehungsstatus."

# Beispielaufrufe
print(beziehungsstatus("vergeben"))
print(beziehungsstatus("single"))
print(beziehungsstatus("kompliziert"))
print(beziehungsstatus("verwitwet"))
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
        self.assertEqual(beziehungsstatus("verwitwet"), "Unbekannter Beziehungsstatus.")

    def test_leerer_string(self):
        self.assertEqual(beziehungsstatus(""), "Unbekannter Beziehungsstatus.")

    def test_none(self):
        self.assertEqual(beziehungsstatus(None), "Unbekannter Beziehungsstatus.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 577
