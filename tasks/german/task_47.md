# Input
- Programmierkonzept: String
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Angeln und Fische

Schreibe eine Funktion namens `fisch_zaehlen(text)`, die einen Text als Eingabe erhält und die Anzahl der Vorkommen des Wortes "Fisch" in diesem Text zurückgibt. Die Funktion soll dabei nicht zwischen Groß- und Kleinschreibung unterscheiden.

Beispielaufruf:
```python
fisch_zaehlen("Ich habe heute drei Fische gefangen. Fisch ist mein Lieblingsessen.")
```

Erwartete Ausgabe:
```
2
```

## Codegerüst
```python
def fisch_zaehlen(text):
    ## Hier Code einfügen
```

## Musterlösung
```python
def fisch_zaehlen(text):
    print(text.lower().count("fisch"))

fisch_zaehlen("Ich habe heute drei Fische gefangen. Fisch ist mein Lieblingsessen.")
```

## Unit Tests
```python
import unittest

from main import fisch_zaehlen

class TestFischZaehlen(unittest.TestCase):
    def test_einfacher_text(self):
        self.assertEqual(fisch_zaehlen("Ich habe heute drei Fische gefangen. Fisch ist mein Lieblingsessen."), 2)

    def test_keine_fische(self):
        self.assertEqual(fisch_zaehlen("Ich habe heute keine Fische gefangen."), 1)

    def test_mehrere_fische(self):
        self.assertEqual(fisch_zaehlen("Fisch Fisch Fisch"), 3)

    def test_gemischte_schreibweise(self):
        self.assertEqual(fisch_zaehlen("fisch Fisch FISCH"), 3)

    def test_leerer_text(self):
        self.assertEqual(fisch_zaehlen(""), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 465
