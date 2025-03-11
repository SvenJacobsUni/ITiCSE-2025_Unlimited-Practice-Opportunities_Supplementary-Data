# Input
- Programmierkonzept: If-Else-Anweisungen
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tierklassifikation

Schreibe eine Funktion namens `tier_klassifikation(tier)`, die eine Nachricht basierend auf dem übergebenen Tier zurückgibt. Die Funktion soll die folgenden Tiere erkennen und entsprechende Nachrichten zurückgeben:

- Bei "Hund" soll die Nachricht "Das ist ein treuer Begleiter!" zurückgegeben werden.
- Bei "Katze" soll die Nachricht "Das ist ein unabhängiger Freund!" zurückgegeben werden.
- Bei "Vogel" soll die Nachricht "Das ist ein gefiederter Freund!" zurückgegeben werden.
- Bei allen anderen Tieren soll die Nachricht "Das ist ein interessantes Tier!" zurückgegeben werden.

Beispielaufrufe:

```python
print(tier_klassifikation("Hund"))  # Ausgabe: Das ist ein treuer Begleiter!
print(tier_klassifikation("Katze"))  # Ausgabe: Das ist ein unabhängiger Freund!
print(tier_klassifikation("Vogel"))  # Ausgabe: Das ist ein gefiederter Freund!
print(tier_klassifikation("Fisch"))  # Ausgabe: Das ist ein interessantes Tier!
```

## Codegerüst
```python
def tier_klassifikation(tier):
    ## Hier Code einfügen
```

## Musterlösung
```python
def tier_klassifikation(tier):
    if tier == "Hund":
        return "Das ist ein treuer Begleiter!"
    elif tier == "Katze":
        return "Das ist ein unabhängiger Freund!"
    elif tier == "Vogel":
        return "Das ist ein gefiederter Freund!"
    else:
        return "Das ist ein interessantes Tier!"

print(tier_klassifikation("Hund"))
print(tier_klassifikation("Katze"))
print(tier_klassifikation("Vogel"))
print(tier_klassifikation("Fisch"))
```

## Unit Tests
```python
import unittest
from main import tier_klassifikation

class TestTierKlassifikation(unittest.TestCase):
    def test_hund(self):
        self.assertEqual(tier_klassifikation("Hund"), "Das ist ein treuer Begleiter!")

    def test_katze(self):
        self.assertEqual(tier_klassifikation("Katze"), "Das ist ein unabhängiger Freund!")

    def test_vogel(self):
        self.assertEqual(tier_klassifikation("Vogel"), "Das ist ein gefiederter Freund!")

    def test_unbekanntes_tier(self):
        self.assertEqual(tier_klassifikation("Fisch"), "Das ist ein interessantes Tier!")

    def test_leerer_string(self):
        self.assertEqual(tier_klassifikation(""), "Das ist ein interessantes Tier!")

    def test_none(self):
        self.assertEqual(tier_klassifikation(None), "Das ist ein interessantes Tier!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 424
