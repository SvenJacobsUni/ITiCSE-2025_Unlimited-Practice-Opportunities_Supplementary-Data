# Input
- Programmierkonzept: Funktionen höherer Ordnung;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Operationen mit Zahlen
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Leistungen bewerten

Schreibe eine Funktion namens `bewerte_leistung(punkte)`, die eine Punktzahl als Argument erhält und eine entsprechende Bewertung zurückgibt. Die Bewertung erfolgt nach folgenden Kriterien:

- Wenn die Punktzahl größer oder gleich 90 ist, soll die Funktion "Hervorragend" zurückgeben.
- Wenn die Punktzahl zwischen 75 und 89 liegt (einschließlich), soll die Funktion "Gut" zurückgeben.
- Wenn die Punktzahl zwischen 50 und 74 liegt (einschließlich), soll die Funktion "Befriedigend" zurückgeben.
- Wenn die Punktzahl kleiner als 50 ist, soll die Funktion "Verbesserungswürdig" zurückgeben.

Beispielaufrufe:

```python
print(bewerte_leistung(95))  # Ausgabe: Hervorragend
print(bewerte_leistung(80))  # Ausgabe: Gut
print(bewerte_leistung(60))  # Ausgabe: Befriedigend
print(bewerte_leistung(45))  # Ausgabe: Verbesserungswürdig
```

## Codegerüst
```python
def bewerte_leistung(punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_leistung(punkte):
    if punkte >= 90:
        return "Hervorragend"
    elif punkte >= 75:
        return "Gut"
    elif punkte >= 50:
        return "Befriedigend"
    else:
        return "Verbesserungswürdig"

print(bewerte_leistung(95))  # Ausgabe: Hervorragend
print(bewerte_leistung(80))  # Ausgabe: Gut
print(bewerte_leistung(60))  # Ausgabe: Befriedigend
print(bewerte_leistung(45))  # Ausgabe: Verbesserungswürdig
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
        self.assertEqual(bewerte_leistung(80), "Gut")
        self.assertEqual(bewerte_leistung(75), "Gut")

    def test_befriedigend(self):
        self.assertEqual(bewerte_leistung(60), "Befriedigend")
        self.assertEqual(bewerte_leistung(50), "Befriedigend")

    def test_verbesserungswuerdig(self):
        self.assertEqual(bewerte_leistung(45), "Verbesserungswürdig")
        self.assertEqual(bewerte_leistung(0), "Verbesserungswürdig")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 594
