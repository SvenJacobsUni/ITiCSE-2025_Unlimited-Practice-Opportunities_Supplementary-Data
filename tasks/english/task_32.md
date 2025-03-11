# Input
- Programming Concept: Tuples
- Context: Amusement Park

# Generated Task Components
## Task Description
### Exercise: Amusement Park Tickets

Write a function named `ticket_prices(tickets)` that takes a list of tuples as an argument. Each tuple represents a ticket and contains two elements: the name of the ride (as a string) and the price of the ticket (as a float).

The function should calculate and return the total cost of all tickets.

Example call:
```python
tickets = [("Roller coaster", 5.50), ("Ferris wheel", 3.75), ("Haunted house", 4.00)]
print(ticket_prices(tickets))  # Output: 13.25
```

Implement the function `ticket_prices(tickets)`, which calculates and returns the total costs of the given tickets.

## Code Framework
```python
def ticket_prices(tickets):
    ## Insert code here
```

## Model Solution
```python
def ticket_prices(tickets):
    return sum(price for _, price in tickets)

tickets = [("Roller coaster", 5.50), ("Ferris wheel", 3.75), ("Haunted house", 4.00)]
print(ticket_prices(tickets))
```

## Unit Tests
```python
import unittest
from main import ticket_prices

class TestTicketPrices(unittest.TestCase):
    def test_simple_case(self):
        tickets = [("Roller coaster", 5.50), ("Ferris wheel", 3.75), ("Haunted house", 4.00)]
        self.assertEqual(ticket_prices(tickets), 13.25)

    def test_empty_list(self):
        tickets = []
        self.assertEqual(ticket_prices(tickets), 0.0)

    def test_single_ticket(self):
        tickets = [("Roller coaster", 5.50)]
        self.assertEqual(ticket_prices(tickets), 5.50)

    def test_mixed_prices(self):
        tickets = [("Roller coaster", 5.50), ("Ferris wheel", 3.75), ("Haunted house", 4.00), ("Carousel", 2.25)]
        self.assertEqual(ticket_prices(tickets), 15.50)

    def test_negative_prices(self):
        tickets = [("Roller coaster", -5.50), ("Ferris wheel", 3.75)]
        self.assertEqual(ticket_prices(tickets), -1.75)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 450
