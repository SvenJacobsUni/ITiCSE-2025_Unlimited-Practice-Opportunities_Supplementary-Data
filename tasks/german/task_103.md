# Input
- Programmierkonzept: Float;Boolean und None
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tierinformationen

Schreibe eine Funktion namens `tier_info(name, gewicht)`, die Informationen über ein Tier basierend auf seinem Namen und Gewicht zurückgibt. Die Funktion soll folgende Anforderungen erfüllen:

1. Wenn der Name des Tieres "Elefant" ist und das Gewicht größer als 5000.0 (in Kilogramm) ist, soll die Funktion `True` zurückgeben.
2. Wenn der Name des Tieres "Maus" ist und das Gewicht kleiner als 0.05 (in Kilogramm) ist, soll die Funktion `True` zurückgeben.
3. In allen anderen Fällen soll die Funktion `None` zurückgeben.

Beispielaufrufe:
- `tier_info("Elefant", 6000.0)` gibt `True` zurück.
- `tier_info("Maus", 0.03)` gibt `True` zurück.
- `tier_info("Hund", 10.0)` gibt `None` zurück.

## Codegerüst
```python
def tier_info(name, gewicht):
    ## Hier Code einfügen
```

## Musterlösung
```python
def tier_info(name, gewicht):
    if name == "Elefant" and gewicht > 5000.0:
        return True
    if name == "Maus" and gewicht < 0.05:
        return True
    return None

print(tier_info("Elefant", 6000.0))  # True
print(tier_info("Maus", 0.03))       # True
print(tier_info("Hund", 10.0))       # None
```

## Unit Tests
```python
import unittest

from main import tier_info

class TestTierInfo(unittest.TestCase):
    def test_elefant_schwer(self):
        self.assertEqual(tier_info("Elefant", 6000.0), True)

    def test_maus_leicht(self):
        self.assertEqual(tier_info("Maus", 0.03), True)

    def test_hund(self):
        self.assertEqual(tier_info("Hund", 10.0), None)

    def test_elefant_leicht(self):
        self.assertEqual(tier_info("Elefant", 4000.0), None)

    def test_maus_schwer(self):
        self.assertEqual(tier_info("Maus", 0.1), None)

    def test_randfall_elefant(self):
        self.assertEqual(tier_info("Elefant", 5000.0), None)

    def test_randfall_maus(self):
        self.assertEqual(tier_info("Maus", 0.05), None)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 535
