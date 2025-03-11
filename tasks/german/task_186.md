# Input
- Programmierkonzept: If-Else-Anweisungen;While-Schleifen;Boolean und None
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Modernes Gaming - Spielerlevel und Erfahrungspunkte

Schreibe eine Funktion `level_up(spieler_level, erfahrungspunkte)`, die überprüft, ob ein Spieler basierend auf seinen Erfahrungspunkten ein Level aufsteigen kann. 

- Wenn der Spieler 1000 oder mehr Erfahrungspunkte hat, steigt er ein Level auf und die Funktion gibt `True` zurück.
- Wenn der Spieler weniger als 1000 Erfahrungspunkte hat, bleibt er auf dem aktuellen Level und die Funktion gibt `False` zurück.
- Wenn der Spieler keine Erfahrungspunkte (None) hat, gibt die Funktion ebenfalls `False` zurück.

Zusätzlich soll die Funktion eine While-Schleife verwenden, um die Erfahrungspunkte des Spielers zu reduzieren, bis sie unter 1000 fallen, falls der Spieler ein Level aufsteigt.

Beispielaufruf:
```python
level_up(5, 1200)  # gibt True zurück und reduziert die Erfahrungspunkte auf 200
level_up(3, 800)   # gibt False zurück
level_up(2, None)  # gibt False zurück
```

## Codegerüst
```python
def level_up(spieler_level, erfahrungspunkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def level_up(spieler_level, erfahrungspunkte):
    if erfahrungspunkte is None or erfahrungspunkte < 1000:
        return False
    while erfahrungspunkte >= 1000:
        erfahrungspunkte -= 1000
        spieler_level += 1
    return True

# Beispielaufrufe
print(level_up(5, 1200))  # True
print(level_up(3, 800))   # False
print(level_up(2, None))  # False
```

## Unit Tests
```python
import unittest

from main import level_up

class TestLevelUp(unittest.TestCase):
    def test_level_up_with_enough_experience(self):
        self.assertTrue(level_up(5, 1200))

    def test_level_up_with_not_enough_experience(self):
        self.assertFalse(level_up(3, 800))

    def test_level_up_with_no_experience(self):
        self.assertFalse(level_up(2, None))

    def test_level_up_with_exact_experience(self):
        self.assertTrue(level_up(1, 1000))

    def test_level_up_with_multiple_levels(self):
        self.assertTrue(level_up(1, 2500))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 618
