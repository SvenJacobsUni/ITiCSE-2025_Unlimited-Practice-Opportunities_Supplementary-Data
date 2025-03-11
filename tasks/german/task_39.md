# Input
- Programmierkonzept: If-Else-Anweisungen
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Olympia-Medaillen

Schreibe eine Funktion namens `medaillen_auswertung(anzahl_gold, anzahl_silber, anzahl_bronze)`, die die Anzahl der gewonnenen Medaillen eines Landes bei den Olympischen Spielen auswertet und eine entsprechende Nachricht zurückgibt.

- Wenn das Land mindestens 10 Goldmedaillen gewonnen hat, soll die Nachricht "Hervorragende Leistung!" zurückgegeben werden.
- Wenn das Land mindestens 5 Goldmedaillen und mindestens 5 Silbermedaillen gewonnen hat, soll die Nachricht "Sehr gute Leistung!" zurückgegeben werden.
- Wenn das Land mindestens 3 Goldmedaillen, 3 Silbermedaillen und 3 Bronzemedaillen gewonnen hat, soll die Nachricht "Gute Leistung!" zurückgegeben werden.
- In allen anderen Fällen soll die Nachricht "Teilnahme ist alles!" zurückgegeben werden.

Beispielaufruf:
```python
print(medaillen_auswertung(12, 4, 3))  # Ausgabe: Hervorragende Leistung!
print(medaillen_auswertung(6, 5, 2))   # Ausgabe: Sehr gute Leistung!
print(medaillen_auswertung(3, 3, 3))   # Ausgabe: Gute Leistung!
print(medaillen_auswertung(1, 2, 1))   # Ausgabe: Teilnahme ist alles!
```

## Codegerüst
```python
def medaillen_auswertung(anzahl_gold, anzahl_silber, anzahl_bronze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def medaillen_auswertung(anzahl_gold, anzahl_silber, anzahl_bronze):
    if anzahl_gold >= 10:
        return "Hervorragende Leistung!"
    elif anzahl_gold >= 5 and anzahl_silber >= 5:
        return "Sehr gute Leistung!"
    elif anzahl_gold >= 3 and anzahl_silber >= 3 and anzahl_bronze >= 3:
        return "Gute Leistung!"
    else:
        return "Teilnahme ist alles!"

print(medaillen_auswertung(12, 4, 3))
print(medaillen_auswertung(6, 5, 2))
print(medaillen_auswertung(3, 3, 3))
print(medaillen_auswertung(1, 2, 1))
```

## Unit Tests
```python
import unittest
from main import medaillen_auswertung

class TestMedaillenAuswertung(unittest.TestCase):
    def test_hervorragende_leistung(self):
        self.assertEqual(medaillen_auswertung(12, 4, 3), "Hervorragende Leistung!")

    def test_sehr_gute_leistung(self):
        self.assertEqual(medaillen_auswertung(6, 5, 2), "Sehr gute Leistung!")

    def test_gute_leistung(self):
        self.assertEqual(medaillen_auswertung(3, 3, 3), "Gute Leistung!")

    def test_teilnahme_ist_alles(self):
        self.assertEqual(medaillen_auswertung(1, 2, 1), "Teilnahme ist alles!")

    def test_grenzfall_hervorragende_leistung(self):
        self.assertEqual(medaillen_auswertung(10, 0, 0), "Hervorragende Leistung!")

    def test_grenzfall_sehr_gute_leistung(self):
        self.assertEqual(medaillen_auswertung(5, 5, 0), "Sehr gute Leistung!")

    def test_grenzfall_gute_leistung(self):
        self.assertEqual(medaillen_auswertung(3, 3, 3), "Gute Leistung!")

    def test_grenzfall_teilnahme_ist_alles(self):
        self.assertEqual(medaillen_auswertung(2, 2, 2), "Teilnahme ist alles!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 457
