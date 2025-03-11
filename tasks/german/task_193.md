# Input
- Programmierkonzept: For-Schleifen;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);If-Else-Anweisungen
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Zutatenprüfung für ein Rezept

Schreibe eine Funktion namens `pruefe_zutaten(zutaten_liste)`, die eine Liste von Zutaten als Argument erhält. Die Funktion soll überprüfen, ob alle notwendigen Zutaten für ein bestimmtes Rezept vorhanden sind. Das Rezept benötigt die folgenden Zutaten: "Mehl", "Eier", "Milch", "Zucker" und "Butter".

Die Funktion soll:
1. Überprüfen, ob jede der benötigten Zutaten in der übergebenen Liste enthalten ist.
2. Eine Nachricht zurückgeben, die angibt, ob alle Zutaten vorhanden sind oder welche Zutaten fehlen.

Beispielaufruf:
```python
pruefe_zutaten(["Mehl", "Eier", "Milch", "Zucker", "Butter"])
```
sollte zurückgeben:
```python
"Alle Zutaten sind vorhanden."
```

Ein anderer Beispielaufruf:
```python
pruefe_zutaten(["Mehl", "Eier", "Milch"])
```
sollte zurückgeben:
```python
"Es fehlen die folgenden Zutaten: Zucker, Butter"
```

## Codegerüst
```python
def pruefe_zutaten(zutaten_liste):
    ## Hier Code einfügen
```

## Musterlösung
```python
def pruefe_zutaten(zutaten_liste):
    rezept_zutaten = {"Mehl", "Eier", "Milch", "Zucker", "Butter"}
    fehlende_zutaten = rezept_zutaten - set(zutaten_liste)
    if fehlende_zutaten:
        print(f"Es fehlen die folgenden Zutaten: {', '.join(fehlende_zutaten)}")
    else:
        print("Alle Zutaten sind vorhanden.")

pruefe_zutaten(["Mehl", "Eier", "Milch", "Zucker", "Butter"])
pruefe_zutaten(["Mehl", "Eier", "Milch"])
```

## Unit Tests
```python
import unittest

from main import pruefe_zutaten

class TestPruefeZutaten(unittest.TestCase):
    def test_alle_zutaten_vorhanden(self):
        self.assertEqual(pruefe_zutaten(["Mehl", "Eier", "Milch", "Zucker", "Butter"]), "Alle Zutaten sind vorhanden.")

    def test_einige_zutaten_fehlen(self):
        self.assertEqual(pruefe_zutaten(["Mehl", "Eier", "Milch"]), "Es fehlen die folgenden Zutaten: Zucker, Butter")

    def test_alle_zutaten_fehlen(self):
        self.assertEqual(pruefe_zutaten([]), "Es fehlen die folgenden Zutaten: Mehl, Eier, Milch, Zucker, Butter")

    def test_eine_zutat_fehlt(self):
        self.assertEqual(pruefe_zutaten(["Mehl", "Eier", "Milch", "Zucker"]), "Es fehlt die folgende Zutat: Butter")

    def test_doppelte_zutaten(self):
        self.assertEqual(pruefe_zutaten(["Mehl", "Eier", "Milch", "Zucker", "Butter", "Butter"]), "Alle Zutaten sind vorhanden.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 625
