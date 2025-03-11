# Input
- Programmierkonzept: For-Schleifen;If-Else-Anweisungen
- Kontext: Restaurant

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Restaurant-Bestellungen

Schreibe eine Funktion namens `bestellung_ueberpruefen(bestellungen)`, die eine Liste von Bestellungen als Argument erhält. Jede Bestellung ist ein Dictionary mit den Schlüsseln "gericht" und "anzahl". Die Funktion soll die Bestellungen durchgehen und überprüfen, ob die Anzahl der bestellten Gerichte größer als 0 ist. Wenn die Anzahl größer als 0 ist, soll die Funktion eine Nachricht ausgeben, die besagt, dass die Bestellung akzeptiert wurde. Andernfalls soll die Funktion eine Nachricht ausgeben, dass die Bestellung abgelehnt wurde.

Beispielaufruf:
```python
bestellungen = [
    {"gericht": "Pizza", "anzahl": 2},
    {"gericht": "Salat", "anzahl": 0},
    {"gericht": "Pasta", "anzahl": 3}
]
bestellung_ueberpruefen(bestellungen)
```

Erwartete Ausgabe:
```
Bestellung für Pizza akzeptiert.
Bestellung für Salat abgelehnt.
Bestellung für Pasta akzeptiert.
```

## Codegerüst
```python
def bestellung_ueberpruefen(bestellungen):
    ## Hier Code einfügen
```

## Musterlösung
```python
def bestellung_ueberpruefen(bestellungen):
    for b in bestellungen:
        if b["anzahl"] > 0:
            print(f"Bestellung für {b['gericht']} akzeptiert.")
        else:
            print(f"Bestellung für {b['gericht']} abgelehnt.")

bestellungen = [
    {"gericht": "Pizza", "anzahl": 2},
    {"gericht": "Salat", "anzahl": 0},
    {"gericht": "Pasta", "anzahl": 3}
]
bestellung_ueberpruefen(bestellungen)
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import bestellung_ueberpruefen

class TestBestellungUeberpruefen(unittest.TestCase):
    def test_alle_bestellungen_akzeptiert(self):
        bestellungen = [
            {"gericht": "Pizza", "anzahl": 2},
            {"gericht": "Pasta", "anzahl": 3}
        ]
        expected_output = "Bestellung für Pizza akzeptiert.\nBestellung für Pasta akzeptiert.\n"
        self._run_test(bestellungen, expected_output)

    def test_alle_bestellungen_abgelehnt(self):
        bestellungen = [
            {"gericht": "Salat", "anzahl": 0},
            {"gericht": "Suppe", "anzahl": 0}
        ]
        expected_output = "Bestellung für Salat abgelehnt.\nBestellung für Suppe abgelehnt.\n"
        self._run_test(bestellungen, expected_output)

    def test_gemischte_bestellungen(self):
        bestellungen = [
            {"gericht": "Pizza", "anzahl": 2},
            {"gericht": "Salat", "anzahl": 0},
            {"gericht": "Pasta", "anzahl": 3}
        ]
        expected_output = "Bestellung für Pizza akzeptiert.\nBestellung für Salat abgelehnt.\nBestellung für Pasta akzeptiert.\n"
        self._run_test(bestellungen, expected_output)

    def test_leere_bestellungsliste(self):
        bestellungen = []
        expected_output = ""
        self._run_test(bestellungen, expected_output)

    def _run_test(self, bestellungen, expected_output):
        captured_output = StringIO()
        sys.stdout = captured_output
        bestellung_ueberpruefen(bestellungen)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 563
