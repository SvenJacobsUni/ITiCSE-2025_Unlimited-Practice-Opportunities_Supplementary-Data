# Input
- Programmierkonzept: While-Schleifen;Funktionen höherer Ordnung
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Kochrezept-Zähler

Schreibe eine Funktion namens `zaehle_zutaten(rezept, kriterium)`, die eine Liste von Zutaten (`rezept`) und eine Funktion (`kriterium`) als Parameter erhält. Die Funktion soll die Anzahl der Zutaten im Rezept zählen, die das Kriterium erfüllen. Verwende eine `while`-Schleife, um durch die Zutatenliste zu iterieren.

Beispielaufruf:
```python
def ist_gemuese(zutat):
    gemuese = ["Karotte", "Tomate", "Gurke", "Paprika"]
    return zutat in gemuese

rezept = ["Karotte", "Hähnchen", "Tomate", "Reis", "Paprika"]
print(zaehle_zutaten(rezept, ist_gemuese))  # Ausgabe: 3
```

In diesem Beispiel wird die Funktion `ist_gemuese` als Kriterium verwendet, um die Anzahl der Gemüsezutaten im Rezept zu zählen.

## Codegerüst
```python
def zaehle_zutaten(rezept, kriterium):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_zutaten(rezept, kriterium):
    count, i = 0, 0
    while i < len(rezept):
        if kriterium(rezept[i]):
            count += 1
        i += 1
    return count

def ist_gemuese(zutat):
    gemuese = ["Karotte", "Tomate", "Gurke", "Paprika"]
    return zutat in gemuese

rezept = ["Karotte", "Hähnchen", "Tomate", "Reis", "Paprika"]
print(zaehle_zutaten(rezept, ist_gemuese))  # Ausgabe: 3
```

## Unit Tests
```python
import unittest

from main import zaehle_zutaten

def ist_gemuese(zutat):
    gemuese = ["Karotte", "Tomate", "Gurke", "Paprika"]
    return zutat in gemuese

def ist_fleisch(zutat):
    fleisch = ["Hähnchen", "Rind", "Schwein"]
    return zutat in fleisch

class TestZaehleZutaten(unittest.TestCase):
    def test_gemuese(self):
        rezept = ["Karotte", "Hähnchen", "Tomate", "Reis", "Paprika"]
        self.assertEqual(zaehle_zutaten(rezept, ist_gemuese), 3)

    def test_fleisch(self):
        rezept = ["Karotte", "Hähnchen", "Tomate", "Reis", "Paprika"]
        self.assertEqual(zaehle_zutaten(rezept, ist_fleisch), 1)

    def test_leeres_rezept(self):
        rezept = []
        self.assertEqual(zaehle_zutaten(rezept, ist_gemuese), 0)

    def test_kein_kriterium_erfuellt(self):
        rezept = ["Reis", "Nudeln", "Kartoffeln"]
        self.assertEqual(zaehle_zutaten(rezept, ist_gemuese), 0)

    def test_alle_kriterien_erfuellt(self):
        rezept = ["Karotte", "Tomate", "Gurke", "Paprika"]
        self.assertEqual(zaehle_zutaten(rezept, ist_gemuese), 4)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 546
