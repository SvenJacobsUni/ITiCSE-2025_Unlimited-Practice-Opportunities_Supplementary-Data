# Input
- Programmierkonzept: Listen;String
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Beliebte Serien auf Streaming-Diensten

Schreibe eine Funktion namens `beliebte_serien(streaming_dienst)`, die eine Liste von Serien zurückgibt, die auf dem angegebenen Streaming-Dienst verfügbar sind. Die Funktion soll eine Liste von Strings als Eingabe erhalten, wobei jeder String den Namen eines Streaming-Dienstes darstellt. Die Funktion soll eine Liste von Seriennamen zurückgeben, die auf dem angegebenen Streaming-Dienst verfügbar sind.

Verwende die folgenden Daten:

- Netflix: ["Stranger Things", "The Crown", "Black Mirror"]
- Amazon Prime: ["The Boys", "The Marvelous Mrs. Maisel", "Fleabag"]
- Disney+: ["The Mandalorian", "WandaVision", "Loki"]

Beispielaufruf:
```python
beliebte_serien("Netflix")
```
sollte die Liste `["Stranger Things", "The Crown", "Black Mirror"]` zurückgeben.

## Codegerüst
```python
def beliebte_serien(streaming_dienst):
    ## Hier Code einfügen
```

## Musterlösung
```python
def beliebte_serien(streaming_dienst):
    serien = {
        "Netflix": ["Stranger Things", "The Crown", "Black Mirror"],
        "Amazon Prime": ["The Boys", "The Marvelous Mrs. Maisel", "Fleabag"],
        "Disney+": ["The Mandalorian", "WandaVision", "Loki"]
    }
    return serien.get(streaming_dienst, [])

# Beispielaufruf
print(beliebte_serien("Netflix"))
```

## Unit Tests
```python
import unittest
from main import beliebte_serien

class TestBeliebteSerien(unittest.TestCase):
    def test_netflix(self):
        self.assertEqual(beliebte_serien("Netflix"), ["Stranger Things", "The Crown", "Black Mirror"])

    def test_amazon_prime(self):
        self.assertEqual(beliebte_serien("Amazon Prime"), ["The Boys", "The Marvelous Mrs. Maisel", "Fleabag"])

    def test_disney_plus(self):
        self.assertEqual(beliebte_serien("Disney+"), ["The Mandalorian", "WandaVision", "Loki"])

    def test_unbekannter_dienst(self):
        self.assertEqual(beliebte_serien("Hulu"), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 567
