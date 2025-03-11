# Input
- Programmierkonzept: If-Else-Anweisungen;Funktionen als Variablen;Boolean und None
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportliche Aktivität

Schreibe eine Funktion namens `sport_aktivitaet(aktivitaet)`, die eine sportliche Aktivität als String entgegennimmt und eine entsprechende Nachricht zurückgibt. Die Funktion soll die folgenden Bedingungen prüfen:

- Wenn die Aktivität "Laufen" ist, soll die Nachricht "Laufen ist eine großartige Möglichkeit, fit zu bleiben!" zurückgegeben werden.
- Wenn die Aktivität "Schwimmen" ist, soll die Nachricht "Schwimmen trainiert den ganzen Körper!" zurückgegeben werden.
- Wenn die Aktivität "Radfahren" ist, soll die Nachricht "Radfahren ist gut für die Ausdauer!" zurückgegeben werden.
- Für alle anderen Aktivitäten soll die Nachricht "Das ist auch eine tolle Sportart!" zurückgegeben werden.

Beispielaufrufe:
- `sport_aktivitaet("Laufen")` gibt "Laufen ist eine großartige Möglichkeit, fit zu bleiben!" zurück.
- `sport_aktivitaet("Schwimmen")` gibt "Schwimmen trainiert den ganzen Körper!" zurück.
- `sport_aktivitaet("Basketball")` gibt "Das ist auch eine tolle Sportart!" zurück.

## Codegerüst
```python
def sport_aktivitaet(aktivitaet):
    ## Hier Code einfügen
```

## Musterlösung
```python
def sport_aktivitaet(aktivitaet):
    if aktivitaet == "Laufen":
        return "Laufen ist eine großartige Möglichkeit, fit zu bleiben!"
    elif aktivitaet == "Schwimmen":
        return "Schwimmen trainiert den ganzen Körper!"
    elif aktivitaet == "Radfahren":
        return "Radfahren ist gut für die Ausdauer!"
    else:
        return "Das ist auch eine tolle Sportart!"

# Beispielaufrufe
print(sport_aktivitaet("Laufen"))
print(sport_aktivitaet("Schwimmen"))
print(sport_aktivitaet("Basketball"))
```

## Unit Tests
```python
import unittest
from main import sport_aktivitaet

class TestSportAktivitaet(unittest.TestCase):
    def test_laufen(self):
        self.assertEqual(sport_aktivitaet("Laufen"), "Laufen ist eine großartige Möglichkeit, fit zu bleiben!")

    def test_schwimmen(self):
        self.assertEqual(sport_aktivitaet("Schwimmen"), "Schwimmen trainiert den ganzen Körper!")

    def test_radfahren(self):
        self.assertEqual(sport_aktivitaet("Radfahren"), "Radfahren ist gut für die Ausdauer!")

    def test_andere_aktivitaet(self):
        self.assertEqual(sport_aktivitaet("Basketball"), "Das ist auch eine tolle Sportart!")
        self.assertEqual(sport_aktivitaet("Yoga"), "Das ist auch eine tolle Sportart!")
        self.assertEqual(sport_aktivitaet("Tennis"), "Das ist auch eine tolle Sportart!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 586
