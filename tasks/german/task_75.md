# Input
- Programmierkonzept: Integer
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustiere zählen

Schreibe eine Funktion namens `zaehle_haustiere(hunde, katzen)`, die zwei Integer-Parameter entgegennimmt: die Anzahl der Hunde und die Anzahl der Katzen in einem Haushalt. Die Funktion soll die Gesamtanzahl der Haustiere berechnen und zurückgeben.

Beispielaufruf:
```python
gesamt = zaehle_haustiere(3, 2)
print(gesamt)  # Ausgabe: 5
```

In diesem Beispiel gibt es 3 Hunde und 2 Katzen, was insgesamt 5 Haustiere ergibt.

## Codegerüst
```python
def zaehle_haustiere(hunde, katzen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_haustiere(hunde, katzen):
    return hunde + katzen

print(zaehle_haustiere(3, 2))  # Ausgabe: 5
```

## Unit Tests
```python
import unittest
from main import zaehle_haustiere

class TestZaehleHaustiere(unittest.TestCase):
    def test_keine_haustiere(self):
        self.assertEqual(zaehle_haustiere(0, 0), 0)

    def test_nur_hunde(self):
        self.assertEqual(zaehle_haustiere(5, 0), 5)

    def test_nur_katzen(self):
        self.assertEqual(zaehle_haustiere(0, 3), 3)

    def test_hunde_und_katzen(self):
        self.assertEqual(zaehle_haustiere(2, 4), 6)

    def test_grosse_zahlen(self):
        self.assertEqual(zaehle_haustiere(1000, 2000), 3000)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 493
