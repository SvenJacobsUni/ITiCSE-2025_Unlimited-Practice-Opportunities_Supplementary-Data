# Input
- Programmierkonzept: Integer;For-Schleifen;Funktionen höherer Ordnung
- Kontext: Musik

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Musiknoten zählen

Schreibe eine Funktion namens `zaehle_noten(musikstueck)`, die eine Liste von Integern als Argument erhält. Jeder Integer in der Liste repräsentiert eine Note in einem Musikstück. Die Funktion soll die Anzahl der Vorkommen jeder Note zählen und das Ergebnis als Dictionary zurückgeben, wobei die Schlüssel die Noten und die Werte die Anzahl der Vorkommen sind.

Beispielaufruf:
```python
musikstueck = [60, 62, 64, 60, 62, 60, 65, 67, 60]
print(zaehle_noten(musikstueck))
```

Erwartete Ausgabe:
```python
{60: 4, 62: 2, 64: 1, 65: 1, 67: 1}
```

Implementiere die Funktion `zaehle_noten(musikstueck)` so, dass sie die Anzahl der Vorkommen jeder Note in der Liste korrekt zählt und als Dictionary zurückgibt.

## Codegerüst
```python
def zaehle_noten(musikstueck):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_noten(musikstueck):
    return {note: musikstueck.count(note) for note in set(musikstueck)}

musikstueck = [60, 62, 64, 60, 62, 60, 65, 67, 60]
print(zaehle_noten(musikstueck))
```

## Unit Tests
```python
import unittest

from main import zaehle_noten

class TestZaehleNoten(unittest.TestCase):
    def test_einfaches_stueck(self):
        self.assertEqual(zaehle_noten([60, 62, 64, 60, 62, 60, 65, 67, 60]), {60: 4, 62: 2, 64: 1, 65: 1, 67: 1})

    def test_leeres_stueck(self):
        self.assertEqual(zaehle_noten([]), {})

    def test_eine_note(self):
        self.assertEqual(zaehle_noten([60]), {60: 1})

    def test_alle_noten_einmal(self):
        self.assertEqual(zaehle_noten([60, 61, 62, 63, 64, 65, 66, 67]), {60: 1, 61: 1, 62: 1, 63: 1, 64: 1, 65: 1, 66: 1, 67: 1})

    def test_alle_noten_mehrfach(self):
        self.assertEqual(zaehle_noten([60, 60, 61, 61, 62, 62, 63, 63, 64, 64, 65, 65, 66, 66, 67, 67]), {60: 2, 61: 2, 62: 2, 63: 2, 64: 2, 65: 2, 66: 2, 67: 2})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 601
