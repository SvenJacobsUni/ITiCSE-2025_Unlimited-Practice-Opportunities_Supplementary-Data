# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rezeptauswahl basierend auf Zutaten

Schreibe eine Funktion namens `rezept_auswahl(zutaten)`, die basierend auf einer Liste von Zutaten entscheidet, welches Rezept gekocht werden kann. Die Funktion soll die folgenden Rezepte berücksichtigen:

- **Pasta**: Wenn sowohl "Nudeln" als auch "Tomatensauce" in der Zutatenliste enthalten sind.
- **Salat**: Wenn sowohl "Salat" als auch "Tomaten" in der Zutatenliste enthalten sind.
- **Omelette**: Wenn sowohl "Eier" als auch "Milch" in der Zutatenliste enthalten sind.

Die Funktion soll den Namen des Rezepts als String zurückgeben, das gekocht werden kann. Wenn keine der Zutatenkombinationen vorhanden ist, soll die Funktion "Kein Rezept gefunden" zurückgeben.

Beispielaufrufe:

```python
print(rezept_auswahl(["Nudeln", "Tomatensauce", "Käse"]))  # Ausgabe: "Pasta"
print(rezept_auswahl(["Salat", "Tomaten", "Gurke"]))        # Ausgabe: "Salat"
print(rezept_auswahl(["Eier", "Milch", "Käse"]))            # Ausgabe: "Omelette"
print(rezept_auswahl(["Brot", "Butter"]))                   # Ausgabe: "Kein Rezept gefunden"
```

## Codegerüst
```python
def rezept_auswahl(zutaten):
    ## Hier Code einfügen
```

## Musterlösung
```python
def rezept_auswahl(zutaten):
    if "Nudeln" in zutaten and "Tomatensauce" in zutaten:
        return "Pasta"
    elif "Salat" in zutaten and "Tomaten" in zutaten:
        return "Salat"
    elif "Eier" in zutaten and "Milch" in zutaten:
        return "Omelette"
    return "Kein Rezept gefunden"

print(rezept_auswahl(["Nudeln", "Tomatensauce", "Käse"]))
print(rezept_auswahl(["Salat", "Tomaten", "Gurke"]))
print(rezept_auswahl(["Eier", "Milch", "Käse"]))
print(rezept_auswahl(["Brot", "Butter"]))
```

## Unit Tests
```python
import unittest
from main import rezept_auswahl

class TestRezeptAuswahl(unittest.TestCase):
    def test_pasta(self):
        self.assertEqual(rezept_auswahl(["Nudeln", "Tomatensauce", "Käse"]), "Pasta")

    def test_salat(self):
        self.assertEqual(rezept_auswahl(["Salat", "Tomaten", "Gurke"]), "Salat")

    def test_omelette(self):
        self.assertEqual(rezept_auswahl(["Eier", "Milch", "Käse"]), "Omelette")

    def test_kein_rezept(self):
        self.assertEqual(rezept_auswahl(["Brot", "Butter"]), "Kein Rezept gefunden")

    def test_leere_liste(self):
        self.assertEqual(rezept_auswahl([]), "Kein Rezept gefunden")

    def test_unvollstaendige_zutaten(self):
        self.assertEqual(rezept_auswahl(["Nudeln"]), "Kein Rezept gefunden")
        self.assertEqual(rezept_auswahl(["Tomatensauce"]), "Kein Rezept gefunden")
        self.assertEqual(rezept_auswahl(["Salat"]), "Kein Rezept gefunden")
        self.assertEqual(rezept_auswahl(["Tomaten"]), "Kein Rezept gefunden")
        self.assertEqual(rezept_auswahl(["Eier"]), "Kein Rezept gefunden")
        self.assertEqual(rezept_auswahl(["Milch"]), "Kein Rezept gefunden")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 456
