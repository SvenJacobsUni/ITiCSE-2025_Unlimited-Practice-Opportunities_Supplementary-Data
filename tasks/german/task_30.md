# Input
- Programmierkonzept: Listen
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Zutatenliste für ein Rezept

Schreibe eine Funktion namens `zutaten_hinzufuegen(zutatenliste, neue_zutat)`, die eine Liste von Zutaten und eine neue Zutat als Parameter erhält. Die Funktion soll die neue Zutat zur Zutatenliste hinzufügen und die aktualisierte Liste zurückgeben.

Beispielaufruf:
```python
zutaten = ["Mehl", "Zucker", "Eier"]
neue_zutat = "Milch"
print(zutaten_hinzufuegen(zutaten, neue_zutat))
```

Erwartete Ausgabe:
```
["Mehl", "Zucker", "Eier", "Milch"]
```

## Codegerüst
```python
def zutaten_hinzufuegen(zutatenliste, neue_zutat):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zutaten_hinzufuegen(zutatenliste, neue_zutat):
    zutatenliste.append(neue_zutat)
    return zutatenliste

zutaten = ["Mehl", "Zucker", "Eier"]
neue_zutat = "Milch"
print(zutaten_hinzufuegen(zutaten, neue_zutat))
```

## Unit Tests
```python
import unittest
from main import zutaten_hinzufuegen

class TestZutatenHinzufuegen(unittest.TestCase):
    def test_einfache_zutat(self):
        self.assertEqual(zutaten_hinzufuegen(["Mehl", "Zucker", "Eier"], "Milch"), ["Mehl", "Zucker", "Eier", "Milch"])

    def test_leere_liste(self):
        self.assertEqual(zutaten_hinzufuegen([], "Milch"), ["Milch"])

    def test_mehrere_zutaten(self):
        self.assertEqual(zutaten_hinzufuegen(["Mehl"], "Zucker"), ["Mehl", "Zucker"])

    def test_doppelte_zutat(self):
        self.assertEqual(zutaten_hinzufuegen(["Mehl", "Zucker", "Eier"], "Zucker"), ["Mehl", "Zucker", "Eier", "Zucker"])

    def test_zutat_als_zahl(self):
        self.assertEqual(zutaten_hinzufuegen(["Mehl", "Zucker", "Eier"], 123), ["Mehl", "Zucker", "Eier", 123])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 448
