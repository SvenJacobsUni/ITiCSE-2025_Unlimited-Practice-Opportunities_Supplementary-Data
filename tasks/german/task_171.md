# Input
- Programmierkonzept: If-Else-Anweisungen;For-Schleifen;Tupel
- Kontext: Basketball

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Basketball-Statistiken

Schreibe eine Funktion namens `bewerte_spieler(spieler_statistiken)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel enthält den Namen eines Spielers und die Anzahl der erzielten Punkte in einem Spiel. Die Funktion soll die Spieler bewerten und eine entsprechende Nachricht zurückgeben.

- Wenn ein Spieler mehr als 20 Punkte erzielt hat, soll die Nachricht "Hervorragend, [Name]!" lauten.
- Wenn ein Spieler zwischen 10 und 20 Punkte erzielt hat, soll die Nachricht "Gut gemacht, [Name]!" lauten.
- Wenn ein Spieler weniger als 10 Punkte erzielt hat, soll die Nachricht "Weiter so, [Name]!" lauten.

Beispielaufruf:
```python
spieler_statistiken = [("Anna", 25), ("Ben", 15), ("Chris", 8)]
bewerte_spieler(spieler_statistiken)
```

Erwartete Ausgabe:
```
Hervorragend, Anna!
Gut gemacht, Ben!
Weiter so, Chris!
```

## Codegerüst
```python
def bewerte_spieler(spieler_statistiken):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bewerte_spieler(spieler_statistiken):
    for name, punkte in spieler_statistiken:
        if punkte > 20:
            print(f"Hervorragend, {name}!")
        elif 10 <= punkte <= 20:
            print(f"Gut gemacht, {name}!")
        else:
            print(f"Weiter so, {name}!")

spieler_statistiken = [("Anna", 25), ("Ben", 15), ("Chris", 8)]
bewerte_spieler(spieler_statistiken)
```

## Unit Tests
```python
import unittest
from main import bewerte_spieler

class TestBewerteSpieler(unittest.TestCase):
    def test_hervorragend(self):
        spieler_statistiken = [("Anna", 25)]
        expected_output = "Hervorragend, Anna!\n"
        with self.assertLogs(level='INFO') as log:
            bewerte_spieler(spieler_statistiken)
            self.assertEqual(log.output, [expected_output])

    def test_gut_gemacht(self):
        spieler_statistiken = [("Ben", 15)]
        expected_output = "Gut gemacht, Ben!\n"
        with self.assertLogs(level='INFO') as log:
            bewerte_spieler(spieler_statistiken)
            self.assertEqual(log.output, [expected_output])

    def test_weiter_so(self):
        spieler_statistiken = [("Chris", 8)]
        expected_output = "Weiter so, Chris!\n"
        with self.assertLogs(level='INFO') as log:
            bewerte_spieler(spieler_statistiken)
            self.assertEqual(log.output, [expected_output])

    def test_gemischte_bewertungen(self):
        spieler_statistiken = [("Anna", 25), ("Ben", 15), ("Chris", 8)]
        expected_output = [
            "Hervorragend, Anna!\n",
            "Gut gemacht, Ben!\n",
            "Weiter so, Chris!\n"
        ]
        with self.assertLogs(level='INFO') as log:
            bewerte_spieler(spieler_statistiken)
            self.assertEqual(log.output, expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 603
