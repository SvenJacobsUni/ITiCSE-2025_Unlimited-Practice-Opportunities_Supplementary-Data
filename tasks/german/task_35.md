# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Olympia-Medaillenvergleich

Schreibe eine Funktion namens `vergleiche_medaillen(land1_gold, land1_silber, land1_bronze, land2_gold, land2_silber, land2_bronze)`, die die Anzahl der gewonnenen Medaillen von zwei Ländern bei den Olympischen Spielen vergleicht und eine entsprechende Nachricht zurückgibt.

Die Funktion soll die Anzahl der Gold-, Silber- und Bronzemedaillen der beiden Länder als Argumente entgegennehmen und folgende Vergleiche durchführen:

1. Wenn ein Land mehr Goldmedaillen hat als das andere, soll die Funktion eine Nachricht zurückgeben, die besagt, welches Land mehr Goldmedaillen gewonnen hat.
2. Wenn beide Länder gleich viele Goldmedaillen haben, soll die Funktion die Anzahl der Silbermedaillen vergleichen und eine entsprechende Nachricht zurückgeben.
3. Wenn auch die Anzahl der Silbermedaillen gleich ist, soll die Funktion die Anzahl der Bronzemedaillen vergleichen und eine entsprechende Nachricht zurückgeben.
4. Wenn beide Länder in allen Medaillenkategorien gleich viele Medaillen haben, soll die Funktion eine Nachricht zurückgeben, die besagt, dass beide Länder gleich viele Medaillen gewonnen haben.

Beispielaufruf:
```python
vergleiche_medaillen(10, 5, 3, 8, 7, 2)
```

Erwartete Ausgabe:
```
Land 1 hat mehr Goldmedaillen gewonnen.
```

## Codegerüst
```python
def vergleiche_medaillen(land1_gold, land1_silber, land1_bronze, land2_gold, land2_silber, land2_bronze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def vergleiche_medaillen(land1_gold, land1_silber, land1_bronze, land2_gold, land2_silber, land2_bronze):
    if land1_gold > land2_gold:
        print("Land 1 hat mehr Goldmedaillen gewonnen.")
    elif land1_gold < land2_gold:
        print("Land 2 hat mehr Goldmedaillen gewonnen.")
    elif land1_silber > land2_silber:
        print("Land 1 hat mehr Silbermedaillen gewonnen.")
    elif land1_silber < land2_silber:
        print("Land 2 hat mehr Silbermedaillen gewonnen.")
    elif land1_bronze > land2_bronze:
        print("Land 1 hat mehr Bronzemedaillen gewonnen.")
    elif land1_bronze < land2_bronze:
        print("Land 2 hat mehr Bronzemedaillen gewonnen.")
    else:
        print("Beide Länder haben gleich viele Medaillen gewonnen.")

vergleiche_medaillen(10, 5, 3, 8, 7, 2)
```

## Unit Tests
```python
import unittest

from main import vergleiche_medaillen

class TestVergleicheMedaillen(unittest.TestCase):
    def test_land1_mehr_gold(self):
        self.assertEqual(vergleiche_medaillen(10, 5, 3, 8, 7, 2), "Land 1 hat mehr Goldmedaillen gewonnen.")

    def test_land2_mehr_gold(self):
        self.assertEqual(vergleiche_medaillen(8, 5, 3, 10, 7, 2), "Land 2 hat mehr Goldmedaillen gewonnen.")

    def test_land1_mehr_silber(self):
        self.assertEqual(vergleiche_medaillen(10, 7, 3, 10, 5, 2), "Land 1 hat mehr Silbermedaillen gewonnen.")

    def test_land2_mehr_silber(self):
        self.assertEqual(vergleiche_medaillen(10, 5, 3, 10, 7, 2), "Land 2 hat mehr Silbermedaillen gewonnen.")

    def test_land1_mehr_bronze(self):
        self.assertEqual(vergleiche_medaillen(10, 5, 4, 10, 5, 3), "Land 1 hat mehr Bronzemedaillen gewonnen.")

    def test_land2_mehr_bronze(self):
        self.assertEqual(vergleiche_medaillen(10, 5, 3, 10, 5, 4), "Land 2 hat mehr Bronzemedaillen gewonnen.")

    def test_gleich_viele_medaillen(self):
        self.assertEqual(vergleiche_medaillen(10, 5, 3, 10, 5, 3), "Beide Länder haben gleich viele Medaillen gewonnen.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 453
