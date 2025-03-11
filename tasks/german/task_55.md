# Input
- Programmierkonzept: Funktionen als Variablen
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen als Variablen im Kontext Sport

Schreibe eine Funktion `sport_auswahl(sportart)`, die eine andere Funktion als Variable zurückgibt. Die zurückgegebene Funktion soll eine Nachricht ausgeben, die spezifisch für die gewählte Sportart ist. 

Definiere mindestens drei verschiedene Sportarten und die entsprechenden Funktionen, die eine Nachricht für jede Sportart ausgeben. 

Beispielaufruf:
```python
fussball_funktion = sport_auswahl("Fussball")
fussball_funktion()  # Gibt eine Nachricht für Fussball aus

basketball_funktion = sport_auswahl("Basketball")
basketball_funktion()  # Gibt eine Nachricht für Basketball aus
```

Erwartete Nachrichten könnten sein:
- Für "Fussball": "Du hast Fussball gewählt! Ein spannendes Spiel auf dem Rasen."
- Für "Basketball": "Du hast Basketball gewählt! Ein dynamisches Spiel auf dem Court."
- Für "Tennis": "Du hast Tennis gewählt! Ein intensives Match auf dem Platz."

Implementiere die Funktion `sport_auswahl(sportart)` und die entsprechenden Funktionen für die Sportarten.

## Codegerüst
```python
def sport_auswahl(sportart):
    ## Hier Code einfügen

def fussball():
    ## Hier Code einfügen

def basketball():
    ## Hier Code einfügen

def tennis():
    ## Hier Code einfügen
```

## Musterlösung
```python
def sport_auswahl(sportart):
    if sportart == "Fussball":
        return fussball
    elif sportart == "Basketball":
        return basketball
    elif sportart == "Tennis":
        return tennis

def fussball():
    print("Du hast Fussball gewählt! Ein spannendes Spiel auf dem Rasen.")

def basketball():
    print("Du hast Basketball gewählt! Ein dynamisches Spiel auf dem Court.")

def tennis():
    print("Du hast Tennis gewählt! Ein intensives Match auf dem Platz.")

# Beispielaufrufe
fussball_funktion = sport_auswahl("Fussball")
fussball_funktion()

basketball_funktion = sport_auswahl("Basketball")
basketball_funktion()

tennis_funktion = sport_auswahl("Tennis")
tennis_funktion()
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import sport_auswahl

class TestSportAuswahl(unittest.TestCase):
    def test_fussball(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        func = sport_auswahl("Fussball")
        func()
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Du hast Fussball gewählt! Ein spannendes Spiel auf dem Rasen.")

    def test_basketball(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        func = sport_auswahl("Basketball")
        func()
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Du hast Basketball gewählt! Ein dynamisches Spiel auf dem Court.")

    def test_tennis(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        func = sport_auswahl("Tennis")
        func()
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Du hast Tennis gewählt! Ein intensives Match auf dem Platz.")

    def test_unbekannte_sportart(self):
        self.assertIsNone(sport_auswahl("Handball"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 473
