# Input
- Programmierkonzept: Integer;String;Boolean und None
- Kontext: Haustiere

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Haustier-Informationen

Schreibe eine Funktion namens `haustier_info(name, alter, art)`, die Informationen über ein Haustier entgegennimmt und eine entsprechende Nachricht zurückgibt. 

- `name` ist ein String, der den Namen des Haustiers enthält.
- `alter` ist ein Integer, der das Alter des Haustiers in Jahren angibt.
- `art` ist ein String, der die Art des Haustiers beschreibt (z.B. "Hund", "Katze").

Die Funktion soll die folgenden Bedingungen erfüllen:
1. Wenn der Name des Haustiers nicht angegeben ist (None), soll die Funktion "Kein Name angegeben" zurückgeben.
2. Wenn das Alter des Haustiers kleiner als 0 ist, soll die Funktion "Ungültiges Alter" zurückgeben.
3. Wenn die Art des Haustiers "Hund" ist, soll die Funktion "Das Haustier ist ein Hund namens [Name] und ist [Alter] Jahre alt." zurückgeben.
4. Wenn die Art des Haustiers "Katze" ist, soll die Funktion "Das Haustier ist eine Katze namens [Name] und ist [Alter] Jahre alt." zurückgeben.
5. Für alle anderen Arten von Haustieren soll die Funktion "Das Haustier ist ein [Art] namens [Name] und ist [Alter] Jahre alt." zurückgeben.

Beispielaufrufe:
- `haustier_info("Bello", 5, "Hund")` gibt "Das Haustier ist ein Hund namens Bello und ist 5 Jahre alt." zurück.
- `haustier_info(None, 3, "Katze")` gibt "Kein Name angegeben" zurück.
- `haustier_info("Mimi", -1, "Katze")` gibt "Ungültiges Alter" zurück.

## Codegerüst
```python
def haustier_info(name, alter, art):
    ## Hier Code einfügen
```

## Musterlösung
```python
def haustier_info(name, alter, art):
    if name is None:
        return "Kein Name angegeben"
    if alter < 0:
        return "Ungültiges Alter"
    if art == "Hund":
        return f"Das Haustier ist ein Hund namens {name} und ist {alter} Jahre alt."
    if art == "Katze":
        return f"Das Haustier ist eine Katze namens {name} und ist {alter} Jahre alt."
    return f"Das Haustier ist ein {art} namens {name} und ist {alter} Jahre alt."

# Beispielaufrufe
print(haustier_info("Bello", 5, "Hund"))
print(haustier_info(None, 3, "Katze"))
print(haustier_info("Mimi", -1, "Katze"))
```

## Unit Tests
```python
import unittest
from main import haustier_info

class TestHaustierInfo(unittest.TestCase):
    def test_hund(self):
        self.assertEqual(haustier_info("Bello", 5, "Hund"), "Das Haustier ist ein Hund namens Bello und ist 5 Jahre alt.")

    def test_katze(self):
        self.assertEqual(haustier_info("Mimi", 3, "Katze"), "Das Haustier ist eine Katze namens Mimi und ist 3 Jahre alt.")

    def test_keine_name(self):
        self.assertEqual(haustier_info(None, 3, "Katze"), "Kein Name angegeben")

    def test_ungueltiges_alter(self):
        self.assertEqual(haustier_info("Mimi", -1, "Katze"), "Ungültiges Alter")

    def test_andere_art(self):
        self.assertEqual(haustier_info("Tweety", 2, "Vogel"), "Das Haustier ist ein Vogel namens Tweety und ist 2 Jahre alt.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 595
