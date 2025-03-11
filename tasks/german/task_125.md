# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);For-Schleifen
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rezeptauswahl basierend auf Zutaten

Schreibe eine Funktion namens `rezept_auswahl(zutaten)`, die eine Liste von Zutaten als Argument erhält und basierend auf den vorhandenen Zutaten ein Rezept auswählt. Die Funktion soll die folgenden Rezepte berücksichtigen:

1. **Pasta mit Tomatensauce**:
   - Zutaten: Nudeln, Tomaten, Knoblauch
2. **Gemüsepfanne**:
   - Zutaten: Paprika, Zucchini, Zwiebeln
3. **Obstsalat**:
   - Zutaten: Apfel, Banane, Orange

Die Funktion soll überprüfen, ob alle benötigten Zutaten für ein Rezept in der übergebenen Liste enthalten sind. Wenn mehrere Rezepte möglich sind, soll das erste passende Rezept ausgewählt werden. Wenn kein Rezept möglich ist, soll die Funktion "Kein passendes Rezept gefunden" zurückgeben.

Beispielaufruf:
```python
zutaten = ["Nudeln", "Tomaten", "Knoblauch", "Apfel"]
print(rezept_auswahl(zutaten))
```

Erwartete Ausgabe:
```
Pasta mit Tomatensauce
```

## Codegerüst
```python
def rezept_auswahl(zutaten):
    ## Hier Code einfügen
```

## Musterlösung
```python
def rezept_auswahl(zutaten):
    rezepte = {
        "Pasta mit Tomatensauce": {"Nudeln", "Tomaten", "Knoblauch"},
        "Gemüsepfanne": {"Paprika", "Zucchini", "Zwiebeln"},
        "Obstsalat": {"Apfel", "Banane", "Orange"}
    }
    for rezept, benötigte_zutaten in rezepte.items():
        if benötigte_zutaten.issubset(zutaten):
            return rezept
    return "Kein passendes Rezept gefunden"

zutaten = ["Nudeln", "Tomaten", "Knoblauch", "Apfel"]
print(rezept_auswahl(zutaten))
```

## Unit Tests
```python
import unittest
from main import rezept_auswahl

class TestRezeptAuswahl(unittest.TestCase):
    def test_pasta_mit_tomatensauce(self):
        self.assertEqual(rezept_auswahl(["Nudeln", "Tomaten", "Knoblauch"]), "Pasta mit Tomatensauce")

    def test_gemuesepfanne(self):
        self.assertEqual(rezept_auswahl(["Paprika", "Zucchini", "Zwiebeln"]), "Gemüsepfanne")

    def test_obstsalat(self):
        self.assertEqual(rezept_auswahl(["Apfel", "Banane", "Orange"]), "Obstsalat")

    def test_mehrere_rezepte(self):
        self.assertEqual(rezept_auswahl(["Nudeln", "Tomaten", "Knoblauch", "Paprika", "Zucchini", "Zwiebeln"]), "Pasta mit Tomatensauce")

    def test_keine_passenden_rezepte(self):
        self.assertEqual(rezept_auswahl(["Reis", "Huhn", "Sojasauce"]), "Kein passendes Rezept gefunden")

    def test_leere_zutatenliste(self):
        self.assertEqual(rezept_auswahl([]), "Kein passendes Rezept gefunden")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 557
