# Input
- Programmierkonzept: Tupel;Integer
- Kontext: Restaurant

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Restaurant-Bestellung

Schreibe eine Funktion namens `bestellung_aufnehmen(bestellung)`, die ein Tupel mit zwei Elementen als Argument erhält. Das erste Element ist der Name des Gerichts (String) und das zweite Element ist die Anzahl der bestellten Portionen (Integer). Die Funktion soll eine Nachricht zurückgeben, die die Bestellung zusammenfasst.

Beispielaufruf: `bestellung_aufnehmen(("Spaghetti Carbonara", 3))` gibt `"Sie haben 3 Portionen Spaghetti Carbonara bestellt."` zurück.

## Codegerüst
```python
def bestellung_aufnehmen(bestellung):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bestellung_aufnehmen(bestellung):
    return f"Sie haben {bestellung[1]} Portionen {bestellung[0]} bestellt."

print(bestellung_aufnehmen(("Spaghetti Carbonara", 3)))
```

## Unit Tests
```python
import unittest

from main import bestellung_aufnehmen

class TestBestellungAufnehmen(unittest.TestCase):
    def test_einfache_bestellung(self):
        self.assertEqual(bestellung_aufnehmen(("Spaghetti Carbonara", 3)), "Sie haben 3 Portionen Spaghetti Carbonara bestellt.")

    def test_eine_portion(self):
        self.assertEqual(bestellung_aufnehmen(("Pizza Margherita", 1)), "Sie haben 1 Portion Pizza Margherita bestellt.")

    def test_null_portionen(self):
        self.assertEqual(bestellung_aufnehmen(("Salat", 0)), "Sie haben 0 Portionen Salat bestellt.")

    def test_grosse_bestellung(self):
        self.assertEqual(bestellung_aufnehmen(("Burger", 100)), "Sie haben 100 Portionen Burger bestellt.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 559
