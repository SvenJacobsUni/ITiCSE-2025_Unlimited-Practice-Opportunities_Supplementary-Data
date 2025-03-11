# Input
- Programmierkonzept: If-Else-Anweisungen
- Kontext: Modernes Gaming

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Modernes Gaming - Spielerauswahl

Schreibe eine Funktion namens `spielerauswahl(level)`, die basierend auf dem übergebenen Level des Spielers eine entsprechende Nachricht zurückgibt. Die Funktion soll die folgenden Bedingungen berücksichtigen:

- Wenn der Spielerlevel kleiner als 10 ist, soll die Nachricht "Anfänger: Willkommen in der Welt des Gamings!" zurückgegeben werden.
- Wenn der Spielerlevel zwischen 10 und 20 liegt (einschließlich), soll die Nachricht "Fortgeschrittener: Du machst Fortschritte!" zurückgegeben werden.
- Wenn der Spielerlevel größer als 20 ist, soll die Nachricht "Profi: Du bist ein echter Gamer!" zurückgegeben werden.

Beispielaufrufe:
- `spielerauswahl(5)` gibt "Anfänger: Willkommen in der Welt des Gamings!" zurück.
- `spielerauswahl(15)` gibt "Fortgeschrittener: Du machst Fortschritte!" zurück.
- `spielerauswahl(25)` gibt "Profi: Du bist ein echter Gamer!" zurück.

## Codegerüst
```python
def spielerauswahl(level):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spielerauswahl(level):
    if level < 10:
        return "Anfänger: Willkommen in der Welt des Gamings!"
    elif 10 <= level <= 20:
        return "Fortgeschrittener: Du machst Fortschritte!"
    else:
        return "Profi: Du bist ein echter Gamer!"

# Beispielaufrufe
print(spielerauswahl(5))
print(spielerauswahl(15))
print(spielerauswahl(25))
```

## Unit Tests
```python
import unittest
from main import spielerauswahl

class TestSpielerauswahl(unittest.TestCase):
    def test_anfaenger(self):
        self.assertEqual(spielerauswahl(5), "Anfänger: Willkommen in der Welt des Gamings!")

    def test_fortgeschrittener(self):
        self.assertEqual(spielerauswahl(15), "Fortgeschrittener: Du machst Fortschritte!")

    def test_profi(self):
        self.assertEqual(spielerauswahl(25), "Profi: Du bist ein echter Gamer!")

    def test_grenze_anfaenger(self):
        self.assertEqual(spielerauswahl(9), "Anfänger: Willkommen in der Welt des Gamings!")

    def test_grenze_fortgeschrittener_unter(self):
        self.assertEqual(spielerauswahl(10), "Fortgeschrittener: Du machst Fortschritte!")

    def test_grenze_fortgeschrittener_ober(self):
        self.assertEqual(spielerauswahl(20), "Fortgeschrittener: Du machst Fortschritte!")

    def test_grenze_profi(self):
        self.assertEqual(spielerauswahl(21), "Profi: Du bist ein echter Gamer!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 444
