# Input
- Programmierkonzept: String
- Kontext: Beziehungen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beziehungen und Strings

Schreibe eine Funktion namens `beziehungsstatus(status)`, die den Beziehungsstatus einer Person als String entgegennimmt und eine entsprechende Nachricht zurückgibt. Die möglichen Beziehungsstatus sind:

- "Single"
- "Vergeben"
- "Verheiratet"
- "Es ist kompliziert"

Die Funktion soll je nach Beziehungsstatus eine passende Nachricht zurückgeben:

- Bei "Single" soll: "Genieße deine Freiheit!" zurückgegeben werden.
- Bei "Vergeben" soll: "Viel Glück euch beiden!" zurückgegeben werden.
- Bei "Verheiratet" soll: "Herzlichen Glückwunsch zur Ehe!" zurückgegeben werden.
- Bei "Es ist kompliziert" soll: "Alles Gute für die Zukunft!" zurückgegeben werden.

Beispielaufruf: `beziehungsstatus("Verheiratet")` gibt "Herzlichen Glückwunsch zur Ehe!" zurück.

## Codegerüst
```python
def beziehungsstatus(status):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beziehungsstatus(status):
    return {
        "Single": "Genieße deine Freiheit!",
        "Vergeben": "Viel Glück euch beiden!",
        "Verheiratet": "Herzlichen Glückwunsch zur Ehe!",
        "Es ist kompliziert": "Alles Gute für die Zukunft!"
    }.get(status, "Unbekannter Status")

# Beispielaufruf
print(beziehungsstatus("Verheiratet"))
```

## Unit Tests
```python
import unittest
from main import beziehungsstatus

class TestBeziehungsstatus(unittest.TestCase):
    def test_single(self):
        self.assertEqual(beziehungsstatus("Single"), "Genieße deine Freiheit!")

    def test_vergeben(self):
        self.assertEqual(beziehungsstatus("Vergeben"), "Viel Glück euch beiden!")

    def test_verheiratet(self):
        self.assertEqual(beziehungsstatus("Verheiratet"), "Herzlichen Glückwunsch zur Ehe!")

    def test_kompliziert(self):
        self.assertEqual(beziehungsstatus("Es ist kompliziert"), "Alles Gute für die Zukunft!")

    def test_unbekannter_status(self):
        self.assertEqual(beziehungsstatus("Unbekannt"), "Unbekannter Status")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 462
