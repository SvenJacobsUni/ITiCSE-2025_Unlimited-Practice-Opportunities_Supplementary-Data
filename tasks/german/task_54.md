# Input
- Programmierkonzept: For-Schleifen
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Einführung in For-Schleifen im Kontext von Modernem Gaming

Schreibe eine Funktion namens `level_up(punkte_liste)`, die eine Liste von Punktzahlen (Integer) als Argument erhält. Die Funktion soll durch die Liste iterieren und für jede Punktzahl überprüfen, ob sie größer oder gleich 1000 ist. Wenn dies der Fall ist, soll die Funktion die Nachricht "Level Up!" ausgeben, andernfalls "Weiter so!".

Beispielaufruf:
```python
level_up([500, 1500, 800, 1200])
```

Erwartete Ausgabe:
```
Weiter so!
Level Up!
Weiter so!
Level Up!
```

## Codegerüst
```python
def level_up(punkte_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def level_up(punkte_liste):
    for punkte in punkte_liste:
        if punkte >= 1000:
            print("Level Up!")
        else:
            print("Weiter so!")

level_up([500, 1500, 800, 1200])
```

## Unit Tests
```python
import unittest
from main import level_up
from io import StringIO
import sys

class TestLevelUp(unittest.TestCase):
    def test_mixed_scores(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([500, 1500, 800, 1200])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Weiter so!\nLevel Up!\nWeiter so!\nLevel Up!")

    def test_all_below_threshold(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([100, 200, 300])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Weiter so!\nWeiter so!\nWeiter so!")

    def test_all_above_threshold(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([1000, 2000, 3000])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Level Up!\nLevel Up!\nLevel Up!")

    def test_empty_list(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        level_up([])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 472
