# Input
- Programmierkonzept: Rekursion;Funktionen höherer Ordnung;Operationen mit Zahlen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Fische zählen

Du bist ein begeisterter Angler und möchtest eine Funktion schreiben, die dir hilft, die Anzahl der Fische in einem See zu zählen. Dabei soll die Funktion rekursiv arbeiten und Funktionen höherer Ordnung verwenden.

Schreibe eine Funktion `zaehle_fische(see)`, die die Anzahl der Fische in einem See zählt. Der See wird als Liste von Listen dargestellt, wobei jede innere Liste eine Gruppe von Fischen repräsentiert. Jeder Fisch wird durch eine Zahl dargestellt, die sein Gewicht in Gramm angibt.

Die Funktion `zaehle_fische(see)` soll die Gesamtanzahl der Fische im See zurückgeben.

Beispiel:

```python
see = [
    [200, 150, 300],  # Gruppe 1
    [100, 250],       # Gruppe 2
    [400, 500, 100]   # Gruppe 3
]

print(zaehle_fische(see))  # Ausgabe: 8
```

In diesem Beispiel gibt es insgesamt 8 Fische im See.

## Codegerüst
```python
def zaehle_fische(see):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(see):
    return sum(map(len, see))

see = [
    [200, 150, 300],
    [100, 250],
    [400, 500, 100]
]

print(zaehle_fische(see))
```

## Unit Tests
```python
import unittest

from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_einfacher_see(self):
        self.assertEqual(zaehle_fische([[200, 150, 300], [100, 250], [400, 500, 100]]), 8)

    def test_leerer_see(self):
        self.assertEqual(zaehle_fische([]), 0)

    def test_see_mit_einer_gruppe(self):
        self.assertEqual(zaehle_fische([[200, 150, 300]]), 3)

    def test_see_mit_leerer_gruppe(self):
        self.assertEqual(zaehle_fische([[200, 150, 300], [], [400, 500, 100]]), 6)

    def test_see_mit_vielen_gruppen(self):
        self.assertEqual(zaehle_fische([[200], [150], [300], [100], [250], [400], [500], [100]]), 8)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 619
