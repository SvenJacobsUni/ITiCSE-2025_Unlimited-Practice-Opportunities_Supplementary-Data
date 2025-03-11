# Input
- Programmierkonzept: Operationen mit Zahlen
- Kontext: Aquarium

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Operationen mit Zahlen im Kontext "Aquarium"

Schreibe eine Funktion namens `berechne_wasservolumen(laenge, breite, hoehe)`, die das Volumen eines rechteckigen Aquariums in Litern berechnet. Die Funktion soll die Länge, Breite und Höhe des Aquariums in Zentimetern als Parameter entgegennehmen und das Volumen in Litern zurückgeben. 

Hinweis: 1 Liter entspricht 1000 Kubikzentimetern.

Beispielaufruf: 
```python
volumen = berechne_wasservolumen(100, 50, 40)
print(volumen)  # Ausgabe: 200.0
```

In diesem Beispiel hat das Aquarium eine Länge von 100 cm, eine Breite von 50 cm und eine Höhe von 40 cm. Das berechnete Volumen beträgt 200 Liter.

## Codegerüst
```python
def berechne_wasservolumen(laenge, breite, hoehe):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_wasservolumen(laenge, breite, hoehe):
    return (laenge * breite * hoehe) / 1000

volumen = berechne_wasservolumen(100, 50, 40)
print(volumen)
```

## Unit Tests
```python
import unittest
from main import berechne_wasservolumen

class TestBerechneWasservolumen(unittest.TestCase):
    def test_standard_fall(self):
        self.assertEqual(berechne_wasservolumen(100, 50, 40), 200.0)

    def test_null_volumen(self):
        self.assertEqual(berechne_wasservolumen(0, 50, 40), 0.0)
        self.assertEqual(berechne_wasservolumen(100, 0, 40), 0.0)
        self.assertEqual(berechne_wasservolumen(100, 50, 0), 0.0)

    def test_ein_liter(self):
        self.assertEqual(berechne_wasservolumen(10, 10, 10), 1.0)

    def test_grosse_werte(self):
        self.assertEqual(berechne_wasservolumen(1000, 1000, 1000), 1000000.0)

    def test_kleine_werte(self):
        self.assertAlmostEqual(berechne_wasservolumen(1, 1, 1), 0.001)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 510
