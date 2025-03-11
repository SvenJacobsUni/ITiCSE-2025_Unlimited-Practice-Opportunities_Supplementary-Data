# Input
- Programmierkonzept: Rekursion
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Zubereitung von Pfannkuchen

Schreibe eine rekursive Funktion namens `pfannkuchen_zubereiten(anzahl)`, die die Zubereitung von Pfannkuchen simuliert. Die Funktion soll für jeden Pfannkuchen eine Nachricht ausgeben, dass ein Pfannkuchen zubereitet wird, und dann die Funktion für den nächsten Pfannkuchen aufrufen, bis keine Pfannkuchen mehr übrig sind.

Beispielaufruf: `pfannkuchen_zubereiten(3)` sollte folgende Ausgaben erzeugen:
```
Pfannkuchen 1 wird zubereitet.
Pfannkuchen 2 wird zubereitet.
Pfannkuchen 3 wird zubereitet.
```

Implementiere die Funktion so, dass sie die Anzahl der Pfannkuchen als Argument erhält und rekursiv arbeitet.

## Codegerüst
```python
def pfannkuchen_zubereiten(anzahl):
    ## Hier Code einfügen
```

## Musterlösung
```python
def pfannkuchen_zubereiten(anzahl, aktueller=1):
    if aktueller > anzahl:
        return
    print(f'Pfannkuchen {aktueller} wird zubereitet.')
    pfannkuchen_zubereiten(anzahl, aktueller + 1)

pfannkuchen_zubereiten(3)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import pfannkuchen_zubereiten

class TestPfannkuchenZubereiten(unittest.TestCase):
    def test_drei_pfannkuchen(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        pfannkuchen_zubereiten(3)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pfannkuchen 1 wird zubereitet.\nPfannkuchen 2 wird zubereitet.\nPfannkuchen 3 wird zubereitet.")

    def test_keine_pfannkuchen(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        pfannkuchen_zubereiten(0)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

    def test_ein_pfannkuchen(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        pfannkuchen_zubereiten(1)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pfannkuchen 1 wird zubereitet.")

    def test_fuenf_pfannkuchen(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        pfannkuchen_zubereiten(5)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Pfannkuchen 1 wird zubereitet.\nPfannkuchen 2 wird zubereitet.\nPfannkuchen 3 wird zubereitet.\nPfannkuchen 4 wird zubereitet.\nPfannkuchen 5 wird zubereitet.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 477
