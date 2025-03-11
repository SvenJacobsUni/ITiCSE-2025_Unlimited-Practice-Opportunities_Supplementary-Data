# Input
- Programmierkonzept: Listen
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustierliste

Schreibe eine Funktion namens `haustier_liste(haustiere)`, die eine Liste von Haustiernamen als Argument erhält. Die Funktion soll die Anzahl der Haustiere in der Liste zählen und eine Nachricht zurückgeben, die die Anzahl der Haustiere angibt. Wenn die Liste leer ist, soll die Nachricht "Keine Haustiere gefunden." zurückgegeben werden.

Beispielaufrufe:

- `haustier_liste(["Bella", "Charlie", "Luna"])` gibt "Du hast 3 Haustiere." zurück.
- `haustier_liste([])` gibt "Keine Haustiere gefunden." zurück.

## Codegerüst
```python
def haustier_liste(haustiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def haustier_liste(haustiere):
    if not haustiere:
        print("Keine Haustiere gefunden.")
    else:
        print(f"Du hast {len(haustiere)} Haustiere.")

haustier_liste(["Bella", "Charlie", "Luna"])
haustier_liste([])
```

## Unit Tests
```python
import unittest
from main import haustier_liste

class TestHaustierListe(unittest.TestCase):
    def test_mehrere_haustiere(self):
        self.assertEqual(haustier_liste(["Bella", "Charlie", "Luna"]), "Du hast 3 Haustiere.")

    def test_keine_haustiere(self):
        self.assertEqual(haustier_liste([]), "Keine Haustiere gefunden.")

    def test_ein_haustier(self):
        self.assertEqual(haustier_liste(["Bella"]), "Du hast 1 Haustier.")

    def test_zwei_haustiere(self):
        self.assertEqual(haustier_liste(["Bella", "Charlie"]), "Du hast 2 Haustiere.")

    def test_viele_haustiere(self):
        self.assertEqual(haustier_liste(["Bella", "Charlie", "Luna", "Max", "Lucy", "Daisy", "Bailey", "Molly", "Coco", "Buddy"]), "Du hast 10 Haustiere.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 433
