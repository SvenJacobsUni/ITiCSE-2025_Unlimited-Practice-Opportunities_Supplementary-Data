# Input
- Programmierkonzept: For-Schleifen
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Highscore-Liste im modernen Gaming

Schreibe eine Funktion namens `highscore_liste(scores)`, die eine Liste von Spielergebnissen (Scores) als Argument erhält. Die Funktion soll die Spielergebnisse in absteigender Reihenfolge sortieren und die Top 5 Ergebnisse zurückgeben. Falls weniger als 5 Ergebnisse vorhanden sind, sollen alle vorhandenen Ergebnisse zurückgegeben werden.

Beispielaufruf:
```python
highscore_liste([1500, 3000, 2500, 5000, 1000, 2000])
```

Erwartete Rückgabe:
```python
[5000, 3000, 2500, 2000, 1500]
```

## Codegerüst
```python
def highscore_liste(scores):
    ## Hier Code einfügen
```

## Musterlösung
```python
def highscore_liste(scores):
    return sorted(scores, reverse=True)[:5]

print(highscore_liste([1500, 3000, 2500, 5000, 1000, 2000]))
```

## Unit Tests
```python
import unittest
from main import highscore_liste

class TestHighscoreListe(unittest.TestCase):
    def test_mehr_als_fuenf_scores(self):
        self.assertEqual(highscore_liste([1500, 3000, 2500, 5000, 1000, 2000]), [5000, 3000, 2500, 2000, 1500])

    def test_genau_fuenf_scores(self):
        self.assertEqual(highscore_liste([1500, 3000, 2500, 5000, 1000]), [5000, 3000, 2500, 1500, 1000])

    def test_weniger_als_fuenf_scores(self):
        self.assertEqual(highscore_liste([1500, 3000, 2500]), [3000, 2500, 1500])

    def test_leere_liste(self):
        self.assertEqual(highscore_liste([]), [])

    def test_alle_scores_gleich(self):
        self.assertEqual(highscore_liste([1000, 1000, 1000, 1000, 1000, 1000]), [1000, 1000, 1000, 1000, 1000])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 419
