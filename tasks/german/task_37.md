# Input
- Programmierkonzept: Operationen mit Zahlen
- Kontext: Restaurant

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Restaurantrechnung berechnen

Schreibe eine Funktion namens `berechne_rechnung(preise, trinkgeld_prozent)`, die die Gesamtrechnung für ein Restaurant berechnet. Die Funktion soll eine Liste von Preisen (`preise`) und einen Prozentsatz für das Trinkgeld (`trinkgeld_prozent`) als Argumente erhalten. Die Funktion soll die Gesamtsumme der Preise berechnen, das Trinkgeld basierend auf dem Prozentsatz hinzufügen und die Gesamtrechnung zurückgeben.

Beispielaufruf:
```python
preise = [10.50, 20.75, 8.99]
trinkgeld_prozent = 15
print(berechne_rechnung(preise, trinkgeld_prozent))  # Erwartete Ausgabe: 45.29
```

In diesem Beispiel sind die Preise der bestellten Gerichte 10.50, 20.75 und 8.99. Das Trinkgeld beträgt 15% der Gesamtsumme der Preise. Die Funktion soll die Gesamtrechnung berechnen und zurückgeben.

## Codegerüst
```python
def berechne_rechnung(preise, trinkgeld_prozent):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_rechnung(preise, trinkgeld_prozent):
    gesamt = sum(preise)
    trinkgeld = gesamt * (trinkgeld_prozent / 100)
    return round(gesamt + trinkgeld, 2)

preise = [10.50, 20.75, 8.99]
trinkgeld_prozent = 15
print(berechne_rechnung(preise, trinkgeld_prozent))
```

## Unit Tests
```python
import unittest
from main import berechne_rechnung

class TestBerechneRechnung(unittest.TestCase):
    def test_einfache_rechnung(self):
        preise = [10.50, 20.75, 8.99]
        trinkgeld_prozent = 15
        self.assertEqual(berechne_rechnung(preise, trinkgeld_prozent), 45.29)

    def test_keine_preise(self):
        preise = []
        trinkgeld_prozent = 15
        self.assertEqual(berechne_rechnung(preise, trinkgeld_prozent), 0.00)

    def test_kein_trinkgeld(self):
        preise = [10.50, 20.75, 8.99]
        trinkgeld_prozent = 0
        self.assertEqual(berechne_rechnung(preise, trinkgeld_prozent), 40.24)

    def test_hohes_trinkgeld(self):
        preise = [10.50, 20.75, 8.99]
        trinkgeld_prozent = 100
        self.assertEqual(berechne_rechnung(preise, trinkgeld_prozent), 80.48)

    def test_rundung(self):
        preise = [10.333, 20.666, 8.999]
        trinkgeld_prozent = 10
        self.assertEqual(berechne_rechnung(preise, trinkgeld_prozent), 43.22)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 455
