# Input
- Programmierkonzept: Listen
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Zutatenliste für ein Rezept

Schreibe eine Funktion namens `zutaten_hinzufuegen(zutaten_liste, neue_zutat)`, die eine Liste von Zutaten und eine neue Zutat als Parameter erhält. Die Funktion soll die neue Zutat zur Zutatenliste hinzufügen und die aktualisierte Liste zurückgeben.

Beispielaufruf:
```python
zutaten = ["Mehl", "Zucker", "Eier"]
neue_zutat = "Milch"
aktualisierte_liste = zutaten_hinzufuegen(zutaten, neue_zutat)
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Zucker", "Eier", "Milch"]
```

Erstelle außerdem eine Funktion `zutaten_entfernen(zutaten_liste, zu_entfernende_zutat)`, die eine Liste von Zutaten und eine zu entfernende Zutat als Parameter erhält. Die Funktion soll die zu entfernende Zutat aus der Zutatenliste entfernen und die aktualisierte Liste zurückgeben.

Beispielaufruf:
```python
zutaten = ["Mehl", "Zucker", "Eier", "Milch"]
zu_entfernende_zutat = "Zucker"
aktualisierte_liste = zutaten_entfernen(zutaten, zu_entfernende_zutat)
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Eier", "Milch"]
```

Implementiere beide Funktionen in Python.

## Codegerüst
```python
def zutaten_hinzufuegen(zutaten_liste, neue_zutat):
    ## Hier Code einfügen

def zutaten_entfernen(zutaten_liste, zu_entfernende_zutat):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zutaten_hinzufuegen(zutaten_liste, neue_zutat):
    zutaten_liste.append(neue_zutat)
    return zutaten_liste

def zutaten_entfernen(zutaten_liste, zu_entfernende_zutat):
    zutaten_liste.remove(zu_entfernende_zutat)
    return zutaten_liste

# Beispielaufrufe
zutaten = ["Mehl", "Zucker", "Eier"]
neue_zutat = "Milch"
aktualisierte_liste = zutaten_hinzufuegen(zutaten, neue_zutat)
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Zucker", "Eier", "Milch"]

zutaten = ["Mehl", "Zucker", "Eier", "Milch"]
zu_entfernende_zutat = "Zucker"
aktualisierte_liste = zutaten_entfernen(zutaten, zu_entfernende_zutat)
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Eier", "Milch"]
```

## Unit Tests
```python
import unittest
from main import zutaten_hinzufuegen, zutaten_entfernen

class TestZutaten(unittest.TestCase):
    def test_zutaten_hinzufuegen_einfach(self):
        self.assertEqual(zutaten_hinzufuegen(["Mehl", "Zucker", "Eier"], "Milch"), ["Mehl", "Zucker", "Eier", "Milch"])

    def test_zutaten_hinzufuegen_leere_liste(self):
        self.assertEqual(zutaten_hinzufuegen([], "Milch"), ["Milch"])

    def test_zutaten_hinzufuegen_doppelt(self):
        self.assertEqual(zutaten_hinzufuegen(["Mehl", "Zucker", "Eier", "Milch"], "Milch"), ["Mehl", "Zucker", "Eier", "Milch", "Milch"])

    def test_zutaten_entfernen_einfach(self):
        self.assertEqual(zutaten_entfernen(["Mehl", "Zucker", "Eier", "Milch"], "Zucker"), ["Mehl", "Eier", "Milch"])

    def test_zutaten_entfernen_letztes_element(self):
        self.assertEqual(zutaten_entfernen(["Mehl", "Zucker", "Eier", "Milch"], "Milch"), ["Mehl", "Zucker", "Eier"])

    def test_zutaten_entfernen_nicht_vorhanden(self):
        with self.assertRaises(ValueError):
            zutaten_entfernen(["Mehl", "Zucker", "Eier"], "Milch")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 449
