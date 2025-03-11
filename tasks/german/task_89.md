# Input
- Programmierkonzept: For-Schleifen
- Kontext: Restaurant

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Restaurant-Bestellungen

Schreibe eine Funktion namens `bestellungen_aufnehmen(bestellungen)`, die eine Liste von Bestellungen als Argument erhält. Jede Bestellung ist ein String, der den Namen eines Gerichts enthält. Die Funktion soll die Anzahl der Bestellungen für jedes Gericht zählen und das Ergebnis als Dictionary zurückgeben. 

Beispielaufruf:
```python
bestellungen = ["Pizza", "Burger", "Salat", "Pizza", "Burger", "Pizza"]
print(bestellungen_aufnehmen(bestellungen))
```

Erwartete Ausgabe:
```python
{'Pizza': 3, 'Burger': 2, 'Salat': 1}
```

## Codegerüst
```python
def bestellungen_aufnehmen(bestellungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bestellungen_aufnehmen(bestellungen):
    ergebnis = {}
    for gericht in bestellungen:
        if gericht in ergebnis:
            ergebnis[gericht] += 1
        else:
            ergebnis[gericht] = 1
    return ergebnis

bestellungen = ["Pizza", "Burger", "Salat", "Pizza", "Burger", "Pizza"]
print(bestellungen_aufnehmen(bestellungen))
```

## Unit Tests
```python
import unittest
from main import bestellungen_aufnehmen

class TestBestellungenAufnehmen(unittest.TestCase):
    def test_einfacher_fall(self):
        self.assertEqual(bestellungen_aufnehmen(["Pizza", "Burger", "Salat", "Pizza", "Burger", "Pizza"]), {'Pizza': 3, 'Burger': 2, 'Salat': 1})

    def test_leere_liste(self):
        self.assertEqual(bestellungen_aufnehmen([]), {})

    def test_einzelne_bestellung(self):
        self.assertEqual(bestellungen_aufnehmen(["Pizza"]), {'Pizza': 1})

    def test_mehrere_verschiedene_bestellungen(self):
        self.assertEqual(bestellungen_aufnehmen(["Pizza", "Burger", "Salat", "Nudeln", "Pizza", "Burger", "Pizza", "Nudeln"]), {'Pizza': 3, 'Burger': 2, 'Salat': 1, 'Nudeln': 2})

    def test_alle_gleichen_bestellungen(self):
        self.assertEqual(bestellungen_aufnehmen(["Pizza", "Pizza", "Pizza", "Pizza"]), {'Pizza': 4})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 507
