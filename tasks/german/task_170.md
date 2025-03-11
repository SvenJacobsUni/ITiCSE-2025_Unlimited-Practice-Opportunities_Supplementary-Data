# Input
- Programmierkonzept: Listen;While-Schleifen;Funktionen als Variablen
- Kontext: Streaming-Dienste

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Streaming-Dienste und Serien

Schreibe eine Funktion `filter_serien(serien_liste, bewertung)`, die eine Liste von Serien und eine Mindestbewertung als Parameter erhält. Die Funktion soll alle Serien aus der Liste zurückgeben, die eine Bewertung gleich oder höher der angegebenen Mindestbewertung haben.

Die Serienliste ist eine Liste von Tupeln, wobei jedes Tupel den Namen der Serie und ihre Bewertung enthält. Die Bewertung ist eine Zahl zwischen 1 und 10.

Verwende eine `while`-Schleife, um durch die Liste zu iterieren und die Serien zu filtern.

Beispiel:

```python
serien = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
print(filter_serien(serien, 8.5))
```

Erwartete Ausgabe:

```
[('Breaking Bad', 9.5), ('Stranger Things', 8.7), ('The Office', 8.9)]
```

## Codegerüst
```python
def filter_serien(serien_liste, bewertung):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_serien(serien_liste, bewertung):
    result = []
    i = 0
    while i < len(serien_liste):
        if serien_liste[i][1] >= bewertung:
            result.append(serien_liste[i])
        i += 1
    return result

serien = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
print(filter_serien(serien, 8.5))
```

## Unit Tests
```python
import unittest
from main import filter_serien

class TestFilterSerien(unittest.TestCase):
    def test_alle_serien(self):
        serien = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_serien(serien, 8.0), serien)

    def test_keine_serien(self):
        serien = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_serien(serien, 10.0), [])

    def test_einige_serien(self):
        serien = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_serien(serien, 8.5), [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9)])

    def test_leere_liste(self):
        serien = []
        self.assertEqual(filter_serien(serien, 8.5), [])

    def test_grenze_bewertung(self):
        serien = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_serien(serien, 8.7), [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9)])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 602
