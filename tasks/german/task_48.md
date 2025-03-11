# Input
- Programmierkonzept: String
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rezeptbeschreibung

Schreibe eine Funktion namens `rezept_beschreibung(rezept)`, die eine Beschreibung eines Rezepts formatiert. Die Funktion soll einen String `rezept` als Eingabe erhalten, der die Zutaten und Zubereitungsschritte enthält. Die Funktion soll den String so formatieren, dass jede Zutat und jeder Zubereitungsschritt in einer neuen Zeile steht. 

Beispielaufruf:
```python
rezept = "Zutaten: Mehl, Zucker, Eier, Milch. Zubereitung: Mischen, Backen, Abkühlen."
print(rezept_beschreibung(rezept))
```

Erwartete Ausgabe:
```
Zutaten:
Mehl
Zucker
Eier
Milch
Zubereitung:
Mischen
Backen
Abkühlen
```

## Codegerüst
```python
def rezept_beschreibung(rezept):
    ## Hier Code einfügen
```

## Musterlösung
```python
def rezept_beschreibung(rezept):
    zutaten, zubereitung = rezept.split("Zubereitung:")
    zutaten = zutaten.replace("Zutaten:", "Zutaten:\n").replace(", ", "\n")
    zubereitung = "Zubereitung:\n" + zubereitung.replace(", ", "\n")
    return zutaten + zubereitung

rezept = "Zutaten: Mehl, Zucker, Eier, Milch. Zubereitung: Mischen, Backen, Abkühlen."
print(rezept_beschreibung(rezept))
```

## Unit Tests
```python
import unittest

from main import rezept_beschreibung

class TestRezeptBeschreibung(unittest.TestCase):
    def test_einfaches_rezept(self):
        rezept = "Zutaten: Mehl, Zucker, Eier, Milch. Zubereitung: Mischen, Backen, Abkühlen."
        expected = "Zutaten:\nMehl\nZucker\nEier\nMilch\nZubereitung:\nMischen\nBacken\nAbkühlen"
        self.assertEqual(rezept_beschreibung(rezept), expected)

    def test_leeres_rezept(self):
        rezept = "Zutaten: . Zubereitung: ."
        expected = "Zutaten:\n\nZubereitung:\n"
        self.assertEqual(rezept_beschreibung(rezept), expected)

    def test_nur_zutaten(self):
        rezept = "Zutaten: Mehl, Zucker. Zubereitung: ."
        expected = "Zutaten:\nMehl\nZucker\nZubereitung:\n"
        self.assertEqual(rezept_beschreibung(rezept), expected)

    def test_nur_zubereitung(self):
        rezept = "Zutaten: . Zubereitung: Mischen, Backen."
        expected = "Zutaten:\n\nZubereitung:\nMischen\nBacken"
        self.assertEqual(rezept_beschreibung(rezept), expected)

    def test_komplexes_rezept(self):
        rezept = "Zutaten: Mehl, Zucker, Eier, Milch, Butter, Salz. Zubereitung: Mischen, Kneten, Backen, Abkühlen, Servieren."
        expected = "Zutaten:\nMehl\nZucker\nEier\nMilch\nButter\nSalz\nZubereitung:\nMischen\nKneten\nBacken\nAbkühlen\nServieren"
        self.assertEqual(rezept_beschreibung(rezept), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 466
