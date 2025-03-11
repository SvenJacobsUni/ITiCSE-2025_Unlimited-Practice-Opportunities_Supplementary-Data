# Input
- Programmierkonzept: Boolean und None;Funktionen höherer Ordnung
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Soziale Medien - Benutzeraktivität prüfen

Schreibe eine Funktion `ist_aktiv(benutzer)`, die überprüft, ob ein Benutzer in einem sozialen Netzwerk aktiv ist. Ein Benutzer wird als aktiv betrachtet, wenn er in den letzten 30 Tagen mindestens einen Beitrag gepostet hat. Die Funktion soll einen Boolean-Wert (`True` oder `False`) zurückgeben.

Zusätzlich soll eine Funktion `filter_aktive_benutzer(benutzer_liste, filter_funktion)` implementiert werden, die eine Liste von Benutzern und eine Filterfunktion als Argumente erhält. Diese Funktion soll eine neue Liste zurückgeben, die nur die aktiven Benutzer enthält.

Ein Benutzer wird durch ein Dictionary repräsentiert, das mindestens die folgenden Schlüssel enthält:
- `name`: Der Name des Benutzers (String)
- `letzter_beitrag`: Das Datum des letzten Beitrags in Tagen seit dem aktuellen Datum (Integer)

Beispiel:
```python
benutzer1 = {"name": "Alice", "letzter_beitrag": 10}
benutzer2 = {"name": "Bob", "letzter_beitrag": 40}
benutzer3 = {"name": "Charlie", "letzter_beitrag": 5}

benutzer_liste = [benutzer1, benutzer2, benutzer3]

# Aufruf der Funktion
aktive_benutzer = filter_aktive_benutzer(benutzer_liste, ist_aktiv)

# Erwartete Ausgabe: [{"name": "Alice", "letzter_beitrag": 10}, {"name": "Charlie", "letzter_beitrag": 5}]
print(aktive_benutzer)
```

Implementiere die Funktionen `ist_aktiv(benutzer)` und `filter_aktive_benutzer(benutzer_liste, filter_funktion)`.

## Codegerüst
```python
def ist_aktiv(benutzer):
    ## Hier Code einfügen

def filter_aktive_benutzer(benutzer_liste, filter_funktion):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ist_aktiv(benutzer):
    return benutzer['letzter_beitrag'] <= 30

def filter_aktive_benutzer(benutzer_liste, filter_funktion):
    return [benutzer for benutzer in benutzer_liste if filter_funktion(benutzer)]

benutzer1 = {"name": "Alice", "letzter_beitrag": 10}
benutzer2 = {"name": "Bob", "letzter_beitrag": 40}
benutzer3 = {"name": "Charlie", "letzter_beitrag": 5}

benutzer_liste = [benutzer1, benutzer2, benutzer3]

aktive_benutzer = filter_aktive_benutzer(benutzer_liste, ist_aktiv)

print(aktive_benutzer)
```

## Unit Tests
```python
import unittest
from main import ist_aktiv, filter_aktive_benutzer

class TestSozialeMedien(unittest.TestCase):
    def test_ist_aktiv_true(self):
        benutzer = {"name": "Alice", "letzter_beitrag": 10}
        self.assertTrue(ist_aktiv(benutzer))

    def test_ist_aktiv_false(self):
        benutzer = {"name": "Bob", "letzter_beitrag": 40}
        self.assertFalse(ist_aktiv(benutzer))

    def test_filter_aktive_benutzer(self):
        benutzer1 = {"name": "Alice", "letzter_beitrag": 10}
        benutzer2 = {"name": "Bob", "letzter_beitrag": 40}
        benutzer3 = {"name": "Charlie", "letzter_beitrag": 5}
        benutzer_liste = [benutzer1, benutzer2, benutzer3]
        erwartete_ausgabe = [benutzer1, benutzer3]
        self.assertEqual(filter_aktive_benutzer(benutzer_liste, ist_aktiv), erwartete_ausgabe)

    def test_leere_liste(self):
        benutzer_liste = []
        erwartete_ausgabe = []
        self.assertEqual(filter_aktive_benutzer(benutzer_liste, ist_aktiv), erwartete_ausgabe)

    def test_alle_inaktiv(self):
        benutzer1 = {"name": "Alice", "letzter_beitrag": 40}
        benutzer2 = {"name": "Bob", "letzter_beitrag": 50}
        benutzer_liste = [benutzer1, benutzer2]
        erwartete_ausgabe = []
        self.assertEqual(filter_aktive_benutzer(benutzer_liste, ist_aktiv), erwartete_ausgabe)

    def test_alle_aktiv(self):
        benutzer1 = {"name": "Alice", "letzter_beitrag": 10}
        benutzer2 = {"name": "Bob", "letzter_beitrag": 20}
        benutzer_liste = [benutzer1, benutzer2]
        erwartete_ausgabe = [benutzer1, benutzer2]
        self.assertEqual(filter_aktive_benutzer(benutzer_liste, ist_aktiv), erwartete_ausgabe)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 549
