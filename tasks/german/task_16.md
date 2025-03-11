# Input
- Programmierkonzept: If-Else-Anweisungen
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tierklassifikation

Schreibe eine Funktion namens `tier_klassifikation(tier)`, die den Typ eines Tieres basierend auf dem übergebenen String klassifiziert. Die Funktion soll eine entsprechende Nachricht mit `return` zurückgeben.

- Wenn das Tier ein "Hund" ist, soll die Nachricht "Das ist ein Säugetier." zurückgegeben werden.
- Wenn das Tier ein "Adler" ist, soll die Nachricht "Das ist ein Vogel." zurückgegeben werden.
- Wenn das Tier ein "Hai" ist, soll die Nachricht "Das ist ein Fisch." zurückgegeben werden.
- Für alle anderen Tiere soll die Nachricht "Unbekannte Tierklasse." zurückgegeben werden.

Beispielaufrufe:
- `tier_klassifikation("Hund")` gibt "Das ist ein Säugetier." zurück.
- `tier_klassifikation("Adler")` gibt "Das ist ein Vogel." zurück.
- `tier_klassifikation("Hai")` gibt "Das ist ein Fisch." zurück.
- `tier_klassifikation("Krokodil")` gibt "Unbekannte Tierklasse." zurück.

## Codegerüst
```python
def tier_klassifikation(tier):
    ## Hier Code einfügen
```

## Musterlösung
```python
def tier_klassifikation(tier):
    if tier == "Hund":
        return "Das ist ein Säugetier."
    elif tier == "Adler":
        return "Das ist ein Vogel."
    elif tier == "Hai":
        return "Das ist ein Fisch."
    else:
        return "Unbekannte Tierklasse."

# Beispielaufrufe
print(tier_klassifikation("Hund"))
print(tier_klassifikation("Adler"))
print(tier_klassifikation("Hai"))
print(tier_klassifikation("Krokodil"))
```

## Unit Tests
```python
import unittest

from main import tier_klassifikation

class TestTierKlassifikation(unittest.TestCase):
    def test_hund(self):
        self.assertEqual(tier_klassifikation("Hund"), "Das ist ein Säugetier.")

    def test_adler(self):
        self.assertEqual(tier_klassifikation("Adler"), "Das ist ein Vogel.")

    def test_hai(self):
        self.assertEqual(tier_klassifikation("Hai"), "Das ist ein Fisch.")

    def test_unbekanntes_tier(self):
        self.assertEqual(tier_klassifikation("Krokodil"), "Unbekannte Tierklasse.")

    def test_leerer_string(self):
        self.assertEqual(tier_klassifikation(""), "Unbekannte Tierklasse.")

    def test_none(self):
        self.assertEqual(tier_klassifikation(None), "Unbekannte Tierklasse.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 434
