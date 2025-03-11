# Input
- Programmierkonzept: While-Schleifen
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Wiederholungen

Schreibe eine Funktion namens `trainingsplan(wiederholungen)`, die eine While-Schleife verwendet, um eine bestimmte Anzahl von Wiederholungen einer Übung zu zählen und auszugeben. Die Funktion soll die Anzahl der Wiederholungen als Argument entgegennehmen und für jede Wiederholung eine Nachricht in der Form "Wiederholung X" ausgeben, wobei X die aktuelle Wiederholungsnummer ist.

Beispielaufruf: `trainingsplan(5)` soll die folgenden Ausgaben erzeugen:
```
Wiederholung 1
Wiederholung 2
Wiederholung 3
Wiederholung 4
Wiederholung 5
```

## Codegerüst
```python
def trainingsplan(wiederholungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def trainingsplan(wiederholungen):
    i = 1
    while i <= wiederholungen:
        print(f"Wiederholung {i}")
        i += 1

trainingsplan(5)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import trainingsplan

class TestTrainingsplan(unittest.TestCase):
    def test_fuenf_wiederholungen(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        trainingsplan(5)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Wiederholung 1\nWiederholung 2\nWiederholung 3\nWiederholung 4\nWiederholung 5")

    def test_keine_wiederholungen(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        trainingsplan(0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

    def test_eine_wiederholung(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        trainingsplan(1)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Wiederholung 1")

    def test_zehn_wiederholungen(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        trainingsplan(10)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Wiederholung 1\nWiederholung 2\nWiederholung 3\nWiederholung 4\nWiederholung 5\nWiederholung 6\nWiederholung 7\nWiederholung 8\nWiederholung 9\nWiederholung 10")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 430
