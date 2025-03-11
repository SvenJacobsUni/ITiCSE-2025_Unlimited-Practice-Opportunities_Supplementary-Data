# Input
- Programmierkonzept: Float;Funktionen höherer Ordnung;Integer
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tiere und ihre Eigenschaften

Schreibe eine Funktion namens `tier_info(tier, eigenschaft)`, die Informationen über verschiedene Tiere und ihre Eigenschaften zurückgibt. Die Funktion soll zwei Parameter akzeptieren: `tier` (ein String) und `eigenschaft` (ein String). 

Die Funktion soll die folgenden Tiere und Eigenschaften unterstützen:

- Hund:
  - "gewicht" (Float): Gibt das durchschnittliche Gewicht eines Hundes in Kilogramm zurück.
  - "beine" (Integer): Gibt die Anzahl der Beine eines Hundes zurück.
- Katze:
  - "gewicht" (Float): Gibt das durchschnittliche Gewicht einer Katze in Kilogramm zurück.
  - "beine" (Integer): Gibt die Anzahl der Beine einer Katze zurück.
- Vogel:
  - "gewicht" (Float): Gibt das durchschnittliche Gewicht eines Vogels in Kilogramm zurück.
  - "beine" (Integer): Gibt die Anzahl der Beine eines Vogels zurück.

Beispielaufrufe:
- `tier_info("Hund", "gewicht")` soll das durchschnittliche Gewicht eines Hundes zurückgeben.
- `tier_info("Katze", "beine")` soll die Anzahl der Beine einer Katze zurückgeben.

Implementiere die Funktion so, dass sie die entsprechenden Werte zurückgibt.

## Codegerüst
```python
def tier_info(tier, eigenschaft):
    ## Hier Code einfügen
```

## Musterlösung
```python
def tier_info(tier, eigenschaft):
    daten = {
        "Hund": {"gewicht": 30.0, "beine": 4},
        "Katze": {"gewicht": 4.5, "beine": 4},
        "Vogel": {"gewicht": 0.1, "beine": 2}
    }
    return daten[tier][eigenschaft]

print(tier_info("Hund", "gewicht"))
print(tier_info("Katze", "beine"))
print(tier_info("Vogel", "gewicht"))
```

## Unit Tests
```python
import unittest
from main import tier_info

class TestTierInfo(unittest.TestCase):
    def test_hund_gewicht(self):
        self.assertEqual(tier_info("Hund", "gewicht"), 30.0)

    def test_hund_beine(self):
        self.assertEqual(tier_info("Hund", "beine"), 4)

    def test_katze_gewicht(self):
        self.assertEqual(tier_info("Katze", "gewicht"), 4.5)

    def test_katze_beine(self):
        self.assertEqual(tier_info("Katze", "beine"), 4)

    def test_vogel_gewicht(self):
        self.assertEqual(tier_info("Vogel", "gewicht"), 0.1)

    def test_vogel_beine(self):
        self.assertEqual(tier_info("Vogel", "beine"), 2)

    def test_unbekanntes_tier(self):
        with self.assertRaises(KeyError):
            tier_info("Elefant", "gewicht")

    def test_unbekannte_eigenschaft(self):
        with self.assertRaises(KeyError):
            tier_info("Hund", "farbe")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 604
