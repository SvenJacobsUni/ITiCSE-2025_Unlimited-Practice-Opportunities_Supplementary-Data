# Input
- Programmierkonzept: Float;Operationen mit Zahlen;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustiergewichtskontrolle

Schreibe eine Funktion namens `gewichtskontrolle(gewicht)`, die das Gewicht eines Haustiers (in Kilogramm) als Float-Wert entgegennimmt und eine entsprechende Nachricht mit `return` zurückgibt. Die Funktion soll anhand des Gewichts des Haustiers entscheiden, ob das Haustier untergewichtig, normalgewichtig oder übergewichtig ist.

- Wenn das Gewicht kleiner als 2.0 kg ist, soll die Nachricht "Das Haustier ist untergewichtig." zurückgegeben werden.
- Wenn das Gewicht zwischen 2.0 kg und 5.0 kg (einschließlich) liegt, soll die Nachricht "Das Haustier hat ein normales Gewicht." zurückgegeben werden.
- Wenn das Gewicht größer als 5.0 kg ist, soll die Nachricht "Das Haustier ist übergewichtig." zurückgegeben werden.

Beispielaufrufe:
- `gewichtskontrolle(1.5)` gibt "Das Haustier ist untergewichtig." zurück.
- `gewichtskontrolle(3.0)` gibt "Das Haustier hat ein normales Gewicht." zurück.
- `gewichtskontrolle(6.0)` gibt "Das Haustier ist übergewichtig." zurück.

## Codegerüst
```python
def gewichtskontrolle(gewicht):
    ## Hier Code einfügen
```

## Musterlösung
```python
def gewichtskontrolle(gewicht):
    if gewicht < 2.0:
        return "Das Haustier ist untergewichtig."
    elif gewicht <= 5.0:
        return "Das Haustier hat ein normales Gewicht."
    else:
        return "Das Haustier ist übergewichtig."

# Beispielaufrufe
print(gewichtskontrolle(1.5))
print(gewichtskontrolle(3.0))
print(gewichtskontrolle(6.0))
```

## Unit Tests
```python
import unittest
from main import gewichtskontrolle

class TestGewichtskontrolle(unittest.TestCase):
    def test_untergewichtig(self):
        self.assertEqual(gewichtskontrolle(1.5), "Das Haustier ist untergewichtig.")

    def test_normales_gewicht_untergrenze(self):
        self.assertEqual(gewichtskontrolle(2.0), "Das Haustier hat ein normales Gewicht.")

    def test_normales_gewicht_mitte(self):
        self.assertEqual(gewichtskontrolle(3.0), "Das Haustier hat ein normales Gewicht.")

    def test_normales_gewicht_obergrenze(self):
        self.assertEqual(gewichtskontrolle(5.0), "Das Haustier hat ein normales Gewicht.")

    def test_uebergewichtig(self):
        self.assertEqual(gewichtskontrolle(6.0), "Das Haustier ist übergewichtig.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 621
