# Input
- Programmierkonzept: Boolean und None;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Soziale Medien - Benutzeraktivität prüfen

Schreibe eine Funktion namens `ist_aktiv(benutzername, beitraege, follower)`, die überprüft, ob ein Benutzer auf einer sozialen Medienplattform als aktiv gilt. Ein Benutzer gilt als aktiv, wenn er mindestens 10 Beiträge veröffentlicht hat **und** mehr als 100 Follower hat. Die Funktion soll einen Boolean Wert (`True` oder `False`) zurückgeben.

Beispielaufrufe:
- `ist_aktiv("MaxMustermann", 15, 150)` gibt `True` zurück.
- `ist_aktiv("ErikaMustermann", 5, 200)` gibt `False` zurück.

## Codegerüst
```python
def ist_aktiv(benutzername, beitraege, follower):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ist_aktiv(benutzername, beitraege, follower):
    return beitraege >= 10 and follower > 100

# Beispielaufrufe
print(ist_aktiv("MaxMustermann", 15, 150))  # True
print(ist_aktiv("ErikaMustermann", 5, 200))  # False
```

## Unit Tests
```python
import unittest
from main import ist_aktiv

class TestIstAktiv(unittest.TestCase):
    def test_aktiv(self):
        self.assertTrue(ist_aktiv("MaxMustermann", 15, 150))

    def test_nicht_aktiv_wenige_beitraege(self):
        self.assertFalse(ist_aktiv("ErikaMustermann", 5, 200))

    def test_nicht_aktiv_wenige_follower(self):
        self.assertFalse(ist_aktiv("HansMustermann", 20, 50))

    def test_nicht_aktiv_wenige_beitraege_und_follower(self):
        self.assertFalse(ist_aktiv("AnnaMustermann", 5, 50))

    def test_grenzwert_beitraege(self):
        self.assertFalse(ist_aktiv("GrenzfallBeitraege", 9, 150))
        self.assertTrue(ist_aktiv("GrenzfallBeitraege", 10, 150))

    def test_grenzwert_follower(self):
        self.assertFalse(ist_aktiv("GrenzfallFollower", 15, 100))
        self.assertTrue(ist_aktiv("GrenzfallFollower", 15, 101))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 542
