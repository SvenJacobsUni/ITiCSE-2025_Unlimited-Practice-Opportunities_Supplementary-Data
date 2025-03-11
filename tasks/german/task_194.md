# Input
- Programmierkonzept: Boolean und None;String;Operationen mit Zahlen
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Leistungen bewerten

Schreibe eine Funktion namens `bewerte_leistung(punkte)`, die eine Punktzahl als Argument erhält und eine entsprechende Bewertung als String zurückgibt. Die Bewertung erfolgt nach folgenden Kriterien:

- Wenn die Punktzahl größer oder gleich 90 ist, soll die Funktion "Hervorragend" zurückgeben.
- Wenn die Punktzahl zwischen 70 und 89 liegt (einschließlich), soll die Funktion "Gut" zurückgeben.
- Wenn die Punktzahl zwischen 50 und 69 liegt (einschließlich), soll die Funktion "Befriedigend" zurückgeben.
- Wenn die Punktzahl zwischen 30 und 49 liegt (einschließlich), soll die Funktion "Ausreichend" zurückgeben.
- Wenn die Punktzahl kleiner als 30 ist, soll die Funktion "Ungenügend" zurückgeben.
- Wenn die Punktzahl `None` ist, soll die Funktion "Keine Bewertung möglich" zurückgeben.

Beispielaufrufe:
- `bewerte_leistung(95)` gibt "Hervorragend" zurück.
- `bewerte_leistung(75)` gibt "Gut" zurück.
- `bewerte_leistung(None)` gibt "Keine Bewertung möglich" zurück.

## Codegerüst
```python
def bewerte_leistung(punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_leistung(punkte):
    if punkte is None:
        return "Keine Bewertung möglich"
    if punkte >= 90:
        return "Hervorragend"
    if punkte >= 70:
        return "Gut"
    if punkte >= 50:
        return "Befriedigend"
    if punkte >= 30:
        return "Ausreichend"
    return "Ungenügend"

# Beispielaufrufe
print(bewerte_leistung(95))  # Hervorragend
print(bewerte_leistung(75))  # Gut
print(bewerte_leistung(None))  # Keine Bewertung möglich
```

## Unit Tests
```python
import unittest
from main import bewerte_leistung

class TestBewerteLeistung(unittest.TestCase):
    def test_hervorragend(self):
        self.assertEqual(bewerte_leistung(95), "Hervorragend")
        self.assertEqual(bewerte_leistung(90), "Hervorragend")

    def test_gut(self):
        self.assertEqual(bewerte_leistung(75), "Gut")
        self.assertEqual(bewerte_leistung(70), "Gut")

    def test_befriedigend(self):
        self.assertEqual(bewerte_leistung(60), "Befriedigend")
        self.assertEqual(bewerte_leistung(50), "Befriedigend")

    def test_ausreichend(self):
        self.assertEqual(bewerte_leistung(40), "Ausreichend")
        self.assertEqual(bewerte_leistung(30), "Ausreichend")

    def test_ungenuegend(self):
        self.assertEqual(bewerte_leistung(20), "Ungenügend")
        self.assertEqual(bewerte_leistung(0), "Ungenügend")

    def test_keine_bewertung(self):
        self.assertEqual(bewerte_leistung(None), "Keine Bewertung möglich")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 626
