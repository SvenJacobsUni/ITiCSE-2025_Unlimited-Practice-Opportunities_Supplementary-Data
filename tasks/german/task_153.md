# Input
- Programmierkonzept: For-Schleifen;If-Else-Anweisungen;Operationen mit Zahlen
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustierfutter-Berechnung

Schreibe eine Funktion namens `berechne_futterbedarf(haustiere)`, die eine Liste von Haustieren und deren Gewichten (in Kilogramm) als Argument erhält. Die Funktion soll den täglichen Futterbedarf für jedes Haustier berechnen und eine Liste mit den Ergebnissen zurückgeben. 

Der tägliche Futterbedarf wird wie folgt berechnet:
- Für Hunde: 5% des Körpergewichts
- Für Katzen: 3% des Körpergewichts
- Für andere Haustiere: 2% des Körpergewichts

Die Liste der Haustiere wird als Liste von Tupeln übergeben, wobei jedes Tupel den Namen des Haustiers und sein Gewicht enthält. Beispiel: `[("Hund", 20), ("Katze", 5), ("Hamster", 0.5)]`

Beispielaufruf:
```python
haustiere = [("Hund", 20), ("Katze", 5), ("Hamster", 0.5)]
print(berechne_futterbedarf(haustiere))
```

Erwartete Ausgabe:
```python
[1.0, 0.15, 0.01]
```

## Codegerüst
```python
def berechne_futterbedarf(haustiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_futterbedarf(haustiere):
    return [gewicht * (0.05 if tier == "Hund" else 0.03 if tier == "Katze" else 0.02) for tier, gewicht in haustiere]

haustiere = [("Hund", 20), ("Katze", 5), ("Hamster", 0.5)]
print(berechne_futterbedarf(haustiere))
```

## Unit Tests
```python
import unittest
from main import berechne_futterbedarf

class TestBerechneFutterbedarf(unittest.TestCase):
    def test_hunde_und_katzen(self):
        self.assertEqual(berechne_futterbedarf([("Hund", 20), ("Katze", 5)]), [1.0, 0.15])

    def test_hamster(self):
        self.assertEqual(berechne_futterbedarf([("Hamster", 0.5)]), [0.01])

    def test_gemischte_haustiere(self):
        self.assertEqual(berechne_futterbedarf([("Hund", 20), ("Katze", 5), ("Hamster", 0.5)]), [1.0, 0.15, 0.01])

    def test_leere_liste(self):
        self.assertEqual(berechne_futterbedarf([]), [])

    def test_unbekanntes_haustier(self):
        self.assertEqual(berechne_futterbedarf([("Papagei", 1)]), [0.02])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 585
