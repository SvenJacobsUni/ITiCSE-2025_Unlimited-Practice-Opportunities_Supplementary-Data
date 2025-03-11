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
aktualisierte_liste = zutaten_hinzufuegen(zutaten, "Milch")
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Zucker", "Eier", "Milch"]
```

### Zusätzliche Aufgabe: Zutaten entfernen

Erweitere die Funktion um die Möglichkeit, eine Zutat aus der Liste zu entfernen. Schreibe eine Funktion namens `zutaten_entfernen(zutaten_liste, entferne_zutat)`, die eine Liste von Zutaten und eine zu entfernende Zutat als Parameter erhält. Die Funktion soll die Zutat aus der Liste entfernen und die aktualisierte Liste zurückgeben.

Beispielaufruf:
```python
zutaten = ["Mehl", "Zucker", "Eier", "Milch"]
aktualisierte_liste = zutaten_entfernen(zutaten, "Zucker")
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Eier", "Milch"]
```

## Codegerüst
```python
def zutaten_hinzufuegen(zutaten_liste, neue_zutat):
    ## Hier Code einfügen

def zutaten_entfernen(zutaten_liste, entferne_zutat):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zutaten_hinzufuegen(zutaten_liste, neue_zutat):
    zutaten_liste.append(neue_zutat)
    return zutaten_liste

def zutaten_entfernen(zutaten_liste, entferne_zutat):
    if entferne_zutat in zutaten_liste:
        zutaten_liste.remove(entferne_zutat)
    return zutaten_liste

# Beispielaufrufe
zutaten = ["Mehl", "Zucker", "Eier"]
aktualisierte_liste = zutaten_hinzufuegen(zutaten, "Milch")
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Zucker", "Eier", "Milch"]

aktualisierte_liste = zutaten_entfernen(zutaten, "Zucker")
print(aktualisierte_liste)  # Ausgabe: ["Mehl", "Eier", "Milch"]
```

## Unit Tests
```python
import unittest
from main import zutaten_hinzufuegen, zutaten_entfernen

class TestZutaten(unittest.TestCase):
    def test_zutat_hinzufuegen(self):
        self.assertEqual(zutaten_hinzufuegen(["Mehl", "Zucker", "Eier"], "Milch"), ["Mehl", "Zucker", "Eier", "Milch"])

    def test_zutat_entfernen(self):
        self.assertEqual(zutaten_entfernen(["Mehl", "Zucker", "Eier", "Milch"], "Zucker"), ["Mehl", "Eier", "Milch"])

    def test_zutat_hinzufuegen_leere_liste(self):
        self.assertEqual(zutaten_hinzufuegen([], "Milch"), ["Milch"])

    def test_zutat_entfernen_nicht_vorhanden(self):
        self.assertEqual(zutaten_entfernen(["Mehl", "Zucker", "Eier"], "Milch"), ["Mehl", "Zucker", "Eier"])

    def test_zutat_entfernen_leere_liste(self):
        self.assertEqual(zutaten_entfernen([], "Milch"), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 511
