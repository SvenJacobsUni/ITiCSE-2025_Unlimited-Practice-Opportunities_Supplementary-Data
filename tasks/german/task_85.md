# Input
- Programmierkonzept: Integer
- Kontext: Aquarium

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Aquarium

Schreibe eine Funktion namens `fische_zaehlen(anzahl_fische)`, die die Anzahl der Fische in einem Aquarium überprüft und eine entsprechende Nachricht zurückgibt. 

- Wenn die Anzahl der Fische weniger als 5 ist, soll die Nachricht "Das Aquarium ist ziemlich leer." zurückgegeben werden.
- Wenn die Anzahl der Fische zwischen 5 und 10 liegt (einschließlich), soll die Nachricht "Das Aquarium hat eine gute Anzahl an Fischen." zurückgegeben werden.
- Wenn die Anzahl der Fische mehr als 10 ist, soll die Nachricht "Das Aquarium ist überfüllt!" zurückgegeben werden.

Beispielaufrufe:
- `fische_zaehlen(3)` gibt "Das Aquarium ist ziemlich leer." zurück.
- `fische_zaehlen(7)` gibt "Das Aquarium hat eine gute Anzahl an Fischen." zurück.
- `fische_zaehlen(12)` gibt "Das Aquarium ist überfüllt!" zurück.

## Codegerüst
```python
def fische_zaehlen(anzahl_fische):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fische_zaehlen(anzahl_fische):
    if anzahl_fische < 5:
        return "Das Aquarium ist ziemlich leer."
    elif 5 <= anzahl_fische <= 10:
        return "Das Aquarium hat eine gute Anzahl an Fischen."
    else:
        return "Das Aquarium ist überfüllt!"

# Beispielaufrufe
print(fische_zaehlen(3))
print(fische_zaehlen(7))
print(fische_zaehlen(12))
```

## Unit Tests
```python
import unittest
from main import fische_zaehlen

class TestFischeZaehlen(unittest.TestCase):
    def test_wenige_fische(self):
        self.assertEqual(fische_zaehlen(3), "Das Aquarium ist ziemlich leer.")

    def test_gute_anzahl_fische(self):
        self.assertEqual(fische_zaehlen(7), "Das Aquarium hat eine gute Anzahl an Fischen.")

    def test_viele_fische(self):
        self.assertEqual(fische_zaehlen(12), "Das Aquarium ist überfüllt!")

    def test_unterer_randwert(self):
        self.assertEqual(fische_zaehlen(5), "Das Aquarium hat eine gute Anzahl an Fischen.")

    def test_oberer_randwert(self):
        self.assertEqual(fische_zaehlen(10), "Das Aquarium hat eine gute Anzahl an Fischen.")

    def test_null_fische(self):
        self.assertEqual(fische_zaehlen(0), "Das Aquarium ist ziemlich leer.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 503
