# Input
- Programmierkonzept: If-Else-Anweisungen;Float;While-Schleifen
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Soziale Medien - Beitragsbewertung

Schreibe eine Funktion namens `bewerte_beitrag(likes, dislikes)`, die die Bewertung eines Beitrags auf einer sozialen Medienplattform berechnet. Die Bewertung soll als ein Float-Wert zwischen -1.0 und 1.0 zurückgegeben werden, wobei:

- Eine Bewertung von 1.0 bedeutet, dass der Beitrag nur Likes und keine Dislikes hat.
- Eine Bewertung von -1.0 bedeutet, dass der Beitrag nur Dislikes und keine Likes hat.
- Eine Bewertung von 0.0 bedeutet, dass der Beitrag gleich viele Likes und Dislikes hat.

Die Funktion soll die folgenden Schritte ausführen:

1. Berechne die Gesamtanzahl der Bewertungen (Likes + Dislikes).
2. Berechne den Bewertungswert als `(Likes - Dislikes) / Gesamtanzahl der Bewertungen`.
3. Gib den Bewertungswert zurück.

Falls die Gesamtanzahl der Bewertungen 0 ist, soll die Funktion eine Bewertung von 0.0 zurückgeben.

Beispielaufrufe:
- `bewerte_beitrag(100, 50)` gibt `0.3333333333333333` zurück.
- `bewerte_beitrag(0, 0)` gibt `0.0` zurück.
- `bewerte_beitrag(20, 80)` gibt `-0.6` zurück.

## Codegerüst
```python
def bewerte_beitrag(likes, dislikes):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_beitrag(likes, dislikes):
    gesamt = likes + dislikes
    return (likes - dislikes) / gesamt if gesamt != 0 else 0.0

# Beispielaufrufe
print(bewerte_beitrag(100, 50))
print(bewerte_beitrag(0, 0))
print(bewerte_beitrag(20, 80))
```

## Unit Tests
```python
import unittest

from main import bewerte_beitrag

class TestBewerteBeitrag(unittest.TestCase):
    def test_nur_likes(self):
        self.assertEqual(bewerte_beitrag(100, 0), 1.0)

    def test_nur_dislikes(self):
        self.assertEqual(bewerte_beitrag(0, 100), -1.0)

    def test_gleiche_anzahl(self):
        self.assertEqual(bewerte_beitrag(50, 50), 0.0)

    def test_mehr_likes(self):
        self.assertAlmostEqual(bewerte_beitrag(75, 25), 0.5)

    def test_mehr_dislikes(self):
        self.assertAlmostEqual(bewerte_beitrag(25, 75), -0.5)

    def test_keine_bewertungen(self):
        self.assertEqual(bewerte_beitrag(0, 0), 0.0)

    def test_gemischte_bewertungen(self):
        self.assertAlmostEqual(bewerte_beitrag(100, 50), 0.3333333333333333)
        self.assertAlmostEqual(bewerte_beitrag(20, 80), -0.6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 591
