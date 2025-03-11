# Input
- Programmierkonzept: While-Schleifen;Boolean und None
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Training

Schreibe eine Funktion namens `basketball_training()`, die eine While-Schleife verwendet, um die Anzahl der erfolgreichen Würfe eines Spielers zu zählen. Die Funktion soll eine Liste von Würfen als Argument erhalten, wobei jeder Wurf entweder `True` (erfolgreich) oder `False` (nicht erfolgreich) ist. Die Schleife soll durch die Liste iterieren und die Anzahl der erfolgreichen Würfe zählen. Wenn die Liste leer ist, soll die Funktion `None` zurückgeben. Andernfalls soll die Funktion die Anzahl der erfolgreichen Würfe zurückgeben.

Beispielaufruf:
```python
basketball_training([True, False, True, True, False])
```
Dieser Aufruf soll `3` zurückgeben, da es drei erfolgreiche Würfe gibt.

## Codegerüst
```python
def basketball_training(throws):
    ## Hier Code einfügen
```

## Musterlösung
```python
def basketball_training(throws):
    if not throws:
        return None
    count = 0
    i = 0
    while i < len(throws):
        if throws[i]:
            count += 1
        i += 1
    return count

# Beispielaufruf
print(basketball_training([True, False, True, True, False]))
```

## Unit Tests
```python
import unittest
from main import basketball_training

class TestBasketballTraining(unittest.TestCase):
    def test_empty_list(self):
        self.assertIsNone(basketball_training([]))

    def test_all_successful(self):
        self.assertEqual(basketball_training([True, True, True]), 3)

    def test_all_unsuccessful(self):
        self.assertEqual(basketball_training([False, False, False]), 0)

    def test_mixed_results(self):
        self.assertEqual(basketball_training([True, False, True, True, False]), 3)

    def test_single_successful(self):
        self.assertEqual(basketball_training([True]), 1)

    def test_single_unsuccessful(self):
        self.assertEqual(basketball_training([False]), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 569
