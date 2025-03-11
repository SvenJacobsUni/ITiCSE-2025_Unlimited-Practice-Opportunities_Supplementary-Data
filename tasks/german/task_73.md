# Input
- Programmierkonzept: Rekursion
- Kontext: Virtuelle Realität

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Berechnung der VR-Welt-Tiefe

In einer virtuellen Realität (VR) gibt es verschiedene Ebenen, die ineinander verschachtelt sind. Jede Ebene kann weitere Unterebenen enthalten, die wiederum weitere Unterebenen enthalten können, und so weiter. Deine Aufgabe ist es, eine Funktion zu schreiben, die die maximale Tiefe dieser verschachtelten Ebenen berechnet.

Schreibe eine Funktion `berechne_tiefe(vr_welt)`, die die Tiefe einer VR-Welt berechnet. Die VR-Welt wird als verschachtelte Liste dargestellt, wobei jede Liste weitere Listen enthalten kann, die die Unterebenen repräsentieren.

Beispiel:
```python
vr_welt = [[], [[], []], [[[]]], [[], [[], [[], []]]]]
```

In diesem Beispiel hat die VR-Welt eine maximale Tiefe von 4.

Implementiere die Funktion `berechne_tiefe(vr_welt)`, die die maximale Tiefe der VR-Welt als Integer zurückgibt.

```python
def berechne_tiefe(vr_welt):
    # Deine Implementierung hier
    pass
```

Beispielaufrufe:
```python
print(berechne_tiefe([[], [[], []], [[[]]], [[], [[], [[], []]]]]))  # Ausgabe: 4
print(berechne_tiefe([[], [[], []], [[[]]]]))  # Ausgabe: 3
print(berechne_tiefe([[]]))  # Ausgabe: 2
print(berechne_tiefe([]))  # Ausgabe: 1
```

## Codegerüst
```python
def berechne_tiefe(vr_welt):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_tiefe(vr_welt):
    if not isinstance(vr_welt, list):
        return 0
    return 1 + max((berechne_tiefe(ebene) for ebene in vr_welt), default=0)

print(berechne_tiefe([[], [[], []], [[[]]], [[], [[], [[], []]]]]))  # Ausgabe: 4
print(berechne_tiefe([[], [[], []], [[[]]]]))  # Ausgabe: 3
print(berechne_tiefe([[]]))  # Ausgabe: 2
print(berechne_tiefe([]))  # Ausgabe: 1
```

## Unit Tests
```python
import unittest
from main import berechne_tiefe

class TestBerechneTiefe(unittest.TestCase):
    def test_einfache_vr_welt(self):
        self.assertEqual(berechne_tiefe([[], [[], []], [[[]]], [[], [[], [[], []]]]]), 4)

    def test_mittlere_vr_welt(self):
        self.assertEqual(berechne_tiefe([[], [[], []], [[[]]]]), 3)

    def test_einfache_verschachtelung(self):
        self.assertEqual(berechne_tiefe([[]]), 2)

    def test_leere_vr_welt(self):
        self.assertEqual(berechne_tiefe([]), 1)

    def test_tief_verschachtelte_vr_welt(self):
        self.assertEqual(berechne_tiefe([[[[[[]]]]]]), 6)

    def test_ohne_verschachtelung(self):
        self.assertEqual(berechne_tiefe([1, 2, 3]), 1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 491
