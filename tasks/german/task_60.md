# Input
- Programmierkonzept: Integer
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Zutaten für ein Rezept berechnen

Schreibe eine Funktion namens `zutaten_berechnen(anzahl_personen)`, die die benötigte Menge an Zutaten für ein Rezept berechnet. Das Rezept ist für 4 Personen ausgelegt und benötigt folgende Zutaten:

- 200 Gramm Mehl
- 100 Gramm Zucker
- 2 Eier

Die Funktion soll die Mengen der Zutaten entsprechend der Anzahl der Personen anpassen und eine Nachricht mit den berechneten Mengen zurückgeben. Beispielaufruf: `zutaten_berechnen(2)` gibt "Für 2 Personen benötigst du: 100 Gramm Mehl, 50 Gramm Zucker, 1 Ei." zurück.

## Codegerüst
```python
def zutaten_berechnen(anzahl_personen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zutaten_berechnen(anzahl_personen):
    mehl = 200 * anzahl_personen / 4
    zucker = 100 * anzahl_personen / 4
    eier = 2 * anzahl_personen / 4
    print(f"Für {anzahl_personen} Personen benötigst du: {mehl} Gramm Mehl, {zucker} Gramm Zucker, {eier} Eier.")

zutaten_berechnen(2)
```

## Unit Tests
```python
import unittest
from main import zutaten_berechnen

class TestZutatenBerechnen(unittest.TestCase):
    def test_zwei_personen(self):
        self.assertEqual(zutaten_berechnen(2), "Für 2 Personen benötigst du: 100 Gramm Mehl, 50 Gramm Zucker, 1 Ei.")

    def test_vier_personen(self):
        self.assertEqual(zutaten_berechnen(4), "Für 4 Personen benötigst du: 200 Gramm Mehl, 100 Gramm Zucker, 2 Eier.")

    def test_null_personen(self):
        self.assertEqual(zutaten_berechnen(0), "Für 0 Personen benötigst du: 0 Gramm Mehl, 0 Gramm Zucker, 0 Eier.")

    def test_acht_personen(self):
        self.assertEqual(zutaten_berechnen(8), "Für 8 Personen benötigst du: 400 Gramm Mehl, 200 Gramm Zucker, 4 Eier.")

    def test_negative_personen(self):
        self.assertEqual(zutaten_berechnen(-2), "Für -2 Personen benötigst du: -100 Gramm Mehl, -50 Gramm Zucker, -1 Ei.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 478
