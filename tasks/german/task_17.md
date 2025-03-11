# Input
- Programmierkonzept: Float
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
```markdown
### Übungsaufgabe: Berechnung der Spielerpunktzahl

In modernen Videospielen ist es wichtig, die Punktzahl eines Spielers präzise zu berechnen, insbesondere wenn es um Highscores geht. Schreibe eine Funktion namens `berechne_punktzahl(kills, assists, deaths)`, die die Punktzahl eines Spielers basierend auf den folgenden Kriterien berechnet:

- Jeder Kill gibt 10.5 Punkte.
- Jeder Assist gibt 5.25 Punkte.
- Jeder Death zieht 2.75 Punkte ab.

Die Funktion soll die berechnete Punktzahl als Float-Wert zurückgeben.

Beispielaufruf:
```python
berechne_punktzahl(10, 5, 2)
```
Dieser Aufruf sollte die Punktzahl für einen Spieler berechnen, der 10 Kills, 5 Assists und 2 Deaths hat.
```

## Codegerüst
```python
def berechne_punktzahl(kills, assists, deaths):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punktzahl(kills, assists, deaths):
    return kills * 10.5 + assists * 5.25 - deaths * 2.75

# Beispielaufruf
print(berechne_punktzahl(10, 5, 2))
```

## Unit Tests
```python
import unittest
from main import berechne_punktzahl

class TestBerechnePunktzahl(unittest.TestCase):
    def test_positive_values(self):
        self.assertAlmostEqual(berechne_punktzahl(10, 5, 2), 123.75)

    def test_zero_values(self):
        self.assertAlmostEqual(berechne_punktzahl(0, 0, 0), 0.0)

    def test_negative_values(self):
        self.assertAlmostEqual(berechne_punktzahl(-10, -5, -2), -123.75)

    def test_mixed_values(self):
        self.assertAlmostEqual(berechne_punktzahl(10, 0, 5), 89.75)

    def test_large_values(self):
        self.assertAlmostEqual(berechne_punktzahl(1000, 500, 200), 12375.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 435
