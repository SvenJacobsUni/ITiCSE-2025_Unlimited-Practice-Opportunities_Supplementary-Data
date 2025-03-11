# Input
- Programmierkonzept: Funktionen als Variablen
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen als Variablen

Schreibe eine Funktion `haustier_aktion(haustier, aktion)`, die eine Aktion für ein bestimmtes Haustier ausführt. Die Funktion soll zwei Parameter akzeptieren: `haustier` (ein String, der den Namen des Haustiers angibt) und `aktion` (eine Funktion, die eine Aktion beschreibt, die mit dem Haustier durchgeführt wird).

Beispielaufruf:
```python
def streicheln(haustier):
    return f"{haustier} wird gestreichelt."

def fuettern(haustier):
    return f"{haustier} wird gefüttert."

haustier_aktion("Bello", streicheln)  # sollte "Bello wird gestreichelt." zurückgeben
haustier_aktion("Mieze", fuettern)    # sollte "Mieze wird gefüttert." zurückgeben
```

Implementiere die Funktion `haustier_aktion(haustier, aktion)` so, dass sie die entsprechende Aktion für das angegebene Haustier ausführt und das Ergebnis zurückgibt.

## Codegerüst
```python
def haustier_aktion(haustier, aktion):
    ## Hier Code einfügen
```

## Musterlösung
```python
def haustier_aktion(haustier, aktion):
    print(aktion(haustier))

def streicheln(haustier):
    return f"{haustier} wird gestreichelt."

def fuettern(haustier):
    return f"{haustier} wird gefüttert."

haustier_aktion("Bello", streicheln)
haustier_aktion("Mieze", fuettern)
```

## Unit Tests
```python
import unittest
from main import haustier_aktion

def streicheln(haustier):
    return f"{haustier} wird gestreichelt."

def fuettern(haustier):
    return f"{haustier} wird gefüttert."

class TestHaustierAktion(unittest.TestCase):
    def test_streicheln(self):
        self.assertEqual(haustier_aktion("Bello", streicheln), "Bello wird gestreichelt.")

    def test_fuettern(self):
        self.assertEqual(haustier_aktion("Mieze", fuettern), "Mieze wird gefüttert.")

    def test_leerer_name(self):
        self.assertEqual(haustier_aktion("", streicheln), " wird gestreichelt.")

    def test_andere_aktion(self):
        def baden(haustier):
            return f"{haustier} wird gebadet."
        self.assertEqual(haustier_aktion("Rex", baden), "Rex wird gebadet.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 496
