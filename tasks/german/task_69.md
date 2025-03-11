# Input
- Programmierkonzept: Float
- Kontext: Musik

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Musik-Streaming-Dauer

Schreibe eine Funktion namens `berechne_spieldauer(lieder)`, die eine Liste von Liedern erhält. Jedes Lied wird durch seine Spieldauer in Minuten als Float-Wert dargestellt. Die Funktion soll die gesamte Spieldauer der Lieder in Stunden berechnen und zurückgeben.

Beispielaufruf:
```python
lieder = [3.5, 4.2, 5.0, 2.8]
print(berechne_spieldauer(lieder))  # Ausgabe: 0.25
```

Hinweis: Die Ausgabe sollte in Stunden und als Float-Wert zurückgegeben werden.

## Codegerüst
```python
def berechne_spieldauer(lieder):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_spieldauer(lieder):
    return sum(lieder) / 60

lieder = [3.5, 4.2, 5.0, 2.8]
print(berechne_spieldauer(lieder))
```

## Unit Tests
```python
import unittest
from main import berechne_spieldauer

class TestBerechneSpieldauer(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertAlmostEqual(berechne_spieldauer([3.5, 4.2, 5.0, 2.8]), 0.25)

    def test_leere_liste(self):
        self.assertAlmostEqual(berechne_spieldauer([]), 0.0)

    def test_ein_lied(self):
        self.assertAlmostEqual(berechne_spieldauer([60.0]), 1.0)

    def test_gemischte_werte(self):
        self.assertAlmostEqual(berechne_spieldauer([30.0, 45.0, 15.0]), 1.5)

    def test_grosse_werte(self):
        self.assertAlmostEqual(berechne_spieldauer([120.0, 180.0, 240.0]), 9.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 487
