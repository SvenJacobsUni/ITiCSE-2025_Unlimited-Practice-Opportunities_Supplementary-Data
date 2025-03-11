# Input
- Programmierkonzept: Integer;String
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Psychische Gesundheit

Schreibe eine Funktion namens `stimmungs_analyse(stimmung)`, die eine Stimmung als String entgegennimmt und eine entsprechende Nachricht zurückgibt. Die Stimmung kann entweder "glücklich", "traurig" oder "gestresst" sein. 

- Bei "glücklich" soll die Funktion "Das ist großartig! Mach weiter so!" zurückgeben.
- Bei "traurig" soll die Funktion "Es ist okay, traurig zu sein. Sprich mit jemandem darüber." zurückgeben.
- Bei "gestresst" soll die Funktion "Versuche, dir eine Pause zu gönnen und zu entspannen." zurückgeben.

Beispielaufrufe:
- `stimmungs_analyse("glücklich")` gibt "Das ist großartig! Mach weiter so!" zurück.
- `stimmungs_analyse("traurig")` gibt "Es ist okay, traurig zu sein. Sprich mit jemandem darüber." zurück.
- `stimmungs_analyse("gestresst")` gibt "Versuche, dir eine Pause zu gönnen und zu entspannen." zurück.

## Codegerüst
```python
def stimmungs_analyse(stimmung):
    ## Hier Code einfügen
```

## Musterlösung
```python
def stimmungs_analyse(stimmung):
    if stimmung == "glücklich":
        return "Das ist großartig! Mach weiter so!"
    elif stimmung == "traurig":
        return "Es ist okay, traurig zu sein. Sprich mit jemandem darüber."
    elif stimmung == "gestresst":
        return "Versuche, dir eine Pause zu gönnen und zu entspannen."

print(stimmungs_analyse("glücklich"))
print(stimmungs_analyse("traurig"))
print(stimmungs_analyse("gestresst"))
```

## Unit Tests
```python
import unittest
from main import stimmungs_analyse

class TestStimmungsAnalyse(unittest.TestCase):
    def test_gluecklich(self):
        self.assertEqual(stimmungs_analyse("glücklich"), "Das ist großartig! Mach weiter so!")

    def test_traurig(self):
        self.assertEqual(stimmungs_analyse("traurig"), "Es ist okay, traurig zu sein. Sprich mit jemandem darüber.")

    def test_gestresst(self):
        self.assertEqual(stimmungs_analyse("gestresst"), "Versuche, dir eine Pause zu gönnen und zu entspannen.")

    def test_unbekannte_stimmung(self):
        self.assertIsNone(stimmungs_analyse("unbekannt"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 580
