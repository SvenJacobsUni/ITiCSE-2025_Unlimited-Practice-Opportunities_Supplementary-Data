# Input
- Programmierkonzept: Tupel
- Kontext: Vergnügungspark

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Vergnügungspark-Tickets

Schreibe eine Funktion namens `ticket_preise(tickets)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel repräsentiert ein Ticket und enthält zwei Elemente: den Namen des Fahrgeschäfts (als String) und den Preis des Tickets (als Float).

Die Funktion soll die Gesamtkosten aller Tickets berechnen und zurückgeben.

Beispielaufruf:
```python
tickets = [("Achterbahn", 5.50), ("Riesenrad", 3.75), ("Geisterbahn", 4.00)]
print(ticket_preise(tickets))  # Ausgabe: 13.25
```

Implementiere die Funktion `ticket_preise(tickets)`, die die Gesamtkosten der übergebenen Tickets berechnet und zurückgibt.

## Codegerüst
```python
def ticket_preise(tickets):
    ## Hier Code einfügen
```

## Musterlösung
```python
def ticket_preise(tickets):
    return sum(preis for _, preis in tickets)

tickets = [("Achterbahn", 5.50), ("Riesenrad", 3.75), ("Geisterbahn", 4.00)]
print(ticket_preise(tickets))
```

## Unit Tests
```python
import unittest
from main import ticket_preise

class TestTicketPreise(unittest.TestCase):
    def test_einfacher_fall(self):
        tickets = [("Achterbahn", 5.50), ("Riesenrad", 3.75), ("Geisterbahn", 4.00)]
        self.assertEqual(ticket_preise(tickets), 13.25)

    def test_leere_liste(self):
        tickets = []
        self.assertEqual(ticket_preise(tickets), 0.0)

    def test_ein_ticket(self):
        tickets = [("Achterbahn", 5.50)]
        self.assertEqual(ticket_preise(tickets), 5.50)

    def test_gemischte_preise(self):
        tickets = [("Achterbahn", 5.50), ("Riesenrad", 3.75), ("Geisterbahn", 4.00), ("Karussell", 2.25)]
        self.assertEqual(ticket_preise(tickets), 15.50)

    def test_negative_preise(self):
        tickets = [("Achterbahn", -5.50), ("Riesenrad", 3.75)]
        self.assertEqual(ticket_preise(tickets), -1.75)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 450
