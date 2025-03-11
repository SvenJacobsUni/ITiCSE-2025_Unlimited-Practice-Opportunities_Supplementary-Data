# Input
- Programmierkonzept: Integer
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Streaming-Dienste und Integer

Schreibe eine Funktion namens `berechne_monatliche_kosten(abonnements)`, die eine Liste von Integern als Argument erhält. Jeder Integer in der Liste repräsentiert die monatlichen Kosten eines Abonnements bei verschiedenen Streaming-Diensten in Euro. Die Funktion soll die Gesamtkosten aller Abonnements berechnen und zurückgeben.

Beispielaufruf:
```python
abonnements = [10, 15, 8, 12]
print(berechne_monatliche_kosten(abonnements))  # Ausgabe: 45
```

## Codegerüst
```python
def berechne_monatliche_kosten(abonnements):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_monatliche_kosten(abonnements):
    return sum(abonnements)

abonnements = [10, 15, 8, 12]
print(berechne_monatliche_kosten(abonnements))
```

## Unit Tests
```python
import unittest
from main import berechne_monatliche_kosten

class TestBerechneMonatlicheKosten(unittest.TestCase):
    def test_mehrere_abonnements(self):
        self.assertEqual(berechne_monatliche_kosten([10, 15, 8, 12]), 45)

    def test_keine_abonnements(self):
        self.assertEqual(berechne_monatliche_kosten([]), 0)

    def test_ein_abonnement(self):
        self.assertEqual(berechne_monatliche_kosten([20]), 20)

    def test_gemischte_abonnements(self):
        self.assertEqual(berechne_monatliche_kosten([5, 10, 15, 20, 25]), 75)

    def test_negativer_wert(self):
        self.assertEqual(berechne_monatliche_kosten([10, -5, 15]), 20)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 489
