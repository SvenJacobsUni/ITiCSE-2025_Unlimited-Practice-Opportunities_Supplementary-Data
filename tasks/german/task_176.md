# Input
- Programmierkonzept: If-Else-Anweisungen;Tupel;Float
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Spielergewicht

Schreibe eine Funktion namens `spieler_gewicht(spieler)`, die ein Tupel als Argument erhält. Das Tupel enthält den Namen des Spielers und sein Gewicht in Kilogramm als Float. Die Funktion soll überprüfen, ob das Gewicht des Spielers über oder unter 100 kg liegt und eine entsprechende Nachricht zurückgeben.

- Wenn das Gewicht des Spielers 100 kg oder mehr beträgt, soll die Nachricht lauten: "`[Name] ist ein schwerer Spieler.`"
- Wenn das Gewicht des Spielers unter 100 kg liegt, soll die Nachricht lauten: "`[Name] ist ein leichter Spieler.`"

Beispielaufruf:
```python
spieler_gewicht(("Max", 105.5))  # gibt "Max ist ein schwerer Spieler." zurück
spieler_gewicht(("Tom", 95.0))   # gibt "Tom ist ein leichter Spieler." zurück
```

## Codegerüst
```python
def spieler_gewicht(spieler):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spieler_gewicht(spieler):
    name, gewicht = spieler
    if gewicht >= 100:
        print(f"{name} ist ein schwerer Spieler.")
    else:
        print(f"{name} ist ein leichter Spieler.")

spieler_gewicht(("Max", 105.5))
spieler_gewicht(("Tom", 95.0))
```

## Unit Tests
```python
import unittest
from main import spieler_gewicht

class TestSpielerGewicht(unittest.TestCase):
    def test_schwerer_spieler(self):
        self.assertEqual(spieler_gewicht(("Max", 105.5)), "Max ist ein schwerer Spieler.")

    def test_leichter_spieler(self):
        self.assertEqual(spieler_gewicht(("Tom", 95.0)), "Tom ist ein leichter Spieler.")

    def test_grenze_schwerer_spieler(self):
        self.assertEqual(spieler_gewicht(("John", 100.0)), "John ist ein schwerer Spieler.")

    def test_grenze_leichter_spieler(self):
        self.assertEqual(spieler_gewicht(("Alex", 99.9)), "Alex ist ein leichter Spieler.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 608
