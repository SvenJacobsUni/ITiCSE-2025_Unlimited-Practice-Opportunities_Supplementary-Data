# Input
- Programmierkonzept: Funktionen als Variablen;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Aquarium

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Aquarium-Temperaturkontrolle

Schreibe eine Funktion namens `kontrolliere_temperatur(temperatur)`, die überprüft, ob die Temperatur in einem Aquarium im optimalen Bereich liegt. Der optimale Temperaturbereich für das Aquarium liegt zwischen 22 und 28 Grad Celsius (einschließlich). Die Funktion soll `True` zurückgeben, wenn die Temperatur im optimalen Bereich liegt, und `False`, wenn sie außerhalb dieses Bereichs liegt.

Zusätzlich soll eine Funktion `ist_zu_heiss_oder_zu_kalt(temperatur)` implementiert werden, die überprüft, ob die Temperatur entweder zu heiß (über 28 Grad) oder zu kalt (unter 22 Grad) ist. Diese Funktion soll `True` zurückgeben, wenn die Temperatur außerhalb des optimalen Bereichs liegt, und `False`, wenn sie innerhalb des Bereichs liegt.

Beispielaufrufe:
- `kontrolliere_temperatur(25)` gibt `True` zurück.
- `kontrolliere_temperatur(30)` gibt `False` zurück.
- `ist_zu_heiss_oder_zu_kalt(18)` gibt `True` zurück.
- `ist_zu_heiss_oder_zu_kalt(24)` gibt `False` zurück.

## Codegerüst
```python
def kontrolliere_temperatur(temperatur):
    ## Hier Code einfügen

def ist_zu_heiss_oder_zu_kalt(temperatur):
    ## Hier Code einfügen
```

## Musterlösung
```python
def kontrolliere_temperatur(temperatur):
    return 22 <= temperatur <= 28

def ist_zu_heiss_oder_zu_kalt(temperatur):
    return temperatur < 22 or temperatur > 28

# Beispielaufrufe
print(kontrolliere_temperatur(25))  # True
print(kontrolliere_temperatur(30))  # False
print(ist_zu_heiss_oder_zu_kalt(18))  # True
print(ist_zu_heiss_oder_zu_kalt(24))  # False
```

## Unit Tests
```python
import unittest

from main import kontrolliere_temperatur, ist_zu_heiss_oder_zu_kalt

class TestAquariumTemperatur(unittest.TestCase):
    def test_kontrolliere_temperatur_optimal(self):
        self.assertTrue(kontrolliere_temperatur(25))

    def test_kontrolliere_temperatur_zu_heiss(self):
        self.assertFalse(kontrolliere_temperatur(30))

    def test_kontrolliere_temperatur_zu_kalt(self):
        self.assertFalse(kontrolliere_temperatur(18))

    def test_ist_zu_heiss_oder_zu_kalt_zu_heiss(self):
        self.assertTrue(ist_zu_heiss_oder_zu_kalt(30))

    def test_ist_zu_heiss_oder_zu_kalt_zu_kalt(self):
        self.assertTrue(ist_zu_heiss_oder_zu_kalt(18))

    def test_ist_zu_heiss_oder_zu_kalt_optimal(self):
        self.assertFalse(ist_zu_heiss_oder_zu_kalt(24))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 556
