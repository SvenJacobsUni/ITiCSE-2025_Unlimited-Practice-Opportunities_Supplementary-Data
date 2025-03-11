# Input
- Programmierkonzept: Operationen mit Zahlen;String;Boolean und None
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Olympia-Medaillenspiegel

Schreibe eine Funktion namens `medaillen_spiegel(gold, silber, bronze)`, die die Anzahl der gewonnenen Medaillen eines Landes bei den Olympischen Spielen entgegennimmt und eine entsprechende Nachricht zurückgibt.

- Wenn das Land keine Medaillen gewonnen hat (alle Werte sind 0), soll die Funktion "Keine Medaillen gewonnen." zurückgeben.
- Wenn das Land mindestens eine Goldmedaille gewonnen hat, soll die Funktion "Goldmedaillen: [Anzahl]" zurückgeben.
- Wenn das Land mindestens eine Silbermedaille gewonnen hat, soll die Funktion "Silbermedaillen: [Anzahl]" zurückgeben.
- Wenn das Land mindestens eine Bronzemedaille gewonnen hat, soll die Funktion "Bronzemedaillen: [Anzahl]" zurückgeben.

Beispielaufrufe:
- `medaillen_spiegel(0, 0, 0)` gibt "Keine Medaillen gewonnen." zurück.
- `medaillen_spiegel(1, 0, 0)` gibt "Goldmedaillen: 1" zurück.
- `medaillen_spiegel(0, 2, 0)` gibt "Silbermedaillen: 2" zurück.
- `medaillen_spiegel(0, 0, 3)` gibt "Bronzemedaillen: 3" zurück.
- `medaillen_spiegel(1, 2, 3)` gibt "Goldmedaillen: 1\nSilbermedaillen: 2\nBronzemedaillen: 3" zurück.

## Codegerüst
```python
def medaillen_spiegel(gold, silber, bronze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def medaillen_spiegel(gold, silber, bronze):
    if gold == silber == bronze == 0:
        return "Keine Medaillen gewonnen."
    result = []
    if gold > 0:
        result.append(f"Goldmedaillen: {gold}")
    if silber > 0:
        result.append(f"Silbermedaillen: {silber}")
    if bronze > 0:
        result.append(f"Bronzemedaillen: {bronze}")
    return "\n".join(result)

# Beispielaufrufe
print(medaillen_spiegel(0, 0, 0))
print(medaillen_spiegel(1, 0, 0))
print(medaillen_spiegel(0, 2, 0))
print(medaillen_spiegel(0, 0, 3))
print(medaillen_spiegel(1, 2, 3))
```

## Unit Tests
```python
import unittest
from main import medaillen_spiegel

class TestMedaillenSpiegel(unittest.TestCase):
    def test_keine_medaillen(self):
        self.assertEqual(medaillen_spiegel(0, 0, 0), "Keine Medaillen gewonnen.")

    def test_nur_gold(self):
        self.assertEqual(medaillen_spiegel(1, 0, 0), "Goldmedaillen: 1")

    def test_nur_silber(self):
        self.assertEqual(medaillen_spiegel(0, 2, 0), "Silbermedaillen: 2")

    def test_nur_bronze(self):
        self.assertEqual(medaillen_spiegel(0, 0, 3), "Bronzemedaillen: 3")

    def test_gold_silber_bronze(self):
        self.assertEqual(medaillen_spiegel(1, 2, 3), "Goldmedaillen: 1\nSilbermedaillen: 2\nBronzemedaillen: 3")

    def test_gold_und_silber(self):
        self.assertEqual(medaillen_spiegel(1, 2, 0), "Goldmedaillen: 1\nSilbermedaillen: 2")

    def test_gold_und_bronze(self):
        self.assertEqual(medaillen_spiegel(1, 0, 3), "Goldmedaillen: 1\nBronzemedaillen: 3")

    def test_silber_und_bronze(self):
        self.assertEqual(medaillen_spiegel(0, 2, 3), "Silbermedaillen: 2\nBronzemedaillen: 3")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 590
