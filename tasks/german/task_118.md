# Input
- Programmierkonzept: Listen;Float
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Olympia - Durchschnittliche Punktzahl berechnen

Schreibe eine Funktion namens `durchschnittliche_punktzahl(punkte)`, die eine Liste von Punktzahlen (als Float-Werte) erhält und die durchschnittliche Punktzahl der Athleten berechnet und zurückgibt. 

Beispielaufruf: 
```python
punkte = [9.5, 8.7, 9.8, 7.6, 8.9]
print(durchschnittliche_punktzahl(punkte))  # Ausgabe: 8.9
```

Die Funktion soll die durchschnittliche Punktzahl der Athleten berechnen und als Float-Wert zurückgeben.

## Codegerüst
```python
def durchschnittliche_punktzahl(punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def durchschnittliche_punktzahl(punkte):
    return sum(punkte) / len(punkte)

punkte = [9.5, 8.7, 9.8, 7.6, 8.9]
print(durchschnittliche_punktzahl(punkte))
```

## Unit Tests
```python
import unittest
from main import durchschnittliche_punktzahl

class TestDurchschnittlichePunktzahl(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertEqual(durchschnittliche_punktzahl([9.5, 8.7, 9.8, 7.6, 8.9]), 8.9)

    def test_leere_liste(self):
        with self.assertRaises(ZeroDivisionError):
            durchschnittliche_punktzahl([])

    def test_ein_element(self):
        self.assertEqual(durchschnittliche_punktzahl([10.0]), 10.0)

    def test_gemischte_werte(self):
        self.assertEqual(durchschnittliche_punktzahl([1.0, 2.0, 3.0, 4.0, 5.0]), 3.0)

    def test_negative_werte(self):
        self.assertEqual(durchschnittliche_punktzahl([-1.0, -2.0, -3.0, -4.0, -5.0]), -3.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 550
