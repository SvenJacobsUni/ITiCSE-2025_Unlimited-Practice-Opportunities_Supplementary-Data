# Input
- Programmierkonzept: Tupel;For-Schleifen
- Kontext: Tiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Tiere und ihre Lebensräume

Schreibe eine Funktion namens `tier_lebensraum(tiere)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel enthält den Namen eines Tieres und seinen Lebensraum. Die Funktion soll eine Liste der Tiere zurückgeben, die im Wald leben.

Beispielaufruf:
```python
tiere = [("Löwe", "Savanne"), ("Fuchs", "Wald"), ("Elefant", "Savanne"), ("Hirsch", "Wald")]
print(tier_lebensraum(tiere))
```

Erwartete Ausgabe:
```
['Fuchs', 'Hirsch']
```

## Codegerüst
```python
def tier_lebensraum(tiere):
    ## Hier Code einfügen
```

## Musterlösung
```python
def tier_lebensraum(tiere):
    return [tier for tier, lebensraum in tiere wenn lebensraum == "Wald"]

tiere = [("Löwe", "Savanne"), ("Fuchs", "Wald"), ("Elefant", "Savanne"), ("Hirsch", "Wald")]
print(tier_lebensraum(tiere))
```

## Unit Tests
```python
import unittest

from main import tier_lebensraum

class TestTierLebensraum(unittest.TestCase):
    def test_lebensraum_wald(self):
        tiere = [("Löwe", "Savanne"), ("Fuchs", "Wald"), ("Elefant", "Savanne"), ("Hirsch", "Wald")]
        self.assertEqual(tier_lebensraum(tiere), ["Fuchs", "Hirsch"])

    def test_keine_tiere_im_wald(self):
        tiere = [("Löwe", "Savanne"), ("Elefant", "Savanne")]
        self.assertEqual(tier_lebensraum(tiere), [])

    def test_alle_tiere_im_wald(self):
        tiere = [("Fuchs", "Wald"), ("Hirsch", "Wald")]
        self.assertEqual(tier_lebensraum(tiere), ["Fuchs", "Hirsch"])

    def test_leere_liste(self):
        tiere = []
        self.assertEqual(tier_lebensraum(tiere), [])

    def test_verschiedene_lebensraeume(self):
        tiere = [("Löwe", "Savanne"), ("Fuchs", "Wald"), ("Pinguin", "Antarktis"), ("Hirsch", "Wald"), ("Känguru", "Australien")]
        self.assertEqual(tier_lebensraum(tiere), ["Fuchs", "Hirsch"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 579
