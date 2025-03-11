# Input
- Programmierkonzept: Funktionen als Variablen
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen als Variablen im Kontext "Kochen"

Schreibe eine Funktion `koch_rezept(rezept_name)`, die eine Funktion als Parameter akzeptiert und diese Funktion ausführt. Erstelle zwei Beispielrezepte als Funktionen: `rezept_pasta()` und `rezept_salat()`. 

- `rezept_pasta()` soll die Nachricht "Pasta wird gekocht!" ausgeben.
- `rezept_salat()` soll die Nachricht "Salat wird zubereitet!" ausgeben.

Die Funktion `koch_rezept(rezept_name)` soll die übergebene Rezeptfunktion ausführen.

Beispielaufrufe:
```python
koch_rezept(rezept_pasta)  # Ausgabe: Pasta wird gekocht!
koch_rezept(rezept_salat)  # Ausgabe: Salat wird zubereitet!
```

## Codegerüst
```python
def koch_rezept(rezept_name):
    ## Hier Code einfügen

def rezept_pasta():
    ## Hier Code einfügen

def rezept_salat():
    ## Hier Code einfügen
```

## Musterlösung
```python
def koch_rezept(rezept_name):
    rezept_name()

def rezept_pasta():
    print("Pasta wird gekocht!")

def rezept_salat():
    print("Salat wird zubereitet!")

koch_rezept(rezept_pasta)
koch_rezept(rezept_salat)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import koch_rezept, rezept_pasta, rezept_salat

class TestKochRezept(unittest.TestCase):
    def test_rezept_pasta(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        koch_rezept(rezept_pasta)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pasta wird gekocht!")

    def test_rezept_salat(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        koch_rezept(rezept_salat)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Salat wird zubereitet!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 454
