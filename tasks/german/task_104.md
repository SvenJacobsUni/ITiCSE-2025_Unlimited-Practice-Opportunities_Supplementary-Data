# Input
- Programmierkonzept: Funktionen als Variablen;Integer
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tieralter in Menschenjahren

Schreibe eine Funktion namens `tier_alter_in_menschenjahren(tier, alter)`, die das Alter eines Tieres in Menschenjahren berechnet. Die Funktion soll zwei Parameter entgegennehmen: `tier` (ein String, der den Typ des Tieres angibt, z.B. "Hund" oder "Katze") und `alter` (ein Integer, der das Alter des Tieres in Jahren angibt).

Die Umrechnung soll wie folgt erfolgen:
- Für Hunde: 1 Tierjahr entspricht 7 Menschenjahren.
- Für Katzen: 1 Tierjahr entspricht 5 Menschenjahren.

Die Funktion soll das berechnete Alter in Menschenjahren zurückgeben.

Beispielaufrufe:
- `tier_alter_in_menschenjahren("Hund", 3)` soll 21 zurückgeben.
- `tier_alter_in_menschenjahren("Katze", 4)` soll 20 zurückgeben.

## Codegerüst
```python
def tier_alter_in_menschenjahren(tier, alter):
    ## Hier Code einfügen
```

## Musterlösung
```python
def tier_alter_in_menschenjahren(tier, alter):
    multiplikator = 7 if tier == "Hund" else 5 if tier == "Katze" else 1
    return alter * multiplikator

print(tier_alter_in_menschenjahren("Hund", 3))  # 21
print(tier_alter_in_menschenjahren("Katze", 4))  # 20
```

## Unit Tests
```python
import unittest

from main import tier_alter_in_menschenjahren

class TestTierAlterInMenschenjahren(unittest.TestCase):
    def test_hund_alter(self):
        self.assertEqual(tier_alter_in_menschenjahren("Hund", 3), 21)

    def test_katze_alter(self):
        self.assertEqual(tier_alter_in_menschenjahren("Katze", 4), 20)

    def test_hund_alter_randbedingung(self):
        self.assertEqual(tier_alter_in_menschenjahren("Hund", 0), 0)

    def test_katze_alter_randbedingung(self):
        self.assertEqual(tier_alter_in_menschenjahren("Katze", 0), 0)

    def test_unbekanntes_tier(self):
        self.assertEqual(tier_alter_in_menschenjahren("Vogel", 3), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 536
