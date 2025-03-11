# Input
- Programmierkonzept: String
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Sportarten filtern

Schreibe eine Funktion namens `filter_sportarten(sportarten_liste, filter_buchstabe)`, die eine Liste von Sportarten und einen Buchstaben als Parameter erhält. Die Funktion soll eine neue Liste zurückgeben, die nur die Sportarten enthält, die mit dem angegebenen Buchstaben beginnen.

Beispielaufruf:
```python
sportarten = ["Basketball", "Baseball", "Fußball", "Tennis", "Badminton"]
resultat = filter_sportarten(sportarten, "B")
print(resultat)  # Ausgabe: ["Basketball", "Baseball", "Badminton"]
```

Implementiere die Funktion so, dass sie die gewünschten Ergebnisse liefert.

## Codegerüst
```python
def filter_sportarten(sportarten_liste, filter_buchstabe):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_sportarten(sportarten_liste, filter_buchstabe):
    return [sport for sport in sportarten_liste if sport.startswith(filter_buchstabe)]

sportarten = ["Basketball", "Baseball", "Fußball", "Tennis", "Badminton"]
resultat = filter_sportarten(sportarten, "B")
print(resultat)  # Ausgabe: ["Basketball", "Baseball", "Badminton"]
```

## Unit Tests
```python
import unittest
from main import filter_sportarten

class TestFilterSportarten(unittest.TestCase):
    def test_filter_b(self):
        self.assertEqual(filter_sportarten(["Basketball", "Baseball", "Fußball", "Tennis", "Badminton"], "B"), ["Basketball", "Baseball", "Badminton"])

    def test_filter_f(self):
        self.assertEqual(filter_sportarten(["Basketball", "Baseball", "Fußball", "Tennis", "Badminton"], "F"), ["Fußball"])

    def test_filter_t(self):
        self.assertEqual(filter_sportarten(["Basketball", "Baseball", "Fußball", "Tennis", "Badminton"], "T"), ["Tennis"])

    def test_filter_no_match(self):
        self.assertEqual(filter_sportarten(["Basketball", "Baseball", "Fußball", "Tennis", "Badminton"], "X"), [])

    def test_empty_list(self):
        self.assertEqual(filter_sportarten([], "B"), [])

    def test_case_sensitivity(self):
        self.assertEqual(filter_sportarten(["Basketball", "baseball", "Fußball", "Tennis", "badminton"], "b"), ["baseball", "badminton"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 452
