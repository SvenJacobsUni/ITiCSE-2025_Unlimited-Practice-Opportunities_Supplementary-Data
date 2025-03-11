# Input
- Programmierkonzept: Tupel;Funktionen als Variablen
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Psychische Gesundheit - Stimmungsanalyse

Schreibe eine Funktion namens `stimmungsanalyse(stimmung)`, die eine Stimmung als Tupel entgegennimmt und eine entsprechende Nachricht zurückgibt. Das Tupel besteht aus zwei Elementen: einem String, der die Stimmung beschreibt (z.B. "glücklich", "traurig", "gestresst"), und einem Integer, der die Intensität der Stimmung auf einer Skala von 1 bis 10 angibt.

Die Funktion soll eine Nachricht zurückgeben, die die Stimmung und ihre Intensität beschreibt. Verwende eine zweite Funktion namens `nachricht_generieren`, die die Nachricht basierend auf den übergebenen Werten erstellt.

Beispielaufruf:
```python
stimmungsanalyse(("glücklich", 8))
```

Beispielausgabe:
```python
"Du fühlst dich sehr glücklich mit einer Intensität von 8."
```

## Codegerüst
```python
def stimmungsanalyse(stimmung):
    ## Hier Code einfügen

def nachricht_generieren(stimmung, intensitaet):
    ## Hier Code einfügen
```

## Musterlösung
```python
def stimmungsanalyse(stimmung):
    print(nachricht_generieren(stimmung[0], stimmung[1]))

def nachricht_generieren(stimmung, intensitaet):
    return f"Du fühlst dich sehr {stimmung} mit einer Intensität von {intensitaet}."

stimmungsanalyse(("glücklich", 8))
```

## Unit Tests
```python
import unittest
from main import stimmungsanalyse, nachricht_generieren

class TestStimmungsanalyse(unittest.TestCase):
    def test_gluecklich(self):
        self.assertEqual(nachricht_generieren("glücklich", 8), "Du fühlst dich sehr glücklich mit einer Intensität von 8.")

    def test_traurig(self):
        self.assertEqual(nachricht_generieren("traurig", 3), "Du fühlst dich sehr traurig mit einer Intensität von 3.")

    def test_gestresst(self):
        self.assertEqual(nachricht_generieren("gestresst", 10), "Du fühlst dich sehr gestresst mit einer Intensität von 10.")

    def test_neutral(self):
        self.assertEqual(nachricht_generieren("neutral", 5), "Du fühlst dich sehr neutral mit einer Intensität von 5.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 544
