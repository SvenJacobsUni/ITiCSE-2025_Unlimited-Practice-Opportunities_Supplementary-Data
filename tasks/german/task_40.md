# Input
- Programmierkonzept: If-Else-Anweisungen
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Soziale Medien - Benutzerstatus

Schreibe eine Funktion namens `benutzer_status(anzahl_follower)`, die den Status eines Benutzers auf einer sozialen Medienplattform basierend auf der Anzahl seiner Follower bestimmt. Die Funktion soll eine entsprechende Nachricht mit `return` zurückgeben.

- Wenn die Anzahl der Follower weniger als 100 beträgt, soll die Nachricht "Neuling" zurückgegeben werden.
- Wenn die Anzahl der Follower zwischen 100 und 1000 liegt (einschließlich), soll die Nachricht "Aufstrebend" zurückgegeben werden.
- Wenn die Anzahl der Follower mehr als 1000 beträgt, soll die Nachricht "Influencer" zurückgegeben werden.

Beispielaufrufe:
- `benutzer_status(50)` gibt "Neuling" zurück.
- `benutzer_status(500)` gibt "Aufstrebend" zurück.
- `benutzer_status(1500)` gibt "Influencer" zurück.

## Codegerüst
```python
def benutzer_status(anzahl_follower):
    ## Hier Code einfügen
```

## Musterlösung
```python
def benutzer_status(anzahl_follower):
    if anzahl_follower < 100:
        return "Neuling"
    elif anzahl_follower <= 1000:
        return "Aufstrebend"
    else:
        return "Influencer"

# Beispielaufrufe
print(benutzer_status(50))    # Neuling
print(benutzer_status(500))   # Aufstrebend
print(benutzer_status(1500))  # Influencer
```

## Unit Tests
```python
import unittest

from main import benutzer_status

class TestBenutzerStatus(unittest.TestCase):
    def test_neuling(self):
        self.assertEqual(benutzer_status(50), "Neuling")

    def test_aufstrebend(self):
        self.assertEqual(benutzer_status(500), "Aufstrebend")

    def test_influencer(self):
        self.assertEqual(benutzer_status(1500), "Influencer")

    def test_grenze_neuling_aufstrebend(self):
        self.assertEqual(benutzer_status(100), "Aufstrebend")

    def test_grenze_aufstrebend_influencer(self):
        self.assertEqual(benutzer_status(1000), "Aufstrebend")

    def test_null_follower(self):
        self.assertEqual(benutzer_status(0), "Neuling")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 458
