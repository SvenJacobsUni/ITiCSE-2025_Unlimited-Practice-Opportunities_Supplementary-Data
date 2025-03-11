# Input
- Programmierkonzept: Boolean und None
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Aktivität

Schreibe eine Funktion namens `ist_sportlich(aktivitaet)`, die überprüft, ob eine übergebene Aktivität als sportlich gilt. Die Funktion soll einen Boolean-Wert zurückgeben: `True`, wenn die Aktivität sportlich ist, und `False`, wenn sie es nicht ist. Wenn die Aktivität nicht in der Liste der bekannten Aktivitäten enthalten ist, soll die Funktion `None` zurückgeben.

Bekannte sportliche Aktivitäten sind:
- "Laufen"
- "Schwimmen"
- "Radfahren"
- "Fußball"
- "Basketball"

Beispielaufrufe:
- `ist_sportlich("Laufen")` gibt `True` zurück.
- `ist_sportlich("Schach")` gibt `False` zurück.
- `ist_sportlich("Tanzen")` gibt `None` zurück.

## Codegerüst
```python
def ist_sportlich(aktivitaet):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ist_sportlich(aktivitaet):
    sportliche_aktivitaeten = ["Laufen", "Schwimmen", "Radfahren", "Fußball", "Basketball"]
    if aktivitaet in sportliche_aktivitaeten:
        return True
    elif aktivitaet in ["Schach", "Tanzen"]:
        return False
    return None

# Beispielaufrufe
print(ist_sportlich("Laufen"))  # True
print(ist_sportlich("Schach"))  # False
print(ist_sportlich("Tanzen"))  # None
```

## Unit Tests
```python
import unittest
from main import ist_sportlich

class TestIstSportlich(unittest.TestCase):
    def test_sportliche_aktivitaet(self):
        self.assertTrue(ist_sportlich("Laufen"))
        self.assertTrue(ist_sportlich("Schwimmen"))
        self.assertTrue(ist_sportlich("Radfahren"))
        self.assertTrue(ist_sportlich("Fußball"))
        self.assertTrue(ist_sportlich("Basketball"))

    def test_nicht_sportliche_aktivitaet(self):
        self.assertFalse(ist_sportlich("Schach"))

    def test_unbekannte_aktivitaet(self):
        self.assertIsNone(ist_sportlich("Tanzen"))
        self.assertIsNone(ist_sportlich("Lesen"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 485
