# Input
- Programmierkonzept: Listen
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Modernes Gaming - Highscore-Liste

Schreibe eine Funktion namens `aktualisiere_highscore(liste, neuer_score)`, die eine Liste von Highscores und einen neuen Score als Argumente erhält. Die Funktion soll den neuen Score in die Liste einfügen und die Liste anschließend in absteigender Reihenfolge sortieren. Wenn die Liste mehr als 10 Einträge enthält, soll der niedrigste Score entfernt werden, sodass die Liste immer nur die Top 10 Scores enthält. Die Funktion soll die aktualisierte Highscore-Liste zurückgeben.

Beispielaufruf:
```python
highscores = [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550]
neuer_score = 920
print(aktualisiere_highscore(highscores, neuer_score))
```

Erwartete Ausgabe:
```
[1000, 950, 920, 900, 850, 800, 750, 700, 650, 600]
```

## Codegerüst
```python
def aktualisiere_highscore(liste, neuer_score):
    ## Hier Code einfügen
```

## Musterlösung
```python
def aktualisiere_highscore(liste, neuer_score):
    liste.append(neuer_score)
    liste.sort(reverse=True)
    return liste[:10]

highscores = [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550]
neuer_score = 920
print(aktualisiere_highscore(highscores, neuer_score))
```

## Unit Tests
```python
import unittest
from main import aktualisiere_highscore

class TestAktualisiereHighscore(unittest.TestCase):
    def test_neuer_score_mittendrin(self):
        self.assertEqual(aktualisiere_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 920), [1000, 950, 920, 900, 850, 800, 750, 700, 650, 600])

    def test_neuer_score_hoechster(self):
        self.assertEqual(aktualisiere_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 1050), [1050, 1000, 950, 900, 850, 800, 750, 700, 650, 600])

    def test_neuer_score_niedrigster(self):
        self.assertEqual(aktualisiere_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 500), [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550])

    def test_neuer_score_zehnter(self):
        self.assertEqual(aktualisiere_highscore([1000, 950, 900, 850, 800, 750, 700, 650, 600, 550], 550), [1000, 950, 900, 850, 800, 750, 700, 650, 600, 550])

    def test_leere_liste(self):
        self.assertEqual(aktualisiere_highscore([], 500), [500])

    def test_weniger_als_zehn_scores(self):
        self.assertEqual(aktualisiere_highscore([1000, 950, 900], 850), [1000, 950, 900, 850])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 460
