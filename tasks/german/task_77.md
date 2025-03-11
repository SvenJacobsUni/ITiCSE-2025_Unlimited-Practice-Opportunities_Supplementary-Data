# Input
- Programmierkonzept: Boolean und None
- Kontext: Aquarium

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Aquarium-Überprüfung

Schreibe eine Funktion namens `ist_aquarium_voll(wasserstand, kapazitaet)`, die überprüft, ob ein Aquarium voll ist. Die Funktion soll zwei Parameter entgegennehmen: `wasserstand` (in Litern) und `kapazitaet` (in Litern). Die Funktion soll `True` zurückgeben, wenn das Aquarium voll ist, `False`, wenn es nicht voll ist, und `None`, wenn der Wasserstand größer als die Kapazität ist.

Beispielaufrufe:
- `ist_aquarium_voll(50, 100)` gibt `False` zurück.
- `ist_aquarium_voll(100, 100)` gibt `True` zurück.
- `ist_aquarium_voll(150, 100)` gibt `None` zurück.

## Codegerüst
```python
def ist_aquarium_voll(wasserstand, kapazitaet):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ist_aquarium_voll(wasserstand, kapazitaet):
    if wasserstand > kapazitaet:
        return None
    return wasserstand == kapazitaet

# Beispielaufrufe
print(ist_aquarium_voll(50, 100))  # False
print(ist_aquarium_voll(100, 100)) # True
print(ist_aquarium_voll(150, 100)) # None
```

## Unit Tests
```python
import unittest
from main import ist_aquarium_voll

class TestIstAquariumVoll(unittest.TestCase):
    def test_aquarium_nicht_voll(self):
        self.assertEqual(ist_aquarium_voll(50, 100), False)

    def test_aquarium_voll(self):
        self.assertEqual(ist_aquarium_voll(100, 100), True)

    def test_aquarium_ueberfuellt(self):
        self.assertEqual(ist_aquarium_voll(150, 100), None)

    def test_aquarium_leer(self):
        self.assertEqual(ist_aquarium_voll(0, 100), False)

    def test_aquarium_genau_voll(self):
        self.assertEqual(ist_aquarium_voll(100, 100), True)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 495
