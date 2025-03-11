# Input
- Programmierkonzept: Tupel
- Kontext: Restaurant

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Restaurant-Menü

Schreibe eine Funktion namens `erstelle_menü()`, die ein Tupel mit den Namen von drei verschiedenen Gerichten aus einem Restaurant-Menü zurückgibt. Jedes Gericht soll als String im Tupel enthalten sein. Beispielaufruf: `erstelle_menü()` könnte ein Tupel wie `("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu")` zurückgeben.

```python
def erstelle_menü():
    # Deine Implementierung hier
    pass
```

Erstelle außerdem eine Funktion `drucke_menü(menü)`, die das übergebene Menü-Tupel durchläuft und jedes Gericht in einer neuen Zeile ausgibt. Beispielaufruf: `drucke_menü(("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu"))` sollte die Gerichte jeweils in einer neuen Zeile ausgeben.

```python
def drucke_menü(menü):
    # Deine Implementierung hier
    pass
```

Verwende die Funktion `erstelle_menü()` und übergebe das zurückgegebene Tupel an die Funktion `drucke_menü()`, um das Menü auf der Konsole auszugeben.

## Codegerüst
```python
def erstelle_menü():
    ## Hier Code einfügen
    pass

def drucke_menü(menü):
    ## Hier Code einfügen
    pass
```

## Musterlösung
```python
def erstelle_menü():
    return ("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu")

def drucke_menü(menü):
    for gericht in menü:
        print(gericht)

menü = erstelle_menü()
drucke_menü(menü)
```

## Unit Tests
```python
import unittest
from main import erstelle_menü, drucke_menü
from io import StringIO
import sys

class TestRestaurantMenü(unittest.TestCase):
    def test_erstelle_menü(self):
        menü = erstelle_menü()
        self.assertIsInstance(menü, tuple)
        self.assertEqual(len(menü), 3)
        for gericht in menü:
            self.assertIsInstance(gericht, str)

    def test_drucke_menü(self):
        menü = ("Pizza Margherita", "Spaghetti Carbonara", "Tiramisu")
        expected_output = "Pizza Margherita\nSpaghetti Carbonara\nTiramisu\n"
        
        captured_output = StringIO()
        sys.stdout = captured_output
        drucke_menü(menü)
        sys.stdout = sys.__stdout__
        
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 451
