# Input
- Programmierkonzept: Rekursion
- Kontext: Kochen

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Rezeptanweisungen

Schreibe eine rekursive Funktion namens `koch_rezept(schritte, index)`, die eine Liste von Kochschritten und einen Index als Argumente erhält. Die Funktion soll die Kochschritte nacheinander ausgeben, beginnend beim angegebenen Index, und dabei rekursiv vorgehen. Wenn der Index das Ende der Liste erreicht, soll die Funktion aufhören.

Beispielaufruf:
```python
kochschritte = ["Schneide die Zwiebeln.", "Erhitze das Öl in der Pfanne.", "Brate die Zwiebeln an.", "Füge die Tomaten hinzu.", "Lasse alles 10 Minuten köcheln."]
koch_rezept(kochschritte, 0)
```

Erwartete Ausgabe:
```
Schneide die Zwiebeln.
Erhitze das Öl in der Pfanne.
Brate die Zwiebeln an.
Füge die Tomaten hinzu.
Lasse alles 10 Minuten köcheln.
```

## Codegerüst
```python
def koch_rezept(schritte, index):
    ## Hier Code einfügen
```

## Musterlösung
```python
def koch_rezept(schritte, index):
    if index < len(schritte):
        print(schritte[index])
        koch_rezept(schritte, index + 1)

kochschritte = ["Schneide die Zwiebeln.", "Erhitze das Öl in der Pfanne.", "Brate die Zwiebeln an.", "Füge die Tomaten hinzu.", "Lasse alles 10 Minuten köcheln."]
koch_rezept(kochschritte, 0)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import koch_rezept

class TestKochRezept(unittest.TestCase):
    def setUp(self):
        self.kochschritte = ["Schneide die Zwiebeln.", "Erhitze das Öl in der Pfanne.", "Brate die Zwiebeln an.", "Füge die Tomaten hinzu.", "Lasse alles 10 Minuten köcheln."]
        self.saved_stdout = sys.stdout
        self.output = StringIO()
        sys.stdout = self.output

    def tearDown(self):
        sys.stdout = self.saved_stdout

    def test_koch_rezept_vollstaendig(self):
        koch_rezept(self.kochschritte, 0)
        self.assertEqual(self.output.getvalue().strip(), "\n".join(self.kochschritte))

    def test_koch_rezept_ab_mitte(self):
        koch_rezept(self.kochschritte, 2)
        self.assertEqual(self.output.getvalue().strip(), "\n".join(self.kochschritte[2:]))

    def test_koch_rezept_letzter_schritt(self):
        koch_rezept(self.kochschritte, 4)
        self.assertEqual(self.output.getvalue().strip(), self.kochschritte[4])

    def test_koch_rezept_ueber_index(self):
        koch_rezept(self.kochschritte, 5)
        self.assertEqual(self.output.getvalue().strip(), "")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 423
