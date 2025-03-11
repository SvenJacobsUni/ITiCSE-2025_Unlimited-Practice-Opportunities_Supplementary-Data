# Input
- Programmierkonzept: Integer
- Kontext: Aquarium

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Fische im Aquarium zählen

Schreibe eine Funktion namens `zaehle_fische(anzahl_fische)`, die die Anzahl der Fische in einem Aquarium zählt und eine entsprechende Nachricht zurückgibt. Die Funktion soll einen Integer-Wert `anzahl_fische` als Parameter nehmen und eine Nachricht in der Form "Es gibt [anzahl_fische] Fische im Aquarium." zurückgeben.

Beispielaufruf:
```python
print(zaehle_fische(10))
```

Erwartete Ausgabe:
```
Es gibt 10 Fische im Aquarium.
```

## Codegerüst
```python
def zaehle_fische(anzahl_fische):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(anzahl_fische):
    return f"Es gibt {anzahl_fische} Fische im Aquarium."

print(zaehle_fische(10))
```

## Unit Tests
```python
import unittest
from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_zehn_fische(self):
        self.assertEqual(zaehle_fische(10), "Es gibt 10 Fische im Aquarium.")

    def test_null_fische(self):
        self.assertEqual(zaehle_fische(0), "Es gibt 0 Fische im Aquarium.")

    def test_ein_fisch(self):
        self.assertEqual(zaehle_fische(1), "Es gibt 1 Fisch im Aquarium.")

    def test_negativ_fische(self):
        self.assertEqual(zaehle_fische(-5), "Es gibt -5 Fische im Aquarium.")

    def test_grosse_anzahl_fische(self):
        self.assertEqual(zaehle_fische(1000), "Es gibt 1000 Fische im Aquarium.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 436
