# Input
- Programmierkonzept: For-Schleifen;While-Schleifen
- Kontext: Vergnügungspark

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Vergnügungspark - Fahrgeschäfte zählen

Schreibe eine Funktion namens `zaehle_fahrgeschaefte(fahrgeschaefte)`, die eine Liste von Fahrgeschäften in einem Vergnügungspark als Argument erhält. Die Funktion soll die Anzahl der Fahrgeschäfte zählen und zurückgeben, die eine bestimmte Mindestanzahl an Fahrten pro Tag durchführen. Verwende eine For-Schleife oder While-Schleife, um die Fahrgeschäfte zu durchlaufen und die Zählung durchzuführen.

Die Liste `fahrgeschaefte` enthält Tupel, wobei jedes Tupel den Namen des Fahrgeschäfts und die Anzahl der Fahrten pro Tag enthält. Die Mindestanzahl an Fahrten pro Tag ist 10.

Beispielaufruf:
```python
fahrgeschaefte = [("Achterbahn", 15), ("Riesenrad", 8), ("Karussell", 12)]
print(zaehle_fahrgeschaefte(fahrgeschaefte))  # Ausgabe: 2
```

In diesem Beispiel gibt es zwei Fahrgeschäfte, die mindestens 10 Fahrten pro Tag durchführen: "Achterbahn" und "Karussell".

## Codegerüst
```python
def zaehle_fahrgeschaefte(fahrgeschaefte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fahrgeschaefte(fahrgeschaefte):
    return sum(1 for _, fahrten in fahrgeschaefte if fahrten >= 10)

fahrgeschaefte = [("Achterbahn", 15), ("Riesenrad", 8), ("Karussell", 12)]
print(zaehle_fahrgeschaefte(fahrgeschaefte))  # Ausgabe: 2
```

## Unit Tests
```python
import unittest
from main import zaehle_fahrgeschaefte

class TestZaehleFahrgeschaefte(unittest.TestCase):
    def test_alle_fahrgeschaefte_zaehlen(self):
        self.assertEqual(zaehle_fahrgeschaefte([("Achterbahn", 15), ("Riesenrad", 8), ("Karussell", 12)]), 2)

    def test_keine_fahrgeschaefte(self):
        self.assertEqual(zaehle_fahrgeschaefte([]), 0)

    def test_alle_unter_minimum(self):
        self.assertEqual(zaehle_fahrgeschaefte([("Achterbahn", 5), ("Riesenrad", 3), ("Karussell", 2)]), 0)

    def test_alle_ueber_minimum(self):
        self.assertEqual(zaehle_fahrgeschaefte([("Achterbahn", 15), ("Riesenrad", 18), ("Karussell", 12)]), 3)

    def test_genau_minimum(self):
        self.assertEqual(zaehle_fahrgeschaefte([("Achterbahn", 10), ("Riesenrad", 10), ("Karussell", 10)]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 554
