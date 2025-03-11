# Input
- Programmierkonzept: Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not);While-Schleifen
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Modernes Gaming - Spielerlevel

Schreibe eine Funktion namens `spieler_level(punkte)`, die das Level eines Spielers basierend auf seinen Punkten bestimmt. Die Funktion soll eine Nachricht mit dem erreichten Level zurückgeben. Verwende Kontrollstrukturen und eine While-Schleife, um die Punkte zu überprüfen und das entsprechende Level zu bestimmen.

Die Level sind wie folgt definiert:
- Level 1: 0 bis 99 Punkte
- Level 2: 100 bis 199 Punkte
- Level 3: 200 bis 299 Punkte
- Level 4: 300 bis 399 Punkte
- Level 5: 400 oder mehr Punkte

Beispielaufruf:
```python
print(spieler_level(150))  # Ausgabe: "Du bist auf Level 2!"
print(spieler_level(350))  # Ausgabe: "Du bist auf Level 4!"
```

Implementiere die Funktion `spieler_level(punkte)`, die die Punkte des Spielers als Argument nimmt und das entsprechende Level als Nachricht zurückgibt.

## Codegerüst
```python
def spieler_level(punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spieler_level(punkte):
    level = 1
    while punkte >= 100:
        punkte -= 100
        level += 1
    return f"Du bist auf Level {level}!"

print(spieler_level(150))  # Ausgabe: "Du bist auf Level 2!"
print(spieler_level(350))  # Ausgabe: "Du bist auf Level 4!"
```

## Unit Tests
```python
import unittest

from main import spieler_level

class TestSpielerLevel(unittest.TestCase):
    def test_level_1(self):
        self.assertEqual(spieler_level(50), "Du bist auf Level 1!")

    def test_level_2(self):
        self.assertEqual(spieler_level(150), "Du bist auf Level 2!")

    def test_level_3(self):
        self.assertEqual(spieler_level(250), "Du bist auf Level 3!")

    def test_level_4(self):
        self.assertEqual(spieler_level(350), "Du bist auf Level 4!")

    def test_level_5(self):
        self.assertEqual(spieler_level(450), "Du bist auf Level 5!")

    def test_exact_boundary_level_1(self):
        self.assertEqual(spieler_level(99), "Du bist auf Level 1!")

    def test_exact_boundary_level_2(self):
        self.assertEqual(spieler_level(100), "Du bist auf Level 2!")

    def test_exact_boundary_level_3(self):
        self.assertEqual(spieler_level(200), "Du bist auf Level 3!")

    def test_exact_boundary_level_4(self):
        self.assertEqual(spieler_level(300), "Du bist auf Level 4!")

    def test_exact_boundary_level_5(self):
        self.assertEqual(spieler_level(400), "Du bist auf Level 5!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 537
