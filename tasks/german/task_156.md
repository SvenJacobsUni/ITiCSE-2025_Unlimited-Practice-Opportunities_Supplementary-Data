# Input
- Programmierkonzept: If-Else-Anweisungen;Funktionen höherer Ordnung;String
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Spieler Bewertung

Schreibe eine Funktion namens `bewerte_spieler(name, punkte)`, die den Namen eines Rugby-Spielers und seine erzielten Punkte als Argumente entgegennimmt. Die Funktion soll den Spieler basierend auf seinen Punkten bewerten und eine entsprechende Nachricht zurückgeben.

- Wenn der Spieler mehr als 20 Punkte erzielt hat, soll die Nachricht lauten: "Hervorragend, [Name]! Du bist ein Star-Spieler!"
- Wenn der Spieler zwischen 10 und 20 Punkte erzielt hat (einschließlich 10 und 20), soll die Nachricht lauten: "Gut gemacht, [Name]! Du hast solide gespielt."
- Wenn der Spieler weniger als 10 Punkte erzielt hat, soll die Nachricht lauten: "Kopf hoch, [Name]! Übung macht den Meister."

Beispielaufruf:
```python
bewerte_spieler("Max", 25)
```
soll die Nachricht "Hervorragend, Max! Du bist ein Star-Spieler!" zurückgeben.

## Codegerüst
```python
def bewerte_spieler(name, punkte):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_spieler(name, punkte):
    if punkte > 20:
        print(f"Hervorragend, {name}! Du bist ein Star-Spieler!")
    elif 10 <= punkte <= 20:
        print(f"Gut gemacht, {name}! Du hast solide gespielt.")
    else:
        print(f"Kopf hoch, {name}! Übung macht den Meister.")

# Beispielaufruf
bewerte_spieler("Max", 25)
```

## Unit Tests
```python
import unittest
from main import bewerte_spieler

class TestBewerteSpieler(unittest.TestCase):
    def test_hervorragend(self):
        self.assertEqual(bewerte_spieler("Max", 25), "Hervorragend, Max! Du bist ein Star-Spieler!")

    def test_gut_gemacht(self):
        self.assertEqual(bewerte_spieler("Anna", 15), "Gut gemacht, Anna! Du hast solide gespielt.")

    def test_kopf_hoch(self):
        self.assertEqual(bewerte_spieler("Tom", 5), "Kopf hoch, Tom! Übung macht den Meister.")

    def test_grenze_20(self):
        self.assertEqual(bewerte_spieler("Lena", 20), "Gut gemacht, Lena! Du hast solide gespielt.")

    def test_grenze_10(self):
        self.assertEqual(bewerte_spieler("Paul", 10), "Gut gemacht, Paul! Du hast solide gespielt.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 588
