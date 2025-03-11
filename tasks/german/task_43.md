# Input
- Programmierkonzept: Float
- Kontext: Virtuelle Realität

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Berechnung der VR-Renderzeit

In der virtuellen Realität (VR) ist es wichtig, dass die Renderzeit pro Frame möglichst gering ist, um eine flüssige und realistische Darstellung zu gewährleisten. Die Renderzeit wird oft in Millisekunden (ms) gemessen.

Schreibe eine Funktion namens `berechne_renderzeit(frames, gesamtzeit)`, die die durchschnittliche Renderzeit pro Frame berechnet. Die Funktion soll zwei Parameter entgegennehmen:
- `frames`: Die Anzahl der gerenderten Frames (ganzzahliger Wert).
- `gesamtzeit`: Die gesamte Renderzeit in Millisekunden (Fließkommawert).

Die Funktion soll die durchschnittliche Renderzeit pro Frame als Fließkommawert zurückgeben.

Beispielaufruf:
```python
durchschnitt = berechne_renderzeit(240, 5000.0)
print(durchschnitt)  # Erwartete Ausgabe: 20.833333333333332
```

## Codegerüst
```python
def berechne_renderzeit(frames, gesamtzeit):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_renderzeit(frames, gesamtzeit):
    return gesamtzeit / frames

durchschnitt = berechne_renderzeit(240, 5000.0)
print(durchschnitt)
```

## Unit Tests
```python
import unittest

from main import berechne_renderzeit

class TestBerechneRenderzeit(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertAlmostEqual(berechne_renderzeit(240, 5000.0), 20.833333333333332)

    def test_null_frames(self):
        with self.assertRaises(ZeroDivisionError):
            berechne_renderzeit(0, 5000.0)

    def test_null_gesamtzeit(self):
        self.assertEqual(berechne_renderzeit(240, 0.0), 0.0)

    def test_ein_frame(self):
        self.assertEqual(berechne_renderzeit(1, 5000.0), 5000.0)

    def test_grosse_werte(self):
        self.assertAlmostEqual(berechne_renderzeit(1000000, 5000000.0), 5.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 461
