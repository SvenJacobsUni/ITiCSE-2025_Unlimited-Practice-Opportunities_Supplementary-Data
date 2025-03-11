# Input
- Programmierkonzept: Funktionen als Variablen
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen als Variablen im Kontext psychischer Gesundheit

Schreibe eine Funktion `psychische_gesundheit(tage)`, die eine Liste von Tagen der Woche als Eingabe erhält. Jeder Tag ist eine Zeichenkette, die den Namen des Tages repräsentiert (z.B. "Montag", "Dienstag", etc.). Die Funktion soll für jeden Tag eine zufällige Aktivität zur Förderung der psychischen Gesundheit auswählen und zurückgeben. 

Definiere dazu drei separate Funktionen:
1. `meditation()`: Gibt die Zeichenkette "Meditation" zurück.
2. `spaziergang()`: Gibt die Zeichenkette "Spaziergang im Park" zurück.
3. `lesen()`: Gibt die Zeichenkette "Ein gutes Buch lesen" zurück.

Die Funktion `psychische_gesundheit(tage)` soll eine Liste von Aktivitäten zurückgeben, wobei für jeden Tag eine der drei Aktivitäten zufällig ausgewählt wird.

Beispielaufruf:
```python
print(psychische_gesundheit(["Montag", "Dienstag", "Mittwoch"]))
```

Mögliche Ausgabe:
```python
["Meditation", "Spaziergang im Park", "Ein gutes Buch lesen"]
```

## Codegerüst
```python
def meditation():
    ## Hier Code einfügen

def spaziergang():
    ## Hier Code einfügen

def lesen():
    ## Hier Code einfügen

def psychische_gesundheit(tage):
    ## Hier Code einfügen
```

## Musterlösung
```python
import random

def meditation():
    return "Meditation"

def spaziergang():
    return "Spaziergang im Park"

def lesen():
    return "Ein gutes Buch lesen"

def psychische_gesundheit(tage):
    aktivitaeten = [meditation, spaziergang, lesen]
    return [random.choice(aktivitaeten)() for tag in tage]

print(psychische_gesundheit(["Montag", "Dienstag", "Mittwoch"]))
```

## Unit Tests
```python
import unittest
from main import meditation, spaziergang, lesen, psychische_gesundheit

class TestPsychischeGesundheit(unittest.TestCase):
    def test_meditation(self):
        self.assertEqual(meditation(), "Meditation")

    def test_spaziergang(self):
        self.assertEqual(spaziergang(), "Spaziergang im Park")

    def test_lesen(self):
        self.assertEqual(lesen(), "Ein gutes Buch lesen")

    def test_psychische_gesundheit(self):
        tage = ["Montag", "Dienstag", "Mittwoch"]
        result = psychische_gesundheit(tage)
        self.assertEqual(len(result), len(tage))
        for aktivitaet in result:
            self.assertIn(aktivitaet, ["Meditation", "Spaziergang im Park", "Ein gutes Buch lesen"])

    def test_leere_liste(self):
        self.assertEqual(psychische_gesundheit([]), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 484
