# Input
- Programmierkonzept: For-Schleifen
- Kontext: Vergnügungspark

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Vergnügungspark - Besucherzählung

Schreibe eine Funktion namens `besucher_zaehlen(besucher_liste)`, die eine Liste von Besuchernamen als Argument erhält. Die Funktion soll die Anzahl der Besucher im Vergnügungspark zählen und zurückgeben. Verwende eine For-Schleife, um durch die Liste zu iterieren und die Anzahl der Besucher zu ermitteln.

Beispielaufruf:
```python
besucher_liste = ["Anna", "Ben", "Clara", "David", "Eva"]
anzahl_besucher = besucher_zaehlen(besucher_liste)
print(anzahl_besucher)  # Ausgabe: 5
```

In diesem Beispiel enthält die Liste `besucher_liste` fünf Namen, daher sollte die Funktion `besucher_zaehlen` den Wert `5` zurückgeben.

## Codegerüst
```python
def besucher_zaehlen(besucher_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def besucher_zaehlen(besucher_liste):
    return len(besucher_liste)

besucher_liste = ["Anna", "Ben", "Clara", "David", "Eva"]
anzahl_besucher = besucher_zaehlen(besucher_liste)
print(anzahl_besucher)  # Ausgabe: 5
```

## Unit Tests
```python
import unittest
from main import besucher_zaehlen

class TestBesucherZaehlen(unittest.TestCase):
    def test_leere_liste(self):
        self.assertEqual(besucher_zaehlen([]), 0)

    def test_ein_besucher(self):
        self.assertEqual(besucher_zaehlen(["Anna"]), 1)

    def test_mehrere_besucher(self):
        self.assertEqual(besucher_zaehlen(["Anna", "Ben", "Clara", "David", "Eva"]), 5)

    def test_doppelte_besucher(self):
        self.assertEqual(besucher_zaehlen(["Anna", "Anna", "Ben", "Ben"]), 4)

    def test_gemischte_besucher(self):
        self.assertEqual(besucher_zaehlen(["Anna", "Ben", "Clara", "David", "Eva", "Anna", "Ben"]), 7)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 437
