# Input
- Programmierkonzept: Rekursion
- Kontext: Aquarium

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursion im Aquarium

Schreibe eine rekursive Funktion namens `fische_zaehlen(aquarium)`, die die Anzahl der Fische in einem verschachtelten Aquarium zählt. Ein Aquarium kann entweder leer sein, eine Liste von Fischen enthalten oder eine Liste von weiteren Aquarien (die wiederum Fische oder weitere Aquarien enthalten können).

Ein Beispielaufruf könnte so aussehen:
```python
aquarium = [[], ["Fisch1", "Fisch2"], [["Fisch3"], []], "Fisch4"]
print(fische_zaehlen(aquarium))  # Ausgabe: 4
```

Implementiere die Funktion `fische_zaehlen(aquarium)`, die die Gesamtzahl der Fische im gesamten verschachtelten Aquarium zurückgibt.

## Codegerüst
```python
def fische_zaehlen(aquarium):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fische_zaehlen(aquarium):
    if not isinstance(aquarium, list):
        return 1
    return sum(fische_zaehlen(item) for item in aquarium)

aquarium = [[], ["Fisch1", "Fisch2"], [["Fisch3"], []], "Fisch4"]
print(fische_zaehlen(aquarium))  # Ausgabe: 4
```

## Unit Tests
```python
import unittest
from main import fische_zaehlen

class TestFischeZaehlen(unittest.TestCase):
    def test_leeres_aquarium(self):
        self.assertEqual(fische_zaehlen([]), 0)

    def test_ein_fisch(self):
        self.assertEqual(fische_zaehlen(["Fisch1"]), 1)

    def test_mehrere_fische(self):
        self.assertEqual(fische_zaehlen(["Fisch1", "Fisch2", "Fisch3"]), 3)

    def test_verschachteltes_aquarium(self):
        self.assertEqual(fische_zaehlen([[], ["Fisch1", "Fisch2"], [["Fisch3"], []], "Fisch4"]), 4)

    def test_tief_verschachteltes_aquarium(self):
        self.assertEqual(fische_zaehlen([[[[[["Fisch1"]]]]]]), 1)

    def test_aquarium_mit_leeren_und_vollen_unteraquarien(self):
        self.assertEqual(fische_zaehlen([[], ["Fisch1"], [], ["Fisch2", ["Fisch3"]], []]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 429
