# Input
- Programmierkonzept: Tupel
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Psychische Gesundheit und Wohlbefinden

Schreibe eine Funktion namens `psychische_gesundheit(daten)`, die ein Tupel mit Informationen zur psychischen Gesundheit einer Person entgegennimmt und eine entsprechende Nachricht zurückgibt. Das Tupel enthält folgende Informationen in dieser Reihenfolge:

1. Name der Person (String)
2. Anzahl der Stunden Schlaf pro Nacht (Integer)
3. Anzahl der Stunden körperlicher Aktivität pro Woche (Integer)
4. Anzahl der Stunden, die mit Entspannungsaktivitäten pro Woche verbracht werden (Integer)

Die Funktion soll eine Nachricht zurückgeben, die den Namen der Person und eine Bewertung ihrer psychischen Gesundheit basierend auf den übergebenen Daten enthält. Beispielaufruf: 

```python
psychische_gesundheit(("Max", 7, 5, 3))
```

Die Funktion könnte eine Nachricht wie folgt zurückgeben:

```python
"Max, deine psychische Gesundheit scheint in einem guten Zustand zu sein!"
```

oder

```python
"Max, es könnte hilfreich sein, mehr Zeit für Entspannung einzuplanen."
```

## Codegerüst
```python
def psychische_gesundheit(daten):
    ## Hier Code einfügen
```

## Musterlösung
```python
def psychische_gesundheit(daten):
    name, schlaf, aktivitaet, entspannung = daten
    if schlaf >= 7 and aktivitaet >= 5 and entspannung >= 3:
        return f"{name}, deine psychische Gesundheit scheint in einem guten Zustand zu sein!"
    else:
        return f"{name, es könnte hilfreich sein, mehr Zeit für Entspannung einzuplanen."

print(psychische_gesundheit(("Max", 7, 5, 3)))
print(psychische_gesundheit(("Anna", 6, 4, 2)))
```

## Unit Tests
```python
import unittest
from main import psychische_gesundheit

class TestPsychischeGesundheit(unittest.TestCase):
    def test_guter_zustand(self):
        self.assertEqual(psychische_gesundheit(("Max", 7, 5, 3)), "Max, deine psychische Gesundheit scheint in einem guten Zustand zu sein!")

    def test_mehr_entspannung_noetig(self):
        self.assertEqual(psychische_gesundheit(("Anna", 6, 4, 2)), "Anna, es könnte hilfreich sein, mehr Zeit für Entspannung einzuplanen.")

    def test_mehr_schlaf_noetig(self):
        self.assertEqual(psychische_gesundheit(("Tom", 6, 5, 3)), "Tom, es könnte hilfreich sein, mehr Zeit für Entspannung einzuplanen.")

    def test_mehr_aktivitaet_noetig(self):
        self.assertEqual(psychische_gesundheit(("Lisa", 7, 4, 3)), "Lisa, es könnte hilfreich sein, mehr Zeit für Entspannung einzuplanen.")

    def test_mehr_entspannung_und_aktivitaet_noetig(self):
        self.assertEqual(psychische_gesundheit(("John", 7, 4, 2)), "John, es könnte hilfreich sein, mehr Zeit für Entspannung einzuplanen.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 475
