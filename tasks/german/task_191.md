# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);Rekursion;Boolean und None
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Spieler Klassifikation

Schreibe eine Funktion `klassifiziere_spieler(gewicht, groesse)`, die einen Rugby-Spieler basierend auf seinem Gewicht (in Kilogramm) und seiner Größe (in Zentimetern) klassifiziert. Die Klassifikation erfolgt nach folgenden Regeln:

- Ein Spieler wird als "Leichtgewicht" klassifiziert, wenn sein Gewicht weniger als 75 kg beträgt.
- Ein Spieler wird als "Schwergewicht" klassifiziert, wenn sein Gewicht 75 kg oder mehr beträgt.
- Ein Spieler wird als "Groß" klassifiziert, wenn seine Größe 185 cm oder mehr beträgt.
- Ein Spieler wird als "Klein" klassifiziert, wenn seine Größe weniger als 185 cm beträgt.

Die Funktion soll eine Nachricht zurückgeben, die die Klassifikation des Spielers beschreibt. Beispiel:

- `klassifiziere_spieler(70, 190)` gibt "Leichtgewicht und Groß" zurück.
- `klassifiziere_spieler(80, 180)` gibt "Schwergewicht und Klein" zurück.

Zusätzlich soll eine rekursive Funktion `ist_gross(gewicht, groesse)` implementiert werden, die überprüft, ob ein Spieler als "Groß" klassifiziert wird. Diese Funktion soll `True` zurückgeben, wenn die Größe des Spielers 185 cm oder mehr beträgt, und `False` sonst.

Beispielaufrufe:
- `klassifiziere_spieler(70, 190)`
- `klassifiziere_spieler(80, 180)`
- `ist_gross(70, 190)`
- `ist_gross(80, 180)`

## Codegerüst
```python
def klassifiziere_spieler(gewicht, groesse):
    ## Hier Code einfügen

def ist_gross(gewicht, groesse):
    ## Hier Code einfügen
```

## Musterlösung
```python
def klassifiziere_spieler(gewicht, groesse):
    gewicht_klassifikation = "Leichtgewicht" if gewicht < 75 else "Schwergewicht"
    groesse_klassifikation = "Groß" if groesse >= 185 else "Klein"
    print(f"{gewicht_klassifikation} und {groesse_klassifikation}")

def ist_gross(gewicht, groesse):
    if groesse >= 185:
        return True
    return False

klassifiziere_spieler(70, 190)
klassifiziere_spieler(80, 180)
print(ist_gross(70, 190))
print(ist_gross(80, 180))
```

## Unit Tests
```python
import unittest
from main import klassifiziere_spieler, ist_gross

class TestKlassifiziereSpieler(unittest.TestCase):
    def test_leichtgewicht_gross(self):
        self.assertEqual(klassifiziere_spieler(70, 190), "Leichtgewicht und Groß")

    def test_schwergewicht_klein(self):
        self.assertEqual(klassifiziere_spieler(80, 180), "Schwergewicht und Klein")

    def test_leichtgewicht_klein(self):
        self.assertEqual(klassifiziere_spieler(70, 180), "Leichtgewicht und Klein")

    def test_schwergewicht_gross(self):
        self.assertEqual(klassifiziere_spieler(80, 190), "Schwergewicht und Groß")

class TestIstGross(unittest.TestCase):
    def test_gross(self):
        self.assertTrue(ist_gross(70, 190))

    def test_nicht_gross(self):
        self.assertFalse(ist_gross(80, 180))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 623
