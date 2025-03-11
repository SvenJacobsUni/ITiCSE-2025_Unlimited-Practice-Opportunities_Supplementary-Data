# Input
- Programmierkonzept: String
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustierbeschreibung

Schreibe eine Funktion namens `haustier_beschreibung(tierart, name)`, die eine Beschreibung eines Haustiers erstellt. Die Funktion soll zwei Parameter entgegennehmen: `tierart` (z.B. "Hund", "Katze") und `name` (z.B. "Bello", "Minka"). Die Funktion soll einen String zurückgeben, der das Haustier beschreibt.

Beispielaufruf: 
```python
haustier_beschreibung("Hund", "Bello")
```

Erwartete Ausgabe:
```python
"Bello ist ein Hund."
```

Beispielaufruf:
```python
haustier_beschreibung("Katze", "Minka")
```

Erwartete Ausgabe:
```python
"Minka ist eine Katze."
```

## Codegerüst
```python
def haustier_beschreibung(tierart, name):
    ## Hier Code einfügen
```

## Musterlösung
```python
def haustier_beschreibung(tierart, name):
    return f"{name} ist ein{'' if tierart.lower() in ['hund', 'vogel'] else 'e'} {tierart}."

print(haustier_beschreibung("Hund", "Bello"))
print(haustier_beschreibung("Katze", "Minka"))
```

## Unit Tests
```python
import unittest
from main import haustier_beschreibung

class TestHaustierBeschreibung(unittest.TestCase):
    def test_hund(self):
        self.assertEqual(haustier_beschreibung("Hund", "Bello"), "Bello ist ein Hund.")

    def test_katze(self):
        self.assertEqual(haustier_beschreibung("Katze", "Minka"), "Minka ist eine Katze.")

    def test_vogel(self):
        self.assertEqual(haustier_beschreibung("Vogel", "Tweety"), "Tweety ist ein Vogel.")

    def test_fisch(self):
        self.assertEqual(haustier_beschreibung("Fisch", "Nemo"), "Nemo ist ein Fisch.")

    def test_leerer_name(self):
        self.assertEqual(haustier_beschreibung("Hund", ""), " ist ein Hund.")

    def test_leere_tierart(self):
        self.assertEqual(haustier_beschreibung("", "Bello"), "Bello ist ein .")

    def test_leere_parameter(self):
        self.assertEqual(haustier_beschreibung("", ""), " ist ein .")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 422
