# Input
- Programmierkonzept: Boolean und None;Float
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Leistung bewerten

Schreibe eine Funktion namens `bewerte_leistung(punkte)`, die die sportliche Leistung eines Athleten basierend auf der Punktzahl bewertet. Die Funktion soll einen `Boolean` Wert zurückgeben, der angibt, ob die Leistung als "gut" (True) oder "schlecht" (False) bewertet wird. 

Zusätzlich soll die Funktion `None` zurückgeben, wenn die Punktzahl ein `Float` ist, um anzuzeigen, dass die Punktzahl ungültig ist.

- Wenn die Punktzahl 50 oder mehr beträgt, soll die Leistung als "gut" (True) bewertet werden.
- Wenn die Punktzahl weniger als 50 beträgt, soll die Leistung als "schlecht" (False) bewertet werden.
- Wenn die Punktzahl ein `Float` ist, soll die Funktion `None` zurückgeben.

Beispielaufrufe:
- `bewerte_leistung(75)` gibt `True` zurück.
- `bewerte_leistung(30)` gibt `False` zurück.
- `bewerte_leistung(45.5)` gibt `None` zurück.

## Codegerüst
```python
def bewerte_leistung(punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_leistung(punkte):
    if isinstance(punkte, float):
        return None
    return punkte >= 50

# Beispielaufrufe
print(bewerte_leistung(75))  # True
print(bewerte_leistung(30))  # False
print(bewerte_leistung(45.5))  # None
```

## Unit Tests
```python
import unittest

from main import bewerte_leistung

class TestBewerteLeistung(unittest.TestCase):
    def test_gute_leistung(self):
        self.assertTrue(bewerte_leistung(75))

    def test_schlechte_leistung(self):
        self.assertFalse(bewerte_leistung(30))

    def test_ungültige_punktzahl(self):
        self.assertIsNone(bewerte_leistung(45.5))

    def test_grenze_gut(self):
        self.assertTrue(bewerte_leistung(50))

    def test_grenze_schlecht(self):
        self.assertFalse(bewerte_leistung(49))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 543
