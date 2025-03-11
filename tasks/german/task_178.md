# Input
- Programmierkonzept: Boolean und None;For-Schleifen;Operationen mit Zahlen
- Kontext: Virtuelle Realität

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Virtuelle Realität - Berechnung der Sichtbarkeit

In der virtuellen Realität ist es wichtig, die Sichtbarkeit von Objekten zu berechnen, um die Leistung zu optimieren. Schreibe eine Funktion `sichtbarkeit_berechnen(objekte)`, die eine Liste von Objekten erhält. Jedes Objekt ist durch eine Zahl repräsentiert, die die Entfernung des Objekts vom Betrachter angibt. 

Die Funktion soll die Anzahl der Objekte zurückgeben, die innerhalb einer bestimmten Sichtweite liegen. Die Sichtweite beträgt 100 Einheiten. Wenn die Liste leer ist, soll die Funktion `None` zurückgeben.

Beispielaufruf:
```python
objekte = [50, 150, 30, 200, 90]
sichtbarkeit_berechnen(objekte)
```
Erwartete Rückgabe:
```
3
```

### Anforderungen:
- Implementiere die Funktion `sichtbarkeit_berechnen(objekte)`.
- Die Funktion soll die Anzahl der Objekte innerhalb der Sichtweite von 100 Einheiten zurückgeben.
- Wenn die Liste leer ist, soll die Funktion `None` zurückgeben.

## Codegerüst
```python
def sichtbarkeit_berechnen(objekte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def sichtbarkeit_berechnen(objekte):
    if not objekte:
        return None
    return sum(1 for obj in objekte if obj <= 100)

objekte = [50, 150, 30, 200, 90]
print(sichtbarkeit_berechnen(objekte))
```

## Unit Tests
```python
import unittest
from main import sichtbarkeit_berechnen

class TestSichtbarkeitBerechnen(unittest.TestCase):
    def test_leere_liste(self):
        self.assertIsNone(sichtbarkeit_berechnen([]))

    def test_alle_objekte_in_sichtweite(self):
        self.assertEqual(sichtbarkeit_berechnen([10, 20, 30, 40, 50]), 5)

    def test_keine_objekte_in_sichtweite(self):
        self.assertEqual(sichtbarkeit_berechnen([110, 120, 130, 140, 150]), 0)

    def test_gemischte_objekte(self):
        self.assertEqual(sichtbarkeit_berechnen([50, 150, 30, 200, 90]), 3)

    def test_grenzwert_sichtweite(self):
        self.assertEqual(sichtbarkeit_berechnen([100, 101, 99, 102, 98]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 610
