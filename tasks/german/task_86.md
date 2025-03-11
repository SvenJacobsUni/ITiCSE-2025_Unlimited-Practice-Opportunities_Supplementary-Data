# Input
- Programmierkonzept: While-Schleifen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Angeln mit While-Schleifen

Schreibe eine Funktion namens `angeln()`, die simuliert, wie oft ein Angler einen Fisch fängt, bis er genug Fische für ein Abendessen hat. Der Angler benötigt mindestens 5 Fische. 

Die Funktion soll eine While-Schleife verwenden, um den Fangprozess zu simulieren. Bei jedem Durchlauf der Schleife soll die Anzahl der gefangenen Fische um 1 erhöht werden. Sobald der Angler 5 oder mehr Fische gefangen hat, soll die Schleife beendet werden und die Funktion die Gesamtzahl der gefangenen Fische zurückgeben.

Beispielaufruf: `angeln()` könnte `5` zurückgeben, wenn der Angler genau 5 Fische gefangen hat.

## Codegerüst
```python
def angeln():
    ## Hier Code einfügen
```

## Musterlösung
```python
def angeln():
    fische = 0
    while fische < 5:
        fische += 1
    print(fische)

angeln()
```

## Unit Tests
```python
import unittest
from main import angeln

class TestAngeln(unittest.TestCase):
    def test_genug_fische(self):
        self.assertEqual(angeln(), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 504
