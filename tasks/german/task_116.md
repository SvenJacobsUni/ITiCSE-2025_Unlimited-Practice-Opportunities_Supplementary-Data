# Input
- Programmierkonzept: If-Else-Anweisungen;Operationen mit Zahlen
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Modernes Gaming - Spielerlevel

Schreibe eine Funktion namens `spieler_level(punkte)`, die das Level eines Spielers basierend auf seiner Punktzahl bestimmt. Die Funktion soll eine Nachricht mit 'return' zurückgeben, die das Level des Spielers angibt.

Die Level sind wie folgt definiert:
- Weniger als 1000 Punkte: "Anfänger"
- 1000 bis 4999 Punkte: "Fortgeschrittener"
- 5000 bis 9999 Punkte: "Profi"
- 10000 oder mehr Punkte: "Legende"

Beispielaufrufe:
- `spieler_level(750)` gibt "Anfänger" zurück.
- `spieler_level(3200)` gibt "Fortgeschrittener" zurück.
- `spieler_level(7500)` gibt "Profi" zurück.
- `spieler_level(12000)` gibt "Legende" zurück.

## Codegerüst
```python
def spieler_level(punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spieler_level(punkte):
    if punkte < 1000:
        return "Anfänger"
    elif punkte < 5000:
        return "Fortgeschrittener"
    elif punkte < 10000:
        return "Profi"
    else:
        return "Legende"

# Beispielaufrufe
print(spieler_level(750))    # Anfänger
print(spieler_level(3200))   # Fortgeschrittener
print(spieler_level(7500))   # Profi
print(spieler_level(12000))  # Legende
```

## Unit Tests
```python
import unittest
from main import spieler_level

class TestSpielerLevel(unittest.TestCase):
    def test_anfaenger(self):
        self.assertEqual(spieler_level(750), "Anfänger")

    def test_fortgeschrittener(self):
        self.assertEqual(spieler_level(3200), "Fortgeschrittener")

    def test_profi(self):
        self.assertEqual(spieler_level(7500), "Profi")

    def test_legende(self):
        self.assertEqual(spieler_level(12000), "Legende")

    def test_grenze_anfaenger_fortgeschrittener(self):
        self.assertEqual(spieler_level(1000), "Fortgeschrittener")

    def test_grenze_fortgeschrittener_profi(self):
        self.assertEqual(spieler_level(5000), "Profi")

    def test_grenze_profi_legende(self):
        self.assertEqual(spieler_level(10000), "Legende")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 548
